---
layout: default
title: Technical Support
nav_order: 8
parent: Home
---

{% if site.support_center %}
Our preferred mechanism for support is via support ticket. It allows us to better track support calls so nothing falls through the cracks, we can assign tickets to the appropriate person, and can do statistics that help us plan things better. The Technical Support function in the Help menu navigates your browser to the Support Center web site. You can also choose the Submit Support Ticket function from the Help menu to automatically create a support ticket.
{% else %}For the best possible service when contacting us for technical support, please provide the name of the product ({{ site.app_name }}) and the version and serial numbers (these can be obtained from the About function in the Help menu).

{% endif %}

Note that your [software maintenance]({% link _docs/software-maintenance.md %}) must be current in order to receive technical support. Also note that services such as assisting with report design and layout, determining which fields to use in a report, or creating custom SQL statements are not technical support but rather consulting. Please contact us for our consulting rates if you are interested in these services.
{% if site.support_kb %}

You can access our Knowledgebase by choosing Knowledgebase from the Help menu. The Knowledgebase is full of "how to" articles that describe how to perform various tasks in {{ site.app_name }}.
{% endif %}
