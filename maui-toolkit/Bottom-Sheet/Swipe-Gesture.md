---
layout: post
title: Swiping in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about Swiping support in Syncfusion .NET MAUI Bottom Sheet (SfBottomSheet) control.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---
# Swiping in .NET MAUI Bottom Sheet (SfBottomSheet)

The BottomSheet supports the swiping for closing and expanding the sheet. 

## Enable Swiping

The `EnableSwiping` property allows you to enable or disable swipe functionality in the SfBottomSheet. By default, the EnableSwiping property is set to `true`.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" EnableSwiping="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %} 

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.EnableSwiping = true;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;
bottomSheet.Show();

{% endhighlight %}
{% endtabs %}
