---
layout: post
title: Animation in .NET MAUI Navigation Drawer | Syncfusion®
description: Learn about Animation Duration and Easing support in the Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: SfNavigationDrawer
documentation: UG
---

# Animation in .NET MAUI Navigation Drawer (SfNavigationDrawer)

## Customizing animation duration

The [Duration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_Duration) property of the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html) specifies the timeline for completing one animation cycle. Setting a smaller duration value accelerates animation speed.

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

## Animation easing effects

The `AnimationEasing` property of the [SfNavigationDrawer](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.SfNavigationDrawer.html) allows you to customize the acceleration and deceleration of the drawer’s transition animations when opening and closing. The default value for `AnimationEasing` is [Easing.Linear](https://learn.microsoft.com/en-us/dotnet/api/microsoft.maui.easing.linear?view=net-maui-9.0#microsoft-maui-easing-linear).

{% tabs %}
{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings AnimationEasing="{x:Static Easing.CubicIn}"/>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}
{% highlight c# %}

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();

navigationDrawer.DrawerSettings = new DrawerSettings()
{
    AnimationEasing = Easing.CubicIn,
};
this.Content = navigationDrawer;

{% endhighlight %}
{% endtabs %}
