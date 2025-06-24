---
layout: post
title: The .NET MAUI Scale Animation | Effects View Control | Syncfusion®
description: Learn all about scale effect support in Syncfusion® .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: SfEffectsView
documentation: UG
---

# Scale Effect in .NET MAUI Effects View (SfEffectsView)

The [SfEffects.Scale](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Scale) provides a smooth transition in the size of the [SfEffectsView.Content](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SfContentView.html#Syncfusion_Maui_Toolkit_SfContentView_Content), adjusting from its actual size to a new size based on the [ScaleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_ScaleFactor) specified in pixels.

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        ScaleFactor="0.85"
        TouchDownEffects="None"
        TouchUpEffects="None"
        LongPressEffects="Scale" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    ScaleFactor = 0.85,
    TouchDownEffects = SfEffects.None,
    TouchUpEffects = SfEffects.None,
    LongPressEffects = SfEffects.Scale
};
this.Content = effectsView;  

{% endhighlight %}

{% endtabs %}

![Scale animation](Effects_images/net_maui_scale_animation.png)