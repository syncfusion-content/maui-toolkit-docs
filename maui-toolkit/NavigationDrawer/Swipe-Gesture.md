---
layout: post
title: Swipe Gesture in .NET MAUI Navigation Drawer | Syncfusion®
description: Learn all about Swipe Gesture support in the Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: SfNavigationDrawer
documentation: UG
---
# Swipe Gesture in .NET MAUI Navigation Drawer (SfNavigationDrawer)

The Navigation Drawer supports the swipe gesture for both opening and closing the drawer. 

## Enabling swipe gesture

The [EnableSwipeGesture](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_EnableSwipeGesture) property can activate or deactivate the swipe functionality in the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html).

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings EnableSwipeGesture="True">
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}	
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    EnableSwipeGesture= true,
};
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

## Swipe sensitivity

The [TouchThreshold](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_TouchThreshold) property in the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html) can expand the swipe region. The default value of TouchThreshold is `120`.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings TouchThreshold="200">
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}	
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    TouchThreshold = 200,
};
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}