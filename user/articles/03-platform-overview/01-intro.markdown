---
header-id: platform-overview
---

# Services

DXP Cloud's built-in *services* are like the sturdy foundation of a house. These 
services provide DXP Cloud's core functionality, which you can use and configure 
to fit your project's needs. Using the foundation that these services provide, 
you can construct and manage your Liferay DXP applications. 

The following services are available in DXP Cloud: 

**Liferay DXP Service:** Runs your Liferay DXP instance. 

**Database Service:** Provides a distributed relational database service that 
simplifies the setup, operation, and scaling of your applications. 

**Search Service:** Provides the full-text search engine for your Liferay DXP 
application. 

**Web Server Service:** Handles all traffic from your users and acts as a 
high-performance web server. 

**Backup Service:** Creates regular backups of your Liferay DXP database and 
Document Library. 

<!-- 
Include section on Docker?

Where should we put the Updating Service Images section? It doesn't seem to fit 
here, since this doc describes services from a higher level.
-->

## Updating Service Images

Check the 
[services changelog](https://help.liferay.com/hc/en-us/categories/360001192512-Liferay-DXP-Cloud-Announcements) 
frequently to make sure you're using the most up-to-date service images. All 
Liferay DXP Cloud images are hosted at 
[https://hub.docker.com/u/liferaycloud](https://hub.docker.com/u/liferaycloud). 
After finding the latest images, update them in your DXP Cloud workspace's 
`gradle.properties`. 

Several services use third-party images as a foundation (e.g., Elasticsearch, 
NGINX, and Jenkins). Although these images get regular updates from their 
maintainers, we only update the corresponding service when necessary for a 
feature or security. This ensures stability. If you want to update an image's 
version, open a ticket 
[here](https://liferay-support.zendesk.com) 
and work with Liferay Support. The 
[services changelog](https://help.liferay.com/hc/en-us/categories/360001192512-Liferay-DXP-Cloud-Announcements) 
lists any such image updates. 
