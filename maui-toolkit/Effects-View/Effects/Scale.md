---
layout: post
title: The .NET MAUI Scale Animation | Effects View control | Syncfusion
description: Learn here all about scale effect support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Scale Effect in .NET MAUI Effects View (SfEffectsView)

[SfEffects.Scale](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Scale) is a smooth transition on the size of the [SfEffectsView.Content](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_Content) from its actual size to the size calculated based on [ScaleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_ScaleFactor) in pixels.

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

![.net maui scale animation](Effects_images/net_maui_scale_animation.png)