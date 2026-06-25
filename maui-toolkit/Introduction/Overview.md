---
layout: post
title: Comprehensive Guide to Syncfusion® Toolkit for .NET MAUI
description: Overview of the Syncfusion® .NET MAUI Toolkit, detailed steps on how to read the user guide effectively, and supported platforms.
platform: maui-toolkit
control: Overview
documentation: UG
---

# Build Modern .NET MAUI Apps with Syncfusion® Toolkit

The Syncfusion<sup>®</sup> Toolkit for .NET MAUI provides a powerful collection of UI components designed to help you create rich, high-performance mobile and desktop applications with ease.

Whether you're building data-driven dashboards, enterprise apps, or feature-rich user interfaces, the toolkit enables you to deliver consistent, polished experiences across platforms.


<img src="../Images/maui-toolkit-banner.webp" alt=".NET MAUI Toolkit banner" />

## Supported Platforms

<table class="platform-table">
  <thead>
    <tr>
      <th>Target Platform</th>
      <th>Supported Version</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Android</td>
      <td>5.0 (API 21) or higher</td>
    </tr>
    <tr>
      <td>iOS</td>
      <td>12.2 or higher</td>
    </tr>
    <tr>
      <td>macOS (Mac Catalyst)</td>
      <td>macOS 12 or higher</td>
    </tr>
    <tr>
      <td>Windows</td>
      <td>Windows 11 and Windows 10 version 1809 or higher</td>
    </tr>
  </tbody>
</table>

## Supported .NET versions

* .NET 9.0
* .NET 10.0

## Controls List

<style>
#table
{
border:0 !important;
line-height: 160% !important;
}
#table tr
{
border:0 !important;
}
#table td
{
border:0 !important;
vertical-align: top;
}
.controlanchorlink {
    font-size: 14px !important;
    text-decoration: none !important;
    text-align: left !important;
    padding: 2px 0px;
}
.category-topics {
    font-size: 14px !important;
    font-weight: 500 !important;
    border: 0 !important;
    line-height: 20px;
    margin-top:  7px;
    margin-bottom: 5px;
}
.category {
    font-size: 14px !important;
    font-weight: 500 !important;
    border: 0 !important;
    text-align: left !important;
    line-height: 20px;
    padding-top: 20px;
}
@font-face {
    font-family: 'Toolkit Icons';
    src: url('data:font/woff2;charset=utf-8;base64,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') format('woff2');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
}


[class^="sf-icon-"], [class*=" sf-icon-"] {
 font-family: 'Toolkit Icons' !important;
speak: none;
top:4px;
    color: #3c78ef;
font-size: 20px;
font-style: normal;
font-weight: normal;
font-variant: normal;
text-transform: none;
line-height: 1;
    padding-right: 10px;
    position: relative;
}

.sf-icon-accordion:before { content: "\e700"; }
.sf-icon-button:before { content: "\e701"; }
.sf-icon-bottom-sheet:before { content: "\e702"; }
.sf-icon-calendars:before { content: "\e703"; }
.sf-icon-cards:before { content: "\e704"; }
.sf-icon-carousel:before { content: "\e705"; }
.sf-icon-Cartesian-chart:before { content: "\e706"; }
.sf-icon-chips:before { content: "\e707"; }
.sf-icon-circular-chart:before { content: "\e708"; }
.sf-icon-circular-progressbar:before { content: "\e709"; }
.sf-icon-date-picker:before { content: "\e70a"; }
.sf-icon-date-time-picker:before { content: "\e70b"; }
.sf-icon-effects-view:before { content: "\e70c"; }
.sf-icon-expander:before { content: "\e70d"; }
.sf-icon-funnel-chart:before { content: "\e70e"; }
.sf-icon-linear-progress-bar:before { content: "\e70f"; }
.sf-icon-navigation-drawer:before { content: "\e710"; }
.sf-icon-numeric-entry:before { content: "\e711"; }
.sf-icon-numeric-updown:before { content: "\e712"; }
.sf-icon-Otp-input:before { content: "\e713"; }
.sf-icon-picker:before { content: "\e714"; }
.sf-icon-polar-chart:before { content: "\e715"; }
.sf-icon-popup:before { content: "\e716"; }
.sf-icon-pull-refresh:before { content: "\e717"; }
.sf-icon-pyramid-chart:before { content: "\e718"; }
.sf-icon-segmented-button:before { content: "\e719"; }
.sf-icon-shimmer:before { content: "\e71a"; }
.sf-icon-spark-chart:before { content: "\e71b"; }
.sf-icon-sunburst-chart:before { content: "\e71c"; }
.sf-icon-tabs:before { content: "\e71d"; }
.sf-icon-text-input:before { content: "\e71e"; }
.sf-icon-time-picker:before { content: "\e71f"; }
.sf-icon-ai-symbol:before { content: "\e720"; }
.sf-icon-arrow-right:before { content: "\e721"; }

</style>

<table id="table">
  <colgroup>
    <col style="width: 33.33%">
    <col style="width: 33.33%">
    <col style="width: 33.33%">
  </colgroup>

<tr>

<!-- COLUMN 1 -->
<td>

<!-- Calendars -->
<div>
    <p class="category-topics">CALENDARS</p>
</div>
<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/calendar/overview">
        <span class="sf-home-icon sf-icon-calendars"></span>Calendar
    </a>
</div>

<div><p class="category-topics">EDITORS</p></div>

<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/datepicker/overview">
    <span class="sf-home-icon sf-icon-date-picker"></span>Date Picker
</a>
</div>

<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/datetimepicker/overview">
    <span class="sf-home-icon sf-icon-date-time-picker"></span>Date Time Picker
</a>
</div>

<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/numericentry/overview">
    <span class="sf-home-icon sf-icon-numeric-entry"></span>Numeric Entry
</a>
</div>
<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/numericentry/overview">
    <span class="sf-home-icon sf-icon-numeric-updown"></span>Numeric Up Down
</a>
</div>
<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/picker/overview">
    <span class="sf-home-icon sf-icon-picker"></span>Picker
</a>
</div>

<div class="controlanchorlink">
<a target="_self" href="https://help.syncfusion.com/maui-toolkit/timepicker/overview">
    <span class="sf-home-icon sf-icon-time-picker"></span>Time Picker
</a>
</div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/otp-input/overview"><span class="sf-home-icon sf-icon-Otp-input"></span>OTP Input</a></div>

<div><p class="category-topics">BUTTONS</p></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/button/overview"><span class="sf-home-icon sf-icon-button"></span>Button</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/chips/overview"><span class="sf-home-icon sf-icon-chips"></span>Chips</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/segmented-control/overview"><span class="sf-home-icon sf-icon-segmented-button"></span>Segmented Control</a></div>

</td>

<!-- COLUMN 2 -->
<td>

<div><p class="category-topics">NAVIGATION</p></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/bottom-sheet/overview"><span class="sf-home-icon sf-icon-bottom-sheet"></span>Bottom Sheet</a></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/navigationdrawer/overview"><span class="sf-home-icon sf-icon-navigation-drawer"></span>Navigation Drawer</a></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/tabview/overview"><span class="sf-home-icon sf-icon-tabs"></span>Tab View</a></div>

<div><p class="category-topics">LAYOUT</p></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/popup/overview"><span class="sf-home-icon sf-icon-popup"></span>Popup</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/textinputlayout/overview"><span class="sf-home-icon sf-icon-text-input"></span>Text Input Layout</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/expander/overview"><span class="sf-home-icon sf-icon-expander"></span>Expander</a></div>

<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/accordion/overview"><span class="sf-home-icon sf-icon-accordion"></span>Accordion</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/carousel-view/overview"><span class="sf-home-icon sf-icon-carousel"></span>Carousel</a></div>
<div class="controlanchorlink"><a target="_self" href="https://help.syncfusion.com/maui-toolkit/cards/overview"><span class="sf-home-icon sf-icon-cards"></span>Cards</a></div>


<!--Miscellaneous-->
<div>
    <p class="category-topics">MISCELLANEOUS</p>
</div>

<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/effects-view/overview">
        <span class="sf-home-icon sf-icon-effects-view"></span>Effects View
    </a>
</div>
<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/shimmer/overview">
        <span class="sf-home-icon sf-icon-shimmer"></span>Shimmer
    </a>
</div>

</td>


<!-- COLUMN 3 -->
<td>

<!-- Notification -->
<div>
    <p class="category-topics">NOTIFICATION</p>
</div>

<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/linearprogressbar/overview">
        <span class="sf-home-icon sf-icon-linear-progress-bar"></span>Linear Progress Bar
    </a>
</div>
<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/circularprogressbar/overview">
        <span class="sf-home-icon sf-icon-circular-progressbar"></span>Circular Progress Bar
    </a>
</div>

<div class="controlanchorlink">
    <a target="_self" href="https://help.syncfusion.com/maui-toolkit/pull-to-refresh/overview">
        <span class="sf-home-icon sf-icon-pull-refresh"></span>Pull to Refresh
    </a>
</div>

<!-- Data Visualization -->
<div>
    <p class="category-topics">DATA VISUALIZATION</p>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/cartesian-charts/overview">
        <span class="sf-home-icon sf-icon-Cartesian-chart"></span>Cartesian Charts
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/circular-charts/overview">
        <span class="sf-home-icon sf-icon-circular-chart"></span>Circular Charts
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/funnel-charts/overview">
        <span class="sf-home-icon sf-icon-funnel-chart"></span>Funnel Charts
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/pyramid-charts/overview">
        <span class="sf-home-icon sf-icon-pyramid-chart"></span>Pyramid Charts
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/polar-charts/overview">
        <span class="sf-home-icon sf-icon-polar-chart"></span>Polar Charts
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/sunburstchart/overview">
        <span class="sf-home-icon sf-icon-sunburst-chart"></span>Sunburst Chart
    </a>
</div>
<div class="controlanchorlink">
    <a href="https://help.syncfusion.com/maui-toolkit/spark-charts/overview">
        <span class="sf-home-icon sf-icon-spark-chart"></span>Spark Chart
    </a>
</div>

</td>
</tr>
</table>

<br>


## Resources

<style>

@media(max-width:900px) {
   .form-card {
       flex: 0 0 calc(33.33% - 10px);
   }
}
@media(max-width:600px) {
   .form-card {
       flex: 0 0 100%;
   }
}
@font-face {
    font-family: 'Toolkit Icons';
    src: url('data:font/woff2;charset=utf-8;base64,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') format('woff2');
    font-weight: normal;
    font-style: normal;
    font-display: swap;
}

.card-icon {
  font-family: 'Toolkit Icons' !important;
  font-size: 20px;
  line-height: 1;
  display: inline-block;
  font-style: normal;
}

.card-ai:before { content: "\e720"; }
.card-arrow:before { content: "\e721"; }
.card-showcase:before { content: "\e722"; }
.card-blogs:before { content: "\e723"; }
.card-videos:before { content: "\e724"; }
.card-knowledge-base:before { content: "\e725"; }
.card-feedback:before { content: "\e726"; }
.card-support:before { content: "\e727"; }

.form-card {
  flex: 0 0 calc(33.33% - 14px);
  max-width: calc(33.33% - 14px);
  box-sizing: border-box;
  padding: 16px;
  border-radius: 16px;
  border: 1px solid #E6E6E6;
  display: flex;
  flex-direction: column;
  background: #ffffff;
  text-decoration: none;
  transition: all 0.25s ease;
  color: inherit;
}

.form-card:hover {
  transform: translateY(-3px);
  text-decoration: none;
  box-shadow: 0 10px 25px rgba(0,0,0,0.08);
}

.form-content {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.icon-circle {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: #EAF3FF;
  display: flex;
  flex-shrink: 0;
  align-items: center;
  justify-content: center;
}

.card-icon {
  font-family: 'Toolkit Icons' !important;
  font-size: 16px;
  line-height: 1;
  color: #0A76FF;
}

.form-title {
  font-size: 16px;
  font-weight: 500;
  margin: 0 !important;
  color: #2d2d2d;
}

.form-description {
  font-size: 14px;
  margin: 0;
  min-height: 60px;
  color: #50565F;
  line-height: 1.5;
}

.card-header {
  display: flex;
  align-items: center;
  gap: 12px;
}

.card-header .form-title {
  margin-top: 0 !important;
  line-height: 1.2;
}

.explore-link {
  margin-top: auto;
  color: #0A76FF;
  font-size: 12;
  font-weight: 400;
  display: flex;
  align-items: center;
  gap: 6px;
}

.explore-link .card-icon {
  font-size: 16px;
}

</style>


<div style="display:flex; flex-wrap:wrap; gap:20px; margin-top:20px;">
<!-- Card 1 -->
<div class="form-card" target="_blank">
  <div class="form-content">
<div class="card-header">
    <div class="icon-circle">
        <span class="card-icon card-ai"></span>
    </div>
    <h3 class="form-title">Feature Tour</h3>
</div>
<div class="form-description">Get a quick overview of key features and capabilities to kick start your journey.</div>
<a href="https://www.syncfusion.com/maui-controls" class="explore-link">
Explore Features
  <span class="card-icon card-arrow"></span>
</a>
  </div>
</div>
<!-- Card 2 -->
<div class="form-card" target="_blank">
  <div class="form-content">
  <div class="card-header">
    <div class="icon-circle">
    <span class="card-icon card-showcase"></span>
  </div>
    <h3 class="form-title">Showcase Samples</h3>
</div>
    <div class="form-description"> Explore real-world sample apps to see components in action and learn by example.</div>
    <a href="https://github.com/syncfusion/maui-toolkit" class="explore-link">
    View Samples
  <span class="card-icon card-arrow"></span>
</a>
  </div>
</div>
<!-- Card 3 -->
<div class="form-card" target="_blank">
  <div class="form-content">
  <div class="card-header">
    <div class="icon-circle">
    <span class="card-icon card-videos"></span>
    </div>
    <h3 class="form-title">Tutorial Videos</h3>
</div>
    <div class="form-description">
      Watch step‑by‑step video guides to quickly understand concepts and implementation.
    </div>
    <a href="https://www.syncfusion.com/tutorial-videos/maui/toolkit" class="explore-link">
    Watch now
  <span class="card-icon card-arrow"></span>
</a>
  </div>
</div>
<!-- Card 4 -->
<div class="form-card" target="_blank">
  <div class="form-content">
   <div class="card-header">
    <div class="icon-circle">
    <span class="card-icon card-knowledge-base"></span>
    </div>
    <h3 class="form-title">Explore KB's</h3>
</div>
    <div class="form-description">
       Find practical solutions, troubleshooting tips and how‑to guides for common scenarios.
    </div>
    <a href="https://support.syncfusion.com/kb/cross-platforms/section/2260" class="explore-link">
Search KB's
  <span class="card-icon card-arrow"></span>
</a>
  </div>
</div>
<!-- Card 5 -->
<div class="form-card" target="_blank">
  <div class="form-content">
   <div class="card-header">
    <div class="icon-circle">
    <span class="card-icon card-blogs"></span>
    </div>
    <h3 class="form-title">Explore Blogs</h3>
</div>
    <div class="form-description">
      Discover in‑depth articles, use cases and expert insights from our developers.
    </div>
    <a href="https://www.syncfusion.com/blogs/category/net-maui" class="explore-link">
Read Blogs
  <span class="card-icon card-arrow"></span>
</div>
  </div>
</div>

</div>


## Support

<div style="display:flex; flex-wrap:wrap; gap:20px; margin-top:10px;">
<div  class="form-card" target="_blank">
    <div class="form-content">
        <div class="card-header">
            <div class="icon-circle">
                <span class="card-icon card-support"></span>
            </div>
            <h3 class="form-title">Support Ticket</h3>
        </div>
        <div class="form-description">
            Need assistance? Submit a support ticket and our team will help you resolve your issue quickly.
        </div>
        <a href="https://mauitoolkit.syncfusion.com/support/tickets/create">Open ticket
            <span class="card-icon card-arrow"></span>
        </a>
    </div>
</div>