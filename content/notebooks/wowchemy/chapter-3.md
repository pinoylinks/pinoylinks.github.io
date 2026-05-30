---
title: Tutorials
linkTitle: Chapter 3
date: 2024-07-24T08:07:27+08:00
type: book
weight: 3
math: false
highlight: false
tags:
  - chapter
---

<!--more-->

{{< toc >}}

## Contribute



### Ref
Hugo Blox, [Contribute](https://bootstrap.hugoblox.com/hugo-tutorials/contribute/)

## Deploy



### Ref
Hugo Blox, [Deploy](https://bootstrap.hugoblox.com/hugo-tutorials/deployment/)

## Update

Learn how to update the Wowchemy website components that your site uses.

## TLDR

1.  Head over to your website project in [Github](https://github.com), click the `go.mod` file, and click the pencil button to edit it
2.  Update the `require` statement to the following to get the latest version:
    
    *   Otherwise, to get a specific version of a module, replace `main` with a commit or [tagged version](https://github.com/wowchemy/wowchemy-hugo-themes/tags) that’s associated with the module.  
        For example, the `wowchemy` module has a `modules/wowchemy/v5.6.0` release which we can update to by replacing `main` with `v5.6.0` in the relevant line below.

```go
module my-website

go 1.15

require (
  github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-netlify-cms main
  github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-netlify main
    github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-reveal main
  github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy/v5 main
)
``` 

Click the green Commit Changes button to save your changes.

3.  Update the module paths in `config/_default/config.yaml` to the following if they are not already:

```go
module:
  imports:
    - path: github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-netlify-cms
    - path: github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-netlify
    - path: github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy-plugin-reveal
    - path: github.com/wowchemy/wowchemy-hugo-themes/modules/wowchemy/v5
````

4.  Update `HUGO_VERSION` in `netlify.toml` to a compatible version from the [Release Notes](https://github.com/wowchemy/wowchemy-hugo-themes/releases)
    *   Or, if you are building on your computer, update your local Hugo Extended to the compatible version
5.  Consecutively apply any breaking changes from the relevant [Release Notes](https://github.com/wowchemy/wowchemy-hugo-themes/releases) (older, pre-v5.3 notes are on the [Blog](/blog/))
6.  Check that the latest [Netlify](https://www.netlify.com/) deployment of your site is successful (otherwise click the failed build to view the issue)

**TIP:** If you are updating from an ancient version, you may find it easier to create a fresh site and migrate your `content/` folder across.

**Join the community** to learn when we release improvements:

*   [Star (and Watch) Wowchemy on Github](https://github.com/wowchemy/wowchemy-hugo-themes/)
*   Join the Announcements channel on [Discord](https://discord.gg/z8wNYzb)
*   Follow [@wowchemy](https://twitter.com/wowchemy) and [@GeorgeCushen](https://twitter.com/GeorgeCushen) on Twitter
*   Subscribe to the blog RSS feed

Full Process[](#full-process)
-----------------------------

The update process consists of:

1.  [Preparation](#preparation)
2.  [Updating Wowchemy](#update-wowchemy)
3.  [Migrating your content](#migrate-content) front matter and configuration by applying any relevant breaking changes

### Preparation[](#preparation)

Before updating Wowchemy, it is strongly recommended to make a full **backup** of your website folder.

Then, **record your current version**, so that after you update Wowchemy, you can apply any relevant breaking changes to the TOML/YAML site configuration and front matter in your `content/` folder.

To find your current version, look in `themes/academic/data/academic.toml` if it exists. Otherwise, you can get the version from `go.mod` where it’ll either be an exact version like `v5.0.0` or it’ll be a build in the form `v<dummy-version-number>-<date>-<build-number>`. The first 7 characters of the build number can be cross-referenced in the [commit log](https://github.com/wowchemy/wowchemy-hugo-themes/commits/master) to check what development updates are available.

Note that if you installed a build in the _master_ version rather than a specific release, then extra care should be taken (such as by checking the git log if you installed with git) as you may be in-between versions and some actions in the relevant release notes may have already been applied.

### Update Wowchemy[](#update-wowchemy)

#### Prerequisites[](#prerequisites)

[**Install**](/getting-started/install-hugo-extended/) a compatible version of Hugo Extended and its dependencies.

If your site **does not have a `go.mod` file**, follow the **Migrate Content** guide below and then update your theme to version 5 to convert your site to use Hugo’s Module system. From Version 5 onward, you can update using the command in the **Update** section below.

#### Update[](#update)

Hugo uses the `go.mod` file to control which version of Wowchemy a site uses.

Open a Terminal (Command Prompt) and navigate to your site’s folder using the [`cd` command](https://linuxize.com/post/linux-cd-command/).

Update to get the very latest developments:

```go
hugo mod get -u ./...
```

Alternatively, update to the latest official release:

```go
hugo mod get -u
```

[Migrate your content](#migrate-content) front matter and configuration if necessary by applying any relevant breaking changes.

### Migrate Content[](#migrate-content)

When you update Wowchemy itself, you can jump straight to the latest and greatest version. However, content migration requires consecutively applying any relevant steps from each release.

To migrate your TOML/YAML front matter and configuration, apply any relevant steps from the _Breaking Changes_ section of each **consecutive [release note](/blog/)** since the version you were originally on. If a release has no _Breaking Changes_ section, then no changes are required.

For example, if you are updating from _v2.4.0_ to _v3.1.0_, then apply the breaking changes for the relevant **consecutive** releases. In this case, that would require **first** applying the breaking changes from v3.0.0 **and then** applying the breaking changes from v3.1.0.

To help migrate content to be compatible with new versions of Hugo and Wowchemy, there are some scripts available in the **[Hugo Scripts](https://github.com/wowchemy/hugo-assistant)** repository which you might find useful.

Troubleshooting[](#troubleshooting)
-----------------------------------

Check out the release notes for the consecutive version that you are updating to, paying attention to the **Breaking Changes** section. You can check which version you currently have, refer to the _Preparation_ section above.

If there are any issues after updating, you may wish to **compare your site with one of the latest templates**, such as the [Academic Template](https://github.com/wowchemy/starter-academic/) to check if the file structure changed, any TOML/YAML settings changed in the configuration files (i.e. all files in the `config/_default/` folder), or any options changed in the [front matter](/content/front-matter/) of content files (i.e. files in the `content/` folder).

**If you overrided any Wowchemy/Academic theme files** by using Hugo’s inheritance principle then these may cause conflicts after updating. For example, if you have modified theme files in a `layouts` folder, your modifications may have become out of sync with the theme they were copied from. Consider temporarily removing your overrides and checking if the original file(s) that you are overriding have changed in any way and require syncing with your custom version of the file(s).

**Solve common issues with the [Troubleshooting Guide](/hugo-tutorials/troubleshooting/)**. If the issue is unresolved, feel free to reach out to the community on Discord or the Forum with your GitHub project link.

### Ref
Hugo Blox, [Update](https://bootstrap.hugoblox.com/hugo-tutorials/update/)

## Get a domain name



### Ref
Hugo Blox, [Get a domain name](https://bootstrap.hugoblox.com/hugo-tutorials/domain/)

## Language and translation



### Ref
Hugo Blox, [Language and translation](https://bootstrap.hugoblox.com/hugo-tutorials/language/)

## Add analytics



### Ref
Hugo Blox, [Add analytics](https://bootstrap.hugoblox.com/hugo-tutorials/analytics/)

## Add search



### Ref
Hugo Blox, [Add search](https://bootstrap.hugoblox.com/hugo-tutorials/search/)

## Extending Wowchemy



### Ref
Hugo Blox, [Extending Wowchemy](https://bootstrap.hugoblox.com/hugo-tutorials/extending-wowchemy/)

## Social media sharing



### Ref
Hugo Blox, [Social media sharing](https://bootstrap.hugoblox.com/hugo-tutorials/page-sharer/)

## Search Engine Optimization

How can you perform more advanced customization or integrate new third-party services?

## Hooks

The Hugo hooks system enables you to easily inject your own code into parts of a site for more advanced customization. No need to edit or override any of the theme’s files!

The following hooks are supported (as of v5.6-dev):

* head-start
* head-end
* body-end
* footer-start
* toc-start (for the right sidebar table of contents only)
* toc-end (for the right sidebar table of contents only)

To inject your code into one of the above places, create a file at `layouts/partials/hooks/<hook>/<your-filename>`.html, replacing `<hook>` with one of the hook names above and `<your-filename>` with any name, such as `custom`. You’ll need to create these new folders relative to the root of your site.

For example, to inject your code into the site head, you can create a file at `layouts/partials/hooks/head-end/custom.html`.

You can have multiple files in each hook folder, with Hugo determining the order which they are rendered in.

### Add scripts (JS)

How can I add custom Javascript to my site, such as a third-party analytics script?

Create a file at `layouts/partials/hooks/body-end/custom.html` and paste your Javascript `<script>...</script>` within it.

*For older sites prior to v5.6, create a file at `layouts/partials/custom_js.html` instead.*

### Custom head

How can I add custom **metadata** to my website’s `<head>` tag?

Create a file at `layouts/partials/hooks/head-end/custom.html` and paste your HTML tags within it.

*For older sites prior to v5.6, create a file at `layouts/partials/custom_head.html` instead.*

Tip: This approach can also be used for adding third party scripts with an async or defer attribute to the site head.

## Customize style (CSS)

To personalize Wowchemy, you can **choose a colour theme and font set** in `config/_default/params.yaml`.

For further personalization, you can **create your own colour theme and font theme**.

If advanced style customization is required, **CSS code** can be written to override or enhance the existing styles:

1. Create the `assets/scss/` folder if it doesn’t exist
2. Create a file named `custom.scss` in the `assets/scss/` folder
3. Add your custom CSS code to the file you created and re-run Hugo to view changes

### Override a template

Hugo uses a [template lookup](https://gohugo.io/templates/lookup-order/) which enables you to override any of Wowchemy’s files without directly changing them. This can make it easier to update Wowchemy in the future since you do not modify any of Wowchemy’s files directly.

Alternatively, you might wish to:

* [Create a new widget](https://github.com/wowchemy/wowchemy-widget-starter)
* [Create a new shortcode](https://gohugo.io/content-management/shortcodes/)

To override a template in the theme, you simply copy the file you are interested in from the version of the [Wowchemy module](https://github.com/wowchemy/wowchemy-hugo-themes/tree/main/modules/wowchemy) your site uses and paste it in your site folder using a similar path. To choose your version, select its tag from GitHub’s dropdown *master* box on the upper left and press enter.

To understand how this works, you should familiarize yourself with template lookup. Finally, when you update Wowchemy, remember to compare your version of the file against Wowchemy’s one, in case you need to propagate any changes across.

For example, say we wish to add some HTML code to the navigation bar. Let’s copy the relevant file `wowchemy/layouts/partials/navbar.html` to `layouts/partials/navbar.html` at the root of your site, creating the `layouts/partials/` folders if they do not already exist. Now you can add the HTML code you want to your copy of the file, which will override Wowchemy’s version.

## Permalinks

*Permalinks*, or *permanent links*, are URLs to individual pages and posts on your website. They are permanent web addresses which can be used to link to your content. Using Hugo’s *permalinks* option these can be easily customized. For example, the blog post URL can be changed to the form *yourURL/2016/05/01/my-post-slug* by adding the following near the end of your `config/_default/config`.yaml:

```yaml
permalinks:
  post: '/:year/:month/:day/:slug'
```

Where `:slug` defaults to the filename of the post, excluding the file extension. However, slug may be overridden on a per post basis if desired, simply by setting `slug: my-short-post-title` in your post preamble.

**Example 2**: let’s consider changing the URL path of posts from `post/` to `blog/`. First, add the following parameters to your `config/_default/config.yaml`:

```yaml
permalinks:
  post: '/blog/:slug'
```

Then add `aliases: [/blog/]` to your post archive page at `post/_index.md` so that it can be accessed from the */blog/* URL.

## Theming Custom Integrations

**How can you theme your customizations and third-party plugins according to the user’s light/dark mode?**

Theming can be performed with styles and/or JS.

Plugins can be themed by creating a custom style (see Style section above) and prefixing dark components with `.dark` such that you might have:

```yaml
/* Light component */
.your-class {color: black;}
/* Dark component */
.dark .your-class {color: white;}
```

Furthermore, Wowchemy v5.0.0+ emits a `wcThemeChange` event to help support themeable user plugins.

One can add a custom `local` JS script (see Scripts section above) and listen to the event.

For example, adding the following snippet to a custom JS script referenced in `params.yaml` outputs the theme change events to the browser console:

```js
document.addEventListener('wcThemeChange', (e) => 
  console.log('isDarkTheme? ' + e.detail.isDarkTheme())
);
```

### Ref
Hugo Blox, [Search Engine Optimization](https://bootstrap.hugoblox.com/hugo-tutorials/seo/)

## Security



### Ref
Hugo Blox, [Security](https://bootstrap.hugoblox.com/hugo-tutorials/security/)

## Optimize performance



### Ref
Hugo Blox, [Optimize performance](https://bootstrap.hugoblox.com/hugo-tutorials/performance/)

## Add comments



### Ref
Hugo Blox, [Add comments](https://bootstrap.hugoblox.com/hugo-tutorials/comments/)

## Build an offline site



### Ref
Hugo Blox, [Build an offline site](https://bootstrap.hugoblox.com/hugo-tutorials/offline-site/)

## Troubleshooting



### Ref
Hugo Blox, [Troubleshooting](https://bootstrap.hugoblox.com/hugo-tutorials/troubleshooting/)
