---
layout: post
title: Right-To-Left in .NET MAUI Segmented Control | Syncfusion®
description: Learn about right-to-left (RTL) flow direction support in Syncfusion® .NET MAUI Segmented Control to render segment items in reverse order.
platform: maui-toolkit
control: Segmented control
documentation: ug
---
 
# Right-To-Left in .NET MAUI Segmented Control

The `SfSegmentedControl` supports changing the flow direction of items rendering in the right-to-left order by setting the `FlowDirection` to `RightToLeft`.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<ContentPage 
xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit">
    <segmentedControl:SfSegmentedControl x:Name="segmentedControl" FlowDirection="RightToLeft"/>
</ContentPage>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

using Syncfusion.Maui.Toolkit.SegmentedControl;

SfSegmentedControl segmentedControl = new SfSegmentedControl();
segmentedControl.FlowDirection = FlowDirection.RightToLeft;
this.Content = segmentedControl;

{% endhighlight %}
{% endtabs %}

![Right to left in .NET MAUI Segmented control.](images/right-to-left/right-to-left.png)
