# yarn-crash-course

Some notes regarding yarn.

# From Traversy

- Faster
- More secure
- Has the same library
- more convenient syntax

# Installation

Follow the instructions on website.

# Commands

## Basics

`yarn -v`
`yarn help`
`yarn init` - starts a project
`yarn init -y `- starts a project with default values

## Defaults

you can change defaults:
`yarn config set init-license ISC`
check the default:
`yarn config get init-license`
restore the default
`yarn config delete init-license`

## Adding packages

`yarn add lodash`

latest version - \*
don't update major version - ^

if you add a package manually in the package.json:
`yarn install`
remove
`yarn remove lodash`

Specific version
yarn add lodash@4.17.3

Outdated versions
`yarn outdated`
will find all your packages that are outdated
or specific package
`yarn outdated lodash`

to update to highest version in package
`yarn upgrade lodash`
if you want to update to latest version
`yarn upgrade lodash --latest`

## Global Modules

`yarn global add nodemon`
it's important to put global just after yarn

Find global packages:
`yarn global bin`

Remove global:
`yarn global remove lodash`

list packages
`yarn list` or
`yarn list --depth=0`
`yarn list --pattern gulp`

dev dependencies:
`yarn add gulp -D`
`yarn add gulp --dev`

remove dev dependencies:
`yarn remove gulp`

`yarn check` - checks if the yarn lock and repos are in sync

`yarn import` - generate new yarn lock file

## Scripts

```
"scripts" : {
    "dev": "nodemon index.js"
}
```

and then `yarn run dev`

## Licenses

`yarn licenses list`

# Zip into a package

`yarn pack`

check cache
`yarn cache list`
`yarn cache list --pattern lodash`

clear cache
`yarn cache clean`

# Yarn 2

info from officials docs.

`yarn init -2`

updating yarn
`yarn set version stable`
latest version
`yarn set version from sources`

## Commands

`yarn help`
`yarn install` or `yarn`
`yarn add lodash` or `yarn add lodash@numbers`
`yarn add lodash --dev` or `yarn add lodash -D`
upgrading:
`yarn up lodash` or `yarn up lodash@version`
`yarn remove lodash`
upgrade yarn
`yart set version latest`

instead of global, use `dlx`
