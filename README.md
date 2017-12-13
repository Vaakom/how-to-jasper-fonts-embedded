# HowToJasperFontsEmbedded
How to include new embedded fonts in Jasper Reports project. Arial font example.

Just create and simple jar file with new fonts and add it in your project path

************ From Jaspersoft WIKI *****************************************************************

This jar has mainly 3 fundamental concepts:

jasperreports_extension.properties - where is declared the factory for loading the fonts and the location of the font mapping xml within the jar.

fonts.xml - the font mapping xml 

And lastly, the font files themselfes in one of the accepted formats, being TTF, EOT, SVG or WOFF.

The jar structure should be somewhat like this, considering that the "path" can be any java valid path:

fonts-extension.jar
    /jasperreports_extension.properties
    /path/fonts.xml
    /path/font/*.TTF (or any of the above file types)
Pay attention for the property declared for containing the factory since the Jaspersoft Studio considers "net.sf.jasperreports.extension.registry.factory.fonts" and the JasperReports Server considers the "net.sf.jasperreports.extension.registry.factory.simple.font.families", at least for the 6.2 versions.
