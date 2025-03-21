---
layout: post
title: Swiping in .NET MAUI Bottom Sheet | Syncfusion®
description: Learn here all about swiping support in Syncfusion® .NET MAUI Bottom Sheet (SfBottomSheet) control and more.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---
# Swiping in .NET MAUI Bottom Sheet (SfBottomSheet)

The [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) supports the swiping for expanding the sheet. 

## Enable Swiping

The [EnableSwiping](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_EnableSwiping) property allows you to enable or disable swipe functionality in the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html). By default, the EnableSwiping property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" EnableSwiping="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
    
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    EnableSwiping = true
};

{% endhighlight %}
{% endtabs %}

{% highlight c# %}

private void OnListViewItemTapped(object? sender, ItemTappedEventArgs e)
{
    bottomSheet.BottomSheetContent.BindingContext = e.Item;
    bottomSheet.Show();
}

{% endhighlight %}

![Swiping Image for BottomSheet](images/swiping.gif)