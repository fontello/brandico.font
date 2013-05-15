Brandico font
=============

[Demo page](http://fontello.github.io/brandico.font/demo.html)

Crowdsourced collection of popular logos, mostly for use in fontello. 
We have no goal to collect all possible logos here. Only popular ones, used at
websites, and missed in other collections:

- icons for links to pages in social networks
- messengers icons
- "login via..." icons


Installation
------------

This step is required, if you wish to contribute icons.

1. You need `node.js` 0.8+ and `fontforge` installed first.
2. run `npm install` in project folder
3. (optional) install [ttfautohint](http://www.freetype.org/ttfautohint/). Under
   Ubuntu just run `make dependencies` command. You can safely skip
   this step.


Contributing
------------

Note, we accept icons under pure CC BY license, without additional requirements.
Please, don't add icons, which require users to give links, mention author and
do any other kinds of promotion.

1. Create fork and clone your repo locally.
2. Add icon to `./src/svg_orig` folder
  - icon should be 1000x1000
  - black and white, no colors
  - no fills, filling is defined by contour direction
3. run `make dump`, it will automatically reoptimize images
4. check result in `./src/svg` folder. It should contain only on `path`
   in it. If you are satisfied, copy your image back to `./svg_orig`
5. Edit `config.yaml`, add your icon description there. Every icon MUST have
   unique id. You can generate those by command
   `node -e "for(var i=10; i>0; i--) console.log(require('crypto').randomBytes(16).toString('hex'));"`
6. That's not mandatory, but you can built font with `make dist` command
7. Commit content of `./src` folder and make pull request on github.
   _Attention! Don't commit font files!_ That can create unnesessary
   merge conflicts.

If this is difficult for you, just create new [ticket](https://github.com/fontello/brandico.font/issues)
and attach there your icon, as described in step 2, and icon description. We will
do the rest


License
-------

Font is distributed under
[SIL](http://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL) licence.

All icons are distributed under
[CC BY](http://creativecommons.org/licenses/by-sa/3.0/) licence.

We suggest to use this font via [fontello](http://fontello.com) project, but
you also can materials in any other way, if follow license.
