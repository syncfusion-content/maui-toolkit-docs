---
layout: post
title: Events in .NET MAUI Segmented control | Syncfusion
description: Learn here all about the Events support in Syncfusion<sup>&reg;</sup> .NET MAUI Segmented Control (SfSegmentedControl).
platform: maui-toolkit
control: Segmented control
documentation: ug
---

# Events in .NET MAUI Segmented Control (SfSegmentedControl)

The Segmented Control supports the `Tapped,` and `SelectionChanged` events to interact with .NET MAUI Segmented Control

## Tapped

A Tapped event occurs, each time a segment tapped.

Below is a list of the arguments:

* `Sender`: This contains the `SfSegmentedControl` object.

* `Tapped`: The tapped action performed on an Segment can be found in the `SegmentTappedEventArgs`, you can see details about the `SegmentItem`.

## SelectionChanged

The [SelectionChanged](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_SfSegmentedControl_SelectionChanged) event is triggered once the segment is selected in the segmented control. The [SelectionChangedEventArgs](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SelectionChangedEventArgs.html) has the following values, which provide information for the `SelectionChanged` event.

* OldIndex
* NewIndex
* OldValue
* NewValue

{% tabs %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl segmentedControl = new SfSegmentedControl();
        segmentedControl.SelectionChanged += OnSegmentedControlSelectionChanged;
        this.Content = segmentedControl;
    }

    private void OnSegmentedControlSelectionChanged(object sender, Syncfusion.Maui.Toolkit.SegmentedControl.SelectionChangedEventArgs e)
    {
        var newValue = e.NewValue;
        var oldValue = e.OldValue;
        var newIndex = e.NewIndex;
        var oldIndex = e.OldIndex;
    }
}

{% endhighlight %}
{% endtabs %}