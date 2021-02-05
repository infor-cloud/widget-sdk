---
title: v3.3.0-rc.2 released
parent: 2021
grand_parent: Blog
nav_order: 3
---

# v3.3.0-rc.2 released

by Johan Åslund on February 5, 2021
{: .fs-3 .text-grey-dk-000 }

Widget SDK v3.3.0-rc.2 has now been released. It's built from Homepages v12.0.46, which is the release for Infor OS 2021-03. Changes in this version include:

* Added support for lower and upper pipe in URL templates. Example for helpUrl with variable Language needed in lowercase.
* Added support in the homepages pack script to pack a standard widget as a tenant widget, using the --asTenant flag.
* Updated to Angular 11.0.7.
* Updated to IDS Enterprise 4.36.1.
* Updated to IDS Enterprise NG 9.1.1.

You'll find the release details and the downloadable zip [here](https://github.com/infor-cloud/homepages-widget-sdk/releases/tag/v3.3.0-rc.2)

The new pack script update will help you deploy & test a widget in an Infor OS Cloud environment a lot easier than before, since it can be packed as a tenant widget without having to modify the actual source code.

If you want to read more about new features & bug fixes included in these versions of the IDS Enterprise controls & components, check out their changelogs:
* [IDS Enterprise](https://github.com/infor-design/enterprise/blob/master/docs/CHANGELOG.md#v4361)
* [IDS Enterprise NG](https://github.com/infor-design/enterprise-ng/blob/master/docs/CHANGELOG.md#v911)
