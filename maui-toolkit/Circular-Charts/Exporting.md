---
layout: post
title: Exporting in .NET MAUI Chart Control | Syncfusion
description: Learn how to export the chart view as an image and stream in the Syncfusion® .NET MAUI Chart (SfCircularChart) control.
platform: maui-toolkit
control: SfCircularChart
documentation: ug
---

# Exporting in .NET MAUI Chart

## Export as an Image

You can export the chart view as an image in the desired file format using the [SaveAsImage](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_SaveAsImage_System_String_) method of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html). The supported image formats are **JPEG and PNG**. By default, if you don’t specify an image format with the filename, the chart view will be exported as a PNG image.

N> The chart view can only be exported as an image when the chart view is added to the visual tree.

The following code snippet demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}

// Create a new instance of SfCircularChart
SfCircularChart chart = new SfCircularChart();

// ... (Other chart configuration code goes here)

// Set the chart as the content of the current page or container
this.Content = chart;

// Dynamically save the chart as an image file named "ChartSample.jpeg"
chart.SaveAsImage("ChartSample.jpeg");

{% endhighlight %}

{% endtabs %}

T> You can change the image format in the code above by changing its extension to .jpg or .png.

The exported image will be saved in different locations depending on the platform:

- **Windows Phone, Android, and macOS**: The image will be saved inside the 'Pictures' directory of the file system.
- **iOS**: The image will be saved inside the 'Photos/Album' directory of the file system.

To save the image on Android and Windows Phone devices, you must enable file writing permissions in the device storage.

To save the image in the photo album on iOS devices, you must enable permission to access the device storage in the Info.plist file.

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

## Get the Stream of the Chart

The [GetStreamAsync](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartBase.html#Syncfusion_Maui_Toolkit_Charts_ChartBase_GetStreamAsync_Syncfusion_Maui_Toolkit_ImageFileFormat_) method of [SfCircularChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCircularChart.html) is used to asynchronously get the chart view as a stream in the desired ImageFileFormat. The output stream can be passed as input to other components that accept streams, such as PDF, Excel, and Word. The supported image file formats are **JPEG and PNG**.

N> The chart stream can only be rendered when the chart view is added to the visual tree.

The following code snippet demonstrates the usage of this method:

{% tabs %}

{% highlight c# %}

// Create a new instance of SfCircularChart
SfCircularChart chart = new SfCircularChart();

// ... (Other chart configuration code goes here)

// Set the chart as the content of the current page or container
this.Content = chart;

// Export the chart as a JPEG image asynchronously
// The GetStreamAsync method returns a stream containing the image data
await chart.GetStreamAsync(ImageFileFormat.Jpeg);

{% endhighlight %}

{% endtabs %}


