---
layout: post
title: Customization in .NET MAUI PullToRefresh control | Syncfusion
description: Learn about customization features support in Syncfusion .NET MAUI PullToRefresh (SfPullToRefresh) control and more.
platform: maui-toolkit
control: SfPullToRefresh
documentation: ug
---

# Customization in .NET MAUI PullToRefresh (SfPullToRefresh)

The .NET MAUI PullToRefresh control supports customization of various features, including TransitionMode, PullingThreshold, ProgressBackground, ProgressColor, and more. The control can be personalized using the following properties.

## PullableContent

The [PullableContent](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_Toolkit_PullToRefresh_SfPullToRefresh_PullableContent) is the main view of the [PullToRefresh](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html) control on which the desired items can be placed.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="6 11" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh"
                                      PullingThreshold="120"
                                      RefreshViewHeight="30"
                                      RefreshViewThreshold="30"
                                      RefreshViewWidth="30">
    <PullToRefreshControl:SfPullToRefresh.PullableContent>
            <Label x:Name="Monthlabel" 
                    TextColor="White" 
                    HorizontalTextAlignment="Center"   
                    VerticalTextAlignment="Start" />
    </PullToRefreshControl:SfPullToRefresh.PullableContent>
</PullToRefreshControl:SfPullToRefresh>

{% endhighlight %}
{% endtabs %}

## TransitionMode

The [TransitionMode](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_PullToRefresh_SfPullToRefresh_TransitionMode) property specifies the mode of the animations. It has the following two modes:

* [SlideOnTop](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_Toolkit_PullToRefresh_SfPullToRefresh_TransitionMode)
* [Push](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.PullToRefreshTransitionType.html#Syncfusion_Maui_Toolkit_PullToRefresh_PullToRefreshTransitionType_Push)

The default transition is `SlideOnTop` that draws the RefreshView on top of the `PullableContent`.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      TransitionMode="SlideOnTop" />

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.TransitionMode = PullToRefreshTransitionType.SlideOnTop;

{% endhighlight %}
{% endtabs %}

![.NET MAUI PullToRefresh with slide on top transition mode.](Images/customization/net-maui-pulltorefresh-getting-started.png)

The following code example shows how to set the `TransitionMode` as `Push` to PullToRefresh. This transition moves the refresh content and main content simultaneously.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name=" pullToRefresh" 
                                      TransitionMode="Push" />

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.TransitionMode = PullToRefreshTransitionType.Push;

{% endhighlight %}
{% endtabs %}

![.NET MAUI PullToRefresh with push transition mode.](Images/customization/net-maui-pulltorefresh-getting-started-push.png)

## RefreshViewThreshold

The threshold value for the refresh view, indicating the starting position of the progress indicator within the view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewThreshold="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewThreshold = 50d;

{% endhighlight %}
{% endtabs %}

## PullingThreshold

The threshold value for the refresh view, indicating the progress indicator's maximum pulling position in view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                            PullingThreshold="200"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.PullingThreshold = 200d;

{% endhighlight %}
{% endtabs %}


## IsRefreshing

The view will get refresh while the [IsRefreshing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_Toolkit_PullToRefresh_SfPullToRefresh_IsRefreshing) property is set to `true,` and View refreshing will be stopped when you set the `IsRefreshing` to `false.`
 
{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      IsRefreshing="True"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.IsRefreshing = true;

{% endhighlight %}
{% endtabs %}


## ProgressBackground

The color to the progress indicator's background.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressBackground = "White"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressBackground = Color.White;

{% endhighlight %}
{% endtabs %}


## ProgressColor

The color to the progress indicator's arc. 

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressColor = "Blue"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressColor = Color.Blue;

{% endhighlight %}

{% endtabs %}


## ProgressThickness

The width of the progress indicator's arc. 

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      ProgressThickness="5"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.ProgressThickness = 5d;

{% endhighlight %}
{% endtabs %}


## RefreshViewWidth

The width of the refresh view.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewWidth="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewWidth = 50d;

{% endhighlight %}

{% endtabs %}


## RefreshViewHeight

The height to the refresh View.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="2" %}

<PullToRefreshControl:SfPullToRefresh x:Name="pullToRefresh" 
                                      RefreshViewHeight="50"/>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.RefreshViewHeight = 50d;

{% endhighlight %}
{% endtabs %}


## Programmatic Support 

### StartRefreshing()

The [StartRefreshing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_Toolkit_PullToRefresh_SfPullToRefresh_StartRefreshing) method is used to refresh the content without interaction in pullable content. When you invoke this StartRefreshing() method,then the Progress indicator will be shown. 

{% tabs %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.StartRefreshing();

{% endhighlight %}
{% endtabs %}

### EndRefreshing()

The [EndRefreshing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.PullToRefresh.SfPullToRefresh.html#Syncfusion_Maui_Toolkit_PullToRefresh_SfPullToRefresh_EndRefreshing) method is used to end the progress animation of the `PullToRefresh`.

{% tabs %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}

pullToRefresh.EndRefreshing();

{% endhighlight %}
{% endtabs %}