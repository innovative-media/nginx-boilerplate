nginx-boilerplate
=================

clone this repo into `/etc/nginx`, then add `include nginx-boilerplate/basic.conf;` to any server block.


### basic.conf
Includes for the entire nginx-boilerplate suite of directives and location blocks detailed below in the relevant sections.

### Directives

#### config.conf
Useful directives for a default web application server. Directives are either instructions for mime/character types, or configurations for speed.

#### x-ua-compatible.conf
The magic header to force IE to render using the highest compatibility available to the client browser. *Note* this header is no longer used in IE11 which defaults to the assigned header value.

#### extra-security.conf
Protection measures to enforce frame loading from same origin, prevent mime type sniffing, and prevent cross site scripting in IE.

#### no-transform.conf
Prevent mobile network providers from modifying your site via proxies.

### Locations

#### expires.conf
Expire rules for static content

#### cross-domain-fonts.conf
Cross domain webfont access

#### web-fonts.conf
Use this in place of cross-domain-fonts.conf if you are using only locally served webfonts.

#### protect-system-files.conf
Prevent clients from accessing hidden files and from accessing to backup/config/source files

#### cache-busting.conf
Built-in filename-based cache busting *Note* you must have this configuration included for any Core project.