# Kiwix-Serve
[Kiwix-Serve](https://www.kiwix.org/en/downloads/kiwix-serve/) is a .zim compatible web server: it allows you to deliver .zim files over the HTTP protocol within your local network – be it a University or your own house. 

Simply start Kiwix-Serve on your machine, and your content will be available for anybody through their web browser.


## Kiwix
Kiwix is an offline reader for online content like Wikipedia, Project Gutenberg, or TED Talks.  It makes knowledge available to people with no or limited internet access.

The Kiwix tools is a collection of Kiwix related command line tools:

- kiwix-manage: Manage XML based library of ZIM files
- kiwix-read: Read ZIM file content
- kiwix-search: Fulltext search in ZIM files
- kiwix-serve: HTTP daemon serving ZIM files

### kiwix-manage example
```console
kiwix-manage /srv/www/htdocs/pub/library_zim.xml add /zimfiles/test.zim 
```

Full [kiwix-manage](https://wiki.kiwix.org/wiki/Kiwix-manage) Readme

### kiwix-serve example

```console
kiwix-serve --library /srv/www/htdocs/pub/library_zim.xml
```  

Full [kiwix-serve](https://wiki.kiwix.org/wiki/Kiwix-serve) Readme

# Chart Info

Configuration file (values.yaml) for Kiwix Helm chart in its simplest form is as follows. It has a value to specify the namespace where the app is going to deployed and contained in , the image and storage its going to use.

```yaml
namespace: kiwix

image:
  repository: smuse/suse-bci-kiwix-serve
  tag: "3.2.0"
  args: []
  env:
  - name: DOWNLOAD
    value: https://download.kiwix.org/zim/wikipedia_bm_all.zim

storage:
  volume_name: kiwix-pvc
  storage_size: 250Gi
```

Kiwix's helm chart can be either be configured using `values.yaml` file or through Rancher's GUI. 


<!-- You can either specify a remote zim file or pass local zim file or library.xml file through the args option.

```yaml
...
  args: 
    - ethiopian_folktales.zim
    - wikipedia_bm_all.zim
  env: []
``` -->

## TODO

- [ ] guide for creating zim files from static html files
- [ ] adding chart to Rancher
- [ ] guide for crearting library.xml file
- [ ] add readiness probe
