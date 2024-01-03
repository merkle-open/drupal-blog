# Merkle Drupal & Acquia Blog
### Merkle developers blog about Drupal and Acquia.

## Installation on your local machine
[Install Hugo](https://gohugo.io/installation/)

```
git clone --recurse-submodules git@github.com:merkle-open/drupal-blog.git
cd drupal-blog
hugo server
```

## Usage
1. Create a folder for your new post under /content/post/[YEAR]/[MONTH]/[NAME-OF-YOUR-POST]
2. Create an `index.md` file and add your content using markdown ([Basic markdown writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax))
3. If you need images, create an `images` folder to add them there
4. When you are done, commit your files
5. GitHub Action will automatically build the page and deploy it.

**Note:** if you don't have the permission to push to this repository, create a Pull Request and assign a maintainer of the [merkle-open Drupal team](https://github.com/orgs/merkle-open/teams/drupal).

## Credits
["Beautiful Hugo" Theme](https://themes.gohugo.io/themes/beautifulhugo/)
