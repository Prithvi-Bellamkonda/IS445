# IS445
<!DOCTYPE html>
<html>
<head>
  <script src="https://cdn.jsdelivr.net/npm/vega@5.25.0"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5.15.0"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6.22.2"></script>
</head>
<body>
  <div id="vis"/>
  <script>
    const spec = {
  "$schema": "https://vega.github.io/schema/vega-lite/v5.json",
  "data": {
    "url": "https://raw.githubusercontent.com/UIUC-iSchool-DataViz/fall2023-acg-acu/main/data/building_inventory.csv"
  },
  "mark": "bar",
  "encoding": {
    "y": {
      "aggregate": "count",
      "field": "Total Floors",
      "type": "quantitative"
    },
    "x": {"aggregate": "", "field": "Year Constructed", "type": "quantitative"}
  },
  "config": {}
};
    vegaEmbed("#vis", spec, {mode: "vega-lite"}).then(console.log).catch(console.warn);
  </script>
</body>
</html>
