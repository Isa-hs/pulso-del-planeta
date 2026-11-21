# Pulso del planeta

Visor ambiental interactivo que reúne información meteorológica, calidad del aire, biodiversidad, CO₂ atmosférico y coberturas terrestres.

## Publicación en GitHub Pages

1. Crea un repositorio público en GitHub, por ejemplo `pulso-del-planeta`.
2. Sube el contenido de esta carpeta conservando la estructura (`index.html`, `css/`, `js/`).
3. En GitHub, abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`, y guarda.
6. Espera la publicación y abre la URL que GitHub Pages indique.

No requiere compilación ni instalación de dependencias: utiliza bibliotecas y servicios remotos.

## Fuentes de datos y servicios

- **Open-Meteo Forecast API**: variables meteorológicas actuales y pronóstico.
  https://open-meteo.com/
- **Open-Meteo Air Quality API**: índice europeo de calidad del aire y contaminantes.
  https://open-meteo.com/en/docs/air-quality-api
- **GBIF**: registros de ocurrencia de biodiversidad.
  https://www.gbif.org/developer/occurrence
- **NOAA Global Monitoring Laboratory**: serie mensual de CO₂ de Mauna Loa.
  https://gml.noaa.gov/ccgg/trends/
- **Esri Sentinel-2 10m Land Cover**: servicio de imágenes/clasificación de coberturas.
  https://livingatlas.arcgis.com/
- **ESA WorldCover**: capa de cobertura terrestre 2021.
  https://worldcover2021.esa.int/
- **NASA GIBS / MODIS**: capa global de cobertura terrestre.
  https://www.earthdata.nasa.gov/
- **Leaflet**: biblioteca de mapas.
  https://leafletjs.com/
- **OpenStreetMap**: colaboradores de cartografía base.
  https://www.openstreetmap.org/copyright

Consulta los términos de uso, atribución, límites y disponibilidad de cada proveedor antes de utilizar el proyecto en un producto institucional o comercial.

## Interpretación y limitaciones

- Las condiciones meteorológicas y la calidad del aire son valores de API para las coordenadas consultadas; no sustituyen estaciones oficiales ni mediciones locales.
- El pronóstico no es una observación.
- Los registros GBIF representan observaciones reportadas en la base de datos, no un inventario exhaustivo de la biodiversidad presente. El recuadro usa una ventana geográfica aproximada de 0,25 grados alrededor del punto y puede variar en tamaño real según la latitud.
- El CO₂ mostrado corresponde a la serie de Mauna Loa, Hawái; no representa una medición local de la ciudad consultada.
- La cobertura terrestre depende del producto seleccionado, su resolución, fecha y metodología. Esri, ESA WorldCover y NASA MODIS no son productos directamente equivalentes.
- El selector anual de Esri solo permanece habilitado cuando el servicio confirma que el filtro temporal funciona. Si el servicio no permite verificar el año, se muestra un aviso y se deshabilita el selector para no presentar la capa más reciente como si fuera un año histórico.
- El acceso a la ubicación requiere permiso del navegador y normalmente HTTPS (GitHub Pages lo proporciona).

## Estructura

```text
pulso-del-planeta/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── app.js
├── README.md
└── LICENSE
```

## Desarrollo

El proyecto es estático. Para probarlo localmente, sirve la carpeta con un servidor HTTP local (por ejemplo, la extensión Live Server de Visual Studio Code). Abrir directamente `index.html` como archivo puede limitar algunas funciones del navegador.

## Licencia

Se incluye una licencia MIT para el código del proyecto. Los datos, mapas, teselas, tipografías y servicios de terceros conservan sus propias licencias y condiciones.
