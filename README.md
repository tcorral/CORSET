# CORSET
This is a method to break the Cross-domain policy with 'script' tags.

Maybe some people can say that the script tag is not under the Cross-domain policy, and this will be almost right.

The problem was to log uncaught errors with [Hermes.js](https://github.com/tcorral/Hermes.js) when the scripts are in
 different domains (subdomains, CDN...)

[Problem definition in stackoverflow](http://stackoverflow
.com/questions/5913978/cryptic-script-error-reported-in-javascript-in-chrome-and-firefox)

Please be carefull with this and only use it under your responsability.

## How to test problem:
* Use files in 'problem' folder.
* Put 'test.js' file in one external domain or simulate it with a proxy, [Fiddler](http://www.fiddler2.com/)...
* Put 'problem.html' in your localhost server.
* Open 'problem.html' url in your localhost server.
* Check the console and you will see one line with the 'Script Error' in line number 0.

## How to test solution:
* Use files in 'solution' folder.
* Put 'test.js' file in one external domain or simulate it with a proxy, [Fiddler](http://www.fiddler2.com/)...
* Put 'iframeXOrigin.html' file in the same external domain where 'test.js' file or simulate it with a proxy,
[Fiddler](http://www.fiddler2.com/)...
* Put 'XOrigin.html' in your localhost server.
* Open 'XOrigin.html' url in your localhost server.
* Check the console and you will see that the 'Script Error' in line number 0 doesn't exist anymore and you will see
instead an Hermes uncaught error type with file url and line number where the error exist.

## Do you want to collaborate?

All constructive comments are welcome. I promise I will answer everyone.

## Agreements

Thanks to [Manuel Flara](https://github.com/manuelflara) to notice me about [this issue](https://github
.com/tcorral/Hermes.js/issues/1).