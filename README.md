<!-- DO NOT EDIT ANYTHING BELOW THIS LINE -->

# integra.content

For image storage use [PostIMG](https://postimg.cc/)

## How to add new page

To add new page you need to create new file in the `content` directory. File name should be the same as page name.
For example if you want to add page named `about` you need to create file named `about.md`.
When you want to create a subpage you need to create a directory with the same name as subpage name and create
a new page in that directory. For example if you want to add subpage named `about` you need to create directory
named `about` and create file named `index.md` in this directory.

## What should be in the page

Every page should have the following snippet at the top of the file:

```yaml
---
created: <page creation date (YYYY-MM-DD)>
lastmod: <page last modification date (YYYY-MM-DD)>
head:
  meta:
    - name: keywords
      content: <page keywords>
    - name: robots
      content: index follow archive
    - name: author
      content: <author name>
    - name: copyright
      content: © 2023 KN Integra
---
```

This snippet is used to store information about the page. You can change the content of this snippet to your needs.

**Note:** You **must** use the provided snippet and update the `lastmod` key every time you change the page.

**Every pull request which doesn't update the `lastmod` key and
doesn't have the provided snippet at the top of the file will be rejected.**

## How to write content

To write content you need to use the markdown syntax. You can find more information about the markdown syntax
[here](https://www.markdownguide.org/).

## How to add new image

To add new image you need to use the image storage use [PostIMG](https://postimg.cc/) and copy the link to the image.
Then you can use this link in your markdown file.

## What you shouldn't do

- You shouldn't edit nor remove any file in the `root` and `docs` directory.
  This directory is used to store information about the website.
- You shouldn't edit nor remove the `README.md` file.
  This file is used to store instructions about the writing content for the website.
- You shouldn't edit nor remove the `index.md` file.
  This file is used to store information about the website.
- You shouldn't edit nor remove any file which is a page for HTTP method.
  This pages are used to display information about HTTP methods (eg. GET, POST, etc.).
- You shouldn't edit nor remove the `teapot.md` file.
  This file is used to store information about the HTTP 418 status code (**INCREDIBLY IMPORTANT**).
  - Really, don't remove this file. It's important.
