---
layout: post
title: Events in .NET MAUI InteractiveViewer | Syncfusion®
description: Learn about available events in Syncfusion® .NET MAUI SfInteractiveViewer control. Explore event handling and interactive features.
platform: maui-toolkit
control: InteractiveViewer
documentation: ug
---

# Events in MAUI InteractiveViewer

## ZoomFactorChanged

The `ZoomFactorChanged` event is triggered after a zoom operation completes on the interactive viewer. The associated argument contains the following information.

* `OldZoomFactor` - Gets the zoom factor before the zoom operation.

* `NewZoomFactor` - Gets the zoom factor after the zoom operation.

{% tabs %}
{% highlight xaml hl_lines="1" %}

<interactiveViewer:SfInteractiveViewer ZoomFactorChanged="OnZoomFactorChanged">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

{% endhighlight %}

{% highlight c# %}

...
InitializeComponent();
SfInteractiveViewer viewer = new SfInteractiveViewer();
viewer.ZoomFactorChanged += OnZoomFactorChanged;
viewer.Content = new Image { Source = "photo.png" };
...

private void OnZoomFactorChanged(object sender, ZoomFactorChangedEventArgs e)
{
    // handle event action.
    var oldZoom = e.OldZoomFactor;
    var newZoom = e.NewZoomFactor;
}
...

{% endhighlight %}
{% endtabs %}

## ScrollChanged

The `ScrollChanged` event is triggered when the pan position of the interactive viewer changes. The associated argument contains the following information.

* `PanAxis` - Gets the directions in which panning is currently allowed.

* `ZoomFactor` - Gets the current zoom factor applied to the content.

{% tabs %}
{% highlight xaml hl_lines="1" %}

<interactiveViewer:SfInteractiveViewer ScrollChanged="OnScrollChanged">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

{% endhighlight %}

{% highlight c# %}

...
InitializeComponent();
SfInteractiveViewer viewer = new SfInteractiveViewer();
viewer.ScrollChanged += OnScrollChanged;
viewer.Content = new Image { Source = "photo.png" };
...

private void OnScrollChanged(object sender, InteractiveScrollChangedEventArgs e)
{
    // handle event action.
    var axis = e.PanAxis;
    var zoom = e.ZoomFactor;
}
...

{% endhighlight %}
{% endtabs %}
