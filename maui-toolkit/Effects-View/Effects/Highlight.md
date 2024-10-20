---
layout: post
title: The .NET MAUI Highlight Effects | Effects View control | Syncfusion
description: Learn here all about highlight effect support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Highlight Effect in .NET MAUI Effects View (SfEffectsView)

[SfEffects.Highlight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffects_Highlight) is a smooth transition on the background color of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html)

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

![.net maui highlight effect](Effects_images/net_maui_highlight_effect.png)