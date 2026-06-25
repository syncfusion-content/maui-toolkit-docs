---
layout: post
title: Customization in .NET MAUI Accordion control | Syncfusion
description: Learn here all about Customization support in Syncfusion® Toolkit for .NET MAUI Accordion control and more details. 
platform: maui-toolkit
control: SfAccordion
documentation: ug
--- 

# Customization in .NET MAUI Accordion (SfAccordion)

## Animation easing

You can customize the rate of change of a parameter over time or the animation style of an accordion item by using the `AnimationEasing` property. By default, the animation easing is set to `Linear`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
         <syncfusion:SfAccordion x:Name="accordion"
                                AnimationEasing="SinOut" />
{% endhighlight %}
{% highlight c# %}
    accordion.AnimationEasing = ExpanderAnimationEasing.SinOut;
{% endhighlight %}
{% endtabs %}

## Auto scroll position

The `SfAccordion` allows you to customize the scroll position of the expanded accordion item using the `AutoScrollPosition` property. By default, the auto-scroll position is set to `MakeVisible`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion"
                             AutoScrollPosition="Top"/>
{% endhighlight %}
{% highlight c# %}
    accordion.AutoScrollPosition = AccordionAutoScrollPosition.Top;
{% endhighlight %}
{% endtabs %}

## Bring an accordion item into view

The `BringIntoView` method is used to bring a specific item into view by scrolling to it programmatically.

{% tabs %}
{% highlight xaml %}
<ContentPage.Content>
    <StackLayout>
        <Button Clicked="Button_Clicked" Text="Button"/>
        <syncfusion:SfAccordion x:Name="accordion">
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
                                <Label Padding="0,10,0,10" Grid.Row="4" Grid.ColumnSpan="3"        LineBreakMode="WordWrap"  
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
    </StackLayout>
</ContentPage.Content>
{% endhighlight %}
{% endtabs %}

{% tabs %}
{% highlight c# hl_lines="3" %}
private void Button_Clicked(object sender, EventArgs e)
{
    accordion.BringIntoView(accordion.Items[15]);
}
{% endhighlight %}
{% endtabs %}

## Expand mode

You can expand single or multiple items using the `ExpandMode` property. By default, the expanded mode is set to `Single`.  

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion" 
                            ExpandMode="Multiple" />
{% endhighlight %}
{% highlight c# %}
    accordion.ExpandMode = AccordionExpandMode.Multiple;
{% endhighlight %}
{% endtabs %}

## Item spacing

The `SfAccordion` allows you to customize the vertical spacing between the accordion items by using the `ItemSpacing` property. 

{% tabs %}
{% highlight xaml hl_lines="2" %}
    <syncfusion:SfAccordion x:Name="accordion" 
                            ItemSpacing="6.0d" />
{% endhighlight %}
{% highlight c# %}
    accordion.ItemSpacing = 6.0d;
{% endhighlight %}
{% endtabs %}