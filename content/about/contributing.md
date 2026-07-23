---
title: Contribution Guidelines
weight: 1
next: .Next
prev: .Prev
---

{{<callout type="note">}}
If you have found a problem on the website, or you would like to suggest an improvement or modification,
please submit a [GitHub issue](https://github.com/waisworkshop/waisworkshop.github.io/issues).
{{</callout>}}

<div class="hx:mt-6 hx:mb-3">

## Updating the website

The WAIS Workshop website is generated with [Hugo](https://github.com/gohugoio/hugo) using the [Hextra theme](https://themes.gohugo.io/themes/hextra/) and deployed via [GitHub Pages](https://pages.github.com/)

The content for the website is hosted on [GitHub](https://github.com/waisworkshop/waisworkshop.github.io/) {{< icon "github" >}}

### Steps to Contribute

If you are interested in directly suggesting changes, try to use the following steps:

1. Fork the repository to your personal GitHub account by clicking the "Fork" button on the project [main page](https://github.com/waisworkshop/waisworkshop.github.io). This creates your own server-side copy of the repository.
2. Clone the repository to your local system and include the `--recursive` to ensure the submodules are cloned
```bash
git clone --recursive https://github.com/waisworkshop/waisworkshop.github.io.git
```
If you forget to include the `--recursive` flag, you can fetch the submodules after cloning
```bash
git submodule update --init --recursive
```
3. Locally, add your fork as the `origin` remote and set the original project repository as the `upstream` remote.
```bash
git remote set-url origin <your-wais-workshop-repo>
git remote set-url upstream https://github.com/waisworkshop/waisworkshop.github.io.git
```
4. Create a new branch to do your work
```bash
git checkout -B <new-branch-name> 
```
5. You can deploy a local copy of the website that includes your local edits by running `hugo server`
6. Make your changes on the new branch and commit them
```
git commit -m <helpful-commit-message>
```
7. Push your work to GitHub under your project fork
```
git push origin <new-branch-name>
```
8. Submit a [Pull Request](https://github.com/waisworkshop/waisworkshop.github.io/pulls) from your forked branch to the project repository. From there we will review your pull request before merging your branch into the live website.

### General PR Guidelines

- Make each pull request as small and simple as possible
- Larger changes should be broken down into their basic components and integrated separately
- Write your commit messages in clear language that describe the changes made
- If possible, associate the pull request with a [GitHub issue](https://github.com/waisworkshop/waisworkshop.github.io/issues)
- Write your pull request with a clear title and descriptive message
- Be patient as reviews of pull requests take time

### Building with ``pixi``

`pixi` can also be used to build the website from scratch after cloning the repository:

```bash
git clone --recursive https://github.com/waisworkshop/waisworkshop.github.io.git
cd waisworkshop.github.io
pixi run webserver
```

To see the available `pixi` tasks:

```bash
pixi task list
```
