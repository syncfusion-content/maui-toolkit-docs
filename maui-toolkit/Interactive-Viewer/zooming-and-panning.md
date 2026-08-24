---
layout: post
title: Zoom and Panning Behavior in MAUI InteractiveViewer | Syncfusion®
description: Learn about the zoom and panning behavior in Syncfusion® .NET MAUI SfInteractiveViewer control. Explore ZoomFactor, MinimumZoomFactor, MaximumZoomFactor, and pan properties.
platform: maui-toolkit
control: InteractiveViewer
documentation: ug
---

# Zoom and Panning Behavior in MAUI InteractiveViewer

## Overview

The SfInteractiveViewer provides comprehensive zoom and pan functionality through the following key properties:

* `ZoomFactor` - Gets or sets the current zoom level applied to the content

* `MinimumZoomFactor` - Gets or sets the minimum allowed zoom level

* `MaximumZoomFactor` - Gets or sets the maximum allowed zoom level

* `IsZoomEnabled` - Gets or sets whether zooming is enabled

* `IsPanEnabled` - Gets or sets whether panning is enabled

* `PanAxis` - Gets or sets the allowed directions for panning

## ZoomFactor

The `ZoomFactor` property controls the current zoom level of the content. A value of 1.0 represents the original content size at 100% scale.

{% tabs %}
{% highlight xaml hl_lines="1" %}

<interactiveViewer:SfInteractiveViewer x:Name="viewer" 
                                       ZoomFactor="2.0"
                                       MinimumZoomFactor="1.0"
                                       MaximumZoomFactor="5.0">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

{% endhighlight %}

{% highlight c# %}

...
InitializeComponent();
SfInteractiveViewer viewer = new SfInteractiveViewer();
viewer.Content = new Image { Source = "photo.png" };
viewer.ZoomFactor = 2.0; // Set zoom to 200%
viewer.MinimumZoomFactor = 1.0;
viewer.MaximumZoomFactor = 5.0;
...

{% endhighlight %}
{% endtabs %}

## MinimumZoomFactor

The `MinimumZoomFactor` property sets the lowest zoom level users can zoom out to. The default value is 1.0 (100% scale).

* `Default Value` - 1.0 (content displayed at original size)

* `Applicable When` - `IsZoomEnabled` is set to `true`

* `Constraint` - The current `ZoomFactor` cannot go below this value

## MaximumZoomFactor

The `MaximumZoomFactor` property sets the highest zoom level users can zoom in to. The default value is 10.0 (1000% scale).

* `Default Value` - 10.0 (content can be zoomed up to 10 times original size)

* `Applicable When` - `IsZoomEnabled` is set to `true`

* `Constraint` - The current `ZoomFactor` cannot exceed this value

## Panning Configuration

### IsPanEnabled

The `IsPanEnabled` property enables or disables the pan functionality. When set to `true`, users can drag to move the content around.

* `Default Value` - `true` (panning is enabled)

### PanAxis

The `PanAxis` property specifies the direction(s) in which panning is allowed.

{% tabs %}
{% highlight xaml hl_lines="1" %}

<!-- Allow panning in both horizontal and vertical directions -->
<interactiveViewer:SfInteractiveViewer PanAxis="Both">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

<!-- Allow panning only horizontally -->
<interactiveViewer:SfInteractiveViewer PanAxis="Horizontal">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

<!-- Allow panning only vertically -->
<interactiveViewer:SfInteractiveViewer PanAxis="Vertical">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

{% endhighlight %}

{% highlight c# %}

// Pan in both directions
viewer.PanAxis = PanAxis.Both;

// Pan only horizontally
viewer.PanAxis = PanAxis.Horizontal;

// Pan only vertically
viewer.PanAxis = PanAxis.Vertical;

{% endhighlight %}
{% endtabs %}

## Pan Axis Options

The `PanAxis` enum provides the following options:

| Pan Axis | Description |
|---|---|
| `Both` | Allows panning in both horizontal and vertical directions (default) |
| `Horizontal` | Allows panning only in the horizontal direction |
| `Vertical` | Allows panning only in the vertical direction |

## Zoom and Pan Example

{% tabs %}
{% highlight c# %}

private void ConfigureViewer()
{
    SfInteractiveViewer viewer = new SfInteractiveViewer();
    
    // Configure zoom settings
    viewer.IsZoomEnabled = true;
    viewer.ZoomFactor = 1.0;
    viewer.MinimumZoomFactor = 0.5;    // Allow zoom out to 50%
    viewer.MaximumZoomFactor = 3.0;    // Allow zoom in to 300%
    
    // Configure pan settings
    viewer.IsPanEnabled = true;
    viewer.PanAxis = PanAxis.Both;
    
    // Set content
    viewer.Content = new Image { Source = "photo.png" };
}

{% endhighlight %}
{% endtabs %}
