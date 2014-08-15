Launchpad DNSimple Plugin
---

This plugin does not expose any endpoints; rather, it registers a server-wide method for updating CNAME records from within other Launchpad plugins.

```javascript
// assuming you have assigned `server` elsewhere
server.methods('dns', {product_slug:string}, {original_url:string}, {callback:function});
```

For example:

```javascript
server.methods('dns', 'awesome-sauce', 'asm-products.github.io/awesome-sauce', function(err, response) {
  // do something with the response
});
```

Will point `awesome-sauce.[DOMAIN].com` to `asm-products.github.io/awesome-sauce`, where `DOMAIN` is the domain passed in to this plugin's options.

### License

#### ASM-BSD

Copyright © 2014, Assembly
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted and provided that the following conditions are met:

* Any redistribution or use is for noncommercial purposes only and is not redistributed or used in connection with any application
  that is substantially similar to the Selected App Idea.
* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following
  disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS “AS IS” AND ANY EXPRESS OR IMPLIED WARRANTIES,
INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR PARTICULAR PURPOSE ARE DISCLAIMED.
IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY,
OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA,
OR PROFITS; OF BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.