---
layout: post
title: Customize the indicator in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn here all about selection indicator customization support in Syncfusion .NET MAUI Tab View (SfTabView) control and more.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Customize the selection indicator in .NET MAUI Tab View (SfTabView)

## Placement options

The .NET MAUI Tab View provides three options for aligning the selection indicator relative to the tab header item: top, bottom, and fill. You can set the alignment by configuring the [IndicatorPlacement](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IndicatorPlacement) property.

### Top

The selection indicator will be positioned at the top of the selected tab. You can set this using the `IndicatorPlacement` property, as shown in the following code snippets:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorPlacement="Top"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorPlacement = TabIndicatorPlacement.Top;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator placed at the top of the tab header:

![.NET MAUI TabView Indicator Placement Top](images/Selection-Indicator-placement-Top.png) 

### Bottom

The selection indicator will be positioned at the bottom of the selected tab. You can set this using the `IndicatorPlacement` property, as shown in the following code snippets:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorPlacement="Bottom"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorPlacement = TabIndicatorPlacement.Bottom;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator placed at the bottom of the tab header:

![.NET MAUI TabView Indicator Placement Bottom](images/Selection-Indicator-placement-Bottom.png) 

### Fill

The selection indicator will fill the selected tab. You can set this using the `IndicatorPlacement` property, as shown in the following code snippets:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorPlacement="Fill"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorPlacement = TabIndicatorPlacement.Fill;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator filling the entire tab header:

![.NET MAUI TabView Indicator Placement Fill](images/Selection-Indicator-placement-Fill.png) 

## Background customization

The background of the indicator can be customized using the [IndicatorBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IndicatorBackground) property of `SfTabView`.

### Solid color 

You can customize the selection indicator's background color using the [`IndicatorBackground`](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IndicatorBackground) property of `SfTabView`. Below are examples of how to set a solid background color using this property in XAML and C#:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorBackground="LightBlue"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorBackground = Colors.LightBlue;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator background customization:

![.NET MAUI TabView Selection Indicator Background](images/Selection-Indicator-background.png) 

### Gradient color 

You can customize the selection indicator's background using linear or radial gradients. Below are examples of how to apply these gradients:

{% tabs %}
{% highlight xaml %}
    <tabView:SfTabView>
        <tabView:SfTabView.IndicatorBackground>
            <LinearGradientBrush EndPoint="0,1">
                <GradientStop Color="#009FFF" Offset="0.1" />
                <GradientStop Color="#ec2F4B" Offset="1.0" />
            </LinearGradientBrush>
        </tabView:SfTabView.IndicatorBackground>
    </tabView:SfTabView>
{% endhighlight %}
{% highlight C# %}
Microsoft.Maui.Controls.GradientStop gradient1 = new Microsoft.Maui.Controls.GradientStop()
{
    Color = Color.FromArgb("#009FFF"),
    Offset = (float)0.1,
};

Microsoft.Maui.Controls.GradientStop gradient2 = new Microsoft.Maui.Controls.GradientStop()
{
    Color = Color.FromArgb("#ec2F4B"),
    Offset = (float)1.0,
};

LinearGradientBrush gradientBrush = new LinearGradientBrush()
{
    EndPoint = new Point(0, 1),
    GradientStops = new GradientStopCollection() { gradient1, gradient2 }
};

SfTabView tabView = new SfTabView();
tabView.IndicatorBackground = gradientBrush;

{% endhighlight %}
{% endtabs %}

The following image shows the selection indicator with a gradient background:

![.NET MAUI TabView Selection Indicator Gradient](images/Selection-Indicator-gradient-background.png) 

## Indicator width modes

The [IndicatorWidthMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IndicatorWidthMode) property allows you to customize the width of the selection indicator. By default, this property is set to [Fit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.IndicatorWidthMode.html#Syncfusion_Maui_Toolkit_TabView_IndicatorWidthMode_Fit), which adjusts the indicator width to fit the content of the header item. You can change the width to stretch across the entire header item by setting the `IndicatorWidthMode` property to [Stretch](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.IndicatorWidthMode.html#Syncfusion_Maui_Toolkit_TabView_IndicatorWidthMode_Stretch).

### Fit mode

In Fit mode, the indicator width adjusts to fit the content of the header item. The following examples demonstrate how to set the `IndicatorWidthMode` property to `Fit`:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorWidthMode="Fit"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorWidthMode = IndicatorWidthMode.Fit;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator with the width mode set to `Fit`:

![.NET MAUI TabView Selection Indicator Background](images/IndicatorWidthMode_Fit.png) 

### Stretch mode

In Stretch mode, the indicator width stretches to cover the entire header item. The following examples demonstrate how to set the `IndicatorWidthMode` property to `Stretch`:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorWidthMode="Stretch"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorWidthMode = IndicatorWidthMode.Stretch;
{% endhighlight %}

{% endtabs %}

The following image shows the selection indicator with the width mode set to `Stretch`:

![.NET MAUI TabView Selection Indicator Background](images/IndicatorWidthMode_Stretch.png) 

## Indicator corner radius

You can customize the corner radius of the selection indicator using the [IndicatorCornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IndicatorCornerRadius) property in the `SfTabView`.

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView IndicatorCornerRadius ="5"/>
{% endhighlight %}

{% highlight C# %}
SfTabView tabView = new SfTabView();
tabView.IndicatorCornerRadius  = 5;
{% endhighlight %}

{% endtabs %} 

The following image shows the selection indicator with the corner radius:

![.NET MAUI TabView Selection Indicator Corner Radius](images/IndicatorCornerRadius.png) 