---
layout: post
title: Features in .NET MAUI Effects View control | Syncfusion<sup>®</sup>
description: Learn here all about Features support in Syncfusion<sup>®</sup> .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Features in .NET MAUI Effects View (SfEffectsView)

The [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) control provides the following additional features to enhance the effects:

## FadeOutRipple

By enabling the [FadeOutRipple](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_FadeOutRipple) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html), the expandable circle will lose its opacity to 0 on growing.

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
    	FadeOutRipple="True"
    	RippleAnimationDuration="1000"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

 var effectsView = new SfEffectsView
 {
     FadeOutRipple = true,
     RippleAnimationDuration = 1000
 };

 this.Content = effectsView;
            
{% endhighlight %}

{% endtabs %}

![.NET MAUI Effects View FadeOutRipple](Features_images/EffectsView_Fadeout_Ripple.gif)

## IsSelected

Enabling the [IsSelected](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_IsSelected) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) sets the view state as selected.

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView IsSelected="true"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    IsSelected = true,
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

## ShouldIgnoreTouches

Enabling the [ShouldIgnoreTouches](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_ShouldIgnoreTouches) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) cancels the direct interaction of the [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html).

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView ShouldIgnoreTouches="true"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    ShouldIgnoreTouches = true
};

this.Content = effectsView;

{% endhighlight %}

{% endtabs %}

