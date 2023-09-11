# PTCSC.VESManagement

Building block manages Vuforia Experience Service (VES) content via Thingworx mashups. These mashups are installed under the SCP Accelerator Administration menu. 

## Disclaimer

By downloading this software, the user acknowledges that it is unsupported, not reviewed for security purposes, and that the user assumes all risk for running it.

Users accept all risk whatsoever regarding the security of the code they download.

This software is not an official PTC product and is not officially supported by PTC.

PTC is not responsible for any maintenance for this software.

PTC will not accept technical support cases logged related to this Software.

This source code is offered freely and AS IS without any warranty.

The author of this code cannot be held accountable for the well-functioning of it.

The author shared the code that worked at a specific moment in time using specific versions of PTC products at that time, without the intention to make the code compliant with past, current or future versions of those PTC products.

The author has not committed to maintain this code and he may not be bound to maintain or fix it.

## Overview

This building block includes services and mashups that allows ThingWorx Administrators to manage content on the VES instance associated with that ThingWorx instance. Features of the mashups include:
- View Vuforia Studio projects pubished to the VES (including the author, published date, screen requirements, access setting, offline setting, etc.)
- Unpublish (delete) a project from the VES
- Change the access setting of a published project (i.e. public vs. requires authentication)
- View a published experience in a Studio-Preview-like browser tab
- View the hyperlink and Vuforia View QR code for the Studio project
- Upload a new Studio project to the VES (note: requires the appropriate Studio generated zip file)
- View the VES version number
- View usage of the VES for a selected time period (Vuforia View user views)

The services included on the management thing shape of this building block (used to facilitate the above mashup functionality) may also be used to create additional custom mashup functionality related to the VES.

## Dependencies

This building block has the following ThingWorx extension/building block dependencies which must be installed on a ThingWorx instance prior to installing this building block:
- PTC.Base (1.2.0 or higher)
- PTCTS.IAMAdmin (1.1.3 or higher)
- PTCTS.UserInterface (1.1.3 or higher)
- QRCode_Extensions (3.0 or higher)

This building block has been tested with ThingWorx 9.3.6 and should be compatible with that version or higher.

-	## SCP Accelerator (SCPA)
Note that this building block was developed for use with SCPA.  This building block can be used outside of SCPA, but please note the following characteristics of SCPA building blocks.
-	SCPA building blocks rely on the PTCTS.UserInterface building block and its master for a consistent look & feel and color scheme across the entire application.  If you are using this building block outside of SCPA, you may need to use a different master in your mashups to work with your application.
-	SCPA building blocks rely on the PTCTS.IAMAdmin building block, which provides a default set of permissions for this building block.
-	If you are using this building block outside of SCPA, some of the menuName values referenced in the manager MenuConfiguration table will likely not exist and will have to be changed.  Also note that SCPA provides additional menu functionality (such as menu icons) by overriding the MenuSectionKey in table MenuConfiguration.  If this value contains JSON, you may need to modify the value when used outside of SCPA. 
-	SCPA building blocks create their localization tokens inside of the entry point DeployComponent service so you do no need to import a localization file.  
-	Make sure to run DeployComponent from the entry point (or run InitializeSolution on the entire application) to perform required building block initialization.  
-	We highly recommend using the non-editable extension version of this building block, then extending it to meet your own needs.  If you install an editable version of this building block and modify it, you will not be able to install an upgrade of this building block in the future.  If this is a one-time use and you do not plan to upgrade, then select either the editable extension (source control entities) or the xml to install.

## Author
| Peter Schmaltz | Digital Thread Advisory Services Fellow |

## License

### MIT License

I accept the MIT License (https://opensource.org/licenses/MIT) and agree that any software downloaded/utilized will be in compliance with that Agreement. However, despite anything to the contrary in the License Agreement, I agree as follows:

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.

I acknowledge that I am not entitled to support assistance with respect to the software, and PTC will have no obligation to maintain the software or provide bug fixes or security patches or new releases.

The software is provided “As Is” and with no warranty, indemnitees or guarantees whatsoever, and PTC will have no liability whatsoever with respect to the software, including with respect to any intellectual property infringement claims or security incidents or data loss.
