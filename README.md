
# Reporte de rendimiento con Python, Notion y GraphAPI

Este proyecto genera reportes de rendimiento semanal utilizando Python, Notion, y GraphAPI, y envía dichos reportes por correo electrónico en formato HTML a los usuarios correspondientes.

## Descripción

El objetivo principal de este proyecto es automatizar la generación y envío de reportes de rendimiento. La información se extrae de una base de datos de Notion, se procesa y se convierte en gráficos y reportes HTML personalizados para cada usuario. Finalmente, estos reportes se envían por correo electrónico utilizando Microsoft Graph API.


## Tecnologías y Librerías Usadas

- **Python:** Lenguaje de programación principal.

- **Notion SDK for Python:** Para interactuar con la API de Notion.

- **Microsoft Graph API:** Para enviar correos electrónicos.

- **requests:** Para realizar solicitudes HTTP.

- **matplotlib:** Para generar gráficos.

- **dotenv:** Para cargar variables de entorno.

- **logging:** Para la gestión de logs.

## Instalación

#### 1. Clonar el repositorio

```bash
  git clone https://github.com/Massuk/email-report-notion.git
  cd email-report-notion
```

#### 2. Crear un entorno virtual

```bash
  python -m venv venv
  source venv/bin/activate  # En Windows: venv\Scripts\activate
```   

#### 3. Instalar las dependencias

```bash
  pip install -r requirements.txt
```   

#### 3. Configurar las variables de entorno

```bash
  # Debes generarlo en Azure
  TENANT_ID=your_tenant_id
  CLIENT_ID=your_client_id
  CLIENT_SECRET=your_client_secret
  REFRESH_TOKEN=your_refresh_token
  PAYLOAD=your_payload
  COOKIE=your_cookie

  # Debes generarlo en Notion
  NOTION_TOKEN=your_notion_token
```   
## Usage/Examples

#### 1. Ejecutar el script principal:
Ejecuta el Jupyter Notebook ```notion-weekly-report.ipynb``` y sigue las instrucciones paso a paso. El script realizará las siguientes tareas:

- Cargar las variables de entorno.
- Configurar el logger.
- Autenticarse con Microsoft Graph API.
- Extraer datos de Notion.
- Generar gráficos y reportes HTML.
- Enviar los reportes por correo electrónico.


## Estructura del proyecto


```bash
├── assets
│   └── template.html           # Plantilla HTML para los reportes
├── reports                     # Directorio donde se guardan los reportes generados
├── notion-weekly-report.ipynb  # Jupyter Notebook principal
├── .env                        # Archivo de configuración de variables de entorno
├── requirements.txt            # Lista de dependencias del proyecto
└── README.md                   

```


## Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue o envía un pull request para mejorar el proyecto.


## License

[MIT](https://choosealicense.com/licenses/mit/)

