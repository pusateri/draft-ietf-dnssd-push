# draft-ietf-dnssd-push
DNSSD Working Group Internet Draft for DNS Push Updates



If you get this error, it is due to an incorrect XML header in the XEP reference.

```
xml2rfc draft-ietf-dnssd-push.xml -o draft-ietf-dnssd-push.txt --text
Parsing file draft-ietf-dnssd-push.xml
ERROR: Unable to parse the XML document: draft-ietf-dnssd-push.xml
 /Users/pusateri/.cache/xml2rfc/reference.XSF.XEP-0060.xml: Line 1: Space needed here
 draft-ietf-dnssd-push.xml: Line 274: Failure to process entity XEP-0060
 draft-ietf-dnssd-push.xml: Line 274: Entity 'XEP-0060' not defined
make: *** [draft-ietf-dnssd-push.txt] Error 1
```

Edit your `~/.cache/xml2rfc/reference.XSF.XEP-0060.xml`

and add the encoding to the first line as shown in the patch below:


```
 1c1
 < <?xml version="1.0"?>
 ---
 > <?xml version='1.0' encoding='UTF-8'?>
```

