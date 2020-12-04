## Product Identity Disabler

A quick fix for issues with large product identities in headers, specifically caused by the `product_identities_extender` plugin.

Are you running Magento 2.3.x on Apache + PHPFPM?

Does your catalog search return a 500 error during the catalog search, and the error logs look something like
`[proxy_fcgi:error] [pid___] (22)Invalid argument: [client ip] AH01075: Error dispatching request to : , referer: yoursite.com/catalogsearch` ? It's probably because you have products with tons of configurable variations and Magento combines all of these into one massive header.

**Note**: This is just a quick fix I made for local development issues, run in production at your own risk.

### References
* https://github.com/magento/magento2/issues/6401
* https://github.com/magento/magento2/commit/3b611a7cc0040c9e5731cbc8e2080c2adb205d86 - the commit that fixes it 2.4
