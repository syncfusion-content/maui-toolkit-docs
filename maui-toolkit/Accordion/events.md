---
layout: post
title: Events in .NET MAUI Accordion control | Syncfusion®
description: Learn about events support in Syncfusion® Toolkit for .NET MAUI Accordion control, its elements and more.
platform: maui-toolkit
control: SfAccordion
documentation: ug
--- 

# Accordion Events in .NET MAUI Accordion (SfAccordion)

There are four built-in events in the SfAccordion control namely:

* `Expanding`
* `Expanded`
* `Collapsing`
* `Collapsed`

### Expanding Event

The `Expanding` event will be triggered when the accordion item is being expanded. It can cancel the expansion using `ExpandingAndCollapsingEventArgs`, which contains the following property:

* `Cancel`: Indicates that the expansion or collapse action should be cancelled.
* `Index`: Gets the index of the current expanding accordion item.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Expanding="accordion_Expanding"/>   
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void accordion_Expanding(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandingAndCollapsingEventArgs e)
{
    if (e.Index == 2)
    {
        e.Cancel = true;
    }
}
{% endhighlight %}
{% endtabs %}

### Expanded Event

The `Expanded` event is triggered when an accordion item is fully expanded. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Expanded="accordion_Expanded"/>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void accordion_Expanded(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandingAndCollapsingEventArgs e)
{
    if (e.Index == 2)
    {
        e.Cancel = true;
    }
}
{% endhighlight %}
{% endtabs %}

### Collapsing Event

The `Collapsing` event will be triggered when the expander control is being collapsed. You can cancel the collapsing using `ExpandingAndCollapsingEventArgs`, which contains the following property:

* `Cancel`: Indicates that the expansion or collapse action should be cancelled.
* `Index`: Gets the index of the current collapsing accordion item.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Collapsing="accordion_Collapsing"/>   
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void accordion_Collapsing(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandingAndCollapsingEventArgs e)
{
    if (e.Index == 2)
    {
        e.Cancel = true;
    }
}
{% endhighlight %}
{% endtabs %}

### Collapsed Event 

The `Collapsed` event is triggered when an accordion item is collapsed. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Collapsed="accordion_Collapsed"/>   
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="4" %}
private void accordion_Collapsed(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandedAndCollapsedEventArgs e)
{
    // Get the index of current accordion item
    int index = e.Index;
}
{% endhighlight %}
{% endtabs %}