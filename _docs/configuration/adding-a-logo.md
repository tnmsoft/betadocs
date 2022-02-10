---
layout: default
title: Adding a Logo to a Report
nav_order: 8
parent: Configuration
---
If you want to add an image, such as a company logo, to all or just certain reports, the easiest way to do that is with a template. Using the [Template Editor]({% link _docs/creating-reports/templates.md %}), you can add a picture object to a template that uses the desired image. Any report using that template then displays that image.

However, there's a little easier way to do this. One of the stock templates, Professional - Blue with Logo, already has a picture object on it. This picture uses whatever image you upload using the Upload a Logo Image function in the Tools menu. So, simply upload a company logo and use that template for your reports. Note that the Upload a Logo Image function is only available for Administrator and Tenant Administrator users.

If you want a different template to work the same way, do the following:

* Use the Template Editor to create or edit the desired template

* Add a parameter to the template named LogoImage

* Add a picture object and set the Data Binding Image property to the LogoImage parameter
