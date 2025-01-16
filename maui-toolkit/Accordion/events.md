---
layout: post
title: Events in .NET MAUI Accordion control | Syncfusion<sup>®</sup>
description: Learn about Events support in Syncfusion<sup>®</sup> Toolkit for .NET MAUI Accordion control, its elements and more.
platform: maui-toolkit
control: SfAccordion
documentation: ug
--- 

# Accordion Events in .NET MAUI Accordion (SfAccordion)

There are four built-in events in the SfAccordion control namely:

* `Expanding`
* `Expanded`
* `Collapsing`
* `Collapsed`

### Expanding Event

The `Expanding` event will be triggered when the accordion item is being expanded. It can cancel the expansion using `ExpandingAndCollapsingEventArgs`, which contains the following property:

* `Cancel`: Indicates that the expansion or collapse action should be cancelled.
* `Index`: Gets the index of the current expanding accordion item.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Expanding="accordion_Expanding">
    <syncfusion:SfAccordion.Items>
            <syncfusion:AccordionItem>
                    <syncfusion:AccordionItem.Header>
                        <Grid  HeightRequest="48">
                            <Label Text="Robin Rane" Margin="16,14,0,14" CharacterSpacing="0.25" FontFamily="Roboto-Regular"  FontSize="14" />
                        </Grid>
                    </syncfusion:AccordionItem.Header>
                    <syncfusion:AccordionItem.Content>
                        <Grid ColumnSpacing="10" RowSpacing="2" BackgroundColor="#f4f4f4"  >
                            <Grid Margin="16,6,0,0">
                                <Grid.Resources>
                                    <Style TargetType="Label">
                                        <Setter Property="FontFamily" Value="Roboto-Regular"/>
                                    </Style>
                                </Grid.Resources>
                                <Grid.RowDefinitions >
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="{OnPlatform Default=90,Android=90,WinUI=70, iOS=100,MacCatalyst=70 }"/>
                                    <RowDefinition Height="Auto"/>
                                </Grid.RowDefinitions>
                                <Grid.ColumnDefinitions>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="*"/>
                                </Grid.ColumnDefinitions>
                                <Frame  Grid.RowSpan="4" BorderColor="Transparent" Grid.Row="0" Grid.Column="0"  Padding="0" Margin="0,0,0,7">
                                    <Image  Source="emp_01.png"/>
                                </Frame>
                                <Label Text="Position" Grid.Column="1" Grid.Row="0" Margin="6,0,0,0"/>
                                <Label Text="Chairman" Grid.Row="0" Grid.Column="2"/>
                                <Label Text="Organization " Grid.Row="1" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="ABC Inc." Grid.Row="1" Grid.Column="2"/>
                                <Label Text="Date Of Birth " Grid.Row="2" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="09/17/1973" Grid.Row="2" Grid.Column="2"/>
                                <Label Text="Location " Grid.Row="3" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="Boston" Grid.Row="3" Grid.Column="2"/>
                                <Label Padding="0,10,0,10" Grid.Row="4" Grid.ColumnSpan="3"  LineBreakMode="WordWrap"  
                                            FontSize="14" CharacterSpacing="0.25" VerticalTextAlignment="Center" 
                                                Text="Robin Rane, Chairman of ABC Inc., leads with dedication and vision.Under his guidance, the company thrives and continues to make a significant impact in the industry.">
                                </Label>
                                <StackLayout Grid.Row="5" Orientation="Horizontal" Margin="0,0,0,12">
                                    <Label Text="&#xe700;" FontSize="16" Margin="0,2,2,2"
                                                   FontFamily='{OnPlatform Android=AccordionFontIcons.ttf#,WinUI=AccordionFontIcons.ttf#AccordionFontIcons,MacCatalyst=AccordionFontIcons,iOS=AccordionFontIcons}'
                                                   VerticalOptions="Center" VerticalTextAlignment="Center"/>
                                    <Label Text="(617) 555-1234" Grid.Column="1" VerticalOptions="Center" CharacterSpacing="0.25" FontSize="14"/>
                                </StackLayout>
                            </Grid>
                        </Grid>
                    </syncfusion:AccordionItem.Content>
                </syncfusion:AccordionItem>
        </syncfusion:SfAccordion.Items>
 </syncfusion:SfAccordion>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void accordion_Expanding(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandingAndCollapsingEventArgs e)
{
    if (e.Index == 2)
    {
        e.Cancel = true;
    }
}
{% endhighlight %}
{% endtabs %}

### Expanded Event

The `Expanded` event is triggered when an accordion item is fully expanded. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Expanded="accordion_Expanded">
    <syncfusion:SfAccordion.Items>
        <syncfusion:AccordionItem>
                    <syncfusion:AccordionItem.Header>
                        <Grid  HeightRequest="48">
                            <Label Text="Robin Rane" Margin="16,14,0,14" CharacterSpacing="0.25" FontFamily="Roboto-Regular"  FontSize="14" />
                        </Grid>
                    </syncfusion:AccordionItem.Header>
                    <syncfusion:AccordionItem.Content>
                        <Grid ColumnSpacing="10" RowSpacing="2" BackgroundColor="#f4f4f4"  >
                            <Grid Margin="16,6,0,0">
                                <Grid.Resources>
                                    <Style TargetType="Label">
                                        <Setter Property="FontFamily" Value="Roboto-Regular"/>
                                    </Style>
                                </Grid.Resources>
                                <Grid.RowDefinitions >
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="25"/>
                                    <RowDefinition Height="{OnPlatform Default=90,Android=90,WinUI=70, iOS=100,MacCatalyst=70 }"/>
                                    <RowDefinition Height="Auto"/>
                                </Grid.RowDefinitions>
                                <Grid.ColumnDefinitions>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="100"/>
                                    <ColumnDefinition Width="*"/>
                                </Grid.ColumnDefinitions>
                                <Frame  Grid.RowSpan="4" BorderColor="Transparent" Grid.Row="0" Grid.Column="0"  Padding="0" Margin="0,0,0,7">
                                    <Image  Source="emp_01.png"/>
                                </Frame>
                                <Label Text="Position" Grid.Column="1" Grid.Row="0" Margin="6,0,0,0"/>
                                <Label Text="Chairman" Grid.Row="0" Grid.Column="2"/>
                                <Label Text="Organization " Grid.Row="1" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="ABC Inc." Grid.Row="1" Grid.Column="2"/>
                                <Label Text="Date Of Birth " Grid.Row="2" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="09/17/1973" Grid.Row="2" Grid.Column="2"/>
                                <Label Text="Location " Grid.Row="3" Grid.Column="1" Margin="6,0,0,0"/>
                                <Label Text="Boston" Grid.Row="3" Grid.Column="2"/>
                                <Label Padding="0,10,0,10" Grid.Row="4" Grid.ColumnSpan="3"  LineBreakMode="WordWrap"  
                                            FontSize="14" CharacterSpacing="0.25" VerticalTextAlignment="Center" 
                                                Text="Robin Rane, Chairman of ABC Inc., leads with dedication and vision.Under his guidance, the company thrives and continues to make a significant impact in the industry.">
                                </Label>
                                <StackLayout Grid.Row="5" Orientation="Horizontal" Margin="0,0,0,12">
                                    <Label Text="&#xe700;" FontSize="16" Margin="0,2,2,2"
                                                   FontFamily='{OnPlatform Android=AccordionFontIcons.ttf#,WinUI=AccordionFontIcons.ttf#AccordionFontIcons,MacCatalyst=AccordionFontIcons,iOS=AccordionFontIcons}'
                                                   VerticalOptions="Center" VerticalTextAlignment="Center"/>
                                    <Label Text="(617) 555-1234" Grid.Column="1" VerticalOptions="Center" CharacterSpacing="0.25" FontSize="14"/>
                                </StackLayout>
                            </Grid>
                        </Grid>
                    </syncfusion:AccordionItem.Content>
                </syncfusion:AccordionItem>
    </syncfusion:SfAccordion.Items>
 </syncfusion:SfAccordion.Item>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="4" %}
private void accordion_Expanded(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandedAndCollapsedEventArgs e)
{
    // Get the index of current accordion item
    int index = e.Index;
}
{% endhighlight %}
{% endtabs %}

### Collapsing Event

The `Collapsing` event will be triggered when the expander control is being collapsed. You can cancel the collapsing using `ExpandingAndCollapsingEventArgs`, which contains the following property:

* `Cancel`: Indicates that the expansion or collapse action should be cancelled.
* `Index`: Gets the index of the current collapsing accordion item.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Collapsing="accordion_Collapsing">
    <syncfusion:SfAccordion.Items>
        <syncfusion:AccordionItem>
            ...
            ...
        </syncfusion:AccordionItem>
    </syncfusion:SfAccordion.Items>
 </syncfusion:SfAccordion>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="3" %}
private void accordion_Collapsing(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandingAndCollapsingEventArgs e)
{
    if (e.Index == 2)
    {
        e.Cancel = true;
    }
}
{% endhighlight %}
{% endtabs %}

### Collapsed Event 

The `Collapsed` event is triggered when an accordion item is collapsed. You can execute your own code when this event occurs.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" hl_lines="1" %}
<syncfusion:SfAccordion x:Name="accordion" Collapsed="accordion_Collapsed">
    <syncfusion:SfAccordion.Items>
        <syncfusion:AccordionItem>
            ...
            ...
        </syncfusion:AccordionItem>
    </syncfusion:SfAccordion.Items>
 </syncfusion:SfAccordion>
{% endhighlight %}

{% highlight c# tabtitle="MainPage.xaml.cs" hl_lines="4" %}
private void accordion_Collapsed(object sender, Syncfusion.Maui.Toolkit.Accordion.ExpandedAndCollapsedEventArgs e)
{
    // Get the index of current accordion item
    int index = e.Index;
}
{% endhighlight %}
{% endtabs %}