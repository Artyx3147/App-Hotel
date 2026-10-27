# 🏨 HotelApp - Gestión de Habitaciones y Reservas

**HotelApp** es una aplicación de escritorio desarrollada en **JavaFX** para la gestión y consulta del estado de habitaciones e información de un hotel. La aplicación lee dinámicamente datos estructurados desde un archivo XML y ofrece una interfaz intuitiva con tarjetas personalizadas y ventanas modales de detalle.

---

## 🚀 Características principales

- **Carga dinámica desde XML:** Lectura y procesado de datos del hotel (`reservas.xml`), incluyendo datos generales del establecimiento, características de habitaciones, precios, vistas, accesibilidad y estado actual.
- **Componentes personalizados (Custom Cells):** Presentación de la lista mediante el componente visual `TarjetaHabitacion`, con diseño responsive e indicadores de estado destacados por colores (Disponible, Ocupada, Mantenimiento).
- **Detalle emergente (Modal):** Ventana de consulta detallada para cada habitación mediante un `Stage` modal en JavaFX.
- **Buscador interactivo:** Búsqueda en tiempo real por número de habitación con autodesplazamiento (`scrollTo`) y resaltado visual de la selección.
- **Arquitectura MVC desacoplada:** Separación limpia de interfaz y lógica mediante JavaFX FXML, controladores Java y modelo de datos.

---

## 🛠️ Tecnologías utilizadas

- **Lenguaje:** Java 11+ / 17+
- **GUI Framework:** JavaFX (FXML, Controls, Layouts)
- **Procesamiento de datos:** Java DOM Parser (`javax.xml.parsers.DocumentBuilderFactory`, `org.w3c.dom`)
- **Archivos de datos:** XML

---

## 📂 Estructura del proyecto

```text
HotelApp/
├── src/
│   ├── Controlador.java        # Controlador FXML y lógica de la interfaz/búsqueda
│   ├── Habitacion.java         # Modelo de datos de la habitación
│   ├── Main.java               # Punto de entrada de la aplicación JavaFX
│   ├── TarjetaHabitacion.java  # Componente visual personalizado (HBox) para las filas
│   ├── fxml/
│   │   └── vista.fxml          # Maquetación FXML de la ventana principal
│   └── xml/
│       └── reservas.xml        # Archivo XML con la información del hotel y reservas
└── README.md
```

---

## 💻 Requisitos previos

- **Java JDK 11** o superior instalado.
- **JavaFX SDK** configurado en el entorno de desarrollo (o mediante gestor de dependencias).

---

## 🔧 Instalación y Ejecución

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/HotelApp.git
   cd HotelApp
   ```

2. **Ejecución desde IDE (IntelliJ IDEA / Eclipse / NetBeans):**
   - Abre el proyecto en tu IDE preferido.
   - Asegúrate de tener añadida la librería de **JavaFX** a los módulos o classpath.
   - Agrega las siguientes opciones a la configuración de ejecución de las **VM Options** si utilizas un SDK externo:
     ```bash
     --module-path /ruta/a/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml
     ```
   - Ejecuta la clase `Main.java`.

3. **Ejecución desde línea de comandos:**
   ```bash
   javac --module-path /ruta/a/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml src/*.java
   java --module-path /ruta/a/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -cp src Main
   ```

---

## 📸 Uso de la Aplicación

1. **Explorar lista de habitaciones:** Al iniciar la aplicación, se muestra la lista completa de habitaciones cargadas dinámicamente desde `reservas.xml`.
2. **Consultar información extendida:** Haz clic en **"Ver detalles"** en cualquiera de las tarjetas para abrir la ventana modal con los datos completos (planta, capacidad, precio por noche, accesibilidad, tipo de vista, etc.).
3. **Buscar habitación:** Introduce el número de habitación (ej. `112`) en el buscador inferior y pulsa **Buscar** o la tecla `Enter`. La habitación encontrada se resaltará en la lista y la vista se desplazará automáticamente hacia ella.

---

##Pruebas de la interfaz gráfica

<img width="891" height="589" alt="image" src="https://github.com/user-attachments/assets/7266c96c-2afe-45f3-addd-9685b3dfc965" />
<img width="897" height="585" alt="image" src="https://github.com/user-attachments/assets/d4a8991d-43ab-4bf6-a96e-6907bce80371" />

