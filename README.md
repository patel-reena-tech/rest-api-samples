# rest-api-examples
This repository contains examples for the Tableau REST API. Official developer docs for the REST API can be found [here](http://onlinehelp.tableau.com/current/api/rest_api/en-us/help.htm).

Getting Started
---------------
* Clone this repository
* Try the examples against your Tableau Server or Tableau Online
* Use 'Issues' to note any bugs or to request new examples
* Let us know if you have examples of your own you'd like to share

Requirements
---------------
* Python 2.7 or 3.x
* Python 'requests' library (http://docs.python-requests.org/en/latest/)

Running the samples
---------------
* All samples can be run using the command prompt or terminal
* All samples require 2 arguments: server adress (without a trailing slash) and username
* Run sample by executing ```python sample_file_name.py <server_address> <username>```
* Specific information for each sample are included at the top of each file
* API version is set to 2.2 by default for Tableau server 9.3, but it can be changed in [version.py](./version.py)
* For Tableau Server 9.0, the REST API namespace must be changed (refer to comment in each sample where namespace, xmlns, is defined)

REST API Examples
---------------
These are created and maintained by Tableau.

Demo | Source Code | Description
-------- |  -------- |  --------
Publish Workbook | [publish_workbook.py](./publish_workbook.py) | Shows how to upload a Tableau workbook using both a single request as well as chunking the upload.
Move Workbook | [move_workbook_projects.py](./move_workbook_projects.py)<br />[move_workbook_sites.py](./move_workbook_sites.py)</br />[move_workbook_server.py](./move_workbook_server.py) | Shows how to move a workbook from one project/site/server to another. Moving across different sites and servers require downloading the workbook. 2 methods of downloading are demonstrated in the sites and servers samples.<br /><br />Moving to another project uses an API call to update workbook.<br />Moving to another site uses in-memory download method.<br />Moving to another server uses a temporary file to download workbook.
Add Permissions | [user_permission_audit.py](./user_permission_audit.py) | Shows how to add permissions for a given user to a given workbook.
Global Workbook Permissions | [update_permission.py](./update_permission.py) | Shows how to add or update user permissions for every workbook on a given site or project.
