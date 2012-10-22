CFML Security Tools
===================

This repository will contain some security tools / utilities for CFML (ColdFusion) developers.

## Example Usage

Copy the `securityutil.cfc` file into your project and then:

```cfm
<cfset securityUtil = CreateObject("component", "securityutil")>
<cfoutput>
	Hello #securityUtil.canonicalize(url.name)# <br /> <!--- ESAPI canonicalize --->
	Hello #securityUtil.encodeHTML(url.name)# <br /> <!--- ESAPI encodeForHTML --->
	Hello #securityUtil.scrub(url.name)# <!--- remove all but a-z0-9 --->
</cfoutput>
```