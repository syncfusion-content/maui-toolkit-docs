---
layout: post
title: Setting Toggle Animations in .NET MAUI Navigation Drawer | Syncfusion®
description: Learn all about setting Toggle Animations support in the Syncfusion® .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: SfNavigationDrawer
documentation: UG
---

# Setting Toggle Animations in .NET MAUI Navigation Drawer

The drawer toggling animation can be changed using the [Transition](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.DrawerSettings.html#Syncfusion_Maui_Toolkit_NavigationDrawer_DrawerSettings_Transition) property. It can be set to three different values.

* [SlideOnTop](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.Transition.html#Syncfusion_Maui_Toolkit_NavigationDrawer_Transition_SlideOnTop)

* [Push](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.Transition.html#Syncfusion_Maui_Toolkit_NavigationDrawer_Transition_Push)

* [Reveal](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.Transition.html#Syncfusion_Maui_Toolkit_NavigationDrawer_Transition_Reveal)

N> The default animation is [SlideOnTop](https://helpstaging.syncfusion.com:14038/cr/maui-toolkit/Syncfusion.Maui.Toolkit.NavigationDrawer.Transition.html#Syncfusion_Maui_Toolkit_NavigationDrawer_Transition_SlideOnTop).

## SlideOnTop

The navigation pane overlays the main content area when it is opened. It can be set as follows:

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings Transition="SlideOnTop">
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>
	
{% endhighlight %}	
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    Transition = Transition.SlideOnTop,
};
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

![SlideOnTop](Images/drawer-animation/slideontop_animation.png)

## Push

The navigation pane is hidden. When opened, it will push the main content area on the opposite side up to the width of the drawer. It can be set as follows:

{% tabs %}	

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings Transition="Push">
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>

{% endhighlight %}
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    Transition = Transition.Push,
};
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

![Push](Images/drawer-animation/push_animation.png)

## Reveal

The navigation pane is hidden behind the main content. The main content moves away on the opposite side up to the drawer width to show the drawer content. It can be set as follows:

{% tabs %}

{% highlight xaml %}

<navigationdrawer:SfNavigationDrawer x:Name="navigationDrawer">
    <navigationdrawer:SfNavigationDrawer.DrawerSettings>
        <navigationdrawer:DrawerSettings Transition="Reveal">
        </navigationdrawer:DrawerSettings>
    </navigationdrawer:SfNavigationDrawer.DrawerSettings>
</navigationdrawer:SfNavigationDrawer>
	
{% endhighlight %}	
	
{% highlight c# %} 

SfNavigationDrawer navigationDrawer = new SfNavigationDrawer();
DrawerSettings drawerSettings = new DrawerSettings()
{
    Transition = Transition.Reveal,
};
navigationDrawer.DrawerSettings = drawerSettings;
this.Content = navigationDrawer;

{% endhighlight %}

{% endtabs %}

![Reveal](Images/drawer-animation/reveal_animation.png)