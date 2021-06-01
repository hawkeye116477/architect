# The Architect theme

*Architect is a port of Jekyll theme to Hugo. You can [preview the theme to see what it looks like](https://hugo-architect-theme-demo.netlify.com/), or even [use it today](#usage).*

## Usage
Just run terminal in directory where you have your site and add submodule with command:
```sh
git submodule add https://github.com/hawkeye116477/hugo-architect-theme.git themes/hugo-architect-theme
```
and then, add the following to your site's `config.toml`:

```toml
theme = "hugo-architect-theme"
```

## Customizing

### Configuration variables

Architect will respect the following variables, if set in your site's `config.toml`:

```toml
title = "The title of your site"
[params]
 description = "A short description of your site's purpose"
```

Additionally, you may choose to set the following optional variables:

```toml
 pygmentsCodeFences = "true" # to enable syntax highlighting in code fences with a language tag in markdown
 pygmentsUseClasses = "true" # to use CSS classes to format your highlighted code (The Architect theme has rouge-github.scss with rules for classes)

[params]
 show_downloads = "true" # to enable providing download URLs to your repo on sidebar
 use_sass = "true" # to enable processing of SCSS files by Hugo Pipes (requires extended version of Hugo, currently doesn't supported by Netlify)
 gh_repo_owner = "OwnersUsernameOfGitHubRepository"
 gh_repo_name = "NameOfYourGitHubRepository"
 google_site_verification = "1234" # for verifying ownership via Google webmaster tools

# Alternatively, verify ownership with several services at once using the following format:
 [params.webmaster_verifications]
  bing = "1234"
  google = "1234"
  alexa = "1234"
  yandex = "1234"
  baidu = "1234"
```

### Stylesheet

If you'd like to add your own custom styles:

**Method 1 (scss, requires extended version of Hugo)**
1. Create a file called `/assets/sass/style.scss` in your site
2. Add the following content to the top of the file, exactly as shown:
    ```scss

    @import 'hugo-theme-architect';
    ```
3. Add any custom CSS (or Sass, including imports) you'd like immediately after the `@import` line

*Note: If you'd like to change the theme's Sass variables, you must set new values before the `@import` line in your stylesheet.*

**Method 2 (css)**
1. Create css files inside static directory in your main site's directory.
2. Add to config.toml similar code to this:
```toml
[params]
 custom_css = ["css/yourcss1.css", "css/yourcss2.css"]
```


### Layouts

If you'd like to change the theme's HTML layouts, you can just copy chosen layout from **layouts** directory from themes original files, paste that file into newly created **layouts** directory in your site's main directory and edit what you want.

## Roadmap

See the [open issues](https://github.com/hawkeye116477/hugo-architect-theme/issues) for a list of proposed features (and known issues).

## Project philosophy

The Architect theme is intended to make it quick and easy for Hugo users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying default layouts). It should also look great, but that goes without saying.

