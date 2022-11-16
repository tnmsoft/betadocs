---
title: Geo Point Maps
layout: default
nav_order: 9
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Geo Point Maps
The topics in this section describe various types of **Geo Point Map** dashboard items that allow you to place callouts, bubbles or pies on the map using geographical coordinates.

![wdd-geo-point-map](/assets/images/dashboards/img126681.png)

## Map Types Overview
The Web Dashboard allows you to create **three types** of Geo Point maps.
* The **Geo Point Map** dashboard item allows you to place callouts on the map using geographical coordinates.
	
	![wdd-dashboard-items-geo-point-map](/assets/images/dashboards/img125121.png)
* The **Bubble Map** dashboard item allows you to place bubbles on the map. Each bubble can represent data using its weight and color.
	
	![wdd-dashboard-items-bubble-map](/assets/images/dashboards/img125115.png)
* The **Pie Map** dashboard item allows you to display pies on the map. Each pie visualizes the contribution of each value to the total.
	
	![wdd-dashboard-items-pie-map](/assets/images/dashboards/img125124.png)

To create the required **Geo Point Map** dashboard item, use the **Maps** section in the Toolbox.

![wdd-toolbox-maps-section](/assets/images/dashboards/img125422.png)


## Providing Maps
This topic describes how to use the default **Dashboard** maps and configure their attributes.
* [Default Maps](#defaultmaps)
* [Custom Maps](#custommaps)

### <a name="defaultmaps"/>Default Maps
The **Web Dashboard**  ships with a set of default maps showing various parts of the world. The following maps are included.
* **World Countries** - a map of the world
* **Europe** - a map of Europe
* **Asia** - a map of Asia
* **North America** - a map of North America
* **South America** - a map of South America
* **Africa** - a map of Africa
* **USA** - a map of the USA
* **Canada** - a map of Canada

{: .note }
The **World Countries** map has a lower level of detail than maps of specific regions and may not contain some of the countries. As an alternative, you can load a custom map with required granularity.

To select a required default map, go to the [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and use the **Default Map** dropdown list located in the **Common** section.

![wdd-geopoint-map-change-map](/assets/images/dashboards/img125426.png)

### <a name="custommaps"/>Custom Maps
The Web Dashboard uses a **Shapefile** vector format to provide custom maps. Commonly, this format includes two file types:
* **.shp file** - holds map shapes (points/lines/polygons)
* **.dbf file** - contains attributes for each shape.

To provide a custom map, go to the **Common** section of the [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and change the **Default Map** value to **Custom**.

![wdd-custom-shape-file](/assets/images/dashboards/img127210.png)

Finally, provide shape data using one of the following ways.
* Specify the path to the **.shp** file using the **Custom Map URL** option. Attributes from the corresponding **.dbf** file located in the same directory will automatically be included in the map.
* Load the existing shapefile using the ellipsis button next to the **Custom Map File** option. In the invoked dialog, locate the required **.shp** file. Use the **Custom Attribute File** option to locate the **.dbf** file containing attributes for each shape.

Note that custom maps created in the Cartesian coordinate system are not supported.


## Clustering
When a Geo Point map contains a large number of objects (callouts, bubbles or pies), showing each object individually on the map is not useful. The Web Dashboard provides the capability to group neighboring map objects. This feature is called Clustering.

For instance, the Geo Point Map dashboard item combines callouts to bubbles.

![wdd-geopoint-map-clusters](/assets/images/dashboards/img125449.png)

The Bubble Map and Pie Map dashboard items cluster bubbles/pies with other bubbles/pies.

![wdd-bubble-map-clusters](/assets/images/dashboards/img125445.png)

![wdd-pie-map-clusters](/assets/images/dashboards/img125447.png)

To enable clustering in the Web Dashboard, use the **Enable Clustering** option in the Geo Point Map's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

![wdd-maps-enable-clustering](/assets/images/dashboards/img125448.png)


## Map Navigation
The Geo Point Map dashboard item allows you to perform navigation actions such as zooming and scrolling using the mouse.

You can enable or disable the capability to scroll/zoom the map using the **Lock Navigation** option in the Geo Point Map's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

![wdd-map-lock-navigation](/assets/images/dashboards/img125404.png)

To display the entire map within the dashboard item, use the **Initial Extent** button (the ![wdd-map-initial-size-icon](/assets/images/dashboards/img125402.png) icon) in the Geo Point Map's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).

![wdd-geo-point-map-initial-state](/assets/images/dashboards/img125453.png)

## Interactivity
This document describes the capabilities that enable interaction between **Geo Point** maps and other dashboard items. These capabilities include **Master Filtering**.

### Master Filtering
You can use the **Geo Point** dashboard item as a filter for other dashboard items.

The Geo Point Map dashboard item supports filtering by callout/bubble/pie. When Master Filtering is enabled, you can click a callout/bubble/pie (or multiple callouts/bubbles/pies) to make other dashboard items only display data related to the selected callout(s)/bubble(s)/pie(s).

![wdd-geo-point-master-filtering](/assets/images/dashboards/img125454.png)

{: .note }
When you select a clustered bubble or pie, master filtering is applied by all points that are clustered into this bubble/pie.

To learn more about filtering concepts common to all dashboard items, see the [Master Filtering]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) topic.

To enable **Master Filtering**, go to the Map's [Interactivity]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu and select the required Master Filtering mode.

![wdd-interactivity-section-without-drill-down](/assets/images/dashboards/img125455.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](/assets/images/dashboards/img125072.png) icon) in the Map's [caption]({% link _docs/dashboard-designer/dashboard-layout/dashboard-item-caption.md %}).

## Labels
Geo Point maps provide the capability to display titles within map shapes and allow you to add supplementary content to the callout/bubble/pie tooltips.

### Shape Titles
To manage map titles, use the **Shape Title Attribute** option of the Map's [Options]({% link _docs/dashboard-designer/ui-elements/dashboard-item-menu.md %}) menu.

Here you can select the attribute whose values are displayed within corresponding map shapes.

![wdd-geopoint-map-shape-title](/assets/images/dashboards/img125459.png)

### Tooltips
Geo Point maps also allow you to add supplementary content to the callout/bubble/pie tooltips using the **Tooltip Measures** and **Tooltip Dimensions** data sections.

To add an additional information, click a placeholder contained in one of the available data sections and select the required measure/dimension in the **Binding** section of the invoked [data item menu]({% link _docs/dashboard-designer/ui-elements/data-item-menu.md %}).

![wdd-geo-point-map-toltips](/assets/images/dashboards/img125462.png)