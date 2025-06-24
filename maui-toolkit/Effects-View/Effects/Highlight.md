---
layout: post
title: The .NET MAUI Highlight Effects | Effects View Control | Syncfusion®
description: Learn about highlight effect support in Syncfusion® .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: SfEffectsView
documentation: UG
---

# Highlight Effect in .NET MAUI Effects View (SfEffectsView)

[SfEffects.Highlight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Highlight) provides a smooth transition on the background color of the [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html)

{% tabs %} 

{% highlight xaml %}

<ContentPage 
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	<effectsView:SfEffectsView  
        TouchDownEffects="Highlight" 
        HighlightBackground="#FF0000"/> 
	</ContentPage.Content>  
</ContentPage>

{% endhighlight %}

{% highlight C# %}

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    TouchDownEffects = SfEffects.Highlight,
    HighlightBackground = new SolidColorBrush(Colors.Aqua)
};
this.Content = effectsView;  

{% endhighlight %}

{% endtabs %}

![Highlight effect](Effects_images/net_maui_highlight_effect.png)