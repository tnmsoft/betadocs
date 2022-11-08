---
title: Tab Container
layout: default
nav_order: 17
parent: Dashboard Item Settings
grand_parent: Dashboard Designer
---
# Tab Container

Like the [Dashboard Item Group]({% link _docs/dashboard-designer/dashboard-item-settings/dashboard-item-group.md %}), the **Tab Container** dashboard item allows you to combine elements within a dashboard. The main Tab Container's purpose is to split the dashboard layout into several pages. For example, you can place common filter elements on a separate tab page to display only data dashboard items. 

![](/assets/images/dashboards/wdd-dashboard-item-tab-container.png)

- [Create a Tab Container](#create-a-tab-container)
- [Interactivity](#interactivity)

## Create a Tab Container
To create a tab container, use the **Tab Container** button (the ![Insert Tab Container](/assets/images/dashboards/wdd-toolbox-insert-tab-container.png) icon) in the [Toolbox]({% link _docs/dashboard-designer/ui-elements/toolbox.md %}). The created tab container always contains one empty tab page (_Page 1_).

![](/assets/images/dashboards/wdd-tab-container-empty-page.png)

Click the **Add page** button (the ![](/assets/images/dashboards/wdd-tab-container-add-page-button.png) icon) to add a new page to the tab container.

A tab page can contain [dashboard items]({% link _docs/dashboard-designer/dashboard-item-settings/index.md %}) and [dashboard item groups]({% link _docs/dashboard-designer/dashboard-item-settings/dashboard-item-group.md %}). You can add them to a tab page using one of the following ways:

* Create a new item using the buttons inside the empty tab page.
* Drag a new item from the [Toolbox]({% link _docs/dashboard-designer/ui-elements/toolbox.md %}) and drop it to the tab page.
* Use [drag-and-drop]({% link _docs/dashboard-designer/dashboard-layout/dashboard-items-layout.md %}) to move existing items to the tab page.

{: .note }
Tab containers cannot be added to another tab container.

## Interactivity

The tab page allows you to manage the [interaction]({% link _docs/dashboard-designer/interactivity/master-filtering.md %}) between dashboard items inside and outside the page. 

The image below shows a tab page's default interactivity settings:

![](/assets/images/dashboards/wdd-tabContainer-interactivity.png)

The **Master Filter** button controls whether the current tab page allows you to filter dashboard items outside the page using master filter items contained within the page. By default, this option is enabled: master filter items in the page can filter any dashboard items.

The **Ignore Master Filters** button allows you to isolate dashboard items contained within the tab page from external master filter items. By default, this option is disabled: external master filter items can filter the dashboard items contained within the tab page.