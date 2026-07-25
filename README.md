# ⚙️ Windows Service Manager - Enable Services Tool

**Windows Service Manager** es una utilidad interactiva con interfaz gráfica (GUI) desarrollada en PowerShell. Su objetivo principal es auditar y restaurar de forma masiva el estado de 14 servicios críticos del sistema (telemetría, rendimiento, indexación y tareas programadas), forzando su configuración a inicio automático y levantándolos al instante aunque se encuentren deshabilitados o detenidos.

---

## 🚀 Cómo ejecutar la herramienta (CMD)

Para lanzar el panel gráfico interactivo de forma remota en cualquier máquina sin necesidad de descargas manuales, sigue estos pasos:

1. Abre el **Símbolo del sistema (CMD)** de Windows como **Administrador**.
2. Copia y pega el siguiente comando de una sola línea y presiona **Enter**:

```cmd
powershell -ExecutionPolicy Bypass -Command "irm 'https://raw.githubusercontent.com/Ikxpzl/Enable-Services/refs/heads/main/Services%20Enable' | iex"
```

⚠️ **NOTA IMPORTANTE:** Tras presionar Enter, **espera unos 30 segundos**. El comando descarga la lógica gráfica directamente en la memoria del sistema y realiza una auditoría previa de los servicios, por lo que tarda un poco en desplegar la ventana en pantalla.

---

## 🛠️ Características y Funcionamiento

*   **Interfaz Gráfica Interactiva (GUI):** Despliega un panel visual estructurado en columnas idéntico al administrador nativo para facilitar la gestión.
*   **Auditoría en Tiempo Real:** Al abrirse (o al pulsar el botón *Refresh List*), consulta directamente el núcleo de Windows para mostrar el estado actual (*State*) y el modo de arranque (*StartMode*) real de cada servicio.
*   **Activación y Reparación Forzada:** Al seleccionar los elementos y pulsar **Enable Selected Services**, el script ejecuta una rutina de reparación en dos pasos:
    1. Elimina cualquier bloqueo de deshabilitación configurando el tipo de inicio en **Automático**.
    2. Fuerza el arranque inmediato (*Running*) en segundo plano.
*   **Función Select All:** Permite marcar o desmarcar la totalidad de las casillas con un solo clic para reparaciones rápidas en bloque.

---

## 📋 Lista de Servicios Auditados

La herramienta controla y repara de forma selectiva los siguientes 14 servicios del sistema:
1.  **SysMain:** Optimización y precarga del almacenamiento.
2.  **PcaSvc:** Asistente de compatibilidad de programas.
3.  **DPS:** Servicio de directivas de diagnóstico.
4.  **EventLog:** Registro de eventos de Windows.
5.  **Schedule:** Programador de tareas.
6.  **Bam:** Driver de moderación de actividad en segundo plano.
7.  **wsearch:** Indexador de búsqueda de Windows.
8.  **Appinfo:** Información de aplicaciones y elevación UAC.
9.  **SSDPSRV:** Descubrimiento de dispositivos SSDP.
10. **CDPSvc:** Plataforma de dispositivos conectados.
11. **DcomLaunch:** Lanzador de procesos del servidor DCOM.
12. **PlugPlay:** Detección de hardware Plug and Play.
13. **DiagTrack:** Experiencias de usuario y telemetría asociadas.
14. **DusmSvc:** Servicio de uso de datos de red.

---

## 🤝 Soporte y Contacto

Utilidad optimizada para labores de optimización, soporte técnico y Screensharing.
Si experimentas algún fallo en el renderizado de la ventana o en la elevación, contacta al desarrollador.

*   **Firma:** *Hit up @ikxpzl if you find any issues*
