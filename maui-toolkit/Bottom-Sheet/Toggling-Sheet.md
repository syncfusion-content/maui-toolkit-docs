---
layout: post
title: Toggle methods in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about Toggle methods support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Toggle methods in .NET MAUI Bottom Sheet (SfBottomSheet)

Bottom sheet can be toggled using

* Show method
* Close method
* Swipe gesture

## Opening Sheet Programmatically
The `Show` method enables programmatically opening the bottom sheet, and the `Close` method enables programmatically closing the bottom sheet.

{% tabs %}

{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet">
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>

{% endhighlight %}

{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}

{% endtabs %}

Using `Show` method,

{% highlight c# %}

bottomSheet.Show();

{% endhighlight %}

Using `Close` method,

{% highlight c# %}

bottomSheet.Close();

{% endhighlight %}
