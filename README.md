# Mapa do Acre em GeoJSON

Mapa do Estado do Acre com os polígonos dos 22 municípios em formato GeoJSON.

## Fonte dos Dados

Os dados geográficos são provenientes do IBGE (Instituto Brasileiro de Geografia e Estatística), código de unidade federativa `12`.

## Conteúdo

O arquivo `geojs-12-mun.json` contém uma `FeatureCollection` com 22 feições (`Feature`), cada uma representando um município do Acre.

Propriedades de cada município:

| Campo       | Descrição                              |
|-------------|----------------------------------------|
| `id`        | Código IBGE de 7 dígitos               |
| `name`      | Nome do município                      |
| `description` | Nome do município (duplicado)        |

### Municípios

| Código IBGE | Município              |
|-------------|------------------------|
| 1200013     | Acrelândia             |
| 1200054     | Assis Brasil           |
| 1200104     | Brasiléia              |
| 1200138     | Bujari                 |
| 1200179     | Capixaba               |
| 1200203     | Cruzeiro do Sul        |
| 1200252     | Epitaciolândia         |
| 1200302     | Feijó                  |
| 1200328     | Jordão                 |
| 1200336     | Mâncio Lima            |
| 1200344     | Manoel Urbano          |
| 1200351     | Marechal Thaumaturgo   |
| 1200385     | Plácido de Castro      |
| 1200393     | Porto Walter           |
| 1200401     | Rio Branco (capital)   |
| 1200427     | Rodrigues Alves        |
| 1200435     | Santa Rosa do Purus    |
| 1200450     | Senador Guiomard       |
| 1200500     | Sena Madureira         |
| 1200609     | Tarauacá               |
| 1200708     | Xapuri                 |
| 1200807     | Porto Acre             |

## Formato

- **Formato:** GeoJSON (RFC 7946)
- **Sistema de coordenadas:** WGS 84 (EPSG:4326)
- **Tipo de geometria:** `Polygon`

## Como usar

### Clonar o repositório

```bash
git clone https://github.com/MVMLima/mapa_acre.git
```

### Visualizar online

Carregue o arquivo `geojs-12-mun.json` no [geojson.io](https://geojson.io) para visualização rápida.

### Web (Leaflet)

```javascript
fetch('geojs-12-mun.json')
  .then(res => res.json())
  .then(data => L.geoJSON(data).addTo(map));
```

### Python (GeoPandas)

```python
import geopandas as gpd

gdf = gpd.read_file("geojs-12-mun.json")
print(gdf.head())
```

### QGIS

Arraste o arquivo para o QGIS ou use `Camada > Adicionar Camada > Adicionar Camada Vetorial`.

## Licença

Dados abertos — IBGE.
