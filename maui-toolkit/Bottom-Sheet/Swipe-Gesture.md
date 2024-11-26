---
layout: post
title: Swiping in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about SwipGesture support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---
# Swiping in .NET MAUI Bottom Sheet (SfBottomSheet)

The BottomSheet supports the swipe gesture for closing the sheet. 

## Enable Swiping

The `EnableSwiping` property can activate or deactivate the swipe functionality in the `SfBottomSheet`.By default, the EnableSwiping property is set to `true`.

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