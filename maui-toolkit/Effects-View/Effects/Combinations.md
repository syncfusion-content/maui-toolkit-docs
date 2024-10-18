---
layout: post
title: The .NET MAUI Combination Effects | Effects View control | Syncfusion
description: Learn here all about the combination of effects support in Syncfusion .NET MAUI Effects View (SfEffectsView) control and more.
platform: maui-toolkit
control: Effects View
documentation: ug
---

# Combination of Effects 

The [SfEffectsView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffectsView.html) control provides support to apply multiple [SfEffects](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html) in combination. The following are some valid combinations of [SfEffects](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.EffectsView.SfEffects.html).

## Highlight and ripple

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
            ...
            xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView TouchDownEffects="Highlight,Ripple" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    TouchDownEffects = SfEffects.Highlight | SfEffects.Ripple
};

{% endhighlight %}

{% endtabs %}

## Highlight and selection

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
            ...
            xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView
    LongPressEffects="Selection"
    TouchDownEffects="Highlight" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    LongPressEffects = SfEffects.Selection,
    TouchDownEffects = SfEffects.Highlight
};

{% endhighlight %}

{% endtabs %}

## Ripple and selection

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
            ...
            xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView
    TouchDownEffects="Ripple"
    TouchUpEffects="Selection" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    TouchDownEffects = SfEffects.Ripple,
    TouchUpEffects = SfEffects.Selection
};

{% endhighlight %}

{% endtabs %}

## Highlight, ripple, and selection

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
            ...
            xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView
    LongPressEffects="Selection"
    TouchDownEffects="Highlight,Ripple" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    LongPressEffects = SfEffects.Selection,
    TouchDownEffects = SfEffects.Highlight | SfEffects.Ripple
};

{% endhighlight %}

{% endtabs %}

## Scale and selection

{% tabs %} 

{% highlight xaml %} 

<ContentPage 
            ...
            xmlns:effectsView="clr-namespace:Syncfusion.Maui.Toolkit.EffectsView;assembly=Syncfusion.Maui.Toolkit">
    <ContentPage.Content> 
	 	<effectsView:SfEffectsView LongPressEffects="Scale,Selection" /> 
	</ContentPage.Content> 
</ContentPage>

{% endhighlight %}

{% highlight C# %} 

using Syncfusion.Maui.Toolkit.EffectsView;

var effectsView = new SfEffectsView()
{
    LongPressEffects = SfEffects.Scale | SfEffects.Selection
};

{% endhighlight %}

{% endtabs %}