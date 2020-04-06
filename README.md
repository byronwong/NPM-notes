Using NPM Basics
================

<!-- TOC -->

- [1. Setting up](#1-setting-up)
- [2. Getting Help](#2-getting-help)
- [3. Setting Defaults (config.json)](#3-setting-defaults-configjson)
- [4. Reading / Returning info](#4-reading--returning-info)
- [5. Return config data](#5-return-config-data)
- [6. Listing](#6-listing)
- [7. Installing Packages](#7-installing-packages)
    - [7.1. Installing from other sources](#71-installing-from-other-sources)
    - [7.2. Install specific version](#72-install-specific-version)
    - [7.3. Installing from a folder](#73-installing-from-a-folder)
- [8. Uninstall Packages:](#8-uninstall-packages)
- [9. Utilities](#9-utilities)
    - [9.1. NPM PRUNE](#91-npm-prune)
    - [9.2. NPM REPO](#92-npm-repo)
    - [9.3. UPDATING NPM](#93-updating-npm)
- [10. Tasks](#10-tasks)
    - [10.1. Default tasks](#101-default-tasks)
    - [10.2. Custom tasks](#102-custom-tasks)
    - [10.3. Running from local packages](#103-running-from-local-packages)
    - [10.4. PRE and POST tasks](#104-pre-and-post-tasks)
    - [10.5. Chaining tasks](#105-chaining-tasks)

<!-- /TOC -->

---

# 1. Setting up
- `npm init`
- `npm init -y` // accept all defaults

# 2. Getting Help
- `npm help-search <keyword>`
- `npm help <keyword>`

# 3. Setting Defaults (config.json)
- `npm set init-license 'MIT'`  

# 4. Reading / Returning info
- `npm get init-<property>`
    e.g.`npm get init-author`

# 5. Return config data 
- `ls ~/.npmrc`

# 6. Listing 
- Listing all installed modules = `ls node_modules/`
- List all packages = `npm list`
- List with depth = `npm list --depth 0`
- List global packages = `npm list --global true`
- Also works with depth = `npm list --global true --depth 0`
- See descriptions of packages = `npm list --long true`
- Short hand for list = `npm ls`
- or local = `npm ls node_modules`
- or `npm list`


# 7. Installing Packages
- `npm install <package_name> -S | -D`
- `npm i <package_name> -S | -D`
- Optionally you can use the `--save` and `--save-dev` flags

## 7.1. Installing from other sources
- `npm i http//:url.com`
- `npm i gist:3ss9s3dd29423`
- `npm i https://github.com/expressjs/express`

## 7.2. Install specific version
- `npm i --save --save-exact lodash@1.8.2`
- `npm i --save-dev --save-exact lodash@1.8.2`

## 7.3. Installing from a folder
- `--save` option if it flags as extraneous
- `npm i ../filepath -S`


# 8. Uninstall Packages: 
- `npm uninstall <package_name>`
- `npm rm <package_name> -S | -D`
- See package.json = `cat package.json`


# 9. Utilities
## 9.1. NPM PRUNE
- `npm prune --production` // clears all dev dependancies

## 9.2. NPM REPO
- `npm repo underscore` // takes you to the underscore repo

## 9.3. UPDATING NPM
- `sudo npm i npm@latest -g` // must have admin status


# 10. Tasks

## 10.1. Default tasks
- There are two default tasks in npm:
- `npm start` // use `-s` to silence other messages
- `npm test`
- `npm stop`
- `npm restart`

## 10.2. Custom tasks
- All other tasks require the `run` command 
- eg. `npm run dev`

## 10.3. Running from local packages
- You can run a local package using the `./node_modules/.bin`
    e.g. `node_modules/.bin/sass-lint -v -q`

## 10.4. PRE and POST tasks
- You can also add tasks before a task by adding `pre` e.g. `prestart`
- You can also add task after a task by adding `post` e.g. `poststart`

## 10.5. Chaining tasks 
- You can chain tasks together using `&&`
    e.g. `"start" : "gulp build && gulp serve"`  

> NOTE: See notes on npm scripts as a build tool.