---
title: v3.1.0 released
parent: October 2020
grand_parent: Blog
nav_order: 3
---

# v3.1.0 released

by Johan Åslund on October 19, 2020
{: .fs-3 .text-grey-dk-000 }

Welcome to the new Widget SDK blog!

We plan to update the blog on a monthly basis, and with this first post, we're announcing the release of Widget SDK v3.1.0, which you'll find [here](https://github.com/infor-cloud/homepages-widget-sdk/releases/tag/v3.1.0). Changes in this version include:

* Added getVersionInfo function to IWidgetContext which provides access to the Homepages version, displayVersion and frameworkVersion.
* The IDS locale is set automatically based on which language file is loaded in index.html (e.g scripts/lime/resources/en-US.js), or the value of the devLanguage attribute on lm-app.
* Updated to IDS Enterprise 4.31.2.
* Updated to IDS Enterprise NG 7.5.3.
