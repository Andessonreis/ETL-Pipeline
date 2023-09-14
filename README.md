# ETL-Pipeline-com-Banco-de-Dados

O objetivo deste projeto é coletar informações atualizadas sobre a COVID-19 a partir de uma API pública e armazená-las em um formato tabular (Excel) e em um banco de dados para posterior análise.

## Passos do Pipeline ETL

### 1. Extração (Extract)

Nesta etapa, os dados são obtidos da API pública de COVID-19: `https://disease.sh/v3/covid-19/all`.Os dados extraídos incluem:

```python
{
    'updated': 1694305273474,
    'cases': 695103130,
    'todayCases': 4903,
    'deaths': 6913935,
    'todayDeaths': 5,
    'recovered': 666967657,
    'todayRecovered': 65807,
    'active': 21221538,
    'critical': 37817,
    'casesPerOneMillion': 89175,
    'deathsPerOneMillion': 887,
    'tests': 7021679307,
    'testsPerOneMillion': 883793.16,
    'population': 7944935131,
    'oneCasePerPeople': 0,
    'oneDeathPerPeople': 0,
    'oneTestPerPeople': 0,
    'activePerOneMillion': 2671.08,
    'recoveredPerOneMillion': 83948.79,
    'criticalPerOneMillion': 4.76,
    'affectedCountries': 231
}
```
### 2. Transformação (Transform)

Os dados extraídos são processados para selecionar as informações relevantes e calculados campos adicionais, como casos ativos, casos por milhão, etc.

### 3. Carga (Load)

Os dados transformados são carregados em duas fontes diferentes:

- Um arquivo Excel para análise ou relatórios.
- Um banco de dados para armazenamento persistente.

## Autor

Desenvolvido por Andesson Reis.

<div style="display: flex; align-items: center;">
  <img src="https://github.com/Andessonreis.png" alt="Andesson Reis" width="70" height="70" style="border-radius: 50%; margin-right: 10px;">
</div>
