---
layout: post
title: Animation Duration in .NET MAUI Navigation Drawer control | Syncfusion<sup>®</sup>
description: Learn about Animation Duration support in Syncfusion<sup>®</sup> .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: SfNavigationDrawer
documentation: ug
---
# Animation Duration in .NET MAUI Navigation Drawer (SfNavigationDrawer)

## Animation Duration in SfNavigationDrawer

The [Duration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_Duration) property of the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html) indicates the timeline for completing one animation cycle. Setting a smaller duration value accelerates animation speed.

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings  Duration="200"/>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}

{% highlight c# %}

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
navigationDrawer.DrawerSettings = new DrawerSettings()
{
    Duration = 200,
};
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

N> The [Duration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_Duration) property for the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html) is measured in milliseconds.

The following screenshot illustrates the result of the above code.

![Duration](Images/animation-duration/navigation_duration.gif)