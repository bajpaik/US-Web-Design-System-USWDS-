# US-Web-Design-System-USWDS-

Description
In accordance with the 21st Century IDEA, the US Web Design System (USWDS) provides the foundation/base template that all US Government sites are to use in order to be in compliance with the act.

 
Additional Information/Notes
To read and learn more about the 21st Century Integrated Digital Experience Act click here.

"Section 3, Part (e) Compliance With United States Website Standards. — Any website of an executive agency that is made available to the public after the date of enactment of this Act shall be in compliance with the website standards of the Technology Transformation Services of the General Services Administration."

The current state of this template is to provide the CSS, Header, and Footer for rapid prototyping of Service Portals.

This template should not be used to produce 'Production Ready' portals. However; it can give you a good jump start.

You can read more about this standard from their site.

The template package contains:

USWDS Service Portal

Configured to use the USWDS Theme and supporting Service Portal (Demo) menus
USWDS Theme Record contains -

CSS Includes (2) - Font(s) import and the USWDS CSS
JS Include - USWDS Javascript API
Bootstrap overrides with SASS variable as part of the CSS variables block
Service Portal Menus - Three (3) menus are provided in order to demonstrate the power of the template. Configuration of the menus is explained below.

USWDS Primary - Demonstrate the 'basic' menu
USWDS Secondary - Demonstrate the 'extended' menu capabilities
USWDS Footer - Menu for demonstrating the footer menu capabilities
Five (5) Widgets –

USWDS Header (uswds-header)
USWDS Header Menu (uswds-header-menu)
USWDS Header Secondary Menu (uswds-header-secondary-menu)
USWDS Footer (uswds-footer)
USWDS Typeahead Search (uswds-typeahead-search)
Installation
Download and install the Zipped Images for the site uswds_images_base.zip

SN Product Documentation - 'Upload one or more images'
Download and install update set tpl-uswds.u-update-set.xml

NOTE: You will get import errors during the update set preview process because of the menu records. Just 'Accept remote update' on all the error records from the Update Set Preview Problems tab.

SN Product Documentation - 'Load a customization from a single XML file'
Configuration
The USWDS standard accounts for multiple presentation formats of Header and Footer. We have built the Header and Footer widgets to dynamically adjust based on the amount of menu choices setup in the respective menus (included).

The Service Portal record's Quick start config is used to identify when different elements of the Header and Footer are to be used.

[{
  "auto_menu": false,
  "secondaryMenu": {"sys_id": "07c3a78f4fc83b008272ece24210c718"},
  "secondaryWishCartList": true,
  "fluid" : true,
  "megamenu" : true,
  "footerMenu" : {
	"sys_id": "d5cc2ef34f44fb008272ece24210c7a2",
    "contact" : {
		"center" : "USWDS PMO",
		"phone" : { "text" : "(800) CALL-WDS", "dial" : "1-800-555-1212" },
		"email" : "info@uswds.gov"
	},
	"social": [
		{"name":"Facebook", "link":"https://www.facebook.com"},
		{"name":"Twitter", "link":"https://www.twitter.com"},
		{"name":"YouTube", "link":"https://www.youtube.com"},
		{"name":"RSS", "link":"https://en.wikipedia.org/wiki/RSS"}
	]
  }
}]
Quick start config
Explanation of the JSON structure and variables in the Quick start config

auto_menu - if no menu is identified then generate menu items for the KB and Service Catalog associated with the portal
secondaryMenu - the sys_id of the Service Portal Menu to be used as the secondary menu in the header
footerMenu - data used to generate the footer
sys_id : Sys ID of the Service Portal Menu to be used
contact : Contact information to be rendered in the footer
social : Social Media links to be rendered Please Note: the images generated are limited to the examples above
secondaryWishCartList, fluid, and megamenu - not currently implemented
