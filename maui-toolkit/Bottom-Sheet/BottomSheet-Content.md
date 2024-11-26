---
layout: post
title: Set Bottom Sheet Content in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about Setting Bottom Sheet Content support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Set Bottom Sheet Content in .NET MAUI Bottom Sheet

The sheet content is only viewable when the sheet is in the FullExpanded, HalfExpanded, Collapsed state. Its content can be set as : `BottomSheetContent`

## BottomSheet Content

It can be set using the `BottomSheetContent` property.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet">
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <!-- Need to add content-->
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}
        
SfBottonSheet bottomSheet = new SfBottonSheet();
// Need to add content
this.Content = bottomSheet;
  
{% endhighlight %}
{% endtabs %}