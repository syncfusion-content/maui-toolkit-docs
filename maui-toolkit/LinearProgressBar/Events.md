---
layout: post
title: Events in .NET MAUI Linear ProgressBar | Syncfusion®
description: Learn about events supported in Syncfusion® .NET MAUI Linear ProgressBar (SfLinearProgressBar) control for progress tracking and user interactions.
platform: MAUI
control: SfLinearProgressBar
documentation: ug
---

# Events in .NET MAUI Linear ProgressBar

## ProgressChanged

This event is triggered when the progress value is changed. This event contains the following event argument.

* [`Progress:`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressValueEventArgs.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressValueEventArgs_Progress) Represents the progress value.

The following code sample demonstrates how to customize the color of a progress indicator based on progress using this event. 

{% tabs %} 

{% highlight xaml %}

<progressBar:SfLinearProgressBar x:Name="linearProgressBar" 
                                 ProgressChanged="LinearProgressBar_ProgressChanged" 
                                 Progress="100" />

{% endhighlight %}

{% highlight c# %}

private void LinearProgressBar_ProgressChanged(object sender, ProgressValueEventArgs e)
{
    if (e.Progress < 50)
    {
        this.linearProgressBar.ProgressFill = Colors.Red;
    }
    else
    {
        this.linearProgressBar.ProgressFill = Colors.Green;
    }
}

{% endhighlight %}

{% endtabs %} 

## ProgressCompleted

This event is triggered when the [`Progress`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_Progress) attains the [`Maximum`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_Maximum) value. This event contains the following argument.

* [`Progress:`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressValueEventArgs.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressValueEventArgs_Progress) Represents the progress value.

The following code sample demonstrates how to customize the progress bar when the progress reaches maximum using this event. 

{% tabs %} 

{% highlight xaml %}

<progressBar:SfLinearProgressBar x:Name="linearProgressBar" 
                                 ProgressCompleted="LinearProgressBar_ProgressCompleted" 
                                 Progress="100" />

{% endhighlight %}

{% highlight c# %}

private void LinearProgressBar_ProgressCompleted(object sender, ProgressValueEventArgs e)
{
    this.linearProgressBar.ProgressFill = Colors.Green;
}

{% endhighlight %}

{% endtabs %} 