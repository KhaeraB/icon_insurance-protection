# icon_insurance-protection
Icon for private or commercial use and dedicated to the insurance sector


Comments on archive content
---------------------------

- /font/* - fonts in different formats

- /css/*  - different kinds of css, for all situations. Should be ok with 
  twitter bootstrap. Also, you can skip <i> style and assign icon classes
  directly to text elements, if you don't mind about IE7.

- demo.html - demo file, to show your webfont content

- LICENSE.txt - license info about source fonts, used to build your one.

- config.json - keeps your settings. You can import it back to fontello anytime,
  to continue your work


Why so many CSS files ?
-----------------------

Because we like to fit all your needs :)

- basic file, <your_font_name>.css - is usually enougth, in contains @font-face
  and character codes definition

- *-ie7.css - if you need IE7 support, but still don't wish to put char codes
  directly into html

- *-codes.css and *-ie7-codes.css - if you like to use your own @font-face
  rules, but still wish to benefit of css generation. That can be very
  convenient for automated assets build systems. When you need to update font -
  no needs to manually edit files, just override old version with archive
  content. See fontello source codes for example.

- *-embedded.css - basic css file, but with embedded WOFF font, to avoid
  CORS issues in Firefox and IE9+, when fonts are hosted on the separate domain.
  We strongly recommend to resolve this issue by `Access-Control-Allow-Origin`
  server headers. But if you ok with dirty hack - this file is for you. Note,
  that data url moved to separate @font-face to avoid problems with <IE9, when
  string is too long.

- animate.css - use it to get ideas about spinner rotation animation.


Attention for server setup
--------------------------

You MUST setup server to reply with proper `mime-types` for font files. In other
case, some browsers will fail to show fonts.

Usually, `apache` already has necessary settings, but `nginx` and other
webservers should be tuned. Here is list of mime types for our file extentions:

- `application/vnd.ms-fontobject` - eot
- `application/x-font-woff` - woff
- `application/x-font-ttf` - ttf
- `image/svg+xml` - svg

