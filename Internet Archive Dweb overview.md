#Internet Archive Dweb overview

This document is a higher level overview of the different parts that make up the Dweb project at the Internet Archive.

THIS DOC IS A WORK IN PROGRESS BEING CULLED FROM OTHER OBSOLETE DOCS ...

Our libraries are a stack intended to make it easy to write applications for the Dweb on top of multiple technologies.

At the base level is **dweb-transports**, which provides a common API for different Dweb technologies. 

Currently supported are: IPFS; WEBTORRENT; GUN; YJS; and HTTP but its easy to add support for new technologies.

A management object is created that can be loaded into Node or a Web Browser and passed URLs to perform actions on:
files (fetch, open a stream or store); on lists (append or list); on tables (set, get, keys etc). 

In particular it is designed to allow fallback so that a resource can be for example requested from IPFS with fallback to HTTP on failure.

On top of this is build **dweb-objects** which provides a set of classes to manipulate higher level objects like 
dictionaries; lists; and tables; and some high level functionality for authentication; name resolution etc.

The decentralized UI for the Archive itself. dweb.archive.org is implemented in **dweb-archive** which includes:
classes to manipulate Internet Archive concepts like Collections, Items, Files and Searches;
and the HTML/Javascript UI.

Between dweb.archive.org and the Archives servers sits **dweb-gateway**, a python server that knows how to access
IA servers, and how to talk to super-peers for the different technologies.

In **dweb-transport** are the Javascript super peers for GUN, and WEBTORRENT (Seeder & Tracker), both of these are 
slightly modified to map IA resources into their technologie. 

**dweb-servicework** is an experimental attempt at a service-worker version, it doesn't work that well yet due to 
limitations in what Service Workers can do. 
There is also **dweb-ext** which provides an alternative via downloadable extensions either with, or without the 
current Wayback Machine extension functionality.

#### Moving forward 

**dweb-mirror** is where the most active development is taking place, building a set of tools to support access to IA 
resources where the internet is unavailable because of cost, bandwidth or censorship.

See [Dweb document index](https://github.com/internetarchive/dweb-transports/blob/master/DOCUMENTINDEX.md) for a list of the repos that make up the Internet Archive's Dweb project, and an index of other documents. 

#### Support status

Technology|Files|Streams|Lists|Tables|Events|Notes
----------|-----|-------|-----|------|------|-----
IPFS|Y|Y|N|N|N|Table & List support via YJS
WEBTORRENT|Y|Y|N|N|N|
GUN|N|N|Y|Y|Y|Also including hijacking of specific paths to fetch metadata
YJS|N|N|Y|Y|Y|Over IPFS as transport
HTTP|Y|Y?|Y|Y|N|Good as a fallback for any technology