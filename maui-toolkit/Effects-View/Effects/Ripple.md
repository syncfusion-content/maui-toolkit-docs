---
layout: post
title: The .NET MAUI Ripple Effects | Effects View Control | Syncfusion®
description: Learn all about ripple effect support in Syncfusion® .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: SfEffectsView
documentation: UG
---

# Ripple Effect in .NET MAUI Effects View (SfEffectsView)

The [SfEffects.Ripple](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Ripple) is an expandable circle that is initially placed at the tapped location and grows until the whole layout is filled. The [SfEffects.Ripple](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Ripple) is rendered based on the [InitialRippleFactor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_InitialRippleFactor).

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

![Ripple effect](Effects_images/net_maui_ripple_effect.gif)