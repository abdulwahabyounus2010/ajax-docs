---
title: Create a Custom Skin
page_title: Create a Custom Skin | UI for ASP.NET AJAX Documentation
description: Create a Custom Skin
slug: fileexplorer/appearance-and-styling/create-a-custom-skin
tags: create,a,custom,skin
published: True
position: 0
---

# Create a Custom Skin



## 

AbstractEach of the controls included in the __Telerik UI for ASP.NET AJAX__suite is styled with two CSS files that are loaded in a certain order. The first one - __ControlName.css,__ also called base stylesheet contains CSS properties and values that are common for all skins, i.e it is layout-specific, not skin-specific. These are CSS float, padding, margin, font-size, font-family, etc. In the general case, when creating a custom skin for a control this file should not be edited, unless the custom skin needs different sizes, padding and/ or margins.

The second file represents the actual skin of the control, and its name consists of the control name plus the skin name, i.e -__FileExplorer.Default.css__. Upon creating a custom skin for the control, one should edit that particular file, as it contains skin-specific CSS properties, and references to images, colors, borders and backgrounds.

From __Q2 2010__, skin specific style sheet files have been created for all __RadFileExplorer__skins. They contain some skin specific colors and borders, and navigation toolbar buttons.

The navigation toolbar buttons are all place in a sprite image: FileExplorerToolbarSprites.png for all browsers and __FileExplorerToolbarSpritesIE6__.gif for Internet Explorer 6 only. Both images are exactly the same, but because IE6 cannot render PNG files properly we use PNG for other browsers and GIF for IE6. From Q2, 2010, that Sprite image is skin specific for every Telerik Skin, and it is placed in the __FileExplorer__folder related to the skin.
>caption 

![RadFileExplorer Toolbar's Sprite](images/FileExplorer-ToolbarSprites.png)

The __RadFileExplorer__ control consists of several controls from Telerik AJAX UI Suite: __RadToolBar, RadGrid, RadTreeView, RadUpload, RadSplitter__.And each of that controls is styled with two CSS files that are loaded in a certain order.

Another change from Q2 2010 is that the Dialog Separator in __RadEditor’s__Dialogs has been changed to be specific for each different skin. Until now, it was grey colored for all skins and its CSS selector was placed in Widgets.css. Its width was also increased from 3px to 5px.

````XML
	        .DialogSeparator
	        {
	            border-left: solid 1px #222;
	            border-right: solid 1px #222;
	            background-color: #ececec;
	        }
````


>caption 

![Dialog Separator](images/FileExplorer-dialogSepWidget.png)





From __Q2 2010__, the above CSS code was removed from __Widgets.css__and moved to __FileExplorer__CSS skin specific files in order to have skin specific __DialogSeprator__.
>caption 

![Dialog Separator new](images/FileExplorer-dialogSepSkinSpecific.png)


>caption 

![RadFileExplorer's scheme](images/FileExplorer-scheme.png)

The __FileExporer.css__file defines the common values for the control and all skins. It also rewrites some of the styles form __RadToolBar, RadGrid, RadTreeView, RadUpload, RadSplitter__. This is needed in order to make the control work properly. In that CSS file there are also skin specific settings for all skins which define some basic styles like colors and border colors of the __FileExplorer’s__wrapping elements to match the other controls’ skins.

To customize RadFileExplorer look and feel you should customize one or more of the skins of the controls that are used for __RadFileExplorer - RadToolBar, RadGrid, RadTreeView, RadUpload, RadSplitter__.

# See Also[Creating Custom RadToolBar Skin](E4860B1D-AA1D-4FF5-85AA-3259128EC121)[Creating Custom RadGrid Skin](ECE2CB6F-3421-4459-8102-1AABD8CD81C2)[Creating Custom RadTreeView Skin](7E70B2E0-1B4D-4553-A367-C274FD272DCF)[Creating Custom RadUpload Skin](51E9E701-B05D-41A7-9186-7B375DE47AE4)[Creating Custom RadSplitter Skin](AD9F5B51-61D0-4672-B7C1-F3E7A1EC8194)