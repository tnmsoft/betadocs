---
title: Images
layout: default
nav_order: 12
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Images
The Image dashboard item is used to display static images within a dashboard.

![wdd-dashboard-items-image](/assets/images/dashboards/img125123.png)

You can either add a static image or you can use the Bound Image as a detail item along with the [Master Filtering](../interactivity/master-filtering.md) feature.

## Image Overview
The Web Dashboard allows you to create two types of **Image** dashboard items.
* The **Image** dashboard item allows you to add a static image to the dashboard.
	
	![Image_Web](/assets/images/dashboards/img22523.png)
* The **Bound Image** dashboard item can be bound to a set of images (for instance, stored in the database). You can use the Bound Image as a detail item along with the [Master Filtering](../../interactivity/master-filtering.md) feature.
	
	![wdd-image-bound](/assets/images/dashboards/img125706.png)

To create a required Image dashboard item, use the **Image** and **Bound Image** buttons in the [Toolbox](../../ui-elements/toolbox.md).

## Providing Images
This topic describes how to provide images for the **Image** and **Bound Image** dashboard items.

### Provide a Static Image
To provide an image to the Image dashboard item, open the Image's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and specify the image path using **URL** option.

![wdd-image-provide-image](/assets/images/dashboards/img125751.png)

The URL option saves the path to the image in the [dashboard definition](../../save-a-dashboard.md).

### Provide a Set of Images
The **Bound Image** dashboard item provides the **Attribute** data section containing the corresponding placeholder.

![wdd-image-bound-image-bindings](/assets/images/dashboards/img125753.png)

You can specify the binding mode for the Bound Image. Go to the Bound Image's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and specify the **Binding Mode**. The following options are available.
* **Binary Array** - Use this mode if images are stored in the data source as byte arrays.
* **URI** - Use this mode to locate images accessible by a predefined URI. In this case, the data source field should return strings that are parts of URIs to these images. For instance, the URI pattern in the form below specifies the path to the folder containing the required images. 
	
	![wdd-image-bound-template-eud](/assets/images/dashboards/img128884.png)
	
	_C:\Images\ProductDetailsImages\{0}.jpg_
	
	Data source field values will be inserted to the position of the _{0}_ placeholder. Thus, the Bound Image maps the current dimension value with the image placed at the specified URI.

> [!NOTE]
> Note that the **Bound Image** can display only a single image simultaneously. If Master Filtering is not applied to the Bound Image, it selects the displayed image in the following ways.
> * In the **Binary Array** mode, the displayed image cannot be predicted precisely as a result of sorting limitations for the image/binary data types. Use the [Master Filtering](../../interactivity/master-filtering.md) feature to display the specified image.
> * In the **URI** mode, the Bound Image displays an image corresponding a first attribute value taking into account the attribute's sort order.


## Interactivity
This document describes the features that enable interaction between the Bound Image and other dashboard items. These features include **Master Filtering**.

### Master Filtering
Data displayed in the Bound Image dashboard item can be filtered by other master filter items. The image below displays the Bound Image dashboard item filtered by [List Box](../filter-elements.md).

![wdd-image-bound](/assets/images/dashboards/img125706.png)

You can prevent the Bound Image from being affected by other master filter items using the **Ignore Master Filters** button in the Bound Image's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

![wdd-pivot-interactivity](/assets/images/dashboards/img125456.png)

To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

## Image Settings
This topic describes settings related to the representation of **Image** dashboard items.

### Image Size Mode
You can specify the image size mode that defines how the image fits within the dashboard item.

To do this, go to the [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and select the required size mode from the list.

![wdd-image-size-mode](/assets/images/dashboards/img125755.png)

The following modes are available.

| Size Mode | Description |
|---|---|
| **Clip** | The image is clipped if it is larger than the Image dashboard item. |
| **Stretch** | The image within the Image dashboard item is stretched or shrunk to fit the size of the Image dashboard item. |
| **Squeeze** | If the dimensions of the Image dashboard item exceed those of the image it contains, the image is shown full-size. Otherwise, the image is resized to fit the dimensions of the Image dashboard item. |
| **Zoom** | The image is sized proportionally without clipping, so that it best fits the Image dashboard item. The closest fitting side of the image (either the height or the width) will be sized to fit the dashboard item, and the remaining side (height or width) will be sized proportionally, leaving empty space. |

### Image Alignment
To specify how the image is aligned within the dashboard item, use the **Horizontal Alignment** and **Vertical Alignment** options in the Image's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

![wdd-image-alignment](/assets/images/dashboards/img125756.png)