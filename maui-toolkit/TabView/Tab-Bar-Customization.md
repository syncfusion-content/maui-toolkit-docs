---
layout: post
title: Customize the Tab Bar in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn here all about custom header support in Syncfusion .NET MAUI Tab View (SfTabView) control and more.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Customize the Tab Bar in .NET MAUI Tab View (SfTabView)

## Tab width options

The .NET MAUI Tab View provides two modes for determining how the width of the tab is calculated on the tab bar while it gets populated. The options are [Default](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabWidthMode.html#Syncfusion_Maui_Toolkit_TabView_TabWidthMode_Default) and [SizeToContent](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabWidthMode.html#Syncfusion_Maui_Toolkit_TabView_TabWidthMode_SizeToContent). You can set these modes using the [TabWidthMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabWidthMode.html) property.

### Default tab width mode

In this mode, the width of the tab is divided equally based on the available control width. This enables a fixed tab bar that will not allow tab scrolling even it contains any number of tabs. You can achieve this by setting the `TabWidthMode` property to `Default`.

N> This mode is recommended when the tab count is not more than four. More tabs in this mode may result in text being trimmed.

To set the tab width mode, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the tab width mode set to Default -->
<tabView:SfTabView TabWidthMode="Default" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the tab width mode to default
tabView.TabWidthMode = TabWidthMode.Default;
{% endhighlight %}

{% endtabs %}

The following image shows the tab bar in default tab width mode.

![Default Tab Width Mode in .NET MAUI TabView](images/Tab-Width-Mode-Default.png)

### Based on the text size

The width of a tab is set to fit the text or image that it contains by setting the `TabWidthMode` as `SizeToContent`. Scroll is enabled in this mode to access the items that are outside the visible area.

To set the tab width mode to fit the content, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the tab width mode set to SizeToContent -->
<tabView:SfTabView TabWidthMode="SizeToContent" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the tab width mode to size-to-content
tabView.TabWidthMode = TabWidthMode.SizeToContent;
{% endhighlight %}

{% endtabs %}

The following image shows the tab bar in size-to-content width mode.

![Tab Width Mode Size to fit](images/Tab-Width-Mode-SizeToFit.png) 

## Customize the tab bar height

The height of the tab bar can be customized by setting the [TabBarHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabBarHeight) property. The default height is 48.

N> It is recommended to set the `TabBarHeight` as 72 while displaying the image and text with ImagePosition as either top or bottom.

To set the tab bar height, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the tab bar height set to 100 -->
<tabView:SfTabView TabBarHeight="100" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the height of the tab bar to 100
tabView.TabBarHeight = 100;
{% endhighlight %}

{% endtabs %}

## Customize the tab header text alignment

The horizontal text alignment of the tab header can be customized by setting the [HeaderHorizontalTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_HeaderHorizontalTextAlignment) property. The default value is Center. This property accepts the following values:

*   **Start** - The text will be placed at the starting position in the header tab.
*   **Center** - The text will be placed at the center of the header tab.
*   **End** - The text will be placed at the end of the header tab.

To set the horizontal text alignment of the tab header, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the header horizontal text alignment set to Center -->
<tabView:SfTabView HeaderHorizontalTextAlignment="Center" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the horizontal text alignment of the tab headers to center
tabView.HeaderHorizontalTextAlignment = TextAlignment.Center; 
{% endhighlight %}

{% endtabs %}

![Tab header text alignment](images/HorizontalTextAlignmentCenter.png) 

## Tab bar placement options 

The .NET MAUI Tab View provides two options for determining how the tab bar aligns relative to the tab content. The options are top and bottom. This can be done using the [TabBarPlacement](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabBarPlacement) property.

### Top

In this option, the tab bar will be placed above the content region of the tab view. To set the tab bar placement to the top, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the tab bar placement set to Top -->
<tabView:SfTabView TabBarPlacement="Top" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the tab bar placement to the top
tabView.TabBarPlacement = TabBarPlacement.Top;
{% endhighlight %}

{% endtabs %}

The following image shows the tab bar placed at the top of the content region.

![Tab Bar Placement Top](images/Tab-bar-Placement-Top.png) 

### Bottom

In this option, the tab bar will be placed below the content region of the tab view. To set the tab bar placement to the bottom, use the following code:

{% tabs %}

{% highlight xaml %}
    <tabView:SfTabView TabBarPlacement="Bottom">
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
 // Set the tab bar placement to the bottom
tabView.TabBarPlacement = TabBarPlacement.Bottom;
{% endhighlight %}

{% endtabs %}

The following image illustrates the tab bar placed at the bottom of the content region.

![Tab Bar Placement Bottom](images/Tab-bar-Placement-Bottom.png) 

## Tab Bar background customization

TYou can customize the tab bar background using the [TabBarBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabBarBackground) property. You can set a solid color or a gradient color as the background.

### Solid Color 

A solid color can be achieved by assigning the `SolidColorBrush` to the [TabBarBackground](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabBarBackground), which represents the color of the tab bar background.

To set a solid color as the background, use the following code:

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with the tab bar background color set to LightBlue -->
<tabView:SfTabView TabBarBackground="LightBlue" />
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();
// Set the background color of the tab bar to light blue
tabView.TabBarBackground = Colors.LightBlue;
{% endhighlight %}

{% endtabs %}

The following image shows the tab bar with a solid color background.

![Tab Bar Solid Color Bottom](images/TabBarSolidColor.png) 

### Gradient Color 

The background can be customized with a linear gradient and radial gradient as like below example.

{% tabs %}
{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Set the tab bar background to a linear gradient brush -->
	<tabView:SfTabView.TabBarBackground>
		<LinearGradientBrush EndPoint="0,1">
			<!-- Define the gradient stops for the linear gradient brush -->
			<GradientStop Color="#009FFF"
						  Offset="0.1" />
			<GradientStop Color="#ec2F4B"
						  Offset="1.0" />
		</LinearGradientBrush>
	</tabView:SfTabView.TabBarBackground>
</tabView:SfTabView>
{% endhighlight %}


{% highlight C# %}
// Create the first gradient stop with color #009FFF and offset 0.1
Microsoft.Maui.Controls.GradientStop gradientStop1 = new Microsoft.Maui.Controls.GradientStop()
{
	Color = Color.FromArgb("#009FFF"),
	Offset = (float)0.1,
};

// Create the second gradient stop with color #ec2F4B and offset 1.0
Microsoft.Maui.Controls.GradientStop gradientStop2 = new Microsoft.Maui.Controls.GradientStop()
{
	Color = Color.FromArgb("#ec2F4B"),
	Offset = (float)1.0,
};

// Create a linear gradient brush with the defined gradient stops
LinearGradientBrush gradientBrush = new LinearGradientBrush()
{
	EndPoint = new Point(0, 1),
	GradientStops = new GradientStopCollection() { gradientStop1, gradientStop2 }
};

// Create an instance of the SfTabView control and set its tab bar background to the gradient brush
SfTabView tabView = new SfTabView();
tabView.TabBarBackground = gradientBrush;
{% endhighlight %}
{% endtabs %}

The following image shows the tab bar with a gradient color background.

![Tab Bar Gradient Color Bottom](images/TabBarGradientColor.png)

N> View [sample](https://github.com/SyncfusionExamples/maui-toolkit-samples/tree/master/TabView/TabBarCustomization) in GitHub.