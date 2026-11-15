# Links de WhatsApp

Página estática para generar links de WhatsApp con mensaje personalizado a partir de una exportación de HubSpot (.xlsx o .csv).

- El archivo se procesa **solo en el navegador**: no se sube a ningún servidor ni al repositorio.
- Detecta automáticamente las columnas de **Nombre**, **Teléfono** (móvil / WhatsApp / teléfono) y **Periodo**; se pueden cambiar a mano.
- El mensaje es editable y acepta `{nombre}` y `{periodo}`.
- Números de 10 dígitos se completan con la lada `52` (configurable).
- "Enviado" se guarda en el navegador para llevar control.

## Qué debe traer el Excel

Exportar desde HubSpot (vista de **Contactos**, o Negocios con propiedades del contacto asociado) incluyendo al menos:

- Nombre
- Número de teléfono móvil (o Número de teléfono / WhatsApp)
- Periodo (opcional: si falta, se usa el "Periodo por defecto")

> No subas archivos de Excel con datos de contactos a este repositorio. `.gitignore` ya los excluye.
