MinimalXY Pelican Theme
=======================

MinimalXY [Pelican](https://getpelican.com/) theme is extended from [minimalX](https://github.com/art1fa/minimalX) by [art1fa](https://github.com/art1fa).

I made some improvements, polishing and SEO optimization. The main purpose of this fork is to keep everything simple and focus on content. I removed all unnecessary parts. You can see this theme live here: [blog.petrnohejl.cz](http://blog.petrnohejl.cz/).


Design focus
------------

- Minimal flat design
- Good usability, simple & intuitive navigation
- Focus on what's really important &ndash; your articles
- Presented in a clean and straightforward way


Features
--------

- Fully responsive and mobile-first
- Comments via Disqus integration
- Social media buttons
- W3.CSS CSS framework & HTML5 semantics


Screenshots
-----------

- [Screenshot #1](screenshot1.png)
- [Screenshot #2](screenshot2.png)


How to use
----------
### Javascript/Nunjucks/KeystoneJS
This template requires custom variables and is setup with some of the Keystone defaults.
To set variables in KeystoneJS set them either in the middleware `initLocals` function.
Or set them in the javascript file for the route, e.g. `gallery.js`.
They are set as locals.{variable_in_template_scope}, e.g.
`locals.section = 'example'` means that `{{ section }}` evaluates to `example`.
```javascript
//Keystone added variables
section = 'The first part of the url after the root';
data.post = {};//Information about the post if in a blog page
title = 'The value of the <title> element';

//Template added variables (these don't exist by default in nunjucks/keystone)
siteurl = 'www.example.com';
sitename = 'example website';

description = 'Page description for tag lines and meta tags'
```

Originally these value were set for the Python Pelican Theme.
```python
# Theme
THEME = '/path/to/MinimalXY'

# Theme customizations
MINIMALXY_CUSTOM_CSS = 'static/custom.css'
MINIMALXY_FAVICON = 'favicon.ico'
MINIMALXY_START_YEAR = 2009
MINIMALXY_CURRENT_YEAR = date.today().year

# Author
AUTHOR_INTRO = u'Hello world! I’m John Doe.'
AUTHOR_DESCRIPTION = u'Hello world! I’m John Doe. I like coffee, birds and Python.'
AUTHOR_AVATAR = 'http://www.gravatar.com/avatar/abcdefghijkl?s=240'
AUTHOR_WEB = 'http://mypersonalsite.com'

# Services
GOOGLE_ANALYTICS = 'UA-12345678-9'
DISQUS_SITENAME = 'johndoe'

# Social
SOCIAL = (
    ('facebook', 'http://www.facebook.com/johndoe'),
    ('twitter', 'http://twitter.com/johndoe'),
    ('github', 'https://github.com/johndoe'),
    ('linkedin', 'http://www.linkedin.com/in/johndoe'),
)

# Menu
MENUITEMS = (
    ('Categories', '/' + CATEGORIES_SAVE_AS),
    ('Archive', '/' + ARCHIVES_SAVE_AS),
)
```


License
-------

[MIT](LICENSE)
