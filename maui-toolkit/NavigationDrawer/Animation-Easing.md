---
layout: post
title: Customize Transition Animation in .NET MAUI Navigation Drawer
description: Learn about Animation Easing support in the Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more. 
platform: maui-toolkit
control: SfNavigationDrawer
documentation: UG
---

# Customize Transition Animation in .NET MAUI Navigation Drawer

The `AnimationEasing` property allows you to specify the easing function for the drawer's transition animations during opening and closing. This provides more control over the animation's acceleration and deceleration, allowing for more natural and visually appealing transitions. The default value of the `AnimationEasing` property is [Easing.Linear](https://learn.microsoft.com/en-us/dotnet/api/microsoft.maui.easing.linear?view=net-maui-9.0#microsoft-maui-easing-linear).

The `AnimationEasing` property can be set in both XAML and C# as shown below.

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

![AnimationEasing](Images/animation-easing/AnimationEasing.gif)