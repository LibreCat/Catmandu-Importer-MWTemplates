# NAME

Catmandu::Importer::MWTemplates - extract MediaWiki template data

# STATUS

[![Build Status](https://travis-ci.org/LibreCat/Catmandu-Importer-MWTemplates.png)](https://travis-ci.org/LibreCat/Catmandu-Importer-MWTemplates)
[![Coverage Status](https://coveralls.io/repos/LibreCat/Catmandu-Importer-MWTemplates/badge.png)](https://coveralls.io/r/LibreCat/Catmandu-Importer-MWTemplates)
[![Kwalitee Score](http://cpants.cpanauthors.org/dist/Catmandu-Importer-MWTemplates.png)](http://cpants.cpanauthors.org/dist/Catmandu-Importer-MWTemplates)

# DESCRIPTION

# SYNOPSIS

Command line client `catmandu`:

    catmandu convert MWTemplates --file example.wiki 
    catmandu convert MWTemplates --site en --page Feminis
    catmandu convert MWTemplates --site de --page Feminism --template Literatur
    

# DESCRIPTION

This [Catmandu::Importer](https://metacpan.org/pod/Catmandu::Importer) extracts [MediaWiki
Templates](http://www.mediawiki.org/wiki/Help:Templates) from wiki pages.

# CONFIGURATION

- site

    The MediaWiki site to get data from. This must either be a base URL such as
    [http://en.wikipedia.org/](http://en.wikipedia.org/) or a Wikipedia name tag, such as `en`. If no site
    is specified, the input is read from `file` or standard input as wiki markup.

- page

    A wiki page to get data from.

- template

    A template to extract data for. If not specified, all templates will be
    extracted with the template name if field `TEMPLATE`.

- tempname

    The field to store template name in. Set to `TEMPLATE` by default.

- wikilinks

    Keep wikilinks if set to 1 (default). If disabled (0), links will be
    transformed to plain text. If set to 0, links will be transformed to their link
    target.

# METHODS

See [Catmandu::Importer](https://metacpan.org/pod/Catmandu::Importer) for general importer methods.

# SEE ALSO

[Catmandu::Wikidata](https://metacpan.org/pod/Catmandu::Wikidata)

The core parsing method is based on a script originally created by Erich
Zachte: [http://meta.wikimedia.org/wiki/User:LA2/Extraktor](http://meta.wikimedia.org/wiki/User:LA2/Extraktor)

# COPYRIGHT AND LICENSE

Copyright Jakob Voss, 2015-

This is free software; you can redistribute it and/or modify it under the same
terms as the Perl 5 programming language system itself.
