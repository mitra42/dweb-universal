# Naming in the Dweb

First draft 26 August 2018 by Mitra mitra@archive.org

PROJECT ABANDONED STILL A GOOD IDEA BUT TOO MUCH WORK TO PUSH ! 

This document is a write up of three conversations I had at the [Decentralized Web Summit](https://decentralizedweb.net), 
with Juan Benet of Protocol Labs, Mark Nadal of GUN and Irakli Gozalishvili of Mozilla.

Until this paragraph is removed/modified, it should not be taken as agreement by Juan, Mark or Irakli to the proposals below.

## Goal

In order to build complex systems you need to be able to refer to documents and resources in some part of the Dweb (or Centralized Web ("Cweb)) 
from somewhere else in the Dweb (or Cweb).

Some examples:
 
To bootstrap into the Dweb, we use http patterns that can be served by an http server, 
or - if recognized by our extension - go straight to the Dweb.

In dweb.archive.org we use GUN for our mutable data, but want to put pointers that say a document can be retrieved from IPFS, WebTorrent or HTTP

If we were to use IPLD, we'd want to be able to have pointers out from IPLD to HTTP, or GUN or WebTorrent. 

Of course, we could just add a field - to a GUN dictionary, or to IPLD, 
but that would have no semantic meaning to the system in which it resides.
In practice, since this gives us the disadvantages of using a proprietrary data structure with none of the advantages of that 
data structure having meaning, so we ended up storing raw JSON in both IPFS and GUN. 

Some sub-goals for interoperability would be.

* Recognizable URLs, as defined by each system's developers, that can be understood as strings in the other systems.
* An understood way to interoperably resolve names across and within systems. 

## Straw person

* Each technology should allow URI's for other (Dweb or Cweb) technologies in places which would otherwise have internal pointers.
* Implementation detail is internal, for example it could be implemented with a different field name, or a flag etc
* When resolving a path, the system when it encounters a external pointer will either:
    * Know enough about a URI to continue resolution in that technology
    * Call out to a optional "resolver" that can be configured by an external app (e.g. in the options passed at start)
    * When calling the resolver it will pass the URL, any remaining path and there will be space for options arguments.
    
    
An example could be .... 

If IPFS has at Q12345 a IPLD which contains { a: gun:/x }

ipfs.start({ resolver: foo })
ipfs.cat(Q12345/a/b)

Would either: 
* Know enough about gun to call gun with  get gun:/x/b
* OR call foo("gun:/x", "b")

## Multi URL
Where possible a resolver should be able to recognize an array of equivalent URIs and fallback if it is unable to resolve some of them, 
For example `[ ipfs/multihash/path, https:foo.com/path ]` means to try and retrieve via IPFS first, and if that fails then fallback to a HTTPS address.

## URI's recognized 

Because there is a lot of ambiguity about what should be the canonical URI's for Dweb resources, 
the following patterns (and any subpath's of them) should be supported by any resolver. 

Rule|Notes
----|-----
`http[s]://dweb.domainname/internal`|proto = "arc", as used by bootloader.html
`http[s]://dweb.proto.domainname/internal`|`domainname` is ignored by GUN and IPFS, used by ARC
`http[s]://gateway/proto/internal`|Only where `gateway` is in a known set (inc IPFS gateways)
`dweb:[/]/proto/internal`|This is Juan's preferred canonical format
`proto:[/]/internal`|Includes Canonical magnet links, and is the preferred format of Irakli
`proto:[/]/proto/internal`|Behavior is undetermined if the two `proto` don't match.
`[/]proto/internal`|
`[/]dweb/proto/internal`|
 
This covers all the formats that we believe are in use at:
* Protocol labs (IPFS, IPNS; IPFS Companion); 
* GUN; 
* Internet Archive (bootloader, arc, dweb-ext, contenthash)
* Torrent (inc WebTorrent, Magnet)

#### Notes
Note that in general :/ and :// are treated identically because of the likelihood of miss-entry by people more familiar with the // format.


### Internal formats
`internal` is the internal use inside a protocol. Examples of usage in each protocol are:

proto|internal|example|notes
-----|--------|-------|-----
IPFS|multihash/path|ipfs/Q123456/a/b/c|Q123456 is a multihash of a IPLD, and /a/b/c is a path within that IPLD and potentially out to other protocols
IPNS|pubkey/path|ipns/TBD/a/b/c|pubkey refers to a signed IPNS name and refers to an equivalent IPFS/multihash
GUN|path|gun:/a/b/c or gun:a.b.c|Internally gun uses ".", will support "/"
TORRENT|[aa=bb]+/path|magnet:|a set of key value pairs especially the BTIH and trackers
ARC|/domain/path|/arc/archive.org/details/foo|Refers to a named system and always resolves to a set of HTTP or Dweb URIs and remaining paths
CONTENTHASH|multihash|contenthash/Q123456|Multihash of the hash of the content

## Bootstrapping via DNS 
In addition a system may recognize the DNS TXT record that IPFS is looking for .

TODO define that format 

So that if this contained TBD then `http://domainname/path` 
would resolve to `ipfs:/multihash/path`

We aren't currently aware of this method being used by any other protocol.

## Current support.

The following tools support all, or a subset of this functionality.

#### @internetarchive/dweb-objects/TBD/bootloader.html

`bootlader.html` is typically pointed to by a nginx or similar configuration file so that it loads for any URL at `https://dweb.domainname`.

Once loaded in a browser it will examine its calling URL, or a url=xxx parameter and apply rules to resolve, retrieve and open a resource at that address.

Currently it only supports `http[s]://dweb.domainname/path` 
which will be converted to `dweb:/arc/domainname/path` 
and resolved through Domain.js (below)

#### @internetarchive/dweb-ext (extension): 
This extension, when activated, recognizes the same URLs as `bootloader.html` and uses `Domain.js` in the same manner, for quicker boot.

It will be merged into the Archive's WayBack extension to support archiving of these dweb urls.

#### @internetarchive/dweb-objects/Domain.js 
Resolves name patterns in a hierarchical naming structure across multiple protocols,
and can be used to retrieve and/or boot into resources. It uses @internetarchive/dweb-transports to support multiple protocols including IPFS, GUN, WEBTORRENT, YJS and HTTP(S).

It currently only recognizes a subset of the patterns above but will be extended to handle them all.

#### IPFS Companion 
TBD

#### Mozilla's Firefox extension (called what?) running on Firefox nightly builds only
TBD

#### GUN
TBD

## Some random Notes

### /arc and Archiving

The Internet Archive will archive urls in the `/arc` namespace, the details of that archiving are TBD. 
The Archive will also support others who want to archive it, for example by providing a feed of URLs discovered.
