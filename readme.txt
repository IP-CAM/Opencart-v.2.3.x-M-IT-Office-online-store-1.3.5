M-IT: Online Store Management
CMS OpenCart and 1C: Enterprise integration module

The module requires PHP 5.3 or higher installed on the web server.


Installation
1. Copy the contents of the upload / folder (directories 1cgw /, admin /) to the root of your store. Existing files will not be overwritten.
Note:
If the administrative panel of your store is not located at / admin, then in upload / rename the admin / folder accordingly.

2. If the administrative panel of your store is not located at / admin, then you need to change the file 1cgw / init.php. On the 6th line
require_once ('../ admin / config.php');
change the file path to
require_once ('../ your_folder_name_with_administrative_part / config.php');

Also, in the ocmod / install.ocmod.xml file, you must correct the paths to the files as needed. In lines:
<file name = "admin / controller / common / menu.php">
<file name = "admin / view / template / common / menu.tpl">
<file name = "admin / model / catalog / product.php">
<file name = "admin / model / catalog / manufacturer.php">
<file name = "admin / model / catalog / category.php">
change admin to your_folder_name with_administrative_part.

3. It is necessary to install the modification
1) In the administrative panel of your store in the section "Modules" -> "Install extensions" download the file /ocmod/install.ocmod.xml
2) In the section "Modules" -> "Modifiers" there will be a new modification "Meteor-IT: UIM 1C". Click the "Refresh" button (upper right corner of the screen).

4. In the administrative panel of your store in the section "System" -> "Users" -> "User groups" go to editing your user group.
Allow viewing and editing "extension / exchange_1c".

5. In the administrative panel of your store, go to the "Add-ons" -> "Meteor-IT: UIM 1C" section. Click the Install Module button at the top right of the screen.
Now you can edit the SEO settings for products and categories and other parameters.
For the module to work correctly, it is necessary that the data on the "Security" tab in the module settings in the online store coincide with the same module data in 1C: Enterprise.


Notes

If the unloading of goods from 1C does not work, you must:
1. In a browser, open the page http: //your_domain/1cgw/index.php and make sure there are no errors. You should see the xml structure of the file.
2. Make sure that the data on the "Security" tab in the online store and in 1C match.
If everything is fine with respect to these points, but the unloading does not proceed, then contact the technical support of the module. 
