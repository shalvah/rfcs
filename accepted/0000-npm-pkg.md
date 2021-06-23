# npm pkg

## Summary

A new top-level command that manages any property in your `package.json`.

## Motivation

Some users prefer managing their `package.json` using **npm cli** comands rather than manually editing a JSON file.

As of today, some of the **npm cli** commands already handle the automated management of the `package.json` file, such as `npm install` adding / updating dependency declarations, `npm version` bumping the version value, or in the case of `npm set-script` a top-level command that serves specifically the purpose of managing `"scripts"` data in the `package.json` file.

## Detailed Explanation

- Add a `npm pkg` command

## Rationale and Alternatives

{{Discuss 2-3 different alternative solutions that were considered. This is required, even if it seems like a stretch. Then explain why this is the best choice out of available ones.}}

## Implementation

- Add a new `lib/pkg.js` top-level command that will handle adding / removing / modifying properties in your `package.json` file.

## Prior Art

- `npm set-script` top-level command that allow users to add new scripts to their package.json
- `npm init -w <ws-path>` init command will add the current path to `"workspaces"` property
- `npm install|uninstall <pkg>` will add/remove deps to `"dependencies"`

## Unresolved Questions and Bikeshedding

- Syntax?
