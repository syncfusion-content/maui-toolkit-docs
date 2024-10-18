---
layout: post
title: Right To Left FlowDirection in .NET MAUI Segmented control
description: Learn about Right To Left support in Syncfusion .NET MAUI Segmented control.
platform: maui-toolkit
control: Segmented control
documentation: ug
---
 
# Right To Left Flow Direction in .NET MAUI Segmented control

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
