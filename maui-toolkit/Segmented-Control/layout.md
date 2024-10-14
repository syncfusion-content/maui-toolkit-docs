---
layout: post
title: Layout in .NET MAUI Segmented Control | Syncfusion
description: Learn about the Layout support Syncfusion .NET MAUI Segmented control (SfSegmentedControl).
platform: maui-toolkit
control: Segmented control
documentation: ug
---
 
# Layout in .NET MAUI Segmented control (SfSegmentedControl)
The `SfSegmentedControl` supports changing the layout width, height and the number of visible segments displayed.

## Change the segment width
Change the width of the segmented control and each segment item.

### Change the segment width for segmented control
Use the [SegmentWidth](https://help.syncfusion.com/cr/maui-toolkit-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_SegmentWidth) property of [SfSegmentedControl](https://help.syncfusion.com/cr/maui-toolkit-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html) to customize the segment width of the segmented control.

{% tabs %}
{% highlight XAML %}

<ContentPage
    xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit.SegmentedControl">
    <segmentedControl:SfSegmentedControl x:Name="segmentedControl"
                                SegmentWidth="50">
        <segmentedControl:SfSegmentedControl.ItemsSource>
            <x:Array Type="{x:Type x:String}">
                <x:String>Day</x:String>
                <x:String>Week</x:String>
                <x:String>Month</x:String>
                <x:String>Year</x:String>
            </x:Array>
        </segmentedControl:SfSegmentedControl.ItemsSource>
    </segmentedControl:SfSegmentedControl>
</ContentPage>

{% endhighlight %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl segmentedControl = new SfSegmentedControl();
        segmentedControl.SegmentWidth = 50;
        this.Content = segmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

![Change the segment width in .NET MAUI Segmented control.](images/layout/segment-width.png)

### Change the each segment item width
You can change the width of each segment item using the [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentItem.html#Syncfusion_Maui_Toolkit_SegmentedControl_SfSegmentItem_Width) property of [SfSegmentItem](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentItem.html).

{% tabs %}
{% highlight C# tabtitle="MainPage.xaml.cs"%}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl segmentedControl = new SfSegmentedControl();
        List<SfSegmentItem> segmentItems = new List<SfSegmentItem>
            {
                new SfSegmentItem() {Text="Day", Width = 40},
                new SfSegmentItem() {Text="Week", Width = 50},
                new SfSegmentItem() {Text="Month", Width = 60},
                new SfSegmentItem() {Text="Year", Width = 70},
            };
        segmentedControl.ItemsSource = segmentItems;
        this.Content = segmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

![Change the segment item width in .NET MAUI Segmented control.](images/layout/segment-item-width.webp)

## Change the segment height
You can use the [SegmentHeight](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_SegmentHeight) property of [SfSegmentedControl](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html) to customize the segment height of the segmented control.

{% tabs %}
{% highlight XAML %}

<ContentPage
    xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit.SegmentedControl">
    <segmentedControl:SfSegmentedControl x:Name="segmentedControl"
                                SegmentHeight="60">
        <segmentedControl:SfSegmentedControl.ItemsSource>
            <x:Array Type="{x:Type x:String}">
                <x:String>Day</x:String>
                <x:String>Week</x:String>
                <x:String>Month</x:String>
                <x:String>Year</x:String>
            </x:Array>
        </segmentedControl:SfSegmentedControl.ItemsSource>
    </segmentedControl:SfSegmentedControl>
</ContentPage>

{% endhighlight %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl segmentedControl = new SfSegmentedControl();
        segmentedControl.SegmentHeight = 60;
        this.Content = segmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

![Change the segment height in .NET MAUI Segmented control.](images/layout/segment-height.png)

## Visible segment count
Set the number of visible segments displayed in the [SfSegmentedControl](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html) using [VisibleSegmentsCount](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_VisibleSegmentsCount) property.

{% tabs %}
{% highlight XAML %}

<ContentPage
    xmlns:segmentedControl="clr-namespace:Syncfusion.Maui.Toolkit.SegmentedControl;assembly=Syncfusion.Maui.Toolkit.SegmentedControl">
    <segmentedControl:SfSegmentedControl x:Name="segmentedControl"
                                VisibleSegmentsCount="3">
        <segmentedControl:SfSegmentedControl.ItemsSource>
            <x:Array Type="{x:Type x:String}">
                <x:String>Day</x:String>
                <x:String>Week</x:String>
                <x:String>Month</x:String>
                <x:String>Year</x:String>
            </x:Array>
        </segmentedControl:SfSegmentedControl.ItemsSource>
    </segmentedControl:SfSegmentedControl>
</ContentPage>

{% endhighlight %}
{% highlight C# %}

using Syncfusion.Maui.Toolkit.SegmentedControl;
. . .

public partial class MainPage : ContentPage
{
    public MainPage()
    {
        InitializeComponent();
        SfSegmentedControl segmentedControl = new SfSegmentedControl();
        segmentedControl.VisibleSegmentsCount = 3;
        this.Content = segmentedControl;
    }
}

{% endhighlight %}
{% endtabs %}

![Visible segment count in .NET MAUI Segmented control.](images/layout/visible-segment-count.png)

N> The layout of segments adjusts automatically once [VisibleSegmentsCount](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_VisibleSegmentsCount) is set. This means that the [SegmentWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.html#Syncfusion_Maui_Toolkit_SegmentedControl_SegmentWidth) and [SfSegmentItem.Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.SegmentedControl.SfSegmentItem.html#Syncfusion_Maui_Toolkit_SegmentedControl_SfSegmentItem_Width) properties will not be applied, and the `WidthRequest` value should be divided by the `VisibleSegmentsCount` to determine the width of each segment.