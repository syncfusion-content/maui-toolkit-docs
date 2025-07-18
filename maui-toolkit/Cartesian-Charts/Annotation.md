---
layout: post
title: Annotations in .NET MAUI Chart control | Syncfusion
description: Learn here all about annotation support and its features in Syncfusion® .NET MAUI Chart (SfCartesianChart) control.
platform: maui-toolkit
control: SfCartesianChart
documentation: ug
keywords: .net maui chart annotations, .net maui annotations customization, syncfusion maui chart annotations, .net maui chart text annotation, .net maui chart shape annotation, .net maui chart view annotation.
---

# Annotations in .NET MAUI Chart

[SfCartesianChart](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html) provides annotation support that allows you to mark specific areas of interest in the chart area. This feature enables you to add text, images, and custom views using the following annotation types:

* Text annotation
* Shape annotation
* View annotation

## Adding Annotations

To add annotations, create an instance of any annotation type and add it to the [Annotations](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Annotations) collection. For example, the [EllipseAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html) can be added as shown below:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    <!-- Other chart elements go here -->
    ...
    <!-- Annotations section of the chart -->
    <chart:SfCartesianChart.Annotations>
        <!-- Ellipse annotation -->
        <chart:EllipseAnnotation 
            X1="2"  
            X2="4"  
            Y1="10" 
            Y2="15" 
            Text="Ellipse"/>        
    </chart:SfCartesianChart.Annotations>    
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

// Create a new SfCartesianChart instance
SfCartesianChart chart = new SfCartesianChart();
...
// Other chart elements go here
// Create a new EllipseAnnotation
var ellipse = new EllipseAnnotation()
{
    X1 = 2,  // Set the X-coordinate of the start point
    Y1 = 10, // Set the Y-coordinate of the start point
    X2 = 4,  // Set the X-coordinate of the end point
    Y2 = 15, // Set the Y-coordinate of the end point
    Text = "Ellipse" // Set the text to display with the annotation
};

// Add the ellipse annotation to the chart's Annotations collection
chart.Annotations.Add(ellipse);

// Set the chart as the content of the current view
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Annotations in MAUI Chart](Annotation_image/Adding_annotation.png)

## Positioning the Annotation

[Annotations](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.SfCartesianChart.html#Syncfusion_Maui_Toolkit_Charts_SfCartesianChart_Annotations) can be positioned in the plot area based on the [X1](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_X1) and [Y1](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_Y1) properties. For shape annotations, specify the [X2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_X2) and [Y2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Y2) properties, if needed. The X and Y values can be specified using axis units or pixel units, which can be identified by the [CoordinateUnit](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_CoordinateUnit) property, as shown in the following code snippet:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>        
        <chart:RectangleAnnotation X1="0" Y1="100" X2="300" Y2="400" Text="Pixel value" CoordinateUnit="Pixel"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}
    
// Create a new SfCartesianChart object
SfCartesianChart chart = new SfCartesianChart();     

// Other chart elements go here

// Create a new RectangleAnnotation object
var rectangle = new RectangleAnnotation()
{
    X1 = 0,
    Y1 = 100,
    X2 = 300,
    Y2 = 400,
    CoordinateUnit = ChartCoordinateUnit.Pixel,  // Set the coordinate unit to Pixel
    Text = "Pixel value"
};

// Add the rectangle annotation to the chart's Annotations collection
chart.Annotations.Add(rectangle);

// Set the Content of the current view to the chart
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Annotations in pixel value in MAUI Chart](Annotation_image/Rectangle_with_pixel.png)

## Adding Annotation for Multiple Axes

When there are multiple axes, annotations can be added to a particular axis using the [XAxisName](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_XAxisName) and [YAxisName](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_YAxisName) properties. This is demonstrated in the code snippet below:

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis Minimum="0" Maximum="1"/>
        <chart:NumericalAxis Name="YAxis" CrossesAt="{Static x:Double.MaxValue}"/>
    </chart:SfCartesianChart.YAxes>

    <chart:SfCartesianChart.Annotations>
        <chart:EllipseAnnotation X1="2" X2="4" Y1="10" Y2="15" Text="Ellipse" YAxisName="YAxis"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

// Create a new Cartesian chart
SfCartesianChart chart = new SfCartesianChart();

// Create and configure the first Y-axis
NumericalAxis yAxis1 = new NumericalAxis();
yAxis1.Minimum = 0;
yAxis1.Maximum = 1;
chart.YAxes.Add(yAxis1);

// Create and configure the second Y-axis
NumericalAxis yAxis2 = new NumericalAxis();
yAxis2.Name = "YAxis";
yAxis2.CrossesAt = double.MaxValue; // Position the axis at the far right
chart.YAxes.Add(yAxis2);

// Create an ellipse annotation
var ellipse = new EllipseAnnotation()
{
    X1 = 2, 
    Y1 = 10, 
    X2 = 4, 
    Y2 = 15, 
    Text = "Ellipse", 
    YAxisName = "YAxis" // Specify which Y-axis to use for positioning
};

// Add the ellipse annotation to the chart
chart.Annotations.Add(ellipse);

// Set the chart as the content of the current view
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Annotations in multiple axes in MAUI Chart](Annotation_image/Annotation_with_multiple_axes.png)

## Text Annotation

The [TextAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TextAnnotation.html) is used to add simple text at specific points in the chart area using the [Text](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TextAnnotation.html#Syncfusion_Maui_Toolkit_Charts_TextAnnotation_Text) property.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:TextAnnotation X1="2" Y1="25" Text="Text Annotation"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

// Create a new instance of SfCartesianChart
SfCartesianChart chart = new SfCartesianChart();

// Other chart elements go here

// Create a new TextAnnotation object
var text = new TextAnnotation()
{
    X1 = 2, 
    Y1 = 25,
    Text = "Text Annotation"  // Set the text content of the annotation    
};

// Add the TextAnnotation to the chart's Annotations collection
chart.Annotations.Add(text);

// Set the chart as the content of the current view/page
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Text annotation in MAUI Chart](Annotation_image/Text_annotation.png)

## Text Customization

The [TextAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TextAnnotation.html) can be customized using the [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TextAnnotation.html#Syncfusion_Maui_Toolkit_Charts_TextAnnotation_LabelStyle) property. The [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.TextAnnotation.html#Syncfusion_Maui_Toolkit_Charts_TextAnnotation_LabelStyle) property provides options to customize the font-family, font-size, font-attributes, and text color of axis labels. The following properties are used to customize the text:

* [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_TextColor) - Gets or sets the text color of the label.
* [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Background) - Gets or sets the background color of the labels.
* [Margin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Margin) - Gets or sets the margin of the label to customize the appearance of label.
* [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontFamily) - Gets or sets the font family name for the label.
* [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontAttributes) - Gets or sets the font style for the label.
* [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontSize) - Gets or sets the font size for the label.
* [HorizontalTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotationLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotationLabelStyle_HorizontalTextAlignment) - Gets or sets the horizontal alignment of the label.
* [VerticalTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotationLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotationLabelStyle_VerticalTextAlignment) - Gets or sets the vertical alignment of the label.
  
## Shape Annotation

The [ShapeAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html) allows you to add annotations in the form of shapes such as rectangles, ellipses, lines, horizontal lines, and vertical lines at specific areas of interest in the chart area.

* [RectangleAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RectangleAnnotation.html) - Used to draw a rectangle over the chart area.
* [EllipseAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html) - Used to draw a circle or an ellipse over the chart area.
* [LineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineAnnotation.html) - Used to draw a line over the chart area.
* [VerticalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.VerticalLineAnnotation.html) - Used to draw a vertical line across the chart area.
* [HorizontalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.HorizontalLineAnnotation.html) - Used to draw a horizontal line across the chart area.

The following APIs are commonly used in all ShapeAnnotation:

* [X2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_X2) - Gets or sets the X2 coordinate of the shape annotation.
* [Y2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Y2) - Gets or sets the Y2 coordinate of the shape annotation.
* [Fill](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Fill) - Gets or sets the background color of the shape annotation.
* [Stroke](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Stroke) - Gets or sets the stroke color of the shape annotation.
* [StrokeWidth](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_StrokeWidth) - Gets or sets the stroke width of the shape annotation.
* [StrokeDashArray](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_StrokeDashArray) - Gets or sets the stroke dash pattern of the shape annotation.
* [Text](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Text) - Gets or sets the annotation text of the shape annotation.
* [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_LabelStyle) - Gets or sets the style for customizing the annotation text of the shape annotation.

## Rectangle Annotation

The [RectangleAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.RectangleAnnotation.html) is used to draw a rectangle or a square at specific points in the chart area.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:RectangleAnnotation X1="1" Y1="40" X2="2" Y2="20"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

// Create a new rectangle annotation
var rectangle = new RectangleAnnotation()
{
    X1 = 1,
    Y1 = 40,
    X2 = 2,
    Y2 = 20,                
};

// Add the rectangle annotation to the chart's annotations collection
chart.Annotations.Add(rectangle);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Rectangle annotation in MAUI Chart](Annotation_image/Rectangle_annotation.png)

## Ellipse Annotation

The [EllipseAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html) is used to draw an oval or a circle at specific points in the chart area. You can also specify the height and width of the [EllipseAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html) by using the [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html#Syncfusion_Maui_Toolkit_Charts_EllipseAnnotation_Height) and [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html#Syncfusion_Maui_Toolkit_Charts_EllipseAnnotation_Width) properties, respectively.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:EllipseAnnotation X1="2" X2="4" Y1="10" Y2="15" Width="20" Height="20"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>

{% endhighlight %} 

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();

// Create an instance of EllipseAnnotation to display an ellipse on the chart.
var ellipse = new EllipseAnnotation()
{
    X1 = 2,
    Y1 = 10,
    X2 = 4,
    Y2 = 15,    
    Width = 20,
    Height = 20
};

// Add the ellipse annotation to the chart's annotations collection.
chart.Annotations.Add(ellipse);
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Ellipse annotation in MAUI Chart](Annotation_image/Ellipse_annotation.png)

N> When the [X2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_X2) and [Y2](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Y2) properties of the [EllipseAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html) are set, the [Height](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html#Syncfusion_Maui_Toolkit_Charts_EllipseAnnotation_Height) and [Width](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.EllipseAnnotation.html#Syncfusion_Maui_Toolkit_Charts_EllipseAnnotation_Width) properties become ineffective.

## Line Annotation
The [LineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineAnnotation.html) is used to draw a line at specific points in the chart area.

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:LineAnnotation X1="0.5" Y1="10" X2="3.5" Y2="20" Text="Line"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %} 
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
// Create and configure a LineAnnotation with specified coordinates
var line = new LineAnnotation()
{
    X1 = 0.5,
    Y1 = 10,
    X2 = 3.5,
    Y2 = 20,
    Text = "Line"
};
// Add the line annotation to the annotations collection of the chart
chart.Annotations.Add(line);
this.Content = chart;
{% endhighlight %}
{% endtabs %}

![Line Annotation in MAUI Chart](Annotation_image/Line_annotation.png)

## Vertical and Horizontal Line Annotations
The [VerticalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.VerticalLineAnnotation.html) and [HorizontalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.HorizontalLineAnnotation.html) are used to draw vertical and horizontal lines at specific points in the chart area.

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:VerticalLineAnnotation X1="2"/>
        <chart:HorizontalLineAnnotation Y1="20"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %} 
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
. . .
// Create a vertical line annotation.
var verticalLineAnnotation = new VerticalLineAnnotation()
{
    X1 = 2,
};
// Create a horizontal line annotation.
var horizontalLineAnnotation = new HorizontalLineAnnotation()
{
    Y1 = 20,
};
// Add the vertical and horizontal line annotations to the chart's annotations.
chart.Annotations.Add(verticalLineAnnotation);
chart.Annotations.Add(horizontalLineAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}  

![Vertical and horizontal Line Annotation in MAUI Chart](Annotation_image/Horizontal_vertical_annotation.png)

## Displaying Axis Label for Vertical and Horizontal Line Annotations
The [VerticalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.VerticalLineAnnotation.html) and [HorizontalLineAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.HorizontalLineAnnotation.html) allow for the display of axis labels at the line's position using the [ShowAxisLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.VerticalLineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_VerticalLineAnnotation_ShowAxisLabel) property. The default value of the [ShowAxisLabel](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.VerticalLineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_VerticalLineAnnotation_ShowAxisLabel) property is `false` as shown in the code snippet below:

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:VerticalLineAnnotation X1="2.5" ShowAxisLabel="True"/>
        <chart:HorizontalLineAnnotation Y1="25" ShowAxisLabel="True"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %} 
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
. . .
var verticalLineAnnotation = new VerticalLineAnnotation()
{
    X1 = 2.5,
    ShowAxisLabel = true // Display the label on the X-axis where the line intersects
};
var horizontalLineAnnotation = new HorizontalLineAnnotation()
{
    Y1 = 25,
    ShowAxisLabel = true // Display the label on the Y-axis where the line intersects
};
chart.Annotations.Add(verticalLineAnnotation);
chart.Annotations.Add(horizontalLineAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}  

![Vertical and horizontal Line Annotation with axis label in MAUI Chart](Annotation_image/axis_label.png)

## Axis Label Customization
The default appearance of the axis label can also be customized using the [AxisLabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.HorizontalLineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_HorizontalLineAnnotation_AxisLabelStyle) property. The [AxisLabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.HorizontalLineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_HorizontalLineAnnotation_AxisLabelStyle) property allows you to customize the axis labels by changing the font family, font size, font attributes, and text color. The following styles are used to customize the axis label:

* [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_TextColor) - Gets or sets the text color of the label.
* [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Background) - Gets or sets the background color of the labels.
* [Margin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Margin) - Gets or sets the margin of the label to customize the appearance of label.
* [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontFamily) - Gets or sets the font family name for the label.
* [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontAttributes) - Gets or sets the font style for the label.
* [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontSize) - Gets or sets the font size for the label.

## Adding Arrow to Vertical and Horizontal Line Annotations
To display a single-headed arrow, set the [LineCap](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_LineAnnotation_LineCap) property to [Arrow](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLineCap.html#Syncfusion_Maui_Toolkit_Charts_ChartLineCap_Arrow). The default value of the [LineCap](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_LineAnnotation_LineCap) property is [None](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLineCap.html#Syncfusion_Maui_Toolkit_Charts_ChartLineCap_None).

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:VerticalLineAnnotation X1="2.5" LineCap="Arrow"/>
        <chart:HorizontalLineAnnotation Y1="25" LineCap="Arrow"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %} 
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
. . .
var verticalLineAnnotation = new VerticalLineAnnotation()
{
    X1 = 2.5,
    LineCap = ChartLineCap.Arrow // Add an arrow cap to the end of the line
};
var horizontalLineAnnotation = new HorizontalLineAnnotation()
{
    Y1 = 25,
    LineCap = ChartLineCap.Arrow // Add an arrow cap to the end of the line
};
chart.Annotations.Add(verticalLineAnnotation);
chart.Annotations.Add(horizontalLineAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}  

![Vertical and horizontal Line Annotations with linecap in MAUI Chart](Annotation_image/Horizontal_vertical_with_cap.png)

N> The [LineCap](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.LineAnnotation.html#Syncfusion_Maui_Toolkit_Charts_LineAnnotation_LineCap) is applicable to line, horizontal, and vertical annotations.

## Adding Text in Shape Annotation
For all shape annotations, the text can be displayed using the [Text](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Text) property.

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:EllipseAnnotation X1="2" X2="4" Y1="10" Y2="15" Text="Ellipse"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %}
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
...
var ellipseAnnotation = new EllipseAnnotation()
{
    X1 = 2,
    Y1 = 10,
    X2 = 4,
    Y2 = 15,
    Text = "Ellipse" // Set the text label for the ellipse.
};
chart.Annotations.Add(ellipseAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}

![Annotation in MAUI Chart](Annotation_image/Adding_annotation.png)

## Text Customization in Shape Annotation
The [Text](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_Text) in shape annotation also can be customized by using the [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_LabelStyle) property. The [LabelStyle](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ShapeAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ShapeAnnotation_LabelStyle) property provides options to customize the font-family, font-size, font-attributes and text color of axis labels.

* [TextColor](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_TextColor) - Gets or sets the text color of the label.
* [Background](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Background) - Gets or sets the background color of the labels.
* [Margin](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_Margin) - Gets or sets the margin of the label to customize the appearance of label.
* [FontFamily](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontFamily) - Gets or sets the font family name for the label.
* [FontAttributes](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontAttributes) - Gets or sets the font style for the label.
* [FontSize](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartLabelStyle_FontSize) - Gets or sets the font size for the label.
* [HorizontalTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotationLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotationLabelStyle_HorizontalTextAlignment) - Gets or sets the horizontal alignment of the label.
* [VerticalTextAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotationLabelStyle.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotationLabelStyle_VerticalTextAlignment) - Gets or sets the vertical alignment of the label.
  
## View Annotation

The [ViewAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ViewAnnotation.html) allows you to add annotations in the form of your own custom view using the [View](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ViewAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ViewAnnotation_View) property at a specific area of interest in the chart area. Additionally, the [ViewAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ViewAnnotation.html) can be aligned using the [VerticalAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ViewAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ViewAnnotation_VerticalAlignment) and [HorizontalAlignment](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ViewAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ViewAnnotation_HorizontalAlignment) properties.

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:ViewAnnotation X1="3" Y1="30">
            <chart:ViewAnnotation.View>
                <Image Source="cloud.png"/>
            </chart:ViewAnnotation.View>
        </chart:ViewAnnotation>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %}
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
...
// Define a new ViewAnnotation to add a graphical element to the chart.
var viewAnnotation = new ViewAnnotation()
{
    X1 = 3,
    Y1 = 30,
    View = new Image() { Source = "cloud.png" }
};

// Add the created ViewAnnotation to the chart's Annotations collection.
chart.Annotations.Add(viewAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}

![View Annotation in .NET MAUI Chart](Annotation_image/View_annotation.png)

## Annotation Visibility

The [IsVisible](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html#Syncfusion_Maui_Toolkit_Charts_ChartAnnotation_IsVisible) property of [ChartAnnotation](https://help.syncfusion.com/cr/maui-toolkit/Syncfusion.Maui.Toolkit.Charts.ChartAnnotation.html) is used to toggle the visibility of the annotation.

{% tabs %}
{% highlight xaml %}
<chart:SfCartesianChart>
    ...
    <chart:SfCartesianChart.Annotations>
        <chart:EllipseAnnotation X1="2" X2="4" Y1="10" Y2="15" Text="Ellipse" IsVisible="False"/>
    </chart:SfCartesianChart.Annotations>
</chart:SfCartesianChart>
{% endhighlight %}
{% highlight c# %}
SfCartesianChart chart = new SfCartesianChart();
...
var ellipseAnnotation = new EllipseAnnotation()
{
    X1 = 2,
    Y1 = 10,
    X2 = 4,
    Y2 = 15,
    Text = "Ellipse",
    IsVisible = false  // Set the visibility of the annotation
};

chart.Annotations.Add(ellipseAnnotation);
this.Content = chart;
{% endhighlight %}
{% endtabs %}
