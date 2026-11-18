INTEGRADOR DE PROGRAMACION 1 

Participantes: ARANA JOAQUIN - MALLA DYLAN 

 Gestión de Datos de Países en Python

Este proyecto consiste en una aplicación de consola desarrollada en Python que permite gestionar información sobre países. Utiliza estructuras de datos como listas y diccionarios, lectura desde archivos CSV, y funciones para aplicar filtros, ordenamientos y estadísticas.

El sistema está modularizado en archivos separados y permite al usuario interactuar mediante un menú para realizar búsquedas, aplicar criterios de filtrado, ordenar los datos y visualizar indicadores clave.

 Estructura del proyecto

- `main.py`: punto de entrada, genera el CSV desde una API externa si no existe.
- `menu.py`: gestiona la interacción con el usuario y muestra el menú principal.
- `listas.py`: contiene funciones de búsqueda, filtrado, ordenamiento y estadísticas.
- `api.py`: obtiene datos de países desde una API pública y los exporta a CSV.
- `paises.csv`: archivo con los datos base (nombre, población, superficie, continente).

 Funcionalidades principales

-  Buscar país por nombre (coincidencia parcial).
-  Filtrar países por:
  - Continente
  - Rango de población
  - Rango de superficie
-  Ordenar países por:
  - Nombre
  - Población
  - Superficie (ascendente o descendente)
-  Mostrar estadísticas:
  - País con mayor y menor población
  - Promedio de población
  - Promedio de superficie
  - Cantidad de países por continente

---

 Ejecución

1. Asegurarse de tener Docker instalado en el sistema.


2. ejectuar el .bat (si esta en windows) o el .sh(si esta en linux) o abrir una terminal y ubicarse en la carpeta raíz del proyecto (donde están el archivo Dockerfile y la carpeta src):

cd ruta/a/la/carpeta/del/proyecto

3. Construir la imagen del contenedor:

docker build -t miprograma .

4. Ejecutar el programa dentro del contenedor:

docker run -it --rm miprograma

5. Al iniciar el programa, si el archivo paises.csv no existe, se generará automáticamente desde la API.
6. Use el menú interactivo para:
1) Buscar países

Ejemplo:
🔍 Ingrese el nombre o parte del nombre: vene
📋 Resultados:
• Venezuela - 28.720.000 hab - 916.445 km² - América
2) Aplicar filtros

Ejemplo:
 FILTROS DISPONIBLES- Por continente
- Por rango de población
- Por rango de superficie
Seleccione filtro (a/b/c): a
 Ingrese continente: america
 Resultados:
• Argentina - 45.851.378 hab - 2.736.690 km² - América
• Bolivia - 12.637.909 hab - 1.083.300 km² - América

3) Ordenar por distintos criterios

Ejemplo:
 ORDENAR POR- Nombre
- Población
- Superficie
Seleccione criterio (a/b/c): a
¿Orden descendente? (s/n): si
 Resultados:
• Afganistán - 42.594.582 hab - 652.230 km² - Asia
• Albania - 2.800.000 hab - 28.748 km² - Europa

4) Ver estadísticas

Ejemplo:
País con mayor población: China (1.444.216.107)

7. Presione ENTER para volver al menú después de cada operación

api.py, main.py, Informe, Marco Teorico y Test/Arreglos hechos por Malla Dylan
lista.py, menu.py, capturas y readme hecho por Arana Joaquín




