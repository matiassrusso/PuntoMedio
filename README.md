# 📍 PuntoMedio

> ¿Dónde nos juntamos? Calculá el punto de encuentro ideal entre varias personas.

## ¿Qué es?

PuntoMedio es una app web con mapa interactivo que te ayuda a encontrar el mejor lugar para juntarte con amigos cuando todos viven lejos. Agregás las ubicaciones de cada persona y la app calcula dos opciones:

- **Opción A — Centro geográfico:** el punto exactamente en el medio de todas las ubicaciones.
- **Opción B — Punto equidistante:** el punto donde todos quedan a la misma distancia (minimiza la diferencia).

Una vez elegida la opción, muestra los bares, restaurantes, cafés y parques más cercanos al punto de encuentro.

## Funcionalidades

- Agregar personas por dirección (búsqueda + Enter) o haciendo clic directamente en el mapa
- Marcadores arrastrables — al mover un pin se recalcula todo automáticamente
- Líneas y polígono visual entre todas las ubicaciones
- Cálculo de distancia para cada persona desde el punto de encuentro
- Indicador de equidad (diferencia entre la distancia más larga y la más corta)
- Búsqueda de lugares cercanos con filtros por categoría (bares, restaurantes, cafés, parques)
- Clic en un lugar del listado para verlo en el mapa con su info

## Tecnologías

- HTML + CSS + JavaScript (vanilla, sin frameworks)
- [Google Maps JavaScript API](https://developers.google.com/maps/documentation/javascript)
- [Places API (New)](https://developers.google.com/maps/documentation/places/web-service/op-overview)
- [Geocoding API](https://developers.google.com/maps/documentation/geocoding)

## Cómo usarlo

### Requisitos

Una API key de Google Maps con las siguientes APIs habilitadas:
- Maps JavaScript API
- Places API (New)
- Geocoding API

### Correr localmente

1. Cloná el repositorio:
   ```bash
   git clone https://github.com/matiassrusso/PuntoMedio.git
   cd PuntoMedio
   ```

2. Abrí `punto-medio.html` y reemplazá la API key en la última línea del script:
   ```js
   key: "TU_API_KEY"
   ```

3. Servilo desde un servidor local (no funciona bien desde `file://`):
   ```bash
   npx serve .
   ```

4. Abrí `http://localhost:3000/punto-medio.html` en el navegador.

## Algoritmo

El **punto equidistante** se calcula con un algoritmo de descenso iterativo (minimax): parte del centroide y busca el punto que minimiza la distancia máxima a todas las ubicaciones, reduciendo el paso de búsqueda progresivamente hasta converger.

El **centro geográfico** es simplemente el promedio de latitudes y longitudes.
