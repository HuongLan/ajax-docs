---
title: OnClientMouseOut
page_title: OnClientMouseOut | UI for ASP.NET AJAX Documentation
description: OnClientMouseOut
slug: treeview/client-side-programming/events/onclientmouseout
tags: onclientmouseout
published: True
position: 23
---

# OnClientMouseOut



## 

The __OnClientMouseOut__client-side event occurs just before the mouse passes out of a node.

The event handler receives parameters:

1. The treeview instance that fired the event.

1. Event arguments with functions:

* __get_node()__ retrieves a reference to the node.

* __get_domEvent()__ retrieves a DOM event object of the mouse movement.

The example below retrieves node text just before the mouse passes out of the node area. The text is displayed in a div.

````ASPNET
	
	    <script type="text/javascript" language="javascript">
	        function ClientMouseOut(sender, eventArgs) {
	            var node = eventArgs.get_node();
	            var myDiv = document.getElementById("myDiv");
	            myDiv.innerHTML = "OnClientMouseOut: " + node.get_text();
	        }
	    </script>
	
	    <telerik:RadTreeView ID="RadTreeView1" runat="server" OnClientMouseOut="ClientMouseOut">
	    </telerik:RadTreeView>
	    <br />
	    <div id="myDiv" style="width: 489px; height: 100px">
	    </div>
````



# See Also

 * [OnClientMouseOver]({%slug treeview/client-side-programming/events/onclientmouseover%})

 * [RadTreeNode]({%slug treeview/client-side-programming/objects/radtreenode%})