# 💧 Cálculo da Precipitação Média na Bacia do Rio Grande  

Este repositório contém um **script em Python** que realiza o processamento de dados pluviométricos do produto **MERGE/CPTEC-INPE**, integrados com o limite geográfico da **Bacia do Rio Grande**.  

O código foi desenvolvido para análises **hidrológicas e climáticas**, com foco em calcular a **precipitação média espacial** dentro da área delimitada pela bacia.  

---

## ⚙️ Etapas principais do script  

1. **Carregamento dos dados**  
   - Shapefile da bacia (`GRANDE.shp`)  
   - Arquivo MERGE (`MERGE_20250315-20250319.dat`) com **longitude, latitude e precipitação**  

2. **Visualização inicial**  
   - Mapa com a bacia (contorno azul)  
   - Pontos da grade MERGE (cinza)  

3. **Conversão para GeoDataFrame**  
   - Transformação de pontos (`longitude`, `latitude`) em geometrias  
   - Definição do sistema de referência geográfica **EPSG:4326**  

4. **Filtragem espacial**  
   - Seleção apenas dos pontos localizados **dentro da bacia**  

5. **Cálculo estatístico**  
   - Média da precipitação dos pontos internos à bacia  

6. **Visualização final**  
   - Bacia em azul  
   - Pontos válidos (dentro da bacia) em vermelho  

---

## 📊 Variáveis de saída  

| Variável                     | Descrição                                           |
|-------------------------------|---------------------------------------------------|
| `df`                         | DataFrame com todos os pontos MERGE               |
| `gdf_pontos`                 | GeoDataFrame com pontos convertidos em geometria  |
| `pontos_na_bacia`            | Subconjunto apenas dos pontos dentro da bacia     |
| `media_precipitacao_bacia`   | Valor médio da precipitação (mm) na bacia         |

---

## 🎯 Aplicações  

- Estudos de **hidrologia de bacias hidrográficas**  
- Avaliação de **chuvas médias espaciais**  
- Modelagem de **recursos hídricos e disponibilidade hídrica**  
- Monitoramento de **eventos climáticos extremos**  

---

## 🛠️ Tecnologias utilizadas  

- [Pandas](https://pandas.pydata.org/) → Manipulação de dados tabulares  
- [GeoPandas](https://geopandas.org/) → Processamento espacial de geometrias  
- [Matplotlib](https://matplotlib.org/) → Geração de mapas e gráficos  
