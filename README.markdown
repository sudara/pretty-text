## Ain't that some pretty text!

Yo, this plugin will take text and on-the-fly create images using rmagick and supplied fonts.

### Whatchu need

This plugin depends on rmagick, so make sure you're all gemmed up!

### How to do it

Throw any fonts you like into /path/to/your/app/fonts and bada bing.

In your views call something like this:

    <%= pretty_text 'text you want rendered into an image', :font => 'Vera.ttf', :pointsize => '35px', :fill => '#CCCCCC' %>

you can also setup some psuedo constants to reuse styles sitewide.

In config/initializers/pretty_text.rb, you could have this, for example:

    Sudara::PrettyText.presets[:h1] = {
      :pointsize => 36,
      :background_color => 'transparent',
      :fill => 'black',
      :format => 'PNG',
      :font => 'SebastianMediumPro.otf'
    }

Allowing you to call:

    <%= pretty_text 'fancy anti-aliased rendered text', :h1 %>

NOTE: Images are generated and cached as needed, so no worries on the "OMG, my server performance"

Copyright (c) 2007 Sudara, released under the MIT license
