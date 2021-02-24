# Packer Docs Artifacts

This package is intended to run in Packer plugin repositories. It generates artifacts that are consumable by the Packer documentation website.

## Usage

Run this command at the root of your plugin repository. There should be a `docs` folder in your repository, with component subfolders for each of the components your plugin contains (`builders`, `datasources`, `post-processors`, `provisioners`). Each of these component subfolders should contain at least one `.mdx` file. Each `.mdx` file will be rendered to the Packer documentation website, using the file name and location in the subfolder as the URL route. Note that files named `index.mdx` will be rendered at a root URL (`/`) rather than at `/index`.

```shell
npx @hashicorp/packer-plugin-docs-artifacts
```
