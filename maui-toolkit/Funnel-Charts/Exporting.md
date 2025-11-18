---
layout: post
title: Exporting in .NET MAUI Chart Funnel control | Syncfusion
description: Learn here how to export the chart view as an image and stream in the Syncfusion® .NET MAUI Chart (SfFunnelChart) control.
platform: maui-toolkit
control: SfFunnelChart
documentation: ug
keywords: .net maui funnel chart, export chart as image, save chart image, get chart stream, image formats, export chart view, maui toolkit
---

# Exporting in .NET MAUI Funnel Chart 

## Export as an image

You can export the chart view as an image in your desired file format using the [SaveAsImage](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_SaveAsImage_System_String_) method of [SfFunnelChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html). The supported image formats are **JPEG and PNG**. By default, if you don't specify an image format with the filename, the chart view will be exported as an image in PNG format.

N> The chart view can be exported as an image only when it is added to the visual tree.

The following code snippet demonstrates how to use this method:

{% tabs %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
// Configure chart properties
...
this.Content = chart;
chart.SaveAsImage("ChartSample.jpeg"); // Export the chart view as an image in JPEG format

{% endhighlight %}

{% endtabs %}

T> You can change the image format by simply changing the file extension to .jpg or .png in the filename.

The exported image will be saved in different locations across platforms:

- **Windows Phone, Android, and MAC** – The image will be saved in the 'Pictures' directory of the file system.
- **iOS** – The image will be saved in the 'Photos/Album' directory of the file system.

For Android and Windows Phone devices, you must enable file writing permissions on the device storage to save images.

For iOS devices, you need to enable permission to access the device storage in the "Info" file. Add the following code snippet to the file:

{% tabs %}

{% highlight xaml %}

<dict>
    ...    
    <key>NSPhotoLibraryUsageDescription</key>    
    <string>This App needs permission to access the Photos</string>    
    <key>NSPhotoLibraryAddUsageDescription</key>    
    <string>This App needs permission to access the Photos</string> 
    ...
</dict>

{% endhighlight %}

{% endtabs %}

## Get the stream of Chart

The [GetStreamAsync](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_GetStreamAsync_Syncfusion_Maui_Toolkit_ImageFileFormat_) method of [SfFunnelChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html) allows you to asynchronously get the chart view as a stream in your desired ImageFileFormat. This output stream can be passed as input to other components that accept streams, such as PDF, Excel, and Word documents. The supported image file formats are **JPEG and PNG**.

N> The chart's stream can only be generated when the chart view is added to the visual tree.

The following code snippet demonstrates how to use this method:

{% tabs %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
// Configure chart properties
...
this.Content = chart;
var stream = await chart.GetStreamAsync(ImageFileFormat.Jpeg); // Get the chart view as a stream in JPEG format

{% endhighlight %}

{% endtabs %}