---
layout: post
title: Customization in .NET MAUI Bottom Sheet (SfBottomSheet) | Syncfusion®
description: Learn how to customize bottom sheet in Syncfusion® .NET MAUI Bottom Sheet (SfbottomSheet). Explore the options to enhance your bottom sheet appearance.
platform: maui-toolkit
control: BottomSheet
documentation: ug
---

# Customization in .NET MAUI Bottom Sheet (SfBottomSheet)

A [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) consists of several elements that can be customized to enhance its appearance and functionality.

## Popup Mode
The [IsModal](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_IsModal) property controls whether background interaction is disabled when a bottom sheet is open. When set to `True`, a gray overlay blocks interaction with the background, and tapping it closes the sheet. When set to `False`, the overlay is invisible, allowing users to interact with the content behind the sheet.

{% tabs %}
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" IsModal="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight C# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    IsModal = true
};

{% endhighlight %}
{% endtabs %}

![PopUpMode image for BottomSheet](images/popUpMode.png)

## State
The state of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) can be controlled using the [State](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_State) property. The default value is `Hidden`. This property accepts the following values:

* **FullExpanded** - The sheet will expand to cover the full screen.
* **HalfExpanded** - The sheet will expand to cover half of the screen.
* **Collapsed** - The sheet will remain collapsed at the bottom of the screen.
* **Hidden** - The sheet will remain hidden.

The [State](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_State) property works together with the [AllowedState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_AllowedState) property to control the allowed states of the BottomSheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" State="FullExpanded">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->    
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.State = BottomSheetState.FullExpanded;

{% endhighlight %}
{% endtabs %}

## Allowed State
The [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) allows to control the transition between the states using the [AllowedState](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_AllowedState) property. The default value is `All`, which allows transitions between all available states. This property accepts the following values:

* **FullExpanded** - It will allow transitions only between the FullExpanded and Collapsed states.
* **HalfExpanded** - It will allow transitions only between the HalfExpanded and Collapsed states.
* **All** - Allows transitions between all available states (FullExpanded, HalfExpanded, Collapsed, and Hidden).

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottonSheet x:Name="bottomSheet" AllowedState="HalfExpanded" >
    <bottomSheet:SfBottonSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottonSheet.BottomSheetContent>
</bottomSheet:SfBottonSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.AllowedState = BottomSheetAllowedState.HalfExpanded;

{% endhighlight %}
{% endtabs %}

## Content Padding
The [ContentPadding](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_ContentPadding) property of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) adds space around the content creating a gap between the bottom sheet content and the edges.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ContentPadding="15">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.ContentPadding = new Thickness(15);

{% endhighlight %}
{% endtabs %}

## Background
The [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_Background) property allows you to customize the background color of the BottomSheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" Background="Beige">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    Background = Colors.Beige
};

{% endhighlight %}
{% endtabs %}

![Background color image for BottomSheet](images/backgroundColor.png)

## CornerRadius
The [CornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_CornerRadius) property allows you to add corner radius to the Bottom sheet.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" CornerRadius="15, 15, 0, 0">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    CornerRadius = new CornerRadius(15, 15, 0, 0)
};

{% endhighlight %}
{% endtabs %}

![Corner radius image for BottomSheet](images/cornerRadius.png)
## Adjust the Height
### Full Expanded Height

The [FullExpandedRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_FullExpandedRatio) property adjusts the height of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) when it is in the `FullExpanded` state. The default value is `1`. You can set a value between 0.1 and 1 to adjust the height.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" FullExpandedRatio="0.8" State="FullExpanded">
 <bottomSheet:SfBottomSheet.BottomSheetContent>
     <!--Add your content here-->
 </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.FullExpandedRatio = 0.8;
bottomSheet.State = BottomSheetState.FullExpanded;

{% endhighlight %}
{% endtabs %}

### Half Expanded Height

The [HalfExpandedRatio](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_HalfExpandedRatio) property adjusts the height of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) when it is in the `HalfExpanded` state. The default value is `0.5`. You can set a value between 0.1 and 0.9 to adjust the height.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" HalfExpandedRatio="0.7" State="HalfExpanded">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.HalfExpandedRatio = 0.7;
bottomSheet.State = BottomSheetState.HalfExpanded;

{% endhighlight %}
{% endtabs %}

### Collapsed Height
The [CollapsedHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_CollapsedHeight) property allows you to specify the height of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html), when it is in the `Collapsed` state. The default value is `100`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" CollapsedHeight="150">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet();
bottomSheet.CollapsedHeight = 150;

{% endhighlight %}
{% endtabs %}

## Adjust the Width
The [ContentWidthMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_ContentWidthMode) property allows you to adjust the width of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html). The default value is `Full`.

* **Full** - The sheet will occupy the entire screen width.
* **Custom** - The sheet will adjust its width based on the value set in the [BottomSheetContentWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_BottomSheetContentWidth) property.

The [BottomSheetContentWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_BottomSheetContentWidth) property allows you to adjust the width of the `BottomSheet`, when it is in `Custom` content width mode. The default value is `300`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ContentWidthMode="Custom" BottomSheetContentWidth="500">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    ContentWidthMode = BottomSheetContentWidthMode.Custom,
    BottomSheetContentWidth = 500
};

{% endhighlight %}
{% endtabs %}

![Content width mode image for BottomSheet](images/contentWidthModeCustom.png)
## Grabber Customization
### Show Grabber
The [ShowGrabber](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_ShowGrabber) property enables users to interact with the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) by dragging it up and down. By default, the ShowGrabber property is set to `true`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" ShowGrabber="True">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    ShowGrabber = true
};

{% endhighlight %}
{% endtabs %}

### Grabber Width and Grabber Height
The [GrabberWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_GrabberWidth) and [GrabberHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_GrabberHeight) properties of the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html) specify the width and height of the grabber element. By default, the GrabberWidth property is set to `32`, and the GrabberHeight property is set to `4`.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberHeight="12" GrabberWidth="100">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    GrabberHeight = 12,
    GrabberWidth = 100
};

{% endhighlight %}
{% endtabs %}

### Grabber CornerRadius
The [GrabberCornerRadius](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_GrabberCornerRadius) property allows you to customize the corner radius of the grabber element in the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html). By adjusting this property, you can create rounded corners for the grabber.

{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberCornerRadius="3">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>

{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    GrabberCornerRadius = new CornerRadius(3)
};

{% endhighlight %}
{% endtabs %}

### Grabber Background
The [GrabberBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html#Syncfusion_Maui_Toolkit_BottomSheet_SfBottomSheet_GrabberBackground) property allows you to customize the background color of the grabber in the [BottomSheet](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.BottomSheet.SfBottomSheet.html).
{% tabs %}	
{% highlight xaml %}

<bottomSheet:SfBottomSheet x:Name="bottomSheet" GrabberBackground="Red">
    <bottomSheet:SfBottomSheet.BottomSheetContent>
        <!--Add your content here-->
    </bottomSheet:SfBottomSheet.BottomSheetContent>
</bottomSheet:SfBottomSheet>
	
{% endhighlight %}
{% highlight c# %}

SfBottomSheet bottomSheet = new SfBottomSheet
{
    GrabberBackground = Colors.Red
};

{% endhighlight %}
{% endtabs %}
![Grabber Customization Image for BottomSheet](images/grabberCustomization.png)