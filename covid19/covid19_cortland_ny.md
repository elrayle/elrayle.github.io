<script>
  function showAuto() {
    var auto_width = document.getElementById("auto-width-display");
    var wide = document.getElementById("wide-display");
    var narrow = document.getElementById("narrow-display");
    auto_width.style.display = "block";
    wide.style.display = "none";
    narrow.style.display = "none";
  }

  function showWide() {
    var auto_width = document.getElementById("auto-width-display");
    var wide = document.getElementById("wide-display");
    var narrow = document.getElementById("narrow-display");
    auto_width.style.display = "none";
    wide.style.display = "block";
    narrow.style.display = "none";
  }

  function showNarrow() {
    var auto_width = document.getElementById("auto-width-display");
    var wide = document.getElementById("wide-display");
    var narrow = document.getElementById("narrow-display");
    auto_width.style.display = "none";
    wide.style.display = "none";
    narrow.style.display = "block";
  }
</script>

<div id="page-title">Coronavirus COVID-19 Confirmed Cases</div>
<div id="covid19-graph">
    <p class="last-updated">Last updated: March 29, 2020  7:50pm ET</p>
    <div id="graph-width-selector">
      Display: <span onclick="showAuto()">auto</span> | 
      <span onclick="showWide()">wide</span> | 
      <span onclick="showNarrow()">narrow</span> 
    </div>
    <div id="auto-width-display">
        <picture>
            <source srcset="graphs/2020-03-29_world-us-ny-cortland_confirmed_cases_graphs_narrow.png" media="(max-width: 1350px)" />
            <source srcset="graphs/2020-03-29_world-us-ny-cortland_confirmed_cases_graphs.png">
            <img src="graphs/2020-03-29_world-us-ny-cortland_confirmed_cases_graphs_narrow.png" alt="Graphs for World, US, NY, and Cortland County and surrounding counties" style="width:auto" />
        </picture>
    </div>
    <div id="wide-display">
        <img src="graphs/2020-03-29_world-us-ny-cortland_confirmed_cases_graphs.png" alt="Graphs for World, US, NY, and Cortland County and surrounding counties" />
    </div>
    <div id="narrow-display">
        <img src="graphs/2020-03-29_world-us-ny-cortland_confirmed_cases_graphs_narrow.png" alt="Graphs for World, US, NY, and Cortland County and surrounding counties" />
    </div>  
</div>

<div class="center-block">
  <div class="center-within-block">
    <div class="data-sources">
    <p>Links to data sources:</p>
    <ul>
      <li>New York county graph:
        <ul>
          <li>starting March 23: 
            <ul>
              <li>end of day data: <a href="https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports" target="_blank">Johns Hopkins CCSEGISandData</a></li>
              <li>during the day data: <a href="https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html?fbclid=IwAR10wt9a2d778FvxQ1MOg_qw5aL80ypVBRVkb-ouk233xEQxuXC6c9XHSGY#/bda7594740fd40299423467b48e9ecf6" target="_blank">Johns Hopkins map</a></li>
            </ul></li> 
          <li>March 17 - March 22: <a href="https://coronavirus.health.ny.gov/county-county-breakdown-positive-cases" target="_blank">New York County by County Breakdown of Positive Cases</a></li>
          <li>before March 17: <a href="https://www.nytimes.com/interactive/2020/world/coronavirus-maps.html#us" target="_blank">New York Times map</a> (rough estimate)</li>
        </ul></li> 
      <li>New York state graph:
        <ul>
          <li>starting March 23: 
            <ul>
              <li>end of day data: <a href="https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports" target="_blank">Johns Hopkins CCSEGISandData</a></li>
              <li>during the day data: <a href="https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html?fbclid=IwAR10wt9a2d778FvxQ1MOg_qw5aL80ypVBRVkb-ouk233xEQxuXC6c9XHSGY#/bda7594740fd40299423467b48e9ecf6" target="_blank">Johns Hopkins map</a></li>
            </ul></li> 
          <li>March 17 - March 22: <a href="https://coronavirus.health.ny.gov/county-county-breakdown-positive-cases" target="_blank">New York County by County Breakdown of Positive Cases</a></li>
          <li>before March 17: <a href="https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports" target="_blank">Johns Hopkins CCSEGISandData</a></li>
        </ul></li> 
      <li>World and US graphs: 
        <ul>
          <li>end of day data: <a href="https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports" target="_blank">Johns Hopkins CCSEGISandData</a></li>
          <li>during the day data: <a href="https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html?fbclid=IwAR10wt9a2d778FvxQ1MOg_qw5aL80ypVBRVkb-ouk233xEQxuXC6c9XHSGY#/bda7594740fd40299423467b48e9ecf6" target="_blank">Johns Hopkins map</a></li>
        </ul></li> 
      <li><a href="https://github.com/elrayle/elrayle.github.io/blob/master/covid19/data" target="_blank">Consolidated data</a> from these sources driving the graphs on this site</li>
    </ul>
    <p>Counties considered to be surrounding counties for Cortland County, NY:</p>
    <ul>
      <li>Tompkins</li>
      <li>Cayuga</li>
      <li>Onondaga</li>
      <li>Madison</li>
      <li>Chenango</li>
      <li>Broome</li>
      <li>Tioga</li>
    </ul>
    </div>
  </div>
</div>
