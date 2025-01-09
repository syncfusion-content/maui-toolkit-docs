---
layout: post
title: The .NET MAUI Rotate Animation | Effects View control | Syncfusion<sup>®</sup>
description: Learn here all about rotation effect support in Syncfusion<sup>®</sup> .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Rotation Effect in .NET MAUI Effects View (SfEffectsView)

[SfEffects.Rotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Rotation) provides a circular movement to [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) around the center of the [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) based on the specified [Angle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_Angle).

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView
        TouchDownEffects="Rotation"
        Angle="180" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    TouchDownEffects = SfEffects.Rotation,
    Angle = 180,
};
this.Content = effectsView;  

{% endhighlight %}

{% endtabs %}

![.net maui rotation animation](Effects_images/net_maui_rotation_animation.gif)