# starter
The new repository will generate with the same files and folders from [rundocs/starter][repo], You can [preview the theme to see what it looks like][preview], or even [generate it today][generate].

## start
```
make
make server
```

## site.pages
{% for item in site.pages %}
1. [{{ item.title | default: item.url }}]({{ site.baseurl | append: item.url }})
{%- endfor %}

## Roadmap
See the [open issues][issues] for a list of proposed features (and known issues).

## Documents
For full documentation, see: [https://jekyll-rtd-theme.rundocs.io][docs]

## The License
The theme is available as open source under the terms of the [MIT License][license].


[repo]: https://github.com/rundocs/starter/
[preview]: https://rundocs.github.io/starter/
[generate]: https://github.com/rundocs/starter/generate
[docs]: https://jekyll-rtd-theme.rundocs.io
[issues]: https://github.com/rundocs/jekyll-rtd-theme/issues
[license]: https://github.com/rundocs/jekyll-rtd-theme/blob/master/LICENSE
