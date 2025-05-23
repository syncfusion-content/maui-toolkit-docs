---
layout: post
title: Swiping in .NET MAUI Tab View (SfTabView) Control | Syncfusion®
description: Learn about the swiping support and more in the Syncfusion® .NET MAUI Tab View (SfTabView) control.
platform: maui-toolkit
control: SfTabView
documentation: UG
---

# Swiping in .NET MAUI Tab View (SfTabView)

The [EnableSwiping](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_EnableSwiping) property of `SfTabView` allows users to switch between tab contents by swiping. By default, the `EnableSwiping` property is set to `false`.

You can enable swiping by setting the `EnableSwiping` property to `true`, as shown in the following code snippets:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with swiping enabled -->
<tabView:SfTabView EnableSwiping="True" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Enable swiping for the tab view
tabView.EnableSwiping = true;
{% endhighlight %}

{% endtabs %}

The following image demonstrates the swiping functionality in action:

![.NET MAUI Tab View Swiping](images/tabview-swiping.gif)

### Limitations

Interference Between Child Controls and Tab View Swiping: When a child control within a Tab View supports horizontal swiping or interaction (e.g., a horizontal ScrollView, a custom swipe-enabled control, or a carousel), it can interfere with the Tab View's touch gestures. This may result in unintended behavior, such as the Tab View swiping when the child control is meant to handle the gesture, or vice versa. The overlapping gestures can cause confusion and disrupt the expected user experience, leading to a less intuitive interface.