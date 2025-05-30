---
layout: post
title: States in .NET MAUI Linear ProgressBar control | Syncfusion<sup>&reg;</sup>
description: Learn here all about States support in Syncfusion<sup>&reg;</sup> .NET MAUI Linear ProgressBar (SfLinearProgressBar) control and more.
platform: MAUI
control: SfLinearProgressBar
documentation: ug
---

# States in .NET MAUI Linear ProgressBar (SfLinearProgressBar)

Configure the states of the linear progress bar control depending on the usage.

## Determinate

This is the default state. Use it when the progress estimation is known.

## Indeterminate

By enabling the [`IsIndeterminate`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_IsIndeterminate) property, the state of the linear progress bar can be changed to indeterminate when the progress cannot be estimated or is not being calculated. It can be combined with a determinate mode to know that the application estimates progress before the actual progress starts.

{% tabs %} 

{% highlight xaml %} 

<progressBar:SfLinearProgressBar IsIndeterminate="True"/>

{% endhighlight %}

{% highlight c# %}

SfLinearProgressBar linearProgressBar = new SfLinearProgressBar { IsIndeterminate = true};
this.Content = linearProgressBar;

{% endhighlight %}

{% endtabs %} 

![.NET MAUI Linear ProgressBar with buffer](images\states\linear-progressbar-indeterminate.gif)

## Buffer

The secondary task’s progress can be defined using the [`SecondaryProgress`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.SfLinearProgressBar.html#Syncfusion_Maui_Toolkit_ProgressBar_SfLinearProgressBar_SecondaryProgress) property as demonstrated in the following code sample.

{% tabs %} 

{% highlight xaml %} 

<progressBar:SfLinearProgressBar Progress="25" 
                                 SecondaryProgress="75"/>

{% endhighlight %}

{% highlight c# %}

SfLinearProgressBar linearProgressBar = new SfLinearProgressBar();
linearProgressBar.Progress = 25;
linearProgressBar.SecondaryProgress = 75;
this.Content = linearProgressBar;

{% endhighlight %}

{% endtabs %} 

![.NET MAUI Linear ProgressBar with buffer](images\states\buffer.png)