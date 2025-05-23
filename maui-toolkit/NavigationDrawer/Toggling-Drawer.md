---
layout: post
title: Toggle Methods in .NET MAUI Navigation Drawer | Syncfusion®
description: Learn here all about Toggle methods support in Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: SfNavigationDrawer
documentation: UG
---

# Toggle Methods in .NET MAUI Navigation Drawer (SfNavigationDrawer)

The drawer in the SfNavigationDrawer can be toggled using the following methods:

* IsOpen property
* ToggleDrawer method
* Swipe gesture

## Opening drawer programmatically

The [IsOpen](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html#Syncfusion_Maui_Toolkit_NavigationDrawer_SfNavigationDrawer_IsOpen) property and [ToggleDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html#Syncfusion_Maui_Toolkit_NavigationDrawer_SfNavigationDrawer_ToggleDrawer) method enable programmatically opening or closing the drawer.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer" IsOpen="True">
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}	
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer()
{
    IsOpen = true,
};

{% endhighlight %}

{% endtabs %}

Using [ToggleDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html#Syncfusion_Maui_Toolkit_NavigationDrawer_SfNavigationDrawer_ToggleDrawer) method:

{% highlight c# %} 

navigationDrawer.ToggleDrawer();

{% endhighlight %}

Toggling drawer by swipe gesture is explained in [Swipe Gesture and Sensitivity](https://help.syncfusion.com/maui/navigationdrawer/swipe-gesture) section.