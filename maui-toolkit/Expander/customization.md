---
layout: post
title: Customization in .NET MAUI Expander control | Syncfusion®
description: Learn here all about Customization in Syncfusion® Toolkit .NET MAUI Expander (SfExpander), its elements and more.
platform: maui-toolkit
control: SfExpander
documentation: ug
---
# Customization in .NET MAUI Expander

## Animation duration

The `SfExpander` allows you to customize the duration of the expanding and collapsing animations by using the `AnimationDuration` property. By default, the animation duration is set to `300 milliseconds`.

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfExpander x:Name="expander" 
                           AnimationDuration="250"/>
{% endhighlight %}
{% highlight c# %}
    expander.AnimationDuration = 250;
{% endhighlight %}
{% endtabs %}

## Animation easing

The `SfExpander` allows you to customize the rate of change of parameters over time or the animation style by using the `AnimationEasing` property. By default, the animation easing is set to `Linear`.

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfExpander x:Name="expander"
                           AnimationEasing="SinOut"/>       
{% endhighlight %}
{% highlight c# %}
    expander.AnimationEasing = ExpanderAnimationEasing.SinOut;
{% endhighlight %}
{% endtabs %}

## Expand and collapse 

The `SfExpander` allows users to programmatically expand or collapse its content using the `IsExpanded` property. Users can manage the expand and collapse actions by handling the `Expanding` and `Collapsing` events.

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfExpander x:Name="expander" 
                           IsExpanded="True"/>        
{% endhighlight %}
{% highlight c# %}
    expander.IsExpanded = true;
{% endhighlight %}
{% endtabs %}

## Events 

There are four built-in events in the SfExpander control namely:

* `Expanding`
* `Expanded`
* `Collapsing`
* `Collapsed`

### Expanding Event

The `Expanding` event will be triggered when the expander control is being expanded.Expansion can be canceled using the `ExpandingAndCollapsingEventArgs`, which includes the following property:

* `Cancel`: Indicates that the expansion or collapse action should be canceled.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<syncfusion:SfExpander Expanding="SfExpander_Expanding"/>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void SfExpander_Expanding(object sender, ExpandingAndCollapsingEventArgs e)
{
    e.Cancel = true;
}
{% endhighlight %}
{% endtabs %}

### Expanded Event

The `Expanded` event is triggered when the expander is fully expanded. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<syncfusion:SfExpander Expanded="SfExpander_Expanded"/>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" %}
private void SfExpander_Expanded(object sender, ExpandedAndCollapsedEventArgs e)
{
    // Codes that need to be executed once the expander is expanded.
}
{% endhighlight %}
{% endtabs %}

### Collapsing Event

The `Collapsing` event will be triggered when the expander control is being collapsed.Collapsing can be canceled using the `ExpandingAndCollapsingEventArgs`, which includes the following property:

* `Cancel`: Indicates that the expansion or collapse action should be canceled.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<syncfusion:SfExpander Collapsing="SfExpander_Collapsing"/>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void SfExpander_Collapsing(object sender, ExpandingAndCollapsingEventArgs e)
{
    e.Cancel = true;
}
{% endhighlight %}
{% endtabs %}

### Collapsed Event 

The `Collapsed` event is triggered when the expander is collapsed. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<syncfusion:SfExpander Collapsed="SfExpander_Collapsed"/>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" %}
private void SfExpander_Collapsed(object sender, ExpandedAndCollapsedEventArgs e)
{
    // Codes that need to be executed once the expander is collapsed.
}
{% endhighlight %}
{% endtabs %}
