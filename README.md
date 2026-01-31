# Simulador de Cluster de Procesadores

## Descripción
Este proyecto es una simulación de un sistema de multiprocesadores distribuidos organizados en una estructura de árbol binario (Cluster). El sistema gestiona la ejecución de procesos, la asignación de memoria y la planificación de tareas a través de un área de espera con prioridades.

Ha sido desarrollado como parte la práctica de la asignatura de **Programación 2 (FIB)**.

## Funcionalidades Principalesº
- **Gestión del Cluster**: Configuración, modificación dinámica y consulta de la estructura de procesadores (árbol binario).
- **Planificación de Procesos**: Asignación inteligente de procesos a procesadores basada en disponibilidad de memoria y huecos óptimos.
- **Área de Espera**: Gestión de procesos pendientes mediante colas de prioridad.
- **Gestión de Memoria**: Simulación de memoria en cada procesador y algoritmos de compactación de memoria.
- **Simulación Temporal**: Avance del tiempo para simular la finalización de procesos.

## Compilación

Para compilar el proyecto, utiliza el siguiente comando con `g++`:

```bash
g++ -o program program.cc Cluster.cc AreaEspera.cc Procesador.cc Proceso.cc
```

## Ejecución y Uso

Ejecuta el programa compilado:

```bash
./program
```

El programa acepta una serie de comandos por entrada estándar. Puedes redirigir un fichero de entrada para automatizar las pruebas:

```bash
./program < input.txt
```

### Comandos Básicos
- `configurar_cluster` (`cc`): Inicializa la estructura del cluster.
- `alta_prioridad` (`ap`), `baja_prioridad` (`bp`): Añade o elimina prioridades.
- `alta_proceso_espera` (`ape`): Añade un nuevo proceso a la espera.
- `enviar_procesos_cluster` (`epc`): Intenta colocar procesos pendientes en el cluster.
- `avanzar_tiempo` (`at`): Avanza el reloj de la simulación.
- `imprimir_estructura_cluster` (`iec`): Muestra la estructura del árbol de procesadores.
- `compactar_memoria_cluster` (`cmc`): Compacta la memoria de todos los procesadores.

## Estructura del Código
- `Cluster`: Clase principal que gestiona el árbol de procesadores.
- `AreaEspera`: Gestiona las colas de prioridad antes de entrar al cluster.
- `Procesador`: Simula un procesador individual y su memoria.
- `Proceso`: Representa una tarea con identificador, memoria requerida y tiempo de ejecución.
