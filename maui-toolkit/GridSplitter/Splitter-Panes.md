---
layout: post
title: Splitter Panes in .NET MAUI Grid Splitter | Syncfusion®
description: Learn how to add and organize panes in the Syncfusion® .NET MAUI Grid Splitter control, including dynamic pane management and nested pane layouts.
platform: maui-toolkit
control: SfGridSplitter
documentation: UG
---

# Splitter Panes in .NET MAUI Grid Splitter

The [.NET MAUI Grid Splitter]() control organizes content into multiple resizable regions known as panes. These panes are represented by the `SplitterPane` class and are maintained through the `SplitterPanes` collection.

Each pane can host any .NET MAUI view such as layouts, text controls, images, charts, data grids, or custom controls. Users can resize adjacent panes at runtime by dragging the separator displayed between them.

## Add panes

The `SplitterPanes` collection allows you to define multiple panes within the GridSplitter. A minimum of two panes is required to display a splitter separator.

The following example creates a GridSplitter with three panes.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SplitterPane>
        <Label Text="Pane 1" />
    </gridSplitter:SplitterPane>
    <gridSplitter:SplitterPane>
        <Label Text="Pane 2" />
    </gridSplitter:SplitterPane>
    <gridSplitter:SplitterPane>
        <Label Text="Pane 3" />
    </gridSplitter:SplitterPane>
</gridSplitter:SfGridSplitter>

{% endhighlight %}

{% highlight c# %}

SfGridSplitter splitter = new SfGridSplitter();

splitter.SplitterPanes.Add(
    new SplitterPane
    {
        Content = new Label
        {
            Text = "Pane 1"
        }
    });

splitter.SplitterPanes.Add(
    new SplitterPane
    {
        Content = new Label
        {
            Text = "Pane 2"
        }
    });

splitter.SplitterPanes.Add(
    new SplitterPane
    {
        Content = new Label
        {
            Text = "Pane 3"
        }
    });

{% endhighlight %}
{% endtabs %}

## Add panes dynamically

You can add panes at runtime using the `AddPane` method. The pane is inserted at the specified index.

{% tabs %}
{% highlight c# %}

SfGridSplitter gridSplitter = new SfGridSplitter();

SplitterPane pane = new SplitterPane()
{
    Content = new Label
    {
        Text = "New Pane"
    }
};

gridSplitter.AddPane(pane);

{% endhighlight %}
{% endtabs %}

In this example, the pane is inserted at index `1`, and the Grid Splitter automatically rebuilds its layout and separators.

## Remove panes dynamically

You can remove an existing pane using the `RemovePane` method.

{% tabs %}
{% highlight c# %}

gridSplitter.RemovePane(1);

{% endhighlight %}
{% endtabs %}

After the pane is removed, the control automatically updates its layout and separator arrangement.

## Nested panes

A `Grid Splitter` can be placed inside another `SplitterPane` to create advanced, multi-level layouts. This approach is useful for building IDE-style interfaces, dashboards, reporting applications, and workspace layouts where different sections need independent resizing behavior.

The following example creates a nested GridSplitter inside the second pane.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>
    <gridSplitter:SplitterPane>
            <Label Text="Navigation Pane" />
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane>

        <gridSplitter:SfGridSplitter Orientation="Vertical">
            <gridSplitter:SplitterPane>
                    <Label Text="Top Content" />
            </gridSplitter:SplitterPane>

            <gridSplitter:SplitterPane>
                <Label Text="Bottom Content" />
            </gridSplitter:SplitterPane>

        </gridSplitter:SfGridSplitter>

    </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

In this layout:

* The outer Grid Splitter divides the screen into left and right sections.
* The right pane hosts another Grid Splitter.
* The nested Grid Splitter divides its content into top and bottom sections.
* Users can independently resize both splitter levels.

## Complex nested layout

The Grid Splitter supports multiple levels of nesting, enabling the creation of sophisticated workspace layouts.

Examples include:

* Code editor layouts with Solution Explorer, Editor, and Output panels.
* Analytics dashboards with resizable charts and summary sections.
* Reporting applications with filter panes and report viewers.
* Content management systems with navigation, editing, and preview regions.

The following illustration shows a typical nested layout:

```text
+--------------------------------------------------+
| Navigation |           Workspace                 |
|            +-------------------------------+     |
|            |           Editor              |     |
|            +-------------------------------+     |
|            |           Output              |     |
+--------------------------------------------------+
```

## Content property support

The `SfGridSplitter` and `SplitterPane` classes support content properties, allowing panes to be declared directly without explicitly specifying the collection elements.

The following simplified syntax produces the same result as the previous examples.

{% tabs %}
{% highlight xaml %}

<gridSplitter:SfGridSplitter>

    <gridSplitter:SplitterPane>
        <Label Text="Pane 1" />
    </gridSplitter:SplitterPane>

    <gridSplitter:SplitterPane>
        <Label Text="Pane 2" />
    </gridSplitter:SplitterPane>

</gridSplitter:SfGridSplitter>

{% endhighlight %}
{% endtabs %}

This concise syntax is useful when defining a small number of panes directly in XAML.