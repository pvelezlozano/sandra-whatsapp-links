# Links de WhatsApp

Página estática para generar links de WhatsApp con mensaje personalizado a partir de una exportación de HubSpot (.xlsx o .csv).

- El archivo se procesa solo en el navegador (no se guarda en ningún servidor).
- Si el archivo no tiene columna de teléfono, la página marca error.
- Detecta automáticamente las columnas de **Nombre**, **Teléfono** (móvil / WhatsApp / teléfono) y **Periodo**; se pueden cambiar a mano.
- El mensaje es editable y acepta `{nombre}` y `{periodo}`.
- Números de 10 dígitos se completan con la lada `52` (configurable).
- Filtro de periodos: muestra los periodos que trae el archivo y se eligen con un clic (por defecto Enero 2027 y Agosto 2027). La selección se recuerda.
- "Enviado" se guarda en el navegador para llevar control.

## Qué debe traer el Excel

Exportar desde HubSpot (vista de **Contactos**, o Negocios con propiedades del contacto asociado) incluyendo al menos:

- Nombre
- Número de teléfono móvil (o Número de teléfono / WhatsApp)
- Periodo (opcional: si falta, se usa el "Periodo por defecto")

> No subas archivos de Excel con datos de contactos a este repositorio. `.gitignore` ya los excluye.

## Archivos de prueba

En [`ejemplos/`](ejemplos/) hay dos archivos con datos ficticios:

- `ejemplo-contactos.xlsx`: 8 contactos con distintos periodos y formatos de teléfono (incluye uno inválido y uno vacío).
- `ejemplo-sin-telefono.xlsx`: misma estructura que la exportación de Negocios sin teléfono; debe marcar error.
