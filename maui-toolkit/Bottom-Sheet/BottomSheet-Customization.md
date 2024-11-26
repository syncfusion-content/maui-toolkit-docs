---
layout: post
title: Bottom Sheet Customization in .NET MAUI Bottom Sheet (SfBottomSheet) | Syncfusion
description: Learn how to customize bottom sheet in Syncfusion .NET MAUI Bottom Sheet (SfbottomSheet). Explore the options to enhance your bottom sheet appearance.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Configure the appearance of Bottom Sheet in .NET MAUI Bottom Sheet (SfBottomSheet)

A `BottomSheet` consists of several elements that can be customized to enhance its appearance and functionality.

## Customizable elements of a Bottom Sheet
### IsModal
The `IsModal` property  whether the background interaction is disabled when a bottom sheet is open.By default, the IsModel property is set to `true`.

* IsModal is `True` : The gray overlay appears above the bottom sheet, blocking interaction with the background. Tapping the overlay will close the bottom sheet.
* IsModal is `False` : The gray overlay is Invisible, allowing users to interact with the content behind the bottom sheet.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" IsModal="False">
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>

{% endhighlight %}
{% highlight C# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.IsModal="False";
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## State
The `state` of the BottomSheet can be controlled using the State property. The default value is Hidden. This property accepts the following values:

* **FullExpanded** - The sheet will expand to cover the full screen.
* **HalfExpanded** - The sheet will expand to cover half of the screen.
* **Collapsed** - The sheet will remain collapsed at the bottom of the screen.
* **Hidden** - The sheet will remain hidden.

The `State` property works together with the `AllowState` property to control the allowed states of the BottomSheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" State="HalfExpanded">
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.State="HalfExpanded";
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Allowed State
The allowed states of the BottomSheet can be controlled using the `AllowState` property. The default value is All, allowing all states. This property accepts the following values:

*   **FullExpanded** - The sheet can expand to cover the full screen.
*   **HalfExpanded** - The sheet can expand to half of the screen height.
*   **All** - The sheet can transition between all available states (FullExpanded, HalfExpanded, and Collapsed).

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" AllowdState="HalfExpanded" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.AllowedState="HalfExpanded";
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Show Grabber
The Grabber in the BottomSheet is a small visual element at the top of the sheet. By default,the `ShowGrabber` property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" ShowGrabber="False" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.ShowGrabber="False";
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Grabber Width
The `GrabberWidth` property in the BottomSheet specifies the width of the grabber element at the top of the sheet. By default, the GrabberWidth property is set to `32`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" GrabberWidth="50" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.GrabberWidth=50;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Grabber Height
The `GrabberHeight` property in the BottomSheet specifies the height of the grabber element at the top of the sheet. By default, the GrabberHeight property is set to `4`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" GrabberHeight="10" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.GrabberHeight=10;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Grabber CornerRadius
The `GrabberCornerRadius` property in the BottomSheet specifies the corner radius of the grabber element at the top of the sheet. By default, the GrabberCornerRadius property is set to `12`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" GrabberCornerRadius="5" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.GrabberCornerRadius=new CornerRadius(5);
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Grabber Color
The `GrabberColor` property in the BottomSheet specifies the background of the grabber element at the top of the sheet.
{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" GrabberColor="Red" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.GrabberColor = Colors.Red;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## HalfExpandedRatio
The `HalfExpandedRatio` property in the BottomSheet sets the height of the BottomSheet when it is in the `HalfExpanded` state. The default value is `0.5`. You can set a value between 0 and 1 to adjust the height. This property works only when the sheet's `State` is `HalfExpanded`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" State="HalfExpanded" HalfExpandedRatio="0.7" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.State="HalfExpanded"
bottomSheet.HalfExpandedRatio = 0.7;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## CornerRadius
The `CornerRadius` property allows you to add corner radius to the Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" CornerRadius="20" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.CornerRadius = 20;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Margin
The `Margin` property allows you to add margin to the Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" Margin="15" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.Margin = 15;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Content Padding
The `ContentPadding` property allows you to add padding to the content in Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" ContentPadding="15" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.ContentPadding = 15;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}

## Background
The `Background` property allows you to add Background to the Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" Background="Red" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <Grid/>
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottonSheet bottomSheet = new SfBottonSheet();
bottomSheet.Background = Colors.Red;
Grid grid = new Grid();
bottomSheet.BottomSheetContent = grid;
this.Content = bottomSheet;

{% endhighlight %}
{% endtabs %}