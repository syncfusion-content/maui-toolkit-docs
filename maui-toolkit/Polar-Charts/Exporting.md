---
layout: post
title: Exporting in .NET MAUI Chart Control | Syncfusion
description: Learn here how to export the chart view as an image and stream in the Syncfusion® .NET MAUI Chart (SfPolarChart) control.
platform: maui-toolkit
control: SfPolarChart
documentation: ug
---

# Exporting in .NET MAUI Chart

## Export as an image

You can export the chart view as an image in your desired file format using the [SaveAsImage](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_SaveAsImage_System_String_) method of [SfPolarChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html). The supported image formats are **JPEG and PNG**. By default, if you don't specify any image format with the filename, the chart view will be exported as an image in PNG format.

N> The chart view can be exported as an image only when it has been added to the visual tree.

The following code sample demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}
// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();

// ... (Other chart configuration code would go here)

// Set the chart as the content of the current page or control
this.Content = chart;

// Export the chart as a JPEG image file named "ChartSample.jpeg"
chart.SaveAsImage("ChartSample.jpeg");
{% endhighlight %}

{% endtabs %}

T> You can change the image format by changing the file extension to .jpg or .png in the filename parameter.

The exported image will be saved in different locations across platforms:

- **Windows Phone, Android, and macOS** – The image will be saved inside the 'Pictures' directory of the file system.
- **iOS** – The image will be saved inside the 'Photos/Album' directory of the file system.

To save images on Android and Windows Phone devices, you must enable file writing permissions on the device storage.

To save images in the photo album on iOS devices, you must enable permission to access the device storage in the "Info.plist" file.

Add the following code snippet to the "Info.plist" file:

{% tabs %}

{% highlight xaml %}
<dict>
    ...    
    <key>NSPhotoLibraryUsageDescription</key>    
    <string>This app needs permission to access the Photos</string>    
    <key>NSPhotoLibraryAddUsageDescription</key>    
    <string>This app needs permission to access the Photos</string> 
    ...
</dict>
{% endhighlight %}

{% endtabs %}

## Get the stream of Chart

The [GetStreamAsync](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_GetStreamAsync_Syncfusion_Maui_Toolkit_ImageFileFormat_) method of [SfPolarChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfPolarChart.html) is used to asynchronously get the chart view as a stream in the desired ImageFileFormat. The output stream can be passed as an input to other components that accept streams, such as PDF, Excel, and Word documents. The supported image file formats are **JPEG and PNG**.

N> The chart's stream can only be generated when the chart view is added to the visual tree.

The following code sample demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}
// Create a new instance of SfPolarChart
SfPolarChart chart = new SfPolarChart();

// ... (Other chart configuration code goes here)

// Set the chart as the content of the current page or container
this.Content = chart;

// Export the chart as a JPEG image stream asynchronously
var stream = await chart.GetStreamAsync(ImageFileFormat.Jpeg);

// Now you can use this stream with other components like PDF, Excel, etc.
{% endhighlight %}

{% endtabs %}