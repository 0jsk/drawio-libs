# diagrams.net Libraries

## Create and share custom libraries:

1. Use the scratchpad or create a new library by clicking File, New Library
2. Once the library appears in the sidebar, you can drag and drop cells and images from the diagram or your harddrive
3. Supported image formats are PNG, JPG, SVG and GIF (including animated GIFs). If you are adding SVG files, you can make the colors of the SVG configurable using this method: https://desk.draw.io/support/solutions/articles/16000079239
4. When all elements have been added, click the pen icon, add titles to the entries and click Export
5. This will download the library file to your computer
6. To share it, the file must be uploaded to the web and made available via a public URL. One way to do this is to upload it to a public GitHub repository.
7. If you are using GitHub, use the _RAW_ URL of the library which is of the form https://raw.githubusercontent.com/ORG/REPO/REF/PATH/FILENAME.xml, eg. https://raw.githubusercontent.com/jgraph/drawio-libs/master/libs/templates.xml
8. Once you have the URL of the library, you can share it by encoding the URL and adding it the clibs parameter. To encode the URL, paste it into the text box at https://jgraph.github.io/drawio-tools/tools/convert.html and click URL Encode. For our example, this will yield https%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ftemplates.xml
9. Then add this to https://app.diagrams.net/?splash=0&clibs=U, eg. https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ftemplates.xml (where splash=0 bypasses the splash screen). Multiple libraries can be specified by separating them with semicolons. Each value must be prefixed with a U if it's a URL, eg. https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons-bluebox.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons.xml
10. You can then share this link and clicking on it will open and install your custom libraries in draw.io

## Library File Format

Libraries consist of an enclosing `<mxlibrary>` node containing a JSON array, which in turn contains entries with either an `xml` property with a compressed or uncompressed mxGraphModel or a `data` property with an image data URI (in PNG, JPG or SVG). All entries must have a `w` and `h` property for the width and height of the cell(s) or image in the entry and an optional `title` property for the title in the sidebar and preview. For entries with a `data` property, an optional `"aspect": "fixed"` may be specified to add `aspect=fixed` to the style of the image cell, and an optional `style` attribute can be specified to be added the default style of the image cell. Eg. for `"data": "data:image/png,[...]", "aspect": "fixed", "style": "resizable=0;rotatable=0;"` the resulting cell style will be `shape=image;verticalLabelPosition=bottom;verticalAlign=top;imageAspect=0;aspect=fixed;image=data:image/png,[...];resizable=0;rotatable=0;`

For uncompressed `xml` properties, `<` must be writter as `&lt;`, `>` must be written as `&gt;` and `"` must written as `\"` (escaped), eg. `"xml": "&lt;mxGraphModel&gt;&lt;root&gt;&lt;mxCell id=\"0\"/&gt;&lt;mxCell id=\"1\" parent=\"0\"/&gt;&lt;mxCell id=\"2\" value=\"Test3\" style=\"whiteSpace=wrap;html=1;fillColor=#ffffff;strokeColor=#000000;\" vertex=\"1\" parent=\"1\"&gt;&lt;mxGeometry width=\"120\" height=\"60\" as=\"geometry\"/&gt;&lt;/mxCell&gt;&lt;/root&gt;&lt;/mxGraphModel&gt;"`

The compressed XML may be obtained by clicking on the Encode button at https://jgraph.github.io/drawio-tools/tools/convert.html, eg. `"xml": "jVBLDoMgED3N7BE2XVdbV131BKROhASE4LTq7TsVWuPCpAuS95lH3gyo2s9t0tHcQocO1AVUnUKgjPxco3Mghe1ANSCl4AfyeuBWqyuiTjjQPwGZAy/tnpiVLIy0uCJwwMaRyXkylvAe9ePjTNyZNUOeSzcVw5D00GP5EBPhfFhqlUqjFoNHSguPTLYjkydOubcwaHtDe02Pmfe/5LYhg7Lkl27HXL3drd8="`

## Image (raster) Libraries

* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ftemplates.xml" target="_blank">Templates:</a> A sample library with basic building blocks for technical diagrams. The Comic template needs <a href="http://antiyawn.com/uploads/humorsans.html" target="_blank">Humor Sans</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons-bluebox.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons.xml" target="_blank">UN-OCHA Icons:</a> United Nations Office for the Coordination of Humanitarian Affairs (<a href="http://www.unocha.org" target="_blank">OCHA</a>) Humanitarian Icons 2012.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fraw.githubusercontent.com%2FLKirst%2Fgenogram%2Fmaster%2Fgenogram_library_lk.xml" target="_blank">Genogram:</a> A library with icons for genograms (also known as family diagrams).
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fdigitalocean.xml" target="_blank">DigitalOcean:</a> A library with icons for DigitalOcean resources (scraped from <https://do.co/diagram-kit> and <https://www.digitalocean.com/press>).
  * WARNING: No license is given by DO for these icons. Use at your own risk!

## Vector Libraries

* <a href="https://app.diagrams.net/?libs=0&clibs=Uhttps%3A%2F%2Fraw.githubusercontent.com%2FCir02%2FApache-logos-drawio%2Fmain%2Flib%2Fapache_software_foundation_logos.xml" target="_blank">Apache Foundation logos:</a> The icon set by <a href="https://github.com/Cir02/Apache-logos-drawio" target="_blank">Cir02</a> of Apache foundation logos.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fdelivery-icons.xml" target="_blank">Checkout & Delivery Icons:</a> The icon set by <a href="http://www.epicpxls.com/" target="_blank">EpicPxls</a> contains 35 icons depicting various actions and entities for the common checkout process on an e-commerce site.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fosa-icons.xml" target="_blank">OSA Icons:</a> Open source free technical icons to create security architecture or other technical drawings <a href="http://www.opensecurityarchitecture.org/cms/library/icon-library" target="_blank">Open Security Architecture/</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fflat-color-icons.xml" target="_blank">Flat Color Icons:</a> A set of colorful flat icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fvoyage-icons.xml" target="_blank">Voyage Icons:</a> 40 free icons to spice up your travel agency or the airline website by <a href="http://www.printexpress.co.uk/" target="_blank">PrintExpress</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fgesture-icons.xml" target="_blank">Gesture and Fingerprints Icons:</a> 100 useful gesture and fingerprints line icons by <a href="http://thesquid.ink/flat-icons/" target="_blank">TheSquid</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fmaterial-design-icons.xml" target="_blank">Material Design Icons:</a> Material design icons are the official icon set from Google that are designed under the material design guidelines by <a href="https://design.google.com/icons/" target="_blank">Google</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fchart-icons.xml" target="_blank">Chart Icons:</a> A set of light color chart icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fwindows-10-icons.xml" target="_blank">Windows 10 Icons:</a> A set of Windows 10 icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fgnome-icons.xml" target="_blank">Gnome Icons:</a> Network icons scheme based on Gnome Gorilla's theme.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffont-awesome.xml" target="_blank">Font Awesome:</a> The iconic font and CSS toolkit <a href="https://fortawesome.github.io/Font-Awesome/" target="_blank">Font Awesome</a>.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Farista.xml" target="_blank">Arista Icons:</a> A set of Arista networking icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fcommvault%2Fcvlt-badges.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fcommvault%2Fcvlt-infrastructure.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fcommvault%2Fcvlt-objects.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fcommvault%2Fcvlt-protected-clients.xml" target="_blank">Commvault Icons:</a> A set of Commvault networking icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-buildings.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-cloud.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-connector-devops-api.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-devices.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-features.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-generic-devices.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-generic-products.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-generic-technology.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-ot-and-iot.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-people-and-noc-soc.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-people-and-red-blue-team.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-platform-core-elements.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-products.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-saas-family-of-offerings.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-solutions-and-deployment-scenarios.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-threats-and-threat-services.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-vertical-related.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ffortinet%2Ffortinet-vm-components.xml
" target="_blank">Fortinet Icons:</a> A set of Fortinet networking icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fadditional-or-support.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fai-machine-learning.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fapps-and-system-logos.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fazure.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fazure-additional-or-support.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fbuildings.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fdatabases.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fdeprecated.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fdeveloper.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fdevices.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Ffiles.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fgeneric.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Finfrastructure.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fintegration.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fintegration-patterns.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fiot-devices.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Foffice365.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fothers.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fpowerapps-and-flows.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fpower-bi.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fsap.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fservers.xml;
Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fintegration%2Fusers-and-roles.xml
" target="_blank">Integration Icons:</a> A set of MS Integration icons.
* <a href="https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fkubernetes.xml" target="_blank">Kubernetes Icons:</a> A set of Kubernetes icons. Obsolete, as there is currently an integrated set in the app.

Click on a link above to open a library or go to File, Open Library from URL in draw.io and enter an URL of the form https://jgraph.github.io/drawio-libs/libs/templates.xml
