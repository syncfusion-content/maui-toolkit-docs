---
layout: post
title: States in .NET MAUI Circular ProgressBar control | Syncfusion<sup>&reg;</sup>
description: Learn here all about States support in Syncfusion<sup>&reg;</sup> .NET MAUI Circular ProgressBar (SfCircularProgressBar) control and more.
platform: MAUI
control: SfCircularProgressBar
documentation: ug
---

# States in .NET MAUI Circular ProgressBar (SfCircularProgressBar)

Configure the states of the circular progress bar control depending on the usage.

## Determinate

This is the default state. Use it when the progress estimation is known.

## Indeterminate

By enabling the [`IsIndeterminate`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.ProgressBar.ProgressBarBase.html#Syncfusion_Maui_Toolkit_ProgressBar_ProgressBarBase_IsIndeterminate) property, the state of the circular progress bar can be changed to indeterminate when the progress cannot be estimated or is not being calculated. It can be combined with a determinate mode to know that the application estimates progress before the actual progress starts.

{% tabs %} 

{% highlight xaml %} 

<progressBar:SfCircularProgressBar IsIndeterminate="True"/>

{% endhighlight %}

{% highlight c# %}

SfCircularProgressBar circularProgressBar = new SfCircularProgressBar { IsIndeterminate = true };
this.Content = circularProgressBar;

{% endhighlight %}

{% endtabs %} 

![.NET MAUI Circular ProgressBar in indeterminate state](images/states/circular-progressbar-indeterminate.gif)