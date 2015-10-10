# API Documentation for ur.ly Web Application #

## Create a New ur.ly ##

All requests must be made using HTTP GET. The href parameter should be URL-encoded.
  * http://ur.ly/new?href={href} - Create a new ur.ly and redirect to it (not useful, we know)
  * http://ur.ly/new.html?href={href} - Create a new ur.ly and show in HTML format
  * http://ur.ly/new.json?href={href} - Create a new ur.ly and show in JSON format
  * http://ur.ly/new.xml?href={href}    - Create a new ur.ly and show in XML format

### HTTP Status Codes ###
  * 200 - We created (or found, if it already exists) an ur.ly and will display in requested format
  * 302 - Used when redirecting to target HREF
  * 400 - There was a problem with the href parameter.

## Lookup an ur.ly ##

All requests must be made using HTTP GET. The code parameter is 1-6 character alpha-numeric.

  * http://ur.ly/{code}       - Redirect an ur.ly to its target HREF
  * http://ur.ly/{code}.html  - Display an ur.ly in HTML format
  * http://ur.ly/{code}.json  - Display an ur.ly in JSON format
  * http://ur.ly/{code}.xml   - Display an ur.ly in XML format

### HTTP Status Codes ###

  * 200 - We found the ur.ly and will display in requested format
  * 302 - Used when redirecting to target HREF
  * 404 - We couldn't find the requested ur.ly

## ur.ly Formats ##

ur.ly records can be displayed in HTML, JSON and XML formats.

Examples in JSON and XML formats:

  * JSON:
```
{"code":"1","href":http://www.google.com/"}
```

  * XML:
```
<urly code="1" href="http://www.google.com/"/>
```