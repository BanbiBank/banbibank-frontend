# 🦌 Banbibank Frontend

<p align="center">
  <a href="https://banbibank-frontend-dex.vercel.app/logo.png">
      <img src="https://banbibank-frontend-dex.vercel.app/logo.png" height="128">
  </a>
</p>

This project contains the main features of the banbibank frontend.

## Release Process

This project uses [Changesets](https://github.com/changesets/changesets) to manage versions, create changelogs, and publish to npm.

### Steps to Release

1. Create a new changeset

```bash
yarn changeset
```

- Select the packages you want to include in the changeset
- Choose the type of version bump (major, minor, patch)
- Provide a description of the changes

2. Update versions and changelogs

```bash
yarn version-packages
```

This command will:
- Update package versions based on the changesets
- Generate/update CHANGELOG.md files
- Update the yarn.lock file

3. Publish packages

```bash
yarn release-packages
```

This command will:
- Build all packages in the packages directory
- Update versions and changelogs
- Publish the packages to npm registry

### Notes
- Make sure you are logged in to npm (`npm login`) before publishing
- Ensure all changes are committed before running the release process
- After publishing, the changesets will be automatically removed
