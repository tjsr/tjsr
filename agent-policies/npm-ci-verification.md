# npm verification for TJSR agents

Use this policy in maintained TJSR npm projects, including applications and
packages that consume private GitHub Packages dependencies.

## Local checks and credentials

- Inspect the repository instructions, package scripts, lockfile, registry
  configuration, and available tools before choosing checks. Run safe local
  checks that are feasible with the environment's existing access.
- If private dependencies require credentials that are unavailable, skip
  dependency installation and the checks that need those dependencies. An
  authenticated Actions agent may use its already configured job credentials.
  For now, treat local Codex on `tjsr-3700x` and GitHub-launched Codex agents
  as lacking private-package access unless explicitly configured otherwise.
  Launching an agent from GitHub does not establish Actions job authentication.
- After an authentication failure such as HTTP 401/403, stop retrying
  `npm ci`, `npm install`, or equivalent commands until access changes. Record
  missing private-package access as an environment blocker, not a code failure.
  Do not ask the user to supply a token, copy tokens from another environment,
  print credentials, or provision credentials as part of ordinary code work.
- Never replace or stub private packages, invent dependency contents, bypass
  dependency resolution with `--force` or `--legacy-peer-deps`, disable checks,
  or fabricate successful verification. Preserve the lockfile unless a real
  dependency change requires it.

## Branch verification through GitHub Actions

1. Inspect all push/PR workflow triggers and called actions before publishing
   a branch. A documentation or verification push must not accidentally publish
   a package/image, create a release, deploy, or modify a remote environment.
   If existing triggers cannot safely verify the branch, retain a local commit
   or patch and report the exact gating change needed.
2. Commit authorized changes to the existing task branch or a new PR branch,
   push it when safe, and open or update a draft PR as appropriate. Use ordinary
   GitHub branches; this does not require delegating work to Copilot.
3. Use the repository's configured verification workflows and existing package
   read grants. GitHub Actions does not automatically have access to every
   private package: report missing job permissions, package grants, required
   approval, fork restrictions, or Dependabot secret restrictions as blockers.
4. Monitor verification for the exact latest pushed commit through a terminal
   result. Inspect failed job logs and fix recoverable issues within the
   authorized scope, then verify the new commit. Do not treat an older green
   commit, a queued job, or a skipped/missing check as success.
5. Report local checks and CI checks separately as passed, failed, or unrun,
   including the head SHA, PR/run links, and any remaining blocker. If no safe
   verification workflow exists, say so explicitly.

Use Node 24 as the primary runtime for new verification work, Node 22 where the
project actually supports it, and the latest npm compatible with the declared
engine floor. Check the repository's supported matrix; this instruction alone
does not authorize changing runtimes, dependencies, or CI configuration.

## Authority and adoption

This policy grants no authority to push directly to main, approve or merge PRs,
enable auto-merge, release dependencies, publish images, deploy, change repository
settings, or provision tokens. An earlier authorized release sequence is not
standing release permission. When separately authorized to merge a repaired
multi-commit Dependabot PR, prefer squash; a single-commit PR may use rebase.

`tjsr/tjsr` is a canonical policy location, not an account-wide instruction
inheritance mechanism. Each adopting repository must include the essential rules
in its root `AGENTS.md` and native Copilot entry point. Keep essential rules inline
so an unavailable remote document does not remove them. More specific npm agent
guides must respect the same credential and verification constraints. For Copilot
CLI subagents, enable `include-custom-instructions: true` where supported or pass
these constraints explicitly; repository files alone cannot guarantee that every
agent client loads them.

Sources: [Codex instruction discovery](https://learn.chatgpt.com/docs/agent-configuration/agents-md),
[Copilot instruction support](https://docs.github.com/en/copilot/reference/custom-instructions-support),
[Copilot CLI subagent instructions](https://docs.github.com/en/copilot/reference/copilot-cli-reference/cli-command-reference#repository-custom-instructions-for-subagents),
and [GitHub npm authentication](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry).
