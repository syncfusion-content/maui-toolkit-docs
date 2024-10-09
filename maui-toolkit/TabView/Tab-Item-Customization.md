---
layout: post
title: Tab Item Customization in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn how to customize tab items in Syncfusion .NET MAUI Tab View (SfTabView). Explore image integration, text styling, font customization, and layout options to enhance your tab view appearance.
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
<tabView:SfTabView>
    <tabView:SfTabItem Header="ITEM 1"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        Header = "ITEM 1",
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the header text:

![.NET MAUI Tab Item Header](images/Tab-Width-Mode-Default.png) 

### Image source 

You can add an image to a tab item to enhance its visual appeal. The [ImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageSource) specifies the image to be displayed in the tab item. you can set the `ImageSource` property in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem Header="ITEM 1" ImageSource="alexandar"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        Header = "ITEM 1",
        ImageSource = "alexandar",
    }
};

{% endhighlight %}

{% endtabs %}

The following image shows a tab item with an image source:

![.NET MAUI Tab Item ImageSource](images/Image-Position-Left.png) 

### Content 

The `Content` property allows you to assign a view that will be displayed in the main area of the tab view. You can set the `Content` property in both XAML and C# code as shown in the examples below.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem Header="ITEM 2">
        <tabView:SfTabItem.Content>
            <ListView>
                <!--Add your items here-->
            </ListView>
        </tabView:SfTabItem.Content>
    </tabView:SfTabItem>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        Header = "ITEM 2",
        Content = new ListView()
        {
            // Add your items here
        }
    }
};
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
 <tabView:SfTabView>
     <tabView:SfTabItem ImagePosition="Top"/>
 </tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Top,
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the top of the text:

![.NET MAUI Image Position Top](images/Image-Position-Top.png) 

### Bottom

When the `ImagePosition` property is set to `Bottom`, the image will be placed below the text, aligned vertically. 

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem ImagePosition="Bottom"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Bottom,
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the bottom of the text:

![.NET MAUI Image Position Bottom](images/Image-Position-Bottom.png) 

### Left

When the `ImagePosition` property is set to `Left`, the image will be placed before the text, aligned horizontally.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem ImagePosition="Left"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Left,
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the left of the text:

![.NET MAUI Image Position Left](images/Image-Position-Left.png) 

### Right

When the `ImagePosition` property is set to `Right`, the image will be placed to the right side of the text, aligned horizontally.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem ImagePosition="Right"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImagePosition = TabImagePosition.Right,
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows the tab item with the image positioned to the right of the text:

![.NET MAUI Image Position Right](images/Image-Position-Right.png) 

## Image text spacing

The [ImageTextSpacing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageTextSpacing) property in [SfTabItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html) allows you to set the spacing between the image and the text of the tab item. This property is particularly useful when you want to fine-tune the layout of tab items that contain both an image and text.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem ImageTextSpacing="20"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        ImageTextSpacing = "20",
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified image text spacing:

![.NET MAUI Image Text Spacing](images/Image-Text-Spacing.png)

## Text color customization 

The [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_TextColor) property allows you to customize the color of the text displayed in the tab item. Below are examples demonstrating how to set the `TextColor` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem TextColor="Blue"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        TextColor = Color.Blue,
    }
};
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
<tabView:SfTabView>
    <tabView:SfTabItem FontFamily="OpenSansRegular"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontFamily = "OpenSansRegular",
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified font family:

![.NET MAUI TabItem FontFamily](images/FontFamily.png) 

### Font attributes

The [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAttributes) defines the font style (e.g., bold, italic) of the tab item text. Below are examples demonstrating how to set the `FontAttributes` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem FontAttributes="Bold"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontAttributes = FontAttributes.Bold,
    }
};
{% endhighlight %}

{% endtabs %}

The following image shows a tab item with the specified font attributes:

![.NET MAUI Tab Item FontAttribute](images/FontAttributes.png) 

### Font size

The [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontSize) property specifies the size of the text in the tab item. Below are examples demonstrating how to set the `FontSize` property in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView>
    <tabView:SfTabItem FontSize="32"/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
var tabItems = new TabItemCollection
{
    new SfTabItem()
    {
        FontSize = 32,
    }
};
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
<tabView:SfTabView TabWidthMode="SizeToContent" TabHeaderPadding="5,10,5,10">
    <tabView:SfTabItem/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
tabView.TabWidthMode = TabWidthMode.SizeToContent;
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
<tabView:SfTabView  IsScrollButtonEnabled="True">
    <tabView:SfTabItem/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
tabView.IsScrollButtonEnabled = true;
{% endhighlight %}

{% endtabs %}

The following image shows the tab view with scroll buttons enabled:

![.NET MAUI Tab View Scroll Mode](images/TabViewScroll.gif) 

## Font auto scaling

The [FontAutoScalingEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAutoScalingEnabled) property allows you to enable or disable automatic font scaling for the tab headers. When enabled, this feature adjusts the font size of the tab headers based on the text size settings of the operating system. The default value of the `FontAutoScalingEnabled` property is `false.`

Below are examples demonstrating how to enable font auto scaling in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView FontAutoScalingEnabled="True">
    <tabView:SfTabItem/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
tabView.FontAutoScalingEnabled = true;
{% endhighlight %}

{% endtabs %}

## Content transition duration

You can customize the animation duration when switching between tabs in the Tab View by setting the [ContentTransitionDuration](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_ContentTransitionDuration) property. This property affects the smooth transition of content when the [SelectedIndex](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_SelectedIndex) changes.

Below are examples demonstrating how to set the content transition duration in both XAML and C#.

{% tabs %}

{% highlight xaml %}
<tabView:SfTabView  ContentTransitionDuration ="300">
    <tabView:SfTabItem/>
</tabView:SfTabView>
{% endhighlight %}

{% highlight C# %}
var tabView = new SfTabView();
tabView.ContentTransitionDuration = 300;
{% endhighlight %}

{% endtabs %}