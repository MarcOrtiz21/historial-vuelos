# ✈️ Flight History - Marc's Flight Tracker

Una aplicación web interactiva para visualizar y analizar tu historial de vuelos personales.

![Flight History Preview](https://img.shields.io/badge/Vuelos-23-blue) ![Hours](https://img.shields.io/badge/Horas-67h-green) ![Distance](https://img.shields.io/badge/Distancia-42k%20km-orange)

## 🌟 Características

### 📊 Dashboard Interactivo
- **KPIs en tiempo real**: Total de vuelos, horas de vuelo, distancia recorrida
- **Animaciones con colores**: Verde cuando aumentan, rojo cuando disminuyen
- **Filtros avanzados**: Por año, aerolínea, avión, país
- **Búsqueda**: Encuentra vuelos por aeropuerto, fecha, número de vuelo
- **Ordenación**: Por fecha, duración o distancia

### 🗺️ Mapa Interactivo
- **Rutas curvas** (Great Circle) que muestran la trayectoria real de los vuelos
- **Marcadores de aeropuertos** con tamaño variable según frecuencia de uso
- **Tooltips** con distancia al pasar el cursor sobre las rutas
- **Animación de avión** al seleccionar un vuelo
- **5 capas de mapa**: Oscuro, Satélite, Híbrido, Topográfico, Estándar

### 🎫 Tarjetas de Vuelo
- Información detallada: aerolínea, avión, matrícula
- Horarios de salida y llegada
- Tipo de asiento (Ventana/Pasillo/Centro)
- Motivo del viaje (Ocio/Trabajo)
- Notas personales
- Etiquetas: Nacional/Internacional

### 📈 Estadísticas
- Gráficos de aerolíneas más utilizadas
- Aviones más frecuentes
- Rutas más populares
- Distribución por tipo de asiento
- Motivos de viaje

### 📄 Exportar
- **PDF**: Exporta tu historial completo de vuelos
- Incluye lista de vuelos con detalles

## 🚀 Instalación

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Servidor web local (opcional, para desarrollo)

### Inicio Rápido

1. **Clona el repositorio**
   ```bash
   git clone https://github.com/MarcOrtiz21/historial-vuelos.git
   cd historial-vuelos
   ```

2. **Inicia un servidor local**
   ```bash
   python3 -m http.server 8000
   ```

3. **Abre en el navegador**
   ```
   http://localhost:8000
   ```

## 📁 Estructura del Proyecto

```
Historial Vuelos/
├── index.html          # Aplicación principal (HTML + CSS + JS)
├── flightdiary.csv     # Datos de vuelos (exportado de myFlightradar24)
├── js/
│   └── airports.js     # Base de datos de 4500+ aeropuertos
└── README.md           # Este archivo
```

## 📋 Formato del CSV

El archivo `flightdiary.csv` debe seguir este formato (compatible con myFlightradar24):

| Campo | Descripción | Ejemplo |
|-------|-------------|---------|
| Date | Fecha del vuelo | 2024-02-06 |
| Flight number | Número de vuelo | LH1809 |
| From | Aeropuerto origen | Barcelona / El Prat (BCN/LEBL) |
| To | Aeropuerto destino | Munich (MUC/EDDM) |
| Dep time | Hora de salida | 09:00:00 |
| Arr time | Hora de llegada | 11:05:00 |
| Duration | Duración | 02:05:00 |
| Airline | Aerolínea | Lufthansa (LH/DLH) |
| Aircraft | Tipo de avión | Airbus A320neo (A20N) |
| Registration | Matrícula | D-AINR |
| Seat number | Asiento | 19B |
| Seat type | Tipo asiento | 1=Ventana, 2=Pasillo, 3=Centro |
| Flight class | Clase | 1=Económica, 2=Business |
| Flight reason | Motivo | 1=Ocio, 2=Trabajo |
| Note | Notas | Tu comentario |

## 🛠️ Tecnologías

- **HTML5/CSS3/JavaScript** - Sin frameworks, vanilla
- **[Leaflet.js](https://leafletjs.com/)** - Mapas interactivos
- **[Papa Parse](https://www.papaparse.com/)** - Parsing de CSV
- **[jsPDF](https://github.com/parallax/jsPDF)** - Generación de PDF
- **[Chart.js](https://www.chartjs.org/)** - Gráficos (implícito en estadísticas)

### Capas de Mapa
- CartoDB Dark (por defecto)
- Esri Satellite
- Esri Hybrid (Satellite + Labels)
- OpenTopoMap
- OpenStreetMap

## 🎨 Diseño

- Estilo **Apple-inspired** con glassmorphism
- Tema oscuro por defecto
- Diseño responsive
- Animaciones suaves y transiciones

## 📱 Uso

### Navegación Básica
1. **Ver todos los vuelos**: El mapa muestra todas las rutas, el panel derecho lista los vuelos
2. **Filtrar por año**: Usa el dropdown "Todos los años"
3. **Buscar**: Escribe en el campo de búsqueda
4. **Ver detalles**: Haz clic en una tarjeta de vuelo

### Estadísticas
1. Haz clic en el icono de gráfico (📊) en la cabecera
2. Explora los diferentes gráficos y estadísticas

### Exportar PDF
1. Haz clic en el icono de PDF (📄) en la cabecera
2. Se descargará automáticamente

## 🔧 Personalización

### Añadir tus vuelos
1. Exporta tus vuelos desde [myFlightradar24](https://my.flightradar24.com/)
2. Reemplaza el archivo `flightdiary.csv`
3. Recarga la página

### Modificar estilos
Los estilos están inline en `index.html` dentro de la etiqueta `<style>`. Principales variables:
- Colores de tema en los selectores CSS
- Tipografía: SF Pro Display (fallback: system fonts)

## 📄 Licencia

Este proyecto es de uso personal. Si deseas usarlo, siéntete libre de hacerlo dando los créditos correspondientes.

## 👤 Autor

**Marc** - Desarrollado con ❤️ para tracking personal de vuelos.

---

*Última actualización: Febrero 2026*
