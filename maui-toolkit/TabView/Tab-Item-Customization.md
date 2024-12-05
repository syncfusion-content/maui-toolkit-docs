---
layout: post
title: Tab Item Customization in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn how to customize tab items in Syncfusion .NET MAUI Tab View (SfTabView). Explore the options to enhance your tab view appearance.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Configure the appearance of Tab Item in .NET MAUI Tab View (SfTabView)

A tab item consists of the several elements that can be customized to enhance its appearance and functionality. This guide will walk you through the various customization options available for tab items in [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html).

## Customizable elements of a Tab Item

### Header

The [Header](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_Header) holds the text of the tab item that is displayed in the tab bar. The `Header` property can be set in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the header set to "ITEM 1" -->
	<tabView:SfTabItem Header="ITEM 1" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
	new SfTabItem()
	{
		Header = "ITEM 1",
	}
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the header text:

![.NET MAUI Tab Item Header](images/Tab-Width-Mode-Default.png) 

### Image source 

You can add an image to a tab item to enhance its visual appeal. The [ImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageSource) specifies the image to be displayed in the tab item. you can set the `ImageSource` property in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
    <!-- Define a tab item with the header set to "ITEM 1" and an image source set to "alexandar" -->
    <tabView:SfTabItem Header="ITEM 1"
                       ImageSource="alexandar" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
	new SfTabItem
	{
		Header = "ITEM 1",
		ImageSource = "alexandar",
	}
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with an image source:

![.NET MAUI Tab Item ImageSource](images/Image-Position-Left.png) 

### Content 

The `Content` property allows you to assign a view that will be displayed in the main area of the tab view. You can set the `Content` property in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the header set to "ITEM 2" -->
	<tabView:SfTabItem Header="ITEM 2">
		<!-- Define the content of the tab item -->
		<tabView:SfTabItem.Content>
			<ListView>
				<!-- Add your items here -->
			</ListView>
		</tabView:SfTabItem.Content>
	</tabView:SfTabItem>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
	new SfTabItem
	{
		Header = "ITEM 2",
		Content = new ListView
		{
			// Add your items here
		}
	}
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with its content:

![.NET MAUI Tab Item Content](images/TabItem_Content.png) 

## Image position options 

The .NET MAUI Tab View provides four options that determine how the image in the tab aligns relative to the text. The options are left, top, right, and bottom. You can set this alignment using the [ImagePosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImagePosition) property of the [SfTabItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html) class.

N> Each tab item can have a different image position. You can use the Visual State Manager to apply the same image position to all tabs.

### Top

When the `ImagePosition` property is set to `Top`, the image will be placed above the text, aligned vertically. You can set the `ImagePosition` property in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the image position set to Top -->
	<tabView:SfTabItem ImagePosition="Top" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
	new SfTabItem
	{
		ImagePosition = TabImagePosition.Top,
	}
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the top of the text:

![.NET MAUI Image Position Top](images/Image-Position-Top.png) 

### Bottom

When the `ImagePosition` property is set to `Bottom`, the image will be placed below the text, aligned vertically. 

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the image position set to Top -->
	<tabView:SfTabItem ImagePosition="Top" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
	new SfTabItem
	{
		ImagePosition = TabImagePosition.Bottom,
	}
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the bottom of the text:

![.NET MAUI Image Position Bottom](images/Image-Position-Bottom.png) 

### Left

When the `ImagePosition` property is set to `Left`, the image will be placed before the text, aligned horizontally.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the image position set to Left -->
	<tabView:SfTabItem ImagePosition="Left" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Left,
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the left of the text:

![.NET MAUI Image Position Left](images/Image-Position-Left.png) 

### Right

When the `ImagePosition` property is set to `Right`, the image will be placed to the right side of the text, aligned horizontally.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the image position set to Right -->
	<tabView:SfTabItem ImagePosition="Right" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Right,
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the right of the text:

![.NET MAUI Image Position Right](images/Image-Position-Right.png) 

## Image text spacing

The [ImageTextSpacing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageTextSpacing) property in [SfTabItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html) allows you to set the spacing between the image and the text of the tab item. This property is particularly useful when you want to fine-tune the layout of tab items that contain both an image and text.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the image text spacing set to 20 -->
	<tabView:SfTabItem ImageTextSpacing="20" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImageTextSpacing = "20",
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified image text spacing:

![.NET MAUI Image Text Spacing](images/Image-Text-Spacing.png)

## Text color customization 

The [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_TextColor) property allows you to customize the color of the text displayed in the tab item. Below are examples demonstrating how to set the `TextColor` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the text color set to Blue -->
	<tabView:SfTabItem TextColor="Blue" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        TextColor = Color.Blue,
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified text color:

![.NET MAUI Tab Image TextColor](images/TextColor.png) 

## Font customization 

Font customization allows you to modify the appearance of the text in tab items. You can adjust the following font properties:

### Font family

The [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontFamily) property sets the font family of the tab item text. Below are examples demonstrating how to set the `FontFamily` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the font family set to OpenSansRegular -->
	<tabView:SfTabItem FontFamily="OpenSansRegular" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontFamily = "OpenSansRegular",
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified font family:

![.NET MAUI TabItem FontFamily](images/FontFamily.png) 

### Font attributes

The [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAttributes) defines the font style (e.g., bold, italic) of the tab item text. Below are examples demonstrating how to set the `FontAttributes` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the font attributes set to Bold -->
	<tabView:SfTabItem FontAttributes="Bold" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontAttributes = FontAttributes.Bold,
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified font attributes:

![.NET MAUI Tab Item FontAttribute](images/FontAttributes.png) 

### Font size

The [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontSize) property specifies the size of the text in the tab item. Below are examples demonstrating how to set the `FontSize` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control -->
<tabView:SfTabView>
	<!-- Define a tab item with the font size set to 32 -->
	<tabView:SfTabItem FontSize="32" />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Create a collection of tab items
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontSize = 32,
    }
};

// Set the Items property of the SfTabView to the collection of tab items
tabView.Items = tabItems;
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified font size:

![.NET MAUI Tab Item FontSize](images/FontSize.png)

## Tab Header padding

The [TabHeaderPadding](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabHeaderPadding) property in [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html) allows you to add padding to the tab header.

N> The `TabHeaderPadding` property is only applicable when [TabWidthMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabWidthMode) is set to [SizeToContent](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabWidthMode.html#Syncfusion_Maui_Toolkit_TabView_TabWidthMode_SizeToContent).

Below are examples demonstrating how to set the `TabHeaderPadding` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with specific tab width mode and header padding -->
<tabView:SfTabView TabWidthMode="SizeToContent"
                   TabHeaderPadding="5,10,5,10">
    <!-- Define a tab item -->
    <tabView:SfTabItem />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Set the tab width mode to size to content
tabView.TabWidthMode = TabWidthMode.SizeToContent;

// Set the tab header padding
tabView.TabHeaderPadding = new Thickness(5, 10, 5, 10);
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified header padding:

![.NET MAUI Tab Header Padding](images/TabViewHeaderItem_Padding.png)

## Scroll buttons on Header

Scroll buttons are used to navigate through the items in the header of the tab view by adjusting the [IsScrollButtonEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IsScrollButtonEnabled) property of [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html?tabs=tabid-1). These buttons are particularly useful when you have many tabs that exceed the available width of the tab view.

Below are examples demonstrating how to enable scroll buttons in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with scroll button enabled -->
<tabView:SfTabView IsScrollButtonEnabled="True">
	<!-- Define a tab item -->
	<tabView:SfTabItem />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Enable scroll buttons for the tab view
tabView.IsScrollButtonEnabled = true;
{% endhighlight %}

{% endtabs %}

The following image shows the tab view with scroll buttons enabled:

![.NET MAUI Tab View Scroll Mode](images/TabViewScroll.gif) 

### Scroll button customization

The `ScrollButtonBackground` and `ScrollButtonColor` property of [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html) allows users to customize the background color and foreground color of scroll button.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView ScrollButtonBackground="Violet" ScrollButtonColor="Red">
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
StackLayout stackLayout = new StackLayout();
var tabView = new SfTabView();
tabView.ScrollButtonBackground = SolidColorBrush.Violet;
tabView.ScrollButtonColor = Colors.Red;
stackLayout.Children.Add(tabView);
this.Content = stackLayout;
{% endhighlight %}

{% endtabs %}

![ScrollButtonCustomization](images/ScrollButtonCustomization.png)

## Font auto scaling

The [FontAutoScalingEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAutoScalingEnabled) property allows you to enable or disable automatic font scaling for the tab headers. When enabled, this feature adjusts the font size of the tab headers based on the text size settings of the operating system. The default value of the `FontAutoScalingEnabled` property is `false.`

Below are examples demonstrating how to enable font auto scaling in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with font auto-scaling enabled -->
<tabView:SfTabView FontAutoScalingEnabled="True">
	<!-- Define a tab item -->
	<tabView:SfTabItem />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Enable font auto-scaling for the tab view
tabView.FontAutoScalingEnabled = true;
{% endhighlight %}

{% endtabs %}

## Content transition duration

You can customize the animation duration when switching between tabs in the Tab View by setting the [ContentTransitionDuration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentTransitionDuration) property. This property affects the smooth transition of content when the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) changes.

Below are examples demonstrating how to set the content transition duration in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<!-- Define the SfTabView control with content transition duration set to 300 -->
<tabView:SfTabView ContentTransitionDuration="300">
	<!-- Define a tab item -->
	<tabView:SfTabItem />
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
// Create an instance of the SfTabView control
SfTabView tabView = new SfTabView();

// Set the content transition duration for the tab view
tabView.ContentTransitionDuration = 300;
{% endhighlight %}

{% endtabs %}

## Image size

You can customize the image size in the .NET MAUI TabView control by setting the `ImageSize` property.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem ImageSize="50"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
StackLayout stackLayout = new StackLayout();
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImageSize = 50,
    }
};
tabView.Items = tabItems;
stackLayout.Children.Add(tabView);
this.Content = stackLayout;
{% endhighlight %}

{% endtabs %}