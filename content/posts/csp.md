+++ 
draft = false
date = 2020-05-03T21:02:24+12:00
title = "Content Security Policy"
slug = "" 
tags = []
categories = []
thumbnail = "images/tn.png"
description = ""
+++

## Content Security Policy
MDN web docs has a very comprehensive documentation about [Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy).

Some common directives:
* [connect-src](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/connect-src)
* [script-src](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/script-src)
* [report-to](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-to)
* [report-uri](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/report-uri)

## In-line Javascript code
If your website uses Google Analytics, you should be familiar with the following inline javascript code.
```javascript
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'UA-XXXXXXXX-X');
    </script>
```
To allow this inline javascript to be able to run on a CSP-enabled website, you'll have to:
* Add `unsafe-inline` in `script-src` directive (not recommended)
* Or explicitly add the hash code of the inline script in `script-src` directive. Use https://report-uri.com/home/hash to generate the hash.

## [Report URI](https://report-uri.com/)
If your website already has CSP, removing any of existing policy can potentially break the website. So, to be safe, don't remove any policies.

If you do need to clean-up some policies, instead of changing `Content-Security-Policy`, you can choose to use `Content-Security-Policy-Report-Only` to experiment on new CSP rules and report any violations without impacting the website.

`report-to` / `report-uri` can be used in `Content-Security-Policy-Report-Only` to report any violations without breaking the website. Go to [Report URI Setup](https://report-uri.com/account/setup/) to check the `report-uri` value and `report-to` API endpoint.

You can monitor the report for some time. If there are no violation reports, and you feel comfortable, you can go ahead to change `Content-Security-Policy` safely.

## [Security Headers](https://securityheaders.com/)
This lovely tool helps identify security issues of your website. You don't have to make your website perfect, however, having A+ score (or being in the Hall of Fame) is always something you shall be proud of or can 'show off' 😊
