---
layout: post
title: Interaction in .NET MAUI Effects View control | Syncfusion
description: Learn here all about Interaction support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Interaction in .NET MAUI Effects View (SfEffectsView)

Effects can be set on different interactions. This section explains how to set effects on different interactions available in effects view.

## TouchDownEffects

The [TouchDownEffects](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_TouchDownEffects) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to render the effects in touch-down interaction.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    ...
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView TouchDownEffects="Ripple"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    TouchDownEffects = SfEffects.Ripple
};

{% endhighlight %}

{% endtabs %}

## LongPressEffects

The [LongPressEffects](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_LongPressEffects) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to render the effects in long-press interaction.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    ...
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView LongPressEffects="Ripple"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    LongPressEffects = SfEffects.Ripple
};

{% endhighlight %}

{% endtabs %}

## TouchUpEffects

The [TouchUpEffects](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html#Syncfusion_Maui_Toolkit_EffectsView_SfEffectsView_TouchUpEffects) property of [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) is used to render the effects in touch-up interaction.

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
    ...
    xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView TouchUpEffects="Ripple"/>
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView
{
    TouchUpEffects = SfEffects.Ripple
};

{% endhighlight %}

{% endtabs %}
