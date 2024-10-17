---
layout: post
title: About .NET MAUI Tab View (SfTabView) control | Syncfusion
description: Learn here all about the swiping support in Syncfusion .NET MAUI Tab View (SfTabView) control and more.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Swiping in .NET MAUI Tab View (SfTabView)

The [EnableSwiping](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_EnableSwiping) property of `SfTabView` allows users to switch between tab contents by swiping. By default, the `EnableSwiping` property is set to `false.`

You can enable swiping by setting the `EnableSwiping` property to `true`, as shown in the following code snippets:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView EnableSwiping="True"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.EnableSwiping = true;
{% endhighlight %}

{% endtabs %}

The following image demonstrates the swiping functionality in action:

![.NET MAUI TabView Swiping](images/tabview-swiping.gif)

### Limitations

Interference Between Child Controls and Tab View Swiping: When a child control within a Tab View supports horizontal swiping or interaction (e.g., a horizontal ScrollView, a custom swipe-enabled control, or a carousel), it can interfere with the Tab View's touch gestures. This may result in unintended behavior, such as the Tab View swiping when the child control is meant to handle the gesture, or vice versa. The overlapping gestures can cause confusion and disrupt the expected user experience, leading to a less intuitive interface.