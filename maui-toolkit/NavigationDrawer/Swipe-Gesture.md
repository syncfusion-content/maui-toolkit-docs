---
layout: post
title: SwipGesture in .NET MAUI Navigation Drawer | Syncfusion
description: Learn here all about SwipGesture support in Syncfusion .NET MAUI Navigation Drawer (SfNavigationDrawer) control and more.
platform: maui-toolkit
control: NavigationDrawer
documentation: ug
---
# Swipe Gesture in .NET MAUI Navigation Drawer (SfNavigationDrawer)

The NavigationDrawer supports the swipe gesture for both opening and closing the drawer. 

## Enabling Swipe Gesture

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

## Swipe Sensitivity

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

### Limitations

* When the navigation drawer is placed inside a `ScrollView`, it can interfere with the navigation drawer's touch gestures.
* This may lead to unintended behavior, such as the navigation drawer responding to swipe gestures meant for the `ScrollView`, or vice versa. Overlapping gestures can cause confusion and disrupt the user experience, resulting in a less intuitive interface.