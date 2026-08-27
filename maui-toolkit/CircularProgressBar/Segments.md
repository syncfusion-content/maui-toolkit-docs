---
layout: post
title: Segments in .NET MAUI Circular Progress Bar | Syncfusion®
description: Learn about segmented progress visualization and multiple progress sections in Syncfusion® .NET MAUI Circular Progress Bar (SfCircularProgressBar) control.
platform: MAUI
control: SfCircularProgressBar
documentation: ug
---

# Segments in .NET MAUI Circular Progress Bar

To visualize the progress of multiple sequential tasks, split the circular progress bar into multiple segments by setting the [`SegmentCount`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_SegmentCount) property as demonstrated in the following code sample.

{% tabs %} 

{% highlight xaml %}

<progressBar:SfCircularProgressBar Progress="25" 
                                   SegmentCount="7" />

{% endhighlight %}

{% highlight c# %}

SfCircularProgressBar circularProgressBar = new SfCircularProgressBar();
circularProgressBar.Progress = 25;
circularProgressBar.SegmentCount = 7;
this.Content = circularProgressBar;

{% endhighlight %}

{% endtabs %} 

![.NET MAUI Circular Progress Bar with segment](images/segment/segment.png)

## Gap customization

Customize the default spacing between the segments using the [`SegmentGapWidth`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_SegmentGapWidth) property as demonstrated in the following code sample.

{% tabs %} 
{% highlight xaml %}

<progressBar:SfCircularProgressBar Progress="25"
                                   SegmentCount="7" 
                                   SegmentGapWidth="10" />

{% endhighlight %}

{% highlight c# %}

SfCircularProgressBar circularProgressBar = new SfCircularProgressBar();
circularProgressBar.Progress = 25;
circularProgressBar.SegmentCount = 7;
circularProgressBar.SegmentGapWidth = 10;
this.Content = circularProgressBar;

{% endhighlight %}

{% endtabs %} 

![.NET MAUI Circular Progress Bar with segment gap width](images/segment/gap-width.png)