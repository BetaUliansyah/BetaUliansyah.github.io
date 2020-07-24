---
title: Easy way to identify Odoo website
date: 2017-10-19 00:00:00 +07:00
categories:
- jekyll
- update
layout: post
---

From so many ways to identify whether a website is using Odoo or not, I have a special technique. It is very easy and not require any technical experience. Just open up your browser and add `/jsonrpc` to a URL without any parameter. For example: [https://www.odoo.com/jsonrpc](https://www.odoo.com/jsonrpc). A default odoo installation will response with recognizable error message: 
>`<function RPC.jsonrpc at 0x7f51dfc01268>, /jsonrpc: Function declared as capable of handling request of type 'json' but called with a request of type 'http'` 

![Identify Odoo with /jsonrpd](https://raw.githubusercontent.com/BetaUliansyah/BetaUliansyah.github.io/master/img/odoo-identify.jpg)

If the website is using Odoo, it will return a **Bad Request** response.  Otherwise, it will return a usual 404 error page.
