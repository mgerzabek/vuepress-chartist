<template>
  <script>
    const charts = document.getElementsByClassName('ct-chart');
    for (let chart of charts)
    {
      const json = JSON.parse(chart.nextSibling.innerText);
      new Chartist.Line(chart, json.data, json.option);
    }
  </script>
</template>
