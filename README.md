# Corrosion
Titanium Network's web proxy.

Project is still in development! Pull requests that contribute a lot will be accepted :)

# Installation:
```
npm i corrosion
```

# Example:
```javascript
const Corrosion = require('corrosion');
const proxy = new Corrosion();
const http = require('http')
http.createServer((req, res) => proxy.request(req, res)).on('upgrade', proxy.upgrade).listen(80);
```
Much more in depth one is in the `demo` folder.

# API:
  
  
# Index
-  `config`
   - `config.prefix` Prefix
   - `config.title` Title used for HTML documents
   - `config.ws` WebSocket rewriting
   - `config.cookie` Request Cookies
   - `config.codec` URL encoding (base64, plain, xor).
   - `config.requestMiddleware` Server only - Array of middleware functions for proxy request. 
   - `config.responseMiddleware` Server only - Array of middleware functions for proxy response.
   - `config.standardMiddleware` Server only - Use the prebuilt middleware used by default. 

# JS Rewriter

## Methods:

### process
  - `source` JS script
  - `url` URL for header
    - ``
