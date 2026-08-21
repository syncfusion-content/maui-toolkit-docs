---
layout: post
title: Rotate Behavior in MAUI InteractiveViewer | Syncfusion®
description: Learn about the rotate behavior in Syncfusion® .NET MAUI SfInteractiveViewer control. Explore rotation features and usage.
platform: maui-toolkit
control: InteractiveViewer
documentation: ug
---

# Rotate Behavior in MAUI InteractiveViewer

## Rotate

The `Rotate` method rotates the hosted content of the SfInteractiveViewer clockwise by 90 degrees. Consecutive calls continue rotating the content in 90-degree increments, cycling through 0°, 90°, 180°, 270°, and back to 0°.

{% tabs %}
{% highlight xaml hl_lines="1" %}

<interactiveViewer:SfInteractiveViewer x:Name="viewer">
    <Image Source="photo.png" />
</interactiveViewer:SfInteractiveViewer>

&lt;Button Text="Rotate" Clicked="OnRotateClicked" /&gt;

{% endhighlight %}

{% highlight c# %}

...
InitializeComponent();
SfInteractiveViewer viewer = new SfInteractiveViewer();
viewer.Content = new Image { Source = "photo.png" };
...

private void OnRotateClicked(object sender, EventArgs e)
{
    // Rotate content clockwise by 90 degrees
    viewer.Rotate();
}

{% endhighlight %}
{% endtabs %}

## Rotation Sequence

The following table shows the rotation sequence when calling the `Rotate()` method consecutively:

* `Initial state` - Content rotation is 0°

* `1st Rotate()` - Content rotation becomes 90°

* `2nd Rotate()` - Content rotation becomes 180°

* `3rd Rotate()` - Content rotation becomes 270°

* `4th Rotate()` - Content rotation wraps back to 0°

## Rotation Behavior Details

* `Clockwise Only` - Rotation is always applied in the clockwise direction

* `90-Degree Increments` - Only 90-degree rotations are supported through the `Rotate()` method; no arbitrary angles

* `Content-Based` - The rotation is applied to the hosted `Content` view property

* `Rotation After Reset` - Rotation only takes effect after the current pan position and zoom factor have been reset to their defaults, providing a clean centered state before rotation.

* `Null Content Handling` - If `Content` is `null`, the rotation call is skipped silently
