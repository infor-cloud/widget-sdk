---
title: Best Practices
has_children: false
nav_order: 3
---

# Best Practices
{: .no_toc }

Here are some best practices to consider when building your widgets. For further reading, please refer to the [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf).

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Use ION APIs to communicate with the backend

The widget should exclusively use ION APIs to communicate with the backend. For example when retrieving data, or creating / updating / deleting data.

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 10: ION API)
* [How to call an ION API](https://www.youtube.com/watch?v=RJCEsnzSdIM)
* [Youtube playlist for ION and ION API Gateway](https://www.youtube.com/watch?v=up5ZLczEQ4c&list=PL84oLmtdP0NPmO0bLcls3E3qTf9w05_r6)
* [ION API Admin guide](https://docs.infor.com/ionapi/12.0.x/en-us/ionapiag/default.html)
* [ION API Github](https://github.com/infor-cloud/ion-api-sdk/blob/master/README.md)

## Focus on speed and performance

The widget should be developed with focus on speed and performance. High performant APIs with short response times, minimizing the number of requests as well as data size and the number of items retrieved to a set of 10-15 items with a max limit of 100. (Purpose built APIs for charts as client side calculations on data sets does not deliver high performance)

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 12: Homepages Widget Certification)

## Use IDS Enterprise component library
When designing your widget, we strongly recommend using the [IDS Enterprise Components](https://github.com/infor-design/enterprise) for the UI. 

![Screenshot of a IDS homepage](assets/images/ids-screenshot.png)

The IDS Enterprise Components is a framework-independent UI component library built in js and css that is pattern-focused, template-driven, touch-enabled, responsive, accessible, and themable.

Complex custom components should always be avoided. If custom styling or components has been used, they must follow the IDS guidelines for look & feel, theming, mobile and accessibility support.

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 2: Overview > **Enterprise Components for Infor Design System**)
* [Infor Design System (IDS)](https://design.infor.com/)
* [IDS Enterprise Components](https://github.com/infor-design/enterprise)

## Theme Support
Widgets should support the three theme variants of the IDS Subtle Theme; Light, Dark and High Contrast.  

![Screenshot of a homepage in Dark Theme](assets/images/homepages_dark-theme.png)

The IDS Enterprise components automatically supports all theme variants. 

If custom styling or components has been used, those must align with the IDS look & feel for each theme variant.

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > **Theme Support**)

## Translate your widgets
We recommend that you translate your widgets so that they support the same languages as supported by Infor OS. For a current list of supported languages, see [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf).

Add translations using the `localization` property in the widget manifest.

### Example
{: .no_toc }
```
"localization": { 
    "en-US": { 
        "widgetTitle": "Hello World", 
        "widgetDescription": "Hello World Sample Widget." 
    } 
}
```
### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > Widget manifest > Optional manifest properties > **Localization**, Chapter 7: Localization)

## Design for all widget sizes 
A widget can be used on a page in 8 different sizes (1x1, 1x2, 1x3, 1x4, 2x1, 2x2, 2x3 and 2x4). Your widget should be runnable in all of these, meaning that all components should be visible and usable. 

![Screenshot of a homepage with widgets](assets/images/homepages_widget-sizes.png)

Consider optimizing your widget for all widget sizes, by for example showing additional content when the widget is larger than 1x1, or adjusting margins, paddings and/or graphic elements when the widget is smaller to make your widget more efficient.

## Add widget screenshots
You can add up to three PNG image files that will be shown when viewing the widget in the Widget Catalog. The screenshots helps communicate the widget's features and visual experience for your end users. 

![Screenshot of Widget Catalog](assets/images/widget-catalog_screenshots-example.png)

Configure your screenshots by adding up to three PNG image files in the widget ZIP. 

The screenshots must be named `screenshot1.png` `screenshot2.png` etc. The image will be displayed in a 200x200px container, and if the image is clicked the image is shown in its original size.

Reference the images using the `screenshots` property in the widget manifest. The value should reflect the number of screenshots. 

### Example
{: .no_toc }
```
"screenshots": "2" 
```

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > Widget manifest > Optional manifest properties > **Screenshots for the widget catalog**)

## Enable your widgets for Infor Go 
Allow your users to access your widget from the Infor Go mobile application for [Android](https://play.google.com/store/apps/details?id=com.infor.go&hl=en) and [IOS](https://apps.apple.com/bs/app/infor-go/id1446388736). When running on a mobile device the widget can access native device features like GPS information and camera.

![Screenshot of widget in Infor Go](assets/images/infor-go_screenshot.png)

Enable your widget for Infor Go by setting the `target` property in the widget manifest to `mobile`.

### Example
{: .no_toc }
```
"target": "mobile"
```

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > **Mobile Widget**)  

## Build your widgets for the banner area
A Banner widget is a widget that can be added to the banner container. The banner container is located at the top of the page directly below the page header, and always spans the entire first row. It holds between one and four banner widgets and has a background color based on the color of the page.

![Screenshot of a homepage with widgets](assets/images/homepages-screenshot.png)

Enable your widget for the banner area by setting the `target` property in the widget manifest to `banner`.

### Example
{: .no_toc }
```
"target": "banner"
```

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > **Banner Widget**)

## Configure a Help URL 
Give your users some help along the way by providing a link to documentation for your widget. The link will be displayed for end users in the About dialog. 

Configure the link by adding the `helpUrl` property in the widget manifest. 

### Examples
{: .no_toc }
```
"helpUrl": "http://www.example.com/" 
"helpUrl": "{Scheme}://{Hostname}:{Port}/{TenantId}/MyApp/Help"
```

### Further reading
{: .no_toc }
* [Developer's Guide](https://github.com/infor-cloud/homepages-widget-sdk/blob/master/DevelopersGuide.pdf) (Chapter 3: Widgets > Widget manifest > Optional manifest properties > **Help URL**)
