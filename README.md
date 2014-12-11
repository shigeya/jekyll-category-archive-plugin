# Category archive plugin for Jekyll

Generate a category archive like MovableType does.

This code is based on following hacks:

- https://gist.github.com/ilkka/707909
- https://gist.github.com/ilkka/707020
- https://gist.github.com/nlindley/6409459


# Installation

To use this plugin,

- Place the file `category_archive_plugin.rb` into `_plugins`
directory of Jekyll site working directory.

- Copy `_layouts/category_archive.html` into `_layouts` directory of
Jekyll site working directory, then edit it appropriately.


# Parameter configuration

Archive layout can be specified by `layout` key in the `category_archive`
site configuration. Default is `category_archive`.

Archive generation directory prefix can be specified by `path` key in the `category_archive`
site configuration. If specified, archive will be generated in
`PATH/CATEGORY/index.html`, where `PATH` is substituted by `path`, `CATEGORY` is the category
the archive for. Default is null string.

If the `slugify` key is set to `true`, then category URLs will be slugified.
ie: the url for "My Category" will be 'categories/my-category' not
'categories/My%20Category'

# Liquid variables for template

`page.category` contains the category name.

# Linking to a category archive

This plugin provides the custom liquid block tag, `categorylink`, which can be used to render a
link to a category's archive. For example:

```
{% categorylink foo %}This is a link to foo{% endcategorylink %}
```

Would create a link to the category archive of `foo` with the content "This is a link to foo". In
addition, if the name of a variable is specified instead of a category, the variable will be
expanded every time the tag block is rendered.


# Copyright

The MIT License (MIT)

Copyright (c) 2013 Shigeya Suzuki

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
