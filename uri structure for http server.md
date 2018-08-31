#URI structure for HTTP server

This outlines the structure of the URIs that the HTTP server needs to understand.

See also [naming.md](https://github.com/mitra42/dweb-universal/blob/master/naming.md)
for a first draft of naming architecture. 

In the table below:

Abbrev|means
------|-----
$ROOT |File system root under which mirror is storing
$PATH |Remainder of URI
$ITEMID|Internet Archive standard item ids
$FILE|File name (within a standard IA item)
$URI|Full URI
Domain()|Passed to dweb-objects/Domain.js to resolve and return

URI|Handler|Notes
---|-------|-----
/arc/archive.org/metadata/$ITEMID|$ROOT/$ITEMID/$ITEMID_meta.json<br/>Domain($URI)|Check disk mirror<br/>then gun (which should fallback)<br/>then http
/gun/$PATH|transports.get("gun:/gun/$PATH")|GUN client > local peer > Remote peers
/ipfs/$PATH|transports.get("ipfs:/ipfs/$PATH")|IPFS which should fallback to https://ipfs.io
/arc/archive.org/download/$ITEMID/$FILE|$ROOT/$ITEMID/$FILE<br/>Domain($URI)|Look locally then try all dweb locations
/arc/*|Domain($URI)|Should resolve name, load and return or redirect

Typically Domain($URI) will be setup to:

URI|Handlers|Notes
---|--------|-----
/arc/archive.org/metadata|GUN, HTTP
/arc/archive.org/download|IPFS, WEBTORRENT, HTTP|Will check metadata to find IPFS/WEBTORRENT
