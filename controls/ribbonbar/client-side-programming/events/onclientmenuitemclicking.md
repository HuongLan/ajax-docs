---
title: OnClientMenuItemClicking
page_title: OnClientMenuItemClicking | UI for ASP.NET AJAX Documentation
description: OnClientMenuItemClicking
slug: ribbonbar/client-side-programming/events/onclientmenuitemclicking
tags: onclientmenuitemclicking
published: True
position: 6
---

# OnClientMenuItemClicking



## 

The __OnClientMenuItemClicking__ client-side event occurs when the user clicks on a ribbonbar menu item, before the ribbonbar responds to the mouse click.

The event handler receives two parameters:

1. The instance of the ribbonbar firing the event.

1. An eventArgs parameter containing the following methods:

* __get_item()__ returns a reference to the ribbonbar menu item that was clicked. In this case it is __RibbonBarMenuItem__.

* __set_cancel()__ lets you prevent the ribbonbar from responding to the mouse click.

You can use this event to respond when the user clicks on a ribbonbar menu item:

````ASPNET
	    <script type="text/javascript">
	
	        function OnClientMenuItemClicking(sender, args) {
	            var item = args.get_item();
	            if (item.get_text() == "Flip Vertical") {
	                args.set_cancel(true);
	            }
	        }       
	    </script>
	
	    <telerik:RadRibbonBar ID="RadRibbonBar1" runat="server" OnClientMenuItemClicking="OnClientMenuItemClicking">
	        <telerik:RibbonBarTab Text="Home">
	            <telerik:RibbonBarGroup Text="Image">
	                <Items>
	                    <telerik:RibbonBarMenu Size="Medium" Text="Rotate" ImageUrl="icons/Rotate.png">
	                        <Items>
	                            <telerik:RibbonBarMenuItem Text="Rotate Right 90�" ImageUrl="icons/Rotate.png" />
	                            <telerik:RibbonBarMenuItem Text="Rotate Left 90�" ImageUrl="icons/RotateLeft.png" />
	                            <telerik:RibbonBarMenuItem Text="Rotate 180�" ImageUrl="icons/Rotate180.png" />
	                            <telerik:RibbonBarMenuItem Text="Flip Horizontal" ImageUrl="icons/FlipHorizontal.png" />
	                            <telerik:RibbonBarMenuItem Text="Flip Vertical" ImageUrl="icons/FlipVertical.png" />
	                        </Items>
	                    </telerik:RibbonBarMenu>
	                </Items>
	            </telerik:RibbonBarGroup>
	        </telerik:RibbonBarTab>
	    </telerik:RadRibbonBar>
	
````



# See Also

 * [Overview]({%slug ribbonbar/client-side-programming/overview%})

 * [Overview]({%slug ribbonbar/client-side-programming/events/overview%})