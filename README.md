# Tim Rowe - Github projects

- Welcome to the updated github home.  Here you'll find mostly a lot of utility projects and libraries intended to be included with other work.  Most personal/opensource projects you'll currently find here are Node/Typescript/React of some flavour.  You'll also find a heap of utility Docker containers and Github actions.

## Current projects

Some current in-flight projects:
|---|Project||
|-|---|---|
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [user-session-middleware](https://github.com/tjsr/user-session-middleware)<br>![user-session-middleware](https://github.com/tjsr/user-session-middleware/actions/workflows/build.yml/badge.svg)| Session handling and user authentication middleware for microservices, intended for rapid user-accessible API scaffolding. Collioqually 'USM'. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")| [tagtool](https://github.com/tjsr/tagtool)<br>![tagtool](https://github.com/tjsr/tagtool/actions/workflows/build.yml/badge.svg)| USM-based data tagging microservice for embedding in to applications. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [express-server-helper](https://github.com/tjsr/express-server-helper)<br>![express-server-helper](https://github.com/tjsr/express-server-helper/actions/workflows/build.yml/badge.svg) | Wrapper utility for including common middleware used to create rapid ExpressJS REST APIs with USM. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [package-json-utils](https://github.com/tjsr/package-json-utils)<br>![package-json-utils](https://github.com/tjsr/package-json-utils/actions/workflows/build.yml/badge.svg) | Utilities for finding and extracting common data out of package.json required by other tools in this list. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [linkteam](https://github.com/tjsr/linkteam)<br>![linkteam](https://github.com/tjsr/linkteam/actions/workflows/build.yml/badge.svg) | CLI tool to search for symlinks or junctions installed in global node_modules used by a project, and link them based on owner, pattern, or everything found. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [girt](https://github.com/tjsr/girt)<br>![girt](https://github.com/tjsr/girt/actions/workflows/build.yml/badge.svg) | Github Repo Tool.  Simple commandline tool for updating github repository properties and settings that aren't available from the Gihub CLI except using complex queries or GraphQL. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [fs-utils](https://github.com/tjsr/fs-utils)<br>![fs-utils](https://github.com/tjsr/fs-utils/actions/workflows/build.yml/badge.svg) | NodeJS filesystem utils including directory traversal search. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [testUtils](https://github.com/tjsr/testUtils)<br>![testUtils](https://github.com/tjsr/testUtils/actions/workflows/build.yml/badge.svg) | NodeJS project testing utils. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![React](https://cdn.simpleicons.org/React/#61DAFB "React")| [pinpanion](https://github.com/tjsr/pinpanion) | A Pinny Arcade pin collection tool.  Uses TS/React/MaterialUI/Vite. |
|![Docker](https://cdn.simpleicons.org/Docker/#2496ED "Docker")| [node-patched-npm](https://github.com/tjsr/node_patched_npm) | A patched node/alpine container with recent vulnerability fixes including npm fixes. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [simple-env-utils](https://github.com/tjsr/simple-env-utils)<br>![simple-env-utils](https://github.com/tjsr/simple-env-utils/actions/workflows/build.yml/badge.svg) | simple methods for ensuring compliant environment variables. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [mysql-pool-utils](https://github.com/tjsr/mysql-pool-utils)<br>![mysql-pool-utils](https://github.com/tjsr/mysql-pool-utils/actions/workflows/build.yml/badge.svg) | simple re-usable database connection pool handling functions. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![Node.JS](https://cdn.simpleicons.org/Node.JS "Node.JS")| [sparse-bit-string](https://github.com/tjsr/sparse-bit-string)<br>![sparse-bit-string](https://github.com/tjsr/sparse-bit-string/actions/workflows/build.yml/badge.svg) | A packed, compressed bit flag suite suitable for including in URLs and QR codes where data limits are factors. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![React](https://cdn.simpleicons.org/React "React")| [absee](https://github.com/tjsr/absee) | A/B See.  An A/B testing tool that allows users to compare and select from presented elements or sets. |
|![Typescript](https://cdn.simpleicons.org/Typescript "Typescript")![ESLint](https://cdn.simpleicons.org/ESLint "ESLint")| [eslint-config](https://github.com/tjsr/eslint-config) | Shared typescript-eslint rules and configuration for use across all TS projects. |

## Github actions

|---|Github action||
|---|---|---|  
|![GitHub](https://cdn.simpleicons.org/GitHub "GitHub")| [@tjsr/action_npm_outdated](https://github.com/tjsr/action_npm_outdated) | Github action check an npm depenency for new versions |
|![GitHub](https://cdn.simpleicons.org/GitHub "GitHub")| [@tjsr/remote_docker_stop](https://github.com/tjsr/remote_docker_stop) | Github action to stop a remote docker container over SSH |
|![GitHub](https://cdn.simpleicons.org/GitHub "GitHub")| [@tjsr/remote_docker_pull](https://github.com/tjsr/remote_docker_pull) | Github action to pull a remote docker image over SSH |

## Early WIP projects

- [prisma-generic](https://github.com/tjsr/prisma-generic) - A generic prisma container that enables launching with a mounted folder of prisma configs to reduce the need for repeatedly re-building the same base prisma deployment helper container. Intended for use with mysql-pool-utils based microservices.
- [dyn53](https://github.com/tjsr/dyn53) - An AWS Cloudformation/Route53/Lambda project to host and manage DynDNS entries and updating.
- [abswipe](https://github.com/tjsr/abswipe) - A React swipy control for A/B element selection.
- [github_node_repo_dep](https://github.com/tjsr/github_node_repo_dep) - A set of github actions which scan for other repos that use this (or a specified) artifact, allowing you to automatically run actions against them (such as open a PR or clone/test them).  Useful for immediately testing libraries against branches by cloning both repos and testing using `npm link`.

# TODO projects

Stuff I want to get around to but haven't had the time.

- @tjsr/ts-base - A two-way project template, for basing new projects on with a commandline selector, which also allows syncing back to other projects and rebasing to keep all small projects and microservices in sync.
- [glob](https://github.com/isaacs/node-glob), [rimraf](https://github.com/isaacs/rimraf), [minimatch](https://github.com/isaacs/minimatch) and [pacote](https://github.com/npm/pacote) updates. Updates to core npm/node libraries to use latest versions, and ensure support with nodejs20/22. Requires some significant work and fixes to timout issues in [tapjs](https://github.com/tapjs/tapjs).
- LWDB - croudsourced data collection tool for the Last War mobile game to help players plan and determine durations and costs of upgrades.

# Older projects

Most of my older projects are hosted on bitbucket at [bitbucket.org/tjsrowe](https://bitbucket.org/tjsrowe).  Predominantly these ones are utilities for helping the cycling/mountain bike community.  They also tend to use Bitbucket pipelines and self-hosted runners.

# Elsewhere

📫 Find me at insta [@tjsr.id.au](https://www.instagram.com/tjsr.id.au) (for chocolate creatioons), twitter [@tjsr](https://x.com/tjsr) (for general 'old man shakes fist at cloud' stuff), or email to [Tim Rowe](mailto:tim@tjsr.id.au)
