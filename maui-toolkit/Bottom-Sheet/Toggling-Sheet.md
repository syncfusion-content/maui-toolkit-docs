---
layout: post
title: Toggle methods in .NET MAUI Bottom Sheet | Syncfusion
description: Learn here all about toggle methods support in Syncfusion .NET MAUI Bottom Sheet(SfBottomSheet) control.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Toggle methods in .NET MAUI Bottom Sheet (SfBottomSheet)

Bottom sheet can be toggled using

* IsOpen property
* Show method
* Close method

## Opening and Closing Sheet Programmatically using property

The [IsOpen](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_IsOpen) property enables programatically opening or closing the bottom sheet. By default, the IsOpen property is set to `false`.

{% tabs %}

{% highlight xaml %}

<Grid>
    <bottomSheet:SfBottomSheet IsOpen="True">
        <bottomSheet:SfBottomSheet.BottomSheetContent>
            <!--Add your content here-->
        </bottomSheet:SfBottomSheet.BottomSheetContent>
    </bottomSheet:SfBottomSheet>
</Grid>

{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.IsOpen = true;

{% endhighlight %}
{% endtabs %}


## Opening and Closing Sheet Programmatically using method
The [Show](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_Show) method enables programmatically opening the bottom sheet, and the [Close](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_Close) method enables programmatically closing the bottom sheet.

{% tabs %}

{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();

{% endhighlight %}
{% endtabs %}

Using `Show` and `Close` methods,

{% highlight c# %}

private void OnListViewItemTapped(object? sender, ItemTappedEventArgs e)
{
    bottomSheet.BottomSheetContent.BindingContext = e.Item;
    bottomSheet.Show();
}

private void CloseBottomSheet(object sender, EventArgs e)
{
    bottomSheet.Close();
}

{% endhighlight %}

![Toggle Gif for BottomSheet](images/toggleMethod.gif)