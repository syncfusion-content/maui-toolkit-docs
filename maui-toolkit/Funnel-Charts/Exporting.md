---
layout: post
title: Exporting in .NET MAUI Chart control | Syncfusion
description: Learn here how to export the chart view as an image and stream in the Syncfusion® .NET MAUI Chart (SfFunnelChart) control.
platform: maui-toolkit
control: SfFunnelChart
documentation: ug
---

# Exporting in .NET MAUI Chart

## Export as an image

You can export the chart view as an image in the desired file format using the [SaveAsImage](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_SaveAsImage_System_String_) method of [SfFunnelChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html). The supported image formats are **JPEG and PNG**. By default, i.e., if you didn’t mention any image format with the filename, the chart view will be exported as an image in the PNG format.

N> The chart view can be exported as an image only when the chart view is added to the visual tree.

The following code snippet demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
...
this.Content = chart;
chart.SaveAsImage("ChartSample.jpeg"); // Export the chart view as an image in the JPEG format.

{% endhighlight %}

{% endtabs %}

T> We can change the image formats in above code by changing its extension as .jpg, .png.

The exported image will be saved in the different location across the platforms.

**Windows Phone, Android and MAC** – The image will be saved inside the 'Pictures' directory of the file system.

**iOS** – The image will be saved inside the 'Photos/Album' directory of the file system.

To save the image on Android and Windows Phone devices, you must enable file writing permissions on the device storage.

To save the image in the photo album on iOS devices, you must enable permission to access the device storage in the "Info" file. 

Add the following code snippet to the "Info" file:

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

The [GetStreamAsync](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_GetStreamAsync_Syncfusion_Maui_Toolkit_ImageFileFormat_) method of [SfFunnelChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfFunnelChart.html) is used to asynchronously get the chart view as a stream in the desired ImageFileFormat. The output stream can be passed as an input to other components that accept streams, such as PDF, Excel, and Word. The supported image file formats are **JPEG and PNG**.

N> The charts stream can only be rendered when the chart view is added to the visual tree.

The following code snippet demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}

SfFunnelChart chart = new SfFunnelChart();
...
this.Content = chart;
await chart.GetStreamAsync(ImageFileFormat.Jpeg); // Get the chart view as a stream in the JPEG format.

{% endhighlight %}

{% endtabs %}