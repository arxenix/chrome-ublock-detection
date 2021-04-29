# Chrome uBlock detection

[Link](https://arxenix.github.io/chrome-ublock-detection/)


This page attempts to detect uBlock origin in **Chrome** by probing for 
`chrome-extension://cjpalhdlnbpafiamejdnhcphjbkeiagm/web_accessible_resources/noop.html`
and observing timing differences in comparison to a fake extension. 
It should work _even if you have the extension disabled for the page_.


This technique is impossible in firefox because firefox extensions'
`web_accessible_resources` are of the format
`moz-extension://<extension-UUID>/images/my-image.png`
where the `extension-UUID` is randomly generated for every browser instance in order to prevent fingerprinting.


Works as of uBlock 1.34.0 & Chrome 90.0.4430.93
