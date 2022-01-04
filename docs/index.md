---
layout: default
title: Home
nav_order: 1
description: "Just the Docs is a responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
permalink: /
---

# Widget SDK
{: .fs-9 }

The Widget SDK is used to develop widgets for Infor Homepages.
{: .fs-6 .fw-300 }

[Get started now](getting-started){: .bg-azure-06 .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2  } [View it on GitHub](https://github.com/infor-cloud/homepages-widget-sdk){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## About Widget SDK

The Widget SDK is used to develop widgets for Infor Homepages. A widget is a small, single-purpose application that provides quick, at-a-glance information or quick access to simple interactive functions.

![Screenshot of a homepage with widgets](/assets/images/homepages-screenshot.png)

The Widget SDK includes the Framework API, which lets you communicate with the Widget framework. The ION API support enables communication with other Infor applications. The SDK is aimed at web developers and includes multiple sample widgets to explore and learn from.

## Getting Started 

Head over to [Getting Started](getting-started) for instructions how to start developing widgets.

---

## About this project

### About Infor Homepages
Infor Homepages is part of the cloud-based collaboration platform Infor OS. Infor Homepages provide role-based home pages with widgets containing information from multiple ERP systems in one place. Homepages are designed to give you insights, call exceptions to your attention, and provide direct links to the areas within applications where you do your daily work.

#### Thank you to the contributors!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>


