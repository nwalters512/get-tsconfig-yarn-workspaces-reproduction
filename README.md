# get-tsconfig-yarn-workspaces-reproduction

Reproduces an issue where `get-tsconfig` cannot resolve an extended config that's located in a Yarn workspace.

## Steps to reproduce

1. Clone this repository
2. Run `yarn install`
3. `cd packages/library`
4. Run `node get-tsconfig.mjs`
5. Observe a failure

To demonstrate that the issue was introduced in version `4.7.4`:

1. Ensure you're still in the `packages/library` directory
2. Run `yarn add get-tsconfig@4.7.3`
3. Run `node get-tsconfig.mjs`
4. Observe success
