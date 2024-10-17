---
layout: post
title: Customization in .NET MAUI Effects View control | Syncfusion
description: Learn here all about Customization support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Customization in .NET MAUI Effects View (SfEffectsView)

The [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html) control provides support to customize the animation duration, color, and more. This section explains how to customize the effects view control.

## RippleAnimationDuration

The [RippleAnimationDuration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_RippleAnimationDuration) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html) is used to customize the duration of ripple animation.

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView RippleAnimationDuration="800"/> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    RippleAnimationDuration = 800
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

## ScaleAnimationDuration

The [ScaleAnimationDuration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_ScaleAnimationDuration) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html) is used to customize the duration of scale animation.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView 
        ScaleAnimationDuration="800"
        LongPressEffects="Scale"
        ScaleFactor="0.85"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    ScaleAnimationDuration = 800,
    LongPressEffects = SfEffects.Scale,
    ScaleFactor = 0.85
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

## RotationAnimationDuration

The [RotationAnimationDuration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_RotationAnimationDuration) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html) is used to customize the duration of rotation animation.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView 
        RotationAnimationDuration="800"
        Angle="180"
        TouchDownEffects="Rotation"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    RotationAnimationDuration = 800,
    Angle = 180,
    TouchDownEffects = SfEffects.Rotation
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

## InitialRippleFactor

The [InitialRippleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_InitialRippleFactor) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to customize the radius of the ripple when ripple animation starts.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView InitialRippleFactor="0.1"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    InitialRippleFactor = 0.1
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View InitialRippleFactor customization](Customization_images/EffectsView_InitialRippleFactor.gif)

## ScaleFactor

The [ScaleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_ScaleFactor) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to customize the scale of the view.

{% tabs %} 

{% highlight xaml %} 

<ContentPage
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        ScaleFactor="0.85"
        LongPressEffects="Scale"
        TouchDownEffects="None"
        TouchUpEffects="None"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    ScaleFactor = 0.85,
    LongPressEffects = SfEffects.Scale,
    TouchDownEffects = SfEffects.None,
    TouchUpEffects = SfEffects.None
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View ScaleFactor customization](Customization_images/EffectsView_Scale.gif)

## HighlightBackground

The [HighlightBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_HighlightBackground) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to customize the color of highlight effect.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        HighlightBackground="#2196F3"
        TouchDownEffects="Highlight"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    effectsView.HighlightBackground = new SolidColorBrush(Colors.Aqua),
    TouchDownEffects = SfEffects.Highlight
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View highlight background customization](Customization_images/EffectsView_Highlight.png)

## RippleBackground

The [RippleBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_RippleBackground) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to customize the color of ripple.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
   xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView RippleBackground="#2196F3"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    RippleBackground = new SolidColorBrush(Colors.Aqua)
};

this.Content = effectsView;
            
{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View ripple background customization](Customization_images/EffectsView_RippleColor.gif)

## SelectionBackground

The [SelectionBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_SelectionBackground) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to customize the color of selection effect.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        LongPressEffects="Selection"
        SelectionBackground="#2196F3"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    LongPressEffects = SfEffects.Selection,
    SelectionBackground = new SolidColorBrush(Colors.Aqua)
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View selection background customization](Customization_images/EffectsView_Selection.png)

## Angle

The [Angle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_Angle) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html?tabs=tabid-1) is used to customize the rotation angle.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        Angle="180"
        TouchDownEffects="Ripple,Rotation"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    Angle = 180,
    TouchDownEffects = SfEffects.Ripple | SfEffects.Rotation
};

this.Content = effectsView;
            
{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View rotation angle customization](Customization_images/EffectsView_Rotation.png)

