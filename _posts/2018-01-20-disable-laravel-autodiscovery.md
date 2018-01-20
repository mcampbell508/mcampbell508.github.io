---
layout: post
title:  "Disable Laravel Package Autodiscovery"
date:   2018-01-20 11:20:59 +0000
tags: composer laravel5.5 auto-discovery
---

This feature [added in Laravel 5.5](https://medium.com/@taylorotwell/package-auto-discovery-in-laravel-5-5-ea9e3ab20518) on paper seems quite nice, but once you get into situations like
loading certain service providers in certain environments, this can become quite troublesome.

From my point of view, it is much prefered to register service providers explicitly, rather than using auto discovery magic.
However, I think for small projects this could be okay.

To disable this functionality simply add the following to `composer.json`:

```json
    "extra": {
        "laravel": {
            "dont-discover": [
                "*"
            ]
        }
    },
```