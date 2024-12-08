---
layout: post
title: Customization in .NET MAUI Bottom Sheet (SfBottomSheet) | Syncfusion
description: Learn how to customize bottom sheet in Syncfusion .NET MAUI Bottom Sheet (SfbottomSheet). Explore the options to enhance your bottom sheet appearance.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Customization in .NET MAUI Bottom Sheet (SfBottomSheet)

A `BottomSheet` consists of several elements that can be customized to enhance its appearance and functionality.

## Popup Mode
The `IsModal` property controls whether background interaction is disabled when a bottom sheet is open. When set to `True`, a gray overlay blocks interaction with the background, and tapping it closes the sheet. When set to `False`, the overlay is invisible, allowing users to interact with the content behind the sheet.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" IsModal="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight C# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.IsModal = true;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

![PopUpMode image for BottomSheet](images/popUpMode.png)

## State
The state of the `BottomSheet` can be controlled using the `State` property. The default value is `Hidden`. This property accepts the following values:

* **FullExpanded** - The sheet will expand to cover the full screen.
* **HalfExpanded** - The sheet will expand to cover half of the screen.
* **Collapsed** - The sheet will remain collapsed at the bottom of the screen.
* **Hidden** - The sheet will remain hidden.

The `State` property works together with the `AllowedState` property to control the allowed states of the BottomSheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" State="FullExpanded">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>    
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.State = BottomSheetState.FullExpanded;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Allowed State
The `BottomSheet` allows to control the transition between the states using the `AllowedState` property. The default value is `All`, which allows transitions between all available states. This property accepts the following values:

* **FullExpanded** - It will allow transitions only between the FullExpanded and Collapsed states.
* **HalfExpanded** - It will allow transitions only between the HalfExpanded and Collapsed states.
* **All** - Allows transitions between all available states (FullExpanded, HalfExpanded, Collapsed, and Hidden).

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" AllowedState="HalfExpanded" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.AllowedState = BottomSheetAllowedState.HalfExpanded;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Content Padding
The `ContentPadding` property of the `BottomSheet` adds space around the content creating a gap between the bottom sheet content and the edges.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ContentPadding="15">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.ContentPadding = new Thickness(15);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Background
The `Background` property allows you to customize the background color of the BottomSheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" Background="MediumPurple">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.Background = new SolidColorBrush(Colors.MediumPurple);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

![Background color image for BottomSheet](images/backgroundColor.png)

## CornerRadius
The `CornerRadius` property allows you to add corner radius to the Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" CornerRadius="15, 15, 0, 0">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.CornerRadius = new CornerRadius(15, 15, 0, 0);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

![Corner radius image for BottomSheet](images/cornerRadius.png)
## Adjust the Height
### Full Expanded Height

The `FullExpandedRatio` property adjusts the height of the `BottomSheet` when it is in the `FullExpanded` state. The default value is `1`. You can set a value between 0.1 and 1 to adjust the height.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" FullExpandedRatio="0.8" State="FullExpanded">
 <bottomSheet:SfBottomSheet.BottomSheetContent>
     <Grid/>
 </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.FullExpandedRatio = 0.8;
bottomSheet.State = BottomSheetState.FullExpanded;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

### Half Expanded Height

The `HalfExpandedRatio` property adjusts the height of the `BottomSheet` when it is in the `HalfExpanded` state. The default value is `0.5`. You can set a value between 0.1 and 0.9 to adjust the height.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" HalfExpandedRatio="0.7" State="HalfExpanded">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.HalfExpandedRatio = 0.7;
bottomSheet.State = BottomSheetState.HalfExpanded;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

### Collapsed Height
The `CollapsedHeight` property allows you to specify the height of the `BottomSheet`, when it is in the `Collapsed` state. The default value is `100`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" CollapsedHeight="150">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.CollapsedHeight = 150;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Adjust the Width
The `ContentWidthMode` property allows you to adjust the width of the `BottomSheet`. The default value is `Full`.

* **Full** - The sheet will occupy the entire screen width.
* **Custom** - The sheet will adjust its width based on the value set in the `BottomSheetContentWidth` property.

The `BottomSheetContentWidth` property allows you to adjust the width of the `BottomSheet`, when it is in `Custom` content width mode. The default value is `300`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ContentWidthMode="Custom" BottomSheetContentWidth="500">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
       <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.ContentWidthMode = BottomSheetContentWidthMode.Custom;
bottomSheet.BottomSheetContentWidth = 500;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

![Content width mode image for BottomSheet](images/contentWidthModeCustom.png)
## Grabber Customization
### Show Grabber
The `ShowGrabber` property enables users to interact with the `BottomSheet` by dragging it up and down. By default, the ShowGrabber property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ShowGrabber="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.ShowGrabber = true;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

### Grabber Width and Grabber Height
The `GrabberWidth` and `GrabberHeight` properties of the `BottomSheet` specify the width and height of the grabber element. By default, the GrabberWidth property is set to `32`, and the GrabberHeight property is set to `4`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberWidth="48" GrabberHeight="6">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.GrabberWidth = 48;
bottomSheet.GrabberHeight = 6;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

### Grabber CornerRadius
The `GrabberCornerRadius` property allows you to customize the corner radius of the grabber element in the `BottomSheet`. By adjusting this property, you can create rounded corners for the grabber.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberCornerRadius="24">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.GrabberCornerRadius = new CornerRadius(24);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

### Grabber Background
The `GrabberBackground` property allows you to customize the background color of the grabber in the `BottomSheet`.
{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberBackground="Red">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.GrabberBackground = new SolidColorBrush(Colors.Red);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
Content = bottomSheet;

{% endhighlight %}
{% endtabs %}
![Grabber Customization Image for BottomSheet](images/grabberCustomization.png)