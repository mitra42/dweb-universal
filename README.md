# dweb-universal - Universal Access to All Knowledge - extending the Internet Archive

The Dweb Universal project's goal is to bring the Internet Archive's resources,
to places where the Internet is poor - either slow, expensive or censored. 

One core output is a set of tools called dweb-mirror (see below). 
Another will be increased integration of the Decentralized Web tools (IPFS, GUN, WebTorrent, etc) into the Archive.

Its a public project, discussion, disagreement, suggestions and help are all welcome. 

## Overview 
TODO - write something here ! 

An [diagram](https://github.com/mitra42/dweb-universal/blob/master/Dweb%20Universal%20architecture.pdf) 
with an overview of the architecture 

## Sub Projects

### [dweb-mirror](https://github.com/internetarchive/dweb-mirror) - cloning and serving portions of the Internet Archive.

This is the first code "output" of the project, currently (Aug2018) an incomplete work in progress. 
It is intended to clone some subset of the Archive, and will then serve them in at least IPFS, WebTorrent and hopefully GUN and DAT.

#### Status
The current version can:
* serve Archive content (collections, images, video, audio) stored locally  
* crawl a configurable set of Archive items to local storage
* proxy, storing as it serves. 

It currently (March 2019) runs on the:
* Rachel 3+ from WorldPossible
* Raspberry Pi - starting from NOOBS.
* Internet In A Box - running on a Raspberry Pi

Each of these has been installed, and will seed or fetch with IPFS. 

Coming soon:
* Automated installation on each of these platforms (its a a simple, but not fully automated install currently)
* Complete integration of IPFS, GUN, WebTorrent
* Better support for videos/audio (cache while streaming) and adding text, and web types
* More platforms

We are looking for test sites who want to use it. 

### Naming - how to name across systems

This outgrowth is to solve a problem that developers of complex systems have, how to reference Dweb urls across platforms,
and in particular how to make sense of a URL inside one system that points at another one.

See [naming doc](https://github.com/mitra42/dweb-universal/blob/master/naming.md) for first draft of naming structure proposed.

#### Status
Used in dweb-archive, but very much a background project

## See Also

The "[Awesome List](./awesomelist.md)" of organizations and projects in the space. 

Please see the following repos which together make up the Internet Archive's decentralized web project

* [dweb-transports](https://github.com/internetarchive/dweb-transports): Provides a common API & resiliency to decentralized tools - IPFS, WEBTORRENT, GUN, YJS, and a fallback to HTTP. 
* [dweb-objects](https://github.com/internetarchive/dweb-objects): Class interface to support Lists, Key Value Tables, Authentication, Naming etc across tools
* [dweb-archive](https://github.com/internetarchive/dweb-archive): The UI to dweb.archive.org, help make it more decentralized and more functional
* [dweb-serviceworker](https://github.com/internetarchive/dweb-serviceworker): Experimental (not really working well) addition of Service Workers
* [dweb-transport](https://github.com/internetarchive/dweb-transport]: Catch all for other projects, especially (currently) has the WebTor]rent superseeder/tracker
* [dweb-mirror](https://github.com/internetarchive/dweb-mirror): Experimental tool for mirroring parts of the Archive
* [dweb-gateway](https://github.com/internetarchive/dweb-gateway): Python gateway, runs at the Archive, runs the super-peers, and modifies metadata
* [dweb-universal](https://github.com/mitra42/dweb-universal): Meta-project for "Universal" access. *YOU ARE HERE*

