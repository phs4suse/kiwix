# Kiwix-Serve
[Kiwix-Serve](https://www.kiwix.org/en/downloads/kiwix-serve/) is a .zim compatible web server: it allows you to deliver .zim files over the HTTP protocol within your local network – be it a University or your own house. 
Simply start Kiwix-Serve on your machine, and your content will be available for anybody through their web browser.

# Kiwix
Kiwix is an offline reader for online content like Wikipedia, Project Gutenberg, or TED Talks. 
It makes knowledge available to people with no or limited internet access.

## The Kiwix tools is a collection of Kiwix related command line tools:

- kiwix-manage: Manage XML based library of ZIM files
- kiwix-read: Read ZIM file content
- kiwix-search: Fulltext search in ZIM files
- kiwix-serve: HTTP daemon serving ZIM files

### kiwix-manage example
``` kiwix-manage /srv/www/htdocs/pub/library_zim.xml add /zimfiles/test.zim ```

Full [kiwix-manage](https://wiki.kiwix.org/wiki/Kiwix-manage) Readme

### kiwix-serve example
```kiwix-serve --library /srv/www/htdocs/pub/library_zim.xml```  

Full [kiwix-serve](https://wiki.kiwix.org/wiki/Kiwix-serve) Readme

# Chart Info
- something1
- something2
- something3

