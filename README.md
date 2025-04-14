# Prova
flowchart TD
``` mermaid 
    A[Inicio] --> B[Inicializar ESP32-S3]
    B --> C[Configurar micrófono, botones y servidor web]
    C --> D[¿Modo automático o manual?]
    D --> |Botón 1: Manual| E[Modo Manual]
    D --> |Automático| F[Modo Automático]
    E --> G[¿Botón 2 pulsado?]
    G --> |Sí| H[Cambiar a siguiente cuerda]
    G --> |No| I[Esperar entrada]
    H --> J[Captar frecuencia del micrófono]
    I --> J
    J --> K[Mostrar frecuencia en página web]
    K --> D
    F --> L[Detectar frecuencia actual]
    L --> M[Comparar con notas estándar]
    M --> N[Determinar cuerda más cercana]
    N --> K
    K --> D
```
