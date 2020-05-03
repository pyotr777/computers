---
id: 378
title: 'Cloud GPU  providers comparison'
date: 2016-11-21T17:11:47+09:00
author: Peter Bryzgalov
layout: post
# guid: http://comp.photo777.org/?p=378
permalink: /cloud-gpu-providers-comparison/
image: /wp-content/uploads/2017/04/stair_eyecatch-1-672x280.png
include_blocks:
  - cloud_gpus
  - cloud_gpus1
categories:
  - Cloud GPU providers
tags:
  - Amazon
  - AMD
  - AWS
  - Cirrascale
  - cloud
  - cloud computing
  - cloud GPU
  - cloud GPU providers
  - cloud providers comparison
  - compare cloud GPUs
  - compare cloud providers
  - compare costs
  - compare price
  - deep neural networks
  - EC2
  - Intel Xeon
  - LeaderTelecom
  - machine learning
  - Nvidia
  - Sakura internet
  - Softlayer
---

There are plenty of cloud GPU offers from many providers. This post is here to help you to compare offers in terms of cost<sup><a href="#notes">*</a></sup>, GPU and CPU performance<sup><a href="#notes">**</a></sup>, memory etc. It has some interactive graphs for comparing offers and a table with details for each offer.

Please find my article on our <a href="https://stair.center/archives/439" target="_blank">STAIR laboratory web site</a> about why I created these graphs and how to use them.

The &#8220;filter&#8221; charts below provide statistical information about offers distribution by some parameters, such as how many offers each provider has. These charts can also be used for filtering offers. Click on a value in any chart to filter out offers with different values. You can select multiple values on one or multiple charts. All graphs and the table below will show data only for the selected offers.

Please note, that only offers with GPU are mentioned on this page. Some providers, like Google and Amazon, have too many offers to show them all here, so I picked up only some representative ones.

<p class="note" id="updated">
  <p>
    <!--more-->
  </p>

  <div class="grouptitle">
    <h3>
      Filter offers in all graphs below using these charts
    </h3>

    <div style="float:none;">
    </div>

    <div id="dc_gpu_models">
      <title>
        Number of offers by GPU model
      </title>
    </div>

    <div class="dc_group">
      <div id="dc_gpus">
        <title>
          Number of GPUs
        </title>
      </div>

      <div id="dc_gpu_perf">
        <title>
          Total GPU performance (TFlops)
        </title>
      </div>
    </div>

    <div class="dc_group">
      <div id="dc_memory">
        <title>
          Memory (GB)
        </title>
      </div>

      <div id="dc_cpu_perf">
        <title>
          Total CPU performance (TFlops)
        </title>
      </div>
    </div>

    <div id="dc_providers">
      <title>
        Number of offers by Providers
      </title>
    </div>

    <div id="dc_end">
    </div>
  </div>

  <div id="messages">
  </div>

  <p>
    The graph below shows theoretical peak CPU and GPU performance<sup><a href="#notes">**</a></sup> in <span title="Floating Point Operations per Second * 10e+12">TFlops</span> for each offer. Hover over offers to display information below the graph. More detailed information can be found in the table at the bottom of the page. Drag across the chart to zoom in. Click on the legend to filter out offers by provider.
  </p>

  <div id="scatter_performance" style="width: 100%; height: 500px;">
  </div>

  <div id="offer_details1" class="note">
    &nbsp;
  </div>

  <p>
    The below graph shows rent cost for a period. X-axis is rent period, Y-axis is rent cost.
  </p>

  <p>
    All offers are charged in time units: minutes, hours, weeks, months or years. That is why some lines on the graph has steps. Only lines for minutely and hourly charged offers are straight. Actually, they should be stepped also, but the graph X-axis resolution is lower (several hours) so these lines look straight on the graph.
  </p>

  <p>
    Click on the graph to select rent period. All graphs below will change to display data for the selected period. You can also set the period with the buttons below. Drag across the graph to zoom in. Click on the legend to filter offers by provider.
  </p>

  <div id="costs_period" style="width: 100%; height: 550px;">
  </div>

  <div id="offer_details2" class="note">
    &nbsp;
  </div>

  <div class="grouptitle">
    <h3>
      Set rent period for below graphs
    </h3>

    <div class="buttons">
      <div class="button" id="day" onclick="displayTime('1 day');">
        1 day
      </div>

      <div class="button" id="week" onclick="displayTime('7 days');">
        1 week
      </div>

      <div class="button" id="month" onclick="displayTime('1 month');">
        1 month
      </div>

      <div class="button" id="3months" onclick="displayTime('3 month');">
        3 month
      </div>

      <div class="button" id="6months" onclick="displayTime('6 months');">
        6 months
      </div>

      <div class="button" id="9months" onclick="displayTime('9 month');">
        9 month
      </div>

      <div class="button" id="12months" onclick="displayTime('1 year');">
        1 year
      </div>
    </div>

    <p>
      The below graph shows total costs if rented for given period.
    </p>

    <div id="slice_cost" style="width: 100%; height: 500px;">
    </div>

    <div id="offer_details3" class="note">
      &nbsp;
    </div>

    <p id="slice_cost_monthly_text">
      The below graph shows per month costs if rented for <span id="r_period"></span>.
    </p>

    <div id="slice_cost_monthly" style="width: 100%; height: 0px;">
    </div>

    <p>
      The below graph shows cost per 1 <span title="Floating Point Operations per Second * 10e+12">TFlops</span> of GPU and CPU performance for the selected rent period in logarithmic scale. To change rent period use the buttons above or click on the &#8220;Cost for rent period&#8221; graph.
    </p>

    <div id="slice_cost_perf" style="width: 100%; height: 500px;">
    </div>

    <div id="offer_details4" class="note">
      &nbsp;
    </div>
  </div>

  <p>
  </p>

  <h1 class="tableTitle">
    Detailed information for selected offers
  </h1>

  <div id="table_div">
  </div>

  <div class="note">
    <p>
      Links:
    </p>

    <p>
      <a href="https://en.wikipedia.org/wiki/List_of_Nvidia_graphics_processing_units" target="_blank">wikipedia.org/wiki/List_of_Nvidia_graphics_processing_units</a><br /> <a href="https://www-01.ibm.com/common/ssi/cgi-bin/ssialias?htmlfid=POD03117USEN" target="_blank">IBM Power System S822LC for HPC</a>
    </p>
  </div>

  <div class="note" id="notes">
    Notes:

    <p>
      * All prices <b>do not include taxes</b>. All sums are in <b>USD</b>. Offers based on other currencies are converted using today&#8217;s rates from
      <a href="http://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html" target="_blank">European Central Bank</a>:
    </p>

    <div id="rates" class="notes_cell">
    </div>

    <p>
      ** Performance data shows single precision <span title="Floating Point Operations per Second">Flops</span> for GPUs and single precision <span title="Floating Point Operations per Second">Flops</span> for CPUs. <b>Beware that performance data are theoretical peak values, and actual performance will be lower and may vary greatly between applications.</b>
    </p>
  </div>

  <p>
    <a href="{{ '/cloud-gpu-providers-more-graphs/' | relative_url }}">Even more graphs: compare calculation time and cost for a fixed amount of calculations.</a>
  </p>