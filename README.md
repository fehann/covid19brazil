# Visualização de dados relacionados ao COVID-19 no Brasil
Visando entender o comportamento da evolução da COVID-19 no Brasil, esta página apresenta o ritmo de aceleração ou desaceleração da doença por estado brasileiro. A inspiração para criação desta visualização veio a partir do gráfico publicado pela organização <a target="_blank" rel="noopener noreferrer" href="https://ourworldindata.org/grapher/covid-confirmed-deaths-since-5th-death">Our World in Data</a> que tem como objetivo apresentar não somente o número de casos mas também o ritmo no qual as morte estão ocorrendo.

## Sobre os dados 
É importante salientar que esta visualização se baseia em dados disponibilizados pelas secretarias estaduais, coletados de forma manual uma vez que não há um banco de dados integrados, conforme site <a target="_blank" rel="noopener noreferrer" href="https://brasil.io/dataset/covid19/caso">Brasil.io</a>. São dados passível de erros e vieses portanto qualquer análise não deve ser baseada somente nestes dados e toda tomada de decisões deve considerar uma análise científica com informações complementares.

## Número de mortes por estado brasileiro a partir da 5a morte notificada

<div id="vis"></div>
<script>
(function(vegaEmbed) {
var spec = {"config": {"view": {"continuousWidth": 400, "continuousHeight": 300}}, "layer": [{"mark": {"type": "line", "opacity": 0.7, "strokeWidth": 4}, "encoding": {"color": {"condition": {"type": "nominal", "field": "state", "selection": "selector001"}, "value": "lightgray"}, "tooltip": [{"type": "nominal", "field": "state"}, {"type": "nominal", "field": "Date", "timeUnit": "yearmonthdate"}, {"type": "nominal", "field": "Deaths"}], "x": {"type": "quantitative", "field": "Day"}, "y": {"type": "quantitative", "field": "Deaths", "scale": {"type": "log"}}}, "height": 650, "selection": {"selector001": {"type": "single", "fields": ["state"]}}, "title": "Total de mortes confirmadas pelo COVID-19 por estado brasileiros", "width": 800}, {"mark": {"type": "line", "opacity": 0.7, "strokeWidth": 4}, "encoding": {"color": {"type": "nominal", "field": "state"}, "opacity": {"value": 0.5}, "x": {"type": "quantitative", "field": "Day"}, "y": {"type": "quantitative", "field": "Deaths", "scale": {"type": "log"}}}, "height": 650, "title": "Total de mortes confirmadas pelo COVID-19 por estado brasileiros", "transform": [{"filter": {"selection": "selector001"}}], "width": 800}, {"mark": {"type": "text", "align": "left", "dx": 5, "size": 10}, "encoding": {"color": {"type": "nominal", "field": "state", "legend": null}, "text": {"type": "nominal", "field": "state"}, "x": {"type": "quantitative", "aggregate": "max", "axis": {"title": "Dias a partir da 5a morte no estado"}, "field": "Day"}, "y": {"type": "quantitative", "aggregate": {"argmax": "Day"}, "axis": {"title": "Mortes confirmadas (escala logar\u00edtmica)"}, "field": "Deaths"}}, "height": 650, "title": "Total de mortes confirmadas pelo COVID-19 por estado brasileiros", "transform": [{"filter": {"selection": "selector001"}}], "width": 800}], "data": {"name": "data-a67d6f0f4c588450ec21228ccb226684"}, "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json", "datasets": {"data-a67d6f0f4c588450ec21228ccb226684": [{"Day": 0, "state": "AM", "Deaths": 7.0, "Date": "2020-04-03T00:00:00"}, {"Day": 1, "state": "AM", "Deaths": 12.0, "Date": "2020-04-04T00:00:00"}, {"Day": 2, "state": "AM", "Deaths": 15.0, "Date": "2020-04-05T00:00:00"}, {"Day": 3, "state": "AM", "Deaths": 19.0, "Date": "2020-04-06T00:00:00"}, {"Day": 4, "state": "AM", "Deaths": 23.0, "Date": "2020-04-07T00:00:00"}, {"Day": 5, "state": "AM", "Deaths": 30.0, "Date": "2020-04-08T00:00:00"}, {"Day": 6, "state": "AM", "Deaths": 40.0, "Date": "2020-04-09T00:00:00"}, {"Day": 7, "state": "AM", "Deaths": 50.0, "Date": "2020-04-10T00:00:00"}, {"Day": 8, "state": "AM", "Deaths": 53.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "AP", "Deaths": 5.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "BA", "Deaths": 6.0, "Date": "2020-04-03T00:00:00"}, {"Day": 1, "state": "BA", "Deaths": 7.0, "Date": "2020-04-04T00:00:00"}, {"Day": 2, "state": "BA", "Deaths": 9.0, "Date": "2020-04-05T00:00:00"}, {"Day": 3, "state": "BA", "Deaths": 10.0, "Date": "2020-04-06T00:00:00"}, {"Day": 4, "state": "BA", "Deaths": 14.0, "Date": "2020-04-07T00:00:00"}, {"Day": 5, "state": "BA", "Deaths": 18.0, "Date": "2020-04-08T00:00:00"}, {"Day": 6, "state": "BA", "Deaths": 19.0, "Date": "2020-04-09T00:00:00"}, {"Day": 7, "state": "BA", "Deaths": 19.0, "Date": "2020-04-10T00:00:00"}, {"Day": 8, "state": "BA", "Deaths": 21.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "CE", "Deaths": 5.0, "Date": "2020-03-29T00:00:00"}, {"Day": 1, "state": "CE", "Deaths": 5.0, "Date": "2020-03-30T00:00:00"}, {"Day": 2, "state": "CE", "Deaths": 7.0, "Date": "2020-03-31T00:00:00"}, {"Day": 3, "state": "CE", "Deaths": 9.0, "Date": "2020-04-01T00:00:00"}, {"Day": 4, "state": "CE", "Deaths": 21.0, "Date": "2020-04-02T00:00:00"}, {"Day": 5, "state": "CE", "Deaths": 22.0, "Date": "2020-04-03T00:00:00"}, {"Day": 6, "state": "CE", "Deaths": 23.0, "Date": "2020-04-04T00:00:00"}, {"Day": 7, "state": "CE", "Deaths": 35.0, "Date": "2020-04-05T00:00:00"}, {"Day": 8, "state": "CE", "Deaths": 35.0, "Date": "2020-04-06T00:00:00"}, {"Day": 9, "state": "CE", "Deaths": 40.0, "Date": "2020-04-07T00:00:00"}, {"Day": 10, "state": "CE", "Deaths": 57.0, "Date": "2020-04-08T00:00:00"}, {"Day": 11, "state": "CE", "Deaths": 57.0, "Date": "2020-04-09T00:00:00"}, {"Day": 12, "state": "CE", "Deaths": 67.0, "Date": "2020-04-10T00:00:00"}, {"Day": 13, "state": "CE", "Deaths": 74.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "DF", "Deaths": 5.0, "Date": "2020-04-02T00:00:00"}, {"Day": 1, "state": "DF", "Deaths": 6.0, "Date": "2020-04-03T00:00:00"}, {"Day": 2, "state": "DF", "Deaths": 7.0, "Date": "2020-04-04T00:00:00"}, {"Day": 3, "state": "DF", "Deaths": 7.0, "Date": "2020-04-05T00:00:00"}, {"Day": 4, "state": "DF", "Deaths": 10.0, "Date": "2020-04-06T00:00:00"}, {"Day": 5, "state": "DF", "Deaths": 12.0, "Date": "2020-04-07T00:00:00"}, {"Day": 6, "state": "DF", "Deaths": 12.0, "Date": "2020-04-08T00:00:00"}, {"Day": 7, "state": "DF", "Deaths": 13.0, "Date": "2020-04-09T00:00:00"}, {"Day": 8, "state": "DF", "Deaths": 14.0, "Date": "2020-04-10T00:00:00"}, {"Day": 9, "state": "DF", "Deaths": 14.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "ES", "Deaths": 5.0, "Date": "2020-04-03T00:00:00"}, {"Day": 1, "state": "ES", "Deaths": 6.0, "Date": "2020-04-04T00:00:00"}, {"Day": 2, "state": "ES", "Deaths": 6.0, "Date": "2020-04-05T00:00:00"}, {"Day": 3, "state": "ES", "Deaths": 6.0, "Date": "2020-04-06T00:00:00"}, {"Day": 4, "state": "ES", "Deaths": 6.0, "Date": "2020-04-07T00:00:00"}, {"Day": 5, "state": "ES", "Deaths": 6.0, "Date": "2020-04-08T00:00:00"}, {"Day": 6, "state": "ES", "Deaths": 7.0, "Date": "2020-04-09T00:00:00"}, {"Day": 7, "state": "ES", "Deaths": 8.0, "Date": "2020-04-10T00:00:00"}, {"Day": 8, "state": "ES", "Deaths": 9.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "GO", "Deaths": 5.0, "Date": "2020-04-06T00:00:00"}, {"Day": 1, "state": "GO", "Deaths": 5.0, "Date": "2020-04-07T00:00:00"}, {"Day": 2, "state": "GO", "Deaths": 7.0, "Date": "2020-04-08T00:00:00"}, {"Day": 3, "state": "GO", "Deaths": 7.0, "Date": "2020-04-09T00:00:00"}, {"Day": 4, "state": "GO", "Deaths": 8.0, "Date": "2020-04-10T00:00:00"}, {"Day": 5, "state": "GO", "Deaths": 10.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "MA", "Deaths": 11.0, "Date": "2020-04-07T00:00:00"}, {"Day": 1, "state": "MA", "Deaths": 12.0, "Date": "2020-04-08T00:00:00"}, {"Day": 2, "state": "MA", "Deaths": 16.0, "Date": "2020-04-09T00:00:00"}, {"Day": 3, "state": "MA", "Deaths": 21.0, "Date": "2020-04-10T00:00:00"}, {"Day": 4, "state": "MA", "Deaths": 24.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "MG", "Deaths": 6.0, "Date": "2020-04-03T00:00:00"}, {"Day": 1, "state": "MG", "Deaths": 6.0, "Date": "2020-04-04T00:00:00"}, {"Day": 2, "state": "MG", "Deaths": 6.0, "Date": "2020-04-05T00:00:00"}, {"Day": 3, "state": "MG", "Deaths": 9.0, "Date": "2020-04-06T00:00:00"}, {"Day": 4, "state": "MG", "Deaths": 11.0, "Date": "2020-04-07T00:00:00"}, {"Day": 5, "state": "MG", "Deaths": 14.0, "Date": "2020-04-08T00:00:00"}, {"Day": 6, "state": "MG", "Deaths": 15.0, "Date": "2020-04-09T00:00:00"}, {"Day": 7, "state": "MG", "Deaths": 17.0, "Date": "2020-04-10T00:00:00"}, {"Day": 8, "state": "MG", "Deaths": 17.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "PA", "Deaths": 5.0, "Date": "2020-04-06T00:00:00"}, {"Day": 1, "state": "PA", "Deaths": 5.0, "Date": "2020-04-07T00:00:00"}, {"Day": 2, "state": "PA", "Deaths": 6.0, "Date": "2020-04-08T00:00:00"}, {"Day": 3, "state": "PA", "Deaths": 7.0, "Date": "2020-04-09T00:00:00"}, {"Day": 4, "state": "PA", "Deaths": 9.0, "Date": "2020-04-10T00:00:00"}, {"Day": 5, "state": "PA", "Deaths": 11.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "PB", "Deaths": 7.0, "Date": "2020-04-08T00:00:00"}, {"Day": 1, "state": "PB", "Deaths": 11.0, "Date": "2020-04-09T00:00:00"}, {"Day": 2, "state": "PB", "Deaths": 11.0, "Date": "2020-04-10T00:00:00"}, {"Day": 3, "state": "PB", "Deaths": 13.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "PE", "Deaths": 5.0, "Date": "2020-03-28T00:00:00"}, {"Day": 1, "state": "PE", "Deaths": 5.0, "Date": "2020-03-29T00:00:00"}, {"Day": 2, "state": "PE", "Deaths": 6.0, "Date": "2020-03-30T00:00:00"}, {"Day": 3, "state": "PE", "Deaths": 6.0, "Date": "2020-03-31T00:00:00"}, {"Day": 4, "state": "PE", "Deaths": 8.0, "Date": "2020-04-01T00:00:00"}, {"Day": 5, "state": "PE", "Deaths": 9.0, "Date": "2020-04-02T00:00:00"}, {"Day": 6, "state": "PE", "Deaths": 10.0, "Date": "2020-04-03T00:00:00"}, {"Day": 7, "state": "PE", "Deaths": 14.0, "Date": "2020-04-04T00:00:00"}, {"Day": 8, "state": "PE", "Deaths": 21.0, "Date": "2020-04-05T00:00:00"}, {"Day": 9, "state": "PE", "Deaths": 30.0, "Date": "2020-04-06T00:00:00"}, {"Day": 10, "state": "PE", "Deaths": 34.0, "Date": "2020-04-07T00:00:00"}, {"Day": 11, "state": "PE", "Deaths": 46.0, "Date": "2020-04-08T00:00:00"}, {"Day": 12, "state": "PE", "Deaths": 56.0, "Date": "2020-04-09T00:00:00"}, {"Day": 13, "state": "PE", "Deaths": 65.0, "Date": "2020-04-10T00:00:00"}, {"Day": 14, "state": "PE", "Deaths": 72.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "PI", "Deaths": 5.0, "Date": "2020-04-07T00:00:00"}, {"Day": 1, "state": "PI", "Deaths": 6.0, "Date": "2020-04-08T00:00:00"}, {"Day": 2, "state": "PI", "Deaths": 7.0, "Date": "2020-04-09T00:00:00"}, {"Day": 3, "state": "PI", "Deaths": 7.0, "Date": "2020-04-10T00:00:00"}, {"Day": 4, "state": "PI", "Deaths": 7.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "PR", "Deaths": 5.0, "Date": "2020-04-03T00:00:00"}, {"Day": 1, "state": "PR", "Deaths": 7.0, "Date": "2020-04-04T00:00:00"}, {"Day": 2, "state": "PR", "Deaths": 10.0, "Date": "2020-04-05T00:00:00"}, {"Day": 3, "state": "PR", "Deaths": 14.0, "Date": "2020-04-06T00:00:00"}, {"Day": 4, "state": "PR", "Deaths": 15.0, "Date": "2020-04-07T00:00:00"}, {"Day": 5, "state": "PR", "Deaths": 17.0, "Date": "2020-04-08T00:00:00"}, {"Day": 6, "state": "PR", "Deaths": 24.0, "Date": "2020-04-09T00:00:00"}, {"Day": 7, "state": "PR", "Deaths": 26.0, "Date": "2020-04-10T00:00:00"}, {"Day": 8, "state": "PR", "Deaths": 27.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "RJ", "Deaths": 6.0, "Date": "2020-03-24T00:00:00"}, {"Day": 1, "state": "RJ", "Deaths": 8.0, "Date": "2020-03-25T00:00:00"}, {"Day": 2, "state": "RJ", "Deaths": 9.0, "Date": "2020-03-26T00:00:00"}, {"Day": 3, "state": "RJ", "Deaths": 10.0, "Date": "2020-03-27T00:00:00"}, {"Day": 4, "state": "RJ", "Deaths": 13.0, "Date": "2020-03-28T00:00:00"}, {"Day": 5, "state": "RJ", "Deaths": 17.0, "Date": "2020-03-29T00:00:00"}, {"Day": 6, "state": "RJ", "Deaths": 18.0, "Date": "2020-03-30T00:00:00"}, {"Day": 7, "state": "RJ", "Deaths": 23.0, "Date": "2020-03-31T00:00:00"}, {"Day": 8, "state": "RJ", "Deaths": 28.0, "Date": "2020-04-01T00:00:00"}, {"Day": 9, "state": "RJ", "Deaths": 41.0, "Date": "2020-04-02T00:00:00"}, {"Day": 10, "state": "RJ", "Deaths": 47.0, "Date": "2020-04-03T00:00:00"}, {"Day": 11, "state": "RJ", "Deaths": 58.0, "Date": "2020-04-04T00:00:00"}, {"Day": 12, "state": "RJ", "Deaths": 64.0, "Date": "2020-04-05T00:00:00"}, {"Day": 13, "state": "RJ", "Deaths": 71.0, "Date": "2020-04-06T00:00:00"}, {"Day": 14, "state": "RJ", "Deaths": 89.0, "Date": "2020-04-07T00:00:00"}, {"Day": 15, "state": "RJ", "Deaths": 106.0, "Date": "2020-04-08T00:00:00"}, {"Day": 16, "state": "RJ", "Deaths": 122.0, "Date": "2020-04-09T00:00:00"}, {"Day": 17, "state": "RJ", "Deaths": 147.0, "Date": "2020-04-10T00:00:00"}, {"Day": 18, "state": "RJ", "Deaths": 155.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "RN", "Deaths": 6.0, "Date": "2020-04-04T00:00:00"}, {"Day": 1, "state": "RN", "Deaths": 7.0, "Date": "2020-04-05T00:00:00"}, {"Day": 2, "state": "RN", "Deaths": 7.0, "Date": "2020-04-06T00:00:00"}, {"Day": 3, "state": "RN", "Deaths": 8.0, "Date": "2020-04-07T00:00:00"}, {"Day": 4, "state": "RN", "Deaths": 11.0, "Date": "2020-04-08T00:00:00"}, {"Day": 5, "state": "RN", "Deaths": 11.0, "Date": "2020-04-09T00:00:00"}, {"Day": 6, "state": "RN", "Deaths": 11.0, "Date": "2020-04-10T00:00:00"}, {"Day": 7, "state": "RN", "Deaths": 13.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "RS", "Deaths": 5.0, "Date": "2020-04-01T00:00:00"}, {"Day": 1, "state": "RS", "Deaths": 5.0, "Date": "2020-04-02T00:00:00"}, {"Day": 2, "state": "RS", "Deaths": 6.0, "Date": "2020-04-03T00:00:00"}, {"Day": 3, "state": "RS", "Deaths": 7.0, "Date": "2020-04-04T00:00:00"}, {"Day": 4, "state": "RS", "Deaths": 7.0, "Date": "2020-04-05T00:00:00"}, {"Day": 5, "state": "RS", "Deaths": 8.0, "Date": "2020-04-06T00:00:00"}, {"Day": 6, "state": "RS", "Deaths": 8.0, "Date": "2020-04-07T00:00:00"}, {"Day": 7, "state": "RS", "Deaths": 10.0, "Date": "2020-04-08T00:00:00"}, {"Day": 8, "state": "RS", "Deaths": 14.0, "Date": "2020-04-09T00:00:00"}, {"Day": 9, "state": "RS", "Deaths": 15.0, "Date": "2020-04-10T00:00:00"}, {"Day": 10, "state": "RS", "Deaths": 16.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "SC", "Deaths": 5.0, "Date": "2020-04-02T00:00:00"}, {"Day": 1, "state": "SC", "Deaths": 5.0, "Date": "2020-04-03T00:00:00"}, {"Day": 2, "state": "SC", "Deaths": 10.0, "Date": "2020-04-04T00:00:00"}, {"Day": 3, "state": "SC", "Deaths": 10.0, "Date": "2020-04-05T00:00:00"}, {"Day": 4, "state": "SC", "Deaths": 11.0, "Date": "2020-04-06T00:00:00"}, {"Day": 5, "state": "SC", "Deaths": 15.0, "Date": "2020-04-07T00:00:00"}, {"Day": 6, "state": "SC", "Deaths": 17.0, "Date": "2020-04-08T00:00:00"}, {"Day": 7, "state": "SC", "Deaths": 18.0, "Date": "2020-04-09T00:00:00"}, {"Day": 8, "state": "SC", "Deaths": 18.0, "Date": "2020-04-10T00:00:00"}, {"Day": 9, "state": "SC", "Deaths": 21.0, "Date": "2020-04-11T00:00:00"}, {"Day": 0, "state": "SP", "Deaths": 5.0, "Date": "2020-03-19T00:00:00"}, {"Day": 1, "state": "SP", "Deaths": 9.0, "Date": "2020-03-20T00:00:00"}, {"Day": 2, "state": "SP", "Deaths": 15.0, "Date": "2020-03-21T00:00:00"}, {"Day": 3, "state": "SP", "Deaths": 22.0, "Date": "2020-03-22T00:00:00"}, {"Day": 4, "state": "SP", "Deaths": 30.0, "Date": "2020-03-23T00:00:00"}, {"Day": 5, "state": "SP", "Deaths": 40.0, "Date": "2020-03-24T00:00:00"}, {"Day": 6, "state": "SP", "Deaths": 48.0, "Date": "2020-03-25T00:00:00"}, {"Day": 7, "state": "SP", "Deaths": 58.0, "Date": "2020-03-26T00:00:00"}, {"Day": 8, "state": "SP", "Deaths": 68.0, "Date": "2020-03-27T00:00:00"}, {"Day": 9, "state": "SP", "Deaths": 84.0, "Date": "2020-03-28T00:00:00"}, {"Day": 10, "state": "SP", "Deaths": 98.0, "Date": "2020-03-29T00:00:00"}, {"Day": 11, "state": "SP", "Deaths": 113.0, "Date": "2020-03-30T00:00:00"}, {"Day": 12, "state": "SP", "Deaths": 136.0, "Date": "2020-03-31T00:00:00"}, {"Day": 13, "state": "SP", "Deaths": 164.0, "Date": "2020-04-01T00:00:00"}, {"Day": 14, "state": "SP", "Deaths": 188.0, "Date": "2020-04-02T00:00:00"}, {"Day": 15, "state": "SP", "Deaths": 219.0, "Date": "2020-04-03T00:00:00"}, {"Day": 16, "state": "SP", "Deaths": 260.0, "Date": "2020-04-04T00:00:00"}, {"Day": 17, "state": "SP", "Deaths": 275.0, "Date": "2020-04-05T00:00:00"}, {"Day": 18, "state": "SP", "Deaths": 304.0, "Date": "2020-04-06T00:00:00"}, {"Day": 19, "state": "SP", "Deaths": 371.0, "Date": "2020-04-07T00:00:00"}, {"Day": 20, "state": "SP", "Deaths": 428.0, "Date": "2020-04-08T00:00:00"}, {"Day": 21, "state": "SP", "Deaths": 496.0, "Date": "2020-04-09T00:00:00"}, {"Day": 22, "state": "SP", "Deaths": 540.0, "Date": "2020-04-10T00:00:00"}, {"Day": 23, "state": "SP", "Deaths": 560.0, "Date": "2020-04-11T00:00:00"}]}};
var embedOpt = {"mode": "vega-lite"};

function showError(el, error){
el.innerHTML = ('<div class="error" style="color:red;">'
+ '<p>JavaScript Error: ' + error.message + '</p>'
+ "<p>This usually means there's a typo in your chart specification. "
+ "See the javascript console for the full traceback.</p>"
+ '</div>');
throw error;
}
const el = document.getElementById('vis');
vegaEmbed("#vis", spec, embedOpt)
.catch(error => showError(el, error));
})(vegaEmbed);
</script>



<a target="_blank" rel="noopener noreferrer" href="https://vega.github.io/editor/#/url/vega-lite/N4KABGBEDGD2B2AzAlgc0gLjMSA3ZApgO6bYwIAuy8ArrDQM4DqyAJhQBakAsADLwBooceFVr0GACQJoOFUgGZ+AX2UDwUADYBDAJ4EATqQDaGiKAiWoAW20GA1qRwVdABwKlIm6h6GRYrtrQyC6kvAB0AOx+DBQGsPYELOxcWNxqZpaQBPBwrNToWBZWWXCasEZFmSXCCPlUCE7VNVAu7p7wsNbU2pqQ6i0lkCgEmqyesdoUvs01kAyjBNAN8BOLyxX8AGyQs5YZgxB4vTQeWF6yFKgGeruDBy2QFLCwmlSuJnvmT25nUJ3deC9fpQEZjCYUKYeB6DZy-DpdHp9Pxg8bnAAiUJBT2Q1gIAFV4CFPPo7NZKBxWFiYS04e1zgCkdjUZ50QQphwGJBlHsALoDR4ADycP3pUAAjjRtKIQlNkLhfKDCOCMbcaVZILomodWvDzpLpVRIVQFf0vkrRmioGyOVyBYN5tBen86X8vLB0Dz7s11VAODJUHJSFsAKyCZrzdYrEULTRLZ4GbYitpuhgFOPM5WsLlYYzzY0eXmqe1ZI0Z84AFVgkM0YFYBDA5IM0wYYBEKAMtiprfc5TAAGEAPIANQAkuiALQARgAnGBXBUwARJqxYGAAEY3NNx5DxO0RohsTikAAc-EyNOKGtsDmTeq0PmxASCIS1WAi0SgsXiiWSx7SvrZLksD5PAhTYHs5DlJUZApgigLAiiWYQtSJYas+wShEUxyaKcYThCGvpHMK2FwfqUoysa8qKsMyGqlqRFQG+EE6qKboGpRcqmmhQwshi7KcPurEME65awfe7qensXolIB-qXMGYY8TiFBiZAVY1nWDZNi2bYIB2XbaD2oxrkOY6TrO86LsukKrhuW7IDue5mnMcTSgwiAVNYJg4CgbyGDGUbII05yxvGmy8Dsqj8geR6pGAZ68BeJZXlkN6OKREnTIK8h+L0aCrOccaILlUCsCRYAhjEyAAF5-FOvCATkeQFNqjxlBUd5ipAjJAsiFoql+BbYnGqA5FatCaJojFPAQOVdW6vWIQNVr5qhkEValrkSRxRpcTMrHaKg1wEKgWLnLYwo8Rq2iCsgOawSEanosgRlgNo852FQBh1h9IYfTpDadEuK6wNy11ZHx1q3NJEOam1DpkRKFF7SaB2HJAR0nWd0winYqCXayaoQ0ct33cmT1ugAshUuntruhmtgAFMuokfeUZ0GAAtxQ3ROgAlOD5q0ZarICZydwtDJVhyQGQZYKG4auZTngab0WmNrTy56UgDPaN284mQOI7jtOc4Lj9Nn62um5GY5MjOcpbnwB5Xk+bR-kwTgYXLMFhVflGEVRcoMVzIeKSnueMsaKHZVTNoIpAninhUpCE7QOurAnls3CIDOrDQIgCgEAATAorBbIgvCsEorDcOuCjQEsJdTiGQtHAAJCJ-q2J4cgUK4DAYAA9MPCpneEqAhBwNDruEwXD93BC2GPp3aBO3jTGP3DhCe4RTuEABWDCNAKkCp0ZBAUA9qXn-H6eZ9nuf54XxdlxXVc19X9eN83refDUHAmJmKCCGudKAABBKm2IbSCVIJ+SAmJcbnBLrwVBE5eDcAwQoCs-AMB4P4O3EoQDbhYCnDEYa5woEwPFg9KcJc-BILdKg9BmCMHcFwbwfBXDCG+hIcxBhYDkGQOgYw2hpBW6MPAZAFhvB2EYJDJw7h3CiFWH4YoCh0jqFiNtBImcUjhEyLQXIthkUlEEN4Koyw6i0iaMMdo604isBlwMcw4x8jeCRHMTwyxfDEGkMqnYt0DjEFOLAEoVxnhZEeJPN4lRfjgHBiCZ4EJsCJZpFAf4wx0TTEzjibwniNiwAIMmPY0RjjdFYCUtDbJ7i2ENXyb4wp-iQHJPOAAIQgTQypYAtiRJQXUrBvAcEWPic0xJZC2lQE6d0uBWAEFMKiYM9hjSrHfAmWAQRa1DEzJ0XMsA+ialuNYUMxRoyCnNCKQoKZkBdkVP2Q1fpUAclDK2KshJATuA3LuaEnpU4vlHKWScjBXjzlNMuS00gVUhFuh+WkuhJ4nlGOBbwWJYK1lkA2X0mFng4VhNnEil5GC8noo+cxEplDpldL2eksABLAUDOBQ00l4yAmZNKW6fsABRWZtLoVZOOSYhQE4S4kp8WMiFGzyE4vONy3lD1+WLMZUKicSh3msoETcuVNKHoLOkTk4VCgpzqslQE65MqoDavubSw5AqgUmKGcallprmIAu2ZynlOrSAt0JcstBJrAGQqqVqz11qHoly2Uq55fqRniouYGrFIb5XevNXa5VHiOHOoTQEil0irW-P2QoRV+q-VnLjeC7NzFEUWsgPm+Fihi21JRW8rNxCg0HKTV6jJvqUWgvLRiopjya11rCSGPVTaHUYLRf2slEjpXus8COnpY6e2Tt4GK5R8a21Sq2RyxdoaC20q2OOwV8jmUzo1WEG56IABiybg0MujSikuAbt0BPnXujEd6u29NXR42Nm6K1vs1TW2997il-tMZmi9LqNGge-WG+BkHTmvrUe2t1n7rQIcPXQzJUbkVrpbTBytULr3YfrWQyNJbe2oese27FC6v3gfochqdtH1k5rI8x1N+GiXrvY5igJ1bGNYeY263jyzz2AYHe29llLIBcoAMrgcbae0xAGLEyalTcpT4GGMSZRdB6Ts7nE6eUz+-T1G11luM5erAqbMMKfM4hhWrGzGtrQxsjD8ndMWbc322zsGH0iac3ptz07AskdczW3zLmIOPoIx4jdmmTPxZC7FnDp5WNSZS3ZsAcnpEAHFBwqbc0RyLwGJE3OK6VhLfGAu5aC5s6rJWf0nvtTEgTVyWvgfa+m3JXX0M9Z-cJgzk6cs+K02ym5VNqVxanPOsbHiGuTdSx++Ts3mNUYnZ1jzdGNm7o23NzLZDLM7YG3tjjzEHNHfAz6urkneCDY2QVwxVNCthYeyijTq28vreke9z7aan1rqM41qLzWa2A78196zz2zUzY+z+21S3THlfB5V2xUOkfzcW1Z5b8PmL8sc9D+b4n8emIixjzzASGMk5xydulqmOsXeI5jtL9PmN9ZB2ep7l3BOtJrQABWOxRwJsOPHo9+01-7hiRe1eB4l0xK2JUQ8O9I+XMPFd8ap9LiHN2Nei7CdzpXQzkt6-Z95w34GUcU6wRN1X7PXtuiF+03r4XCdVeF27n9C23Pm8dzTkDIXXfMbx+d+3fO2dB6vcLg9Yvmf9eFSXXXgf9vvpuUL+Po7IPJ4D1umPpm49A9R4aqPFXC-hMz9nnpZ21OGqddH9Prrq-gdG3bjBjeK-N9I8X5HbmX386KXT+TWfmN4Y78Mz38zW++-JxHlZQ-23Ccc2Pn993telunx2vvcWIkS7R9vodIea+Fvn2poZKuC897IbLl3p-aXcDryzoZqfr9XYkeruXD+FXP-62bo-A3b-PTRPHnepcvanG-fLTPUcBXVHS-I-GAkvSfN-IDSvL-F3WAtrf3bfIAzA93A-SPbfZ3TwIXAAJTgMnx+zTw-0mWFwoOwMIMXyb1oMhxDwYPmwnwX14Bs0gNYLwNII4MZ3+TK23ytzlyELF0kSYM8W32J1H0kPxRNx123xHw10UJ6RLnPxf2JW31zQkLuz-zAKIKXxexuTIIAClkDztk8wcLdK879PBLC29c8RVeD7CoCMCnCrD+8D9k8pcaCBc4MQtnDfcuD68RUr80CoDxC3RQj5seMKdk9UCpsidzCfD5tlC6k89VD0jmN28bDVUICPDWD9C4iMjGcXE-DVUu8+CgisAV95N4jKiCiL9O9t9bVHNmixduBw82j-VTD30SDzhuiwluAsjvsj9HCRiKiE9WidDMEj8vCZi9NtD-8FFAC8i2s+iFiAj396i6VYjvC29bduCojUiJF5DpFRi-lIoPdBjmIpw1DDEbiHkI0cCHiJEyjji58JjxtijAiilhioAyCAA5aw-ouwwE9taYkE8ExgzfFFdw6Eg7cw+EuLP4yXXAtElwmQ841LI4kY9E4QnY9Y1FOQnE33Uk4w3Qz46LEI4kqQ6k03acAE-YoE8w5zRnUAlk3gWokog42EyAMgrkhPAfbfZYkE0UsJIw3k6g9k9tAQkY6UnpTEqDMQzkggxEuHOk8XEIlU-ZeYskvY6I1g54uIg02lI0mk2Q3U745U8fe4lgg4xo64y0uhNYm0-PU0g4zopo90y47LNkn0jkmtRTfsSg7gwfZ0wdG5cMyM-o+UkM9tSUyAeMsItzKEhUjZJUqAdMzgtzZE7Mz5OMiMqk0Q3Uq4wxfM4Qnk+rXIsMsszIp07vUo0s-Ij4mM5fds33a0lkh3YswXELRTIXBMlnYVWcRAsM0c3w7U7BEVYMi4ovYcmc+bOs7IkVfklEhHacu7bbCIiNDU3cn9ffOc4ZEVJMpcvUxzEc8DPgVwrQhslcu8vsg1NwvQuM1c7k18jckuE0q8106sr8sXLYH81hZPfEvLP06RW8kbT0pXZIo-YEtM4CsJGcMClVUVKYz8sPRIwotVXUljY8hI2Ut8o1TY4i4QnONzLcwciRQkvM1Cv5E8DCjxaM1swUqst0WCuLFuU4xMo-c0zwHiyorYcIhYrM5MqVe0xiu7SIdcpEo-QC7ipiwtTBCsrsqVaCoC8DBQSIZk+s3U1BHCn9bgFPFsuoopDfG81Sx-GcUiv1b0q894yihPe8pggc3xTIXkDQHkZQIAA/view">-> CLIQUE AQUI para abrir gráfico interativo</a>

<img 
    src="visualization.svg" 
    alt="Mortes por estado brasileiro"
    height="600"
    width="1000" />

## Considerações
O único tratamento nos dados originais foi o preenchimento dos números faltantes, provavelmente devido à falta de disponibilidade de informação oficial pela secretaria em um determinado dia, porém não acontece com frequência. Os dados pendentes foram preenchidos com o mesmo número total de mortes válido antes daquele dia para aquele estado. Normalmente esta lacuna ocorre nos dias mais recentes portanto, para fins de visualização, não foram considerados os últimos 2 dias. Como o intuito deste gráfico é mostrar a tendência é importante termos os dados completos para não tirarmos conclusões precipitadas.

## Referências

* <a target="_blank" rel="noopener noreferrer" href="https://brasil.io/dataset/covid19/caso">Brasil.io</a>
* <a target="_blank" rel="noopener noreferrer" href="https://ourworldindata.org/grapher/covid-confirmed-deaths-since-5th-death">Our World in Data</a>
* <a target="_blank" rel="noopener noreferrer" href="https://www.facebook.com/726282547396228/videos/861466570947781/">DataCamp Live Coding: Covid-19 Exploratory Data Analysis</a>
* <a target="_blank" rel="noopener noreferrer" href="https://matthewkudija.com/blog/2018/06/22/altair-interactive/">Altair: Interactive Plots on the Web</a>

---

- *Atualizado em: 13/04/2020*
- *O código original para geração desta visualização pode ser acessado aqui: <a target="_blank" rel="noopener noreferrer" href="https://github.com/fehann/COVID-19-Brazil/blob/master/covid19estadosbrasileiros.py">Python</a>.*
- *Cuidem da saúde e da familia, colaborando vamos sair desta situação o mais breve possível.*


<!---
Para atualizar o gráfico:
1) Google Colab - rodar o notebook
2) Salvar imagem em SVG e substituir no Github
3) Abrir no editor do Vega Lite e copiar link para Github
-->
