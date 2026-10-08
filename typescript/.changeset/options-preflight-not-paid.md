---
"@x402/core": patch
---

A route keyed without an HTTP method (for example `"/api/data"`), or a single route config, no longer matches `OPTIONS` requests. The CORS preflight now falls through to the app instead of getting a 402, which stopped browsers from sending the paid request. Routes keyed explicitly as `"OPTIONS /path"` still require payment.
