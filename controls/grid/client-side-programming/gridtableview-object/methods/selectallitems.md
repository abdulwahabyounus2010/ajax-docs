---
title: selectAllItems
page_title: selectAllItems | UI for ASP.NET AJAX Documentation
description: selectAllItems
slug: grid/client-side-programming/gridtableview-object/methods/selectallitems
tags: selectallitems
published: True
position: 37
---

# selectAllItems



## 

Selects all items in the GridTableView for which the method is invoked.

>note The AllowMultiRowSelection property of RadGrid should be set to true to select multiple items!
>



|  __selectAllItems()__  |
| ------ |
||

Example:

````JavaScript
	        function SelectMasterTableItems() {
	            var masterTable = $find("<%= RadGrid1.ClientID %>").get_masterTableView();
	            //select all master table items
	            masterTable.selectAllItems();
	        }
````

