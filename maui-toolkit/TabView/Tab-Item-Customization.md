---
layout: post
title: Tab Item Customization in .NET MAUI Tab View (SfTabView) | Syncfusion
description: Learn how to customize tab items in Syncfusion .NET MAUI Tab View (SfTabView). Explore image integration, text styling, font customization, and layout options to enhance your tab view appearance.
platform: maui-toolkit
control: Tab View
documentation: ug
---

# Configure the appearance of Tab Item in .NET MAUI Tab View (SfTabView)

A tab item consists of the following elements that can be customized.

## Adding image in tab item

### Header

The [Header](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_Header) holds the text of the tab item that is displayed in the tab bar.

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

![Tab Item Header](images/Tab-Width-Mode-Default.png) 

### Image Source 

The [ImageSource](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageSource) Specifies the image to be displayed in the tab item.

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

![Tab Item ImageSource](images/Image-Position-Left.png) 

### Content 

The assigned view will get displayed in the main area of the tab view.

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

![Tab Item Content](images/TabItem_Content.png) 

## Image position options 

The .NET MAUI Tab View provides four options that determine how the image in the tab aligns relative to the text. The options are left, top, right and bottom. It can be achieved using the [ImagePosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImagePosition) property of [SfTabItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html) of type [ImagePosition](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImagePosition).

N> Each tab item can be set with different image positions. Visual State Manager can be used to apply same value to all tabs.

### Top

The image will be placed above the text vertically.

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

![Image Position Top](images/Image-Position-Top.png) 

### Bottom

The image will be placed below the text vertically.

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

![Image Position Bottom](images/Image-Position-Bottom.png) 

### Left

The image will be placed before the text horizontally.

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

![Image Position Left](images/Image-Position-Left.png) 

### Right

The image will be placed to the right side of the text horizontally.

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

![Image Position Right](images/Image-Position-Right.png) 

## Image Text Spacing

The [ImageTextSpacing](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_ImageTextSpacing) property in `SfTabItem` allows you to set the spacing between the image and the text of the tab item. This property is particularly useful when you want to fine-tune the layout of tab items that contain both an image and text.

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

![Image Text Spacing](images/Image-Text-Spacing.png)

## Text Color Customization 

The TextColor(https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_TextColor) property allows you to customize the color of the text displayed in the tab item.

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

![Tab Image TextColor](images/TextColor.png) 

## Font Customization 

Font customization allows you to modify the appearance of the text in tab items. You can adjust the following font properties:

### Font Family

The [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontFamily) property sets the font family of the tab item text.

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

![TabItem FontFamily](images/FontFamily.png) 

### Font Attributes

The [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAttributes) defines the font style (e.g., bold, italic) of the tab item text.

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

![Tab Item FontAttribute](images/FontAttributes.png) 

### Font Size

The [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontSize) property specifies the size of the text in the tab item.

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

![Tab Item FontSize](images/FontSize.png)

## Tab Header Padding

The [TabHeaderPadding](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabHeaderPadding) property in [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html) allows you to add padding to the tab header.

N> The `TabHeaderPadding` property is only applicable when [TabWidthMode](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_TabWidthMode) is set to [SizeToContent](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.TabWidthMode.html#Syncfusion_Maui_Toolkit_TabView_TabWidthMode_SizeToContent).

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

![Image Text Spacing](images/TabViewHeaderItem_Padding.png)

## Scroll buttons on Header

Scroll buttons are used to navigate through the items in the header of the tab view by adjusting the [IsScrollButtonEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html#Syncfusion_Maui_Toolkit_TabView_SfTabView_IsScrollButtonEnabled) property of [SfTabView](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabView.html?tabs=tabid-1). These buttons are particularly useful when you have many tabs that exceed the available width of the tab view.

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

![TabView Scroll Mode](images/TabViewScroll.gif) 
## Font auto scaling enabled

The [FontAutoScalingEnabled](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.TabView.SfTabItem.html#Syncfusion_Maui_Toolkit_TabView_SfTabItem_FontAutoScalingEnabled) property allows you to enable or disable automatic font scaling for the tab headers. When enabled, this feature adjusts the font size of the tab headers based on the text size settings of the operating system. The default value of the `FontAutoScalingEnabled` property is `false.`

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