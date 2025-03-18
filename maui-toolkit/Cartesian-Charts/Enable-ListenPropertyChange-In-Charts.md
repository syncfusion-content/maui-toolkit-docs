---
layout: post
title: Enable ListenPropertyChange in .NET MAUI Charts | Syncfusion
description: Learn how ListenPropertyChange in Syncfusion® .NET MAUI Chart (SfCartesianChart) enables real-time data updates while considering performance impact with large datasets.
platform: maui
control: SfCartesianChart
documentation: ug
keywords: .net maui chart ListenPropertyChange, syncfusion maui chart property change, real-time chart updates .net maui, maui chart dynamic updates, .net maui chart listen property change feature, syncfusion maui chart real-time data, listen property change
---

## ListenPropertyChange 

The ListenPropertyChange property in .NET MAUI Charts allows the chart to update dynamically when the underlying data source properties change. This enables real-time dynamic and data visualization. 

By leveraging INotifyPropertyChanged, the data points now automatically reflect changes, ensuring the chart remains in real time and responsive to data updates.

To enable property change notifications, your data model must implement the INotifyPropertyChanged interface, as shown in the code below:

**C#**

{% highlight C# %}

    public class DataModel : INotifyPropertyChanged
    {
        private string category;
        private double metric;

        public string Category
        {
            get => category;
            set
            {
                if (category !=  value)
                {
                    category = value;
                    OnPropertyChanged(nameof(Category));
                }
            }
        }

        public double Metric
        {
            get => metric;
            set
            {
                if (metric != value)
                {
                    metric = value;
                    OnPropertyChanged(nameof(Metric));
                }
            }
        }

        public event PropertyChangedEventHandler? PropertyChanged;

        protected void OnPropertyChanged(string propertyName)
        {
            PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
        }
    }

{% endhighlight %}

## Enabling ListenPropertyChange in Charts

When your data model implements INotifyPropertyChanged, you need to set the ListenPropertyChange property of the series to `true`, to make the chart listen to the property changes of your data object.

**XAML**

{% highlight xaml %}

    <chart:SfCartesianChart>

    . . .

    <chart:LineSeries ItemsSource="{Binding DataSource}"
                      XBindingPath="Category"
                      YBindingPath="Metric"
                      ListenPropertyChange="True" />

    . . .

    </chart:SfCartesianChart>

{% endhighlight %}

By default, ListenPropertyChange is set to `false` to prevent unnecessary event registrations and potential performance overhead. 

N> Enabling ListenPropertyChange registers the PropertyChanged event of every object in the data source. If your dataset contains a large number of data points, this may impact on the chart’s loading performance.

