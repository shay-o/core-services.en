---
title: api methods - id synchronization by url or data source
description: id synchronization by url or data source for the adobe experience cloud id service api
seo-title: adobe experience cloud id service api methods - id synchronization by url or data source
seo-description: id synchronization by url or data source for the adobe experience cloud id service api
short-title: id sync
doc-type: reference
audience: admin
index: true
translate: true
version: false
private-feature-pack: false
beta: false
redirect: false
product: core services id service
cloud: experience cloud
archetype: admin
user-guide: id service admin guide
git-edit: https://git.corp.adobe.com/AdobeDocs/core-services.en/tree/master/help/id-service/id-service-api/id-service-api-methods/id-service-api-methods-idsync.md
git-issue: https://git.corp.adobe.com/AdobeDocs/core-services.en/issues/new
git-repo: https://git.corp.adobe.com/adobedocs/core-services.en
---
<!--Meta Data Values

**Required Meta for search optimization and page data**

title: free text string

description: free text string

seo-title: free text string

seo-description: free text string

**Optional Meta for extended capabilities**

audience:
all (default), admin, developer, end-user
 
index: true (default), false
 
translate:
true (default), false
 
doc-type:
reference (default), tutorials

version:
false (default), Classic, Standard, 6.5, 6.4, 6.3, 6.2
 
private-feature-pack:
false (default), true
 
beta:
false (default), true
 
redirect:
false (default), pathname
-->

# ID Synchronization by URL or Data Source

The ID service functions `idSyncByURL` and `idSyncByDataSource` let you manually implement an ID sync in the Destination Publishing iFrame. These are available in `VisitorAPI.js` versions 1.10, or higher.


## Syntax

| Code                            | Synchronized User IDs                                                                                                 |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `visitor.idSyncByURL();`        | Between different data partners and Audience Manager by using a custom ID sync URL.                                   |
| `visitor.idSyncByDataSource();` | When you already know the DPID and DPUUID and want to send it to Audience Manager in the standard ID sync URL format. |

## Properties

The following table lists and defines the properties available to both functions.

| Name            | Type   | Description                                                                                           |
| --------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| `dpid`          | String | Data provider ID assigned by Audience Manager.                                                        |
| `dpuuid`        | String | The data provider's unique ID for the user.                                                           |
| `minutesToLive` | Number | \(Optional\) Sets the cookie expiration time. Must be an integer. Default is 20160 minutes (14 days). |
| `url`           | String | Destination URL.                                                                                      |

## Macros

Both functions accept the following macros:

+ `%TIMESTAMP%`: Generates a timestamp \(in milliseconds\). Used for cache busting.
+ `%DID%`: Inserts the Audience Manager ID for the user.
+ `%HTTP_PROTO%`: Sets the communication protocol \(`http` or `https`\).

## Sample Code and Output

Both functions return `Successfully queued` if successful. They return an error message string if not.

### visitor.idSyncByURL

**Sample Code**

```javascript
//Instatiate Visitor
var visitor = Visitor.getInstance("MARKETING-CLOUD-ORG-ID-HERE",{});

// Fires url with macros replaced
visitor.idSyncByURL({
	dpid: '24', // must be a string
	url: '//su.addthis.com/red/usync?pid=16&puid=%DID%&url=%HTTP_PROTO%%3A%2F%2Fdpm.demdex.net%2Fibs%3Adpid%3D420%26dpuuid%3D%7B%7Buid%7D%7D',
	minutesToLive: 20160 // optional, defaults to 20160 minutes (14 days) 
});
```

**Sample Output**

`http://su.addthis.com/red/usync?pid=16&puid=28777806459181003670799219185178493848&url=http%3A%2F%2Fdpm.demdex.net%2Fibs%3Adpid%3D420%26dpuuid%3D%7B%7Buid%7D%7D`

### visitor.idSyncByDataSource

**Sample Code**

```javascript
//Instantiate Visitor
var visitor = Visitor.getInstance("MARKETING-CLOUD-ORG-ID-HERE",{});
// Fires 'http:/https:' + '//dpm.demdex.net/ibs:dpid=<dpid>&dpuuid=<dpuuid>'
visitor.idSyncByDataSource({
	dpid: '24', // must be a string
	dpuuid: '98765', // must be a string
	minutesToLive: 20160 // optional, defaults to 20160 minutes (14 days) 
});
```

**Sample Output**

`http://dpm.demdex.net/ibs:dpid=24&dpuuid=98765`

For more see [DIL idSync](https://marketing.adobe.com/resources/help/en_US/aam/r_dil_idsync.html)