---
layout: post
title: The .NET MAUI Ripple Effects | Effects View control | Syncfusion<sup>®</sup>
description: Learn here all about ripple effect support in Syncfusion<sup>®</sup> .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Ripple Effect in .NET MAUI Effects View (SfEffectsView)

The [SfEffects.Ripple](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Ripple) is a expandable circle, which is initially placed on the tapped location, and it grows till the whole layout is filled. [SfEffects.Ripple](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Ripple) is rendered based on [InitialRippleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_InitialRippleFactor).

{% tabs %} 

{% highlight xaml %}

<ContentPage 
   xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView TouchDownEffects="Ripple" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    TouchDownEffects = SfEffects.Ripple
};
this.Content = effectsView;  

{% endhighlight %}

{% endtabs %}

![.net maui ripple effect](Effects_images/net_maui_ripple_effect.gif)