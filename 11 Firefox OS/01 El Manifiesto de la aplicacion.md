El Manifiesto de la aplicación
==============================

El **Manifiesto** de la aplicación es una parte esencial de toda aplicaión firefox OS ya que es la que gestiona la integración con el sistema operativo. El archivo manifesto debe llevar el nombre `manifest.webapp` y contiene toda información de tu *App*, descripción, requerimientos, datos del desarrollador, enlace a los iconos, lenguajes soportados, entre otros tantos datos. 

Veamos como luce un archivo `manifest.webapp`

```json
{
  "name": "El nombre de mi App",
  "description": "Descripcion del proyecto, un elevator pitch iria bien aqui",
  "launch_path": "/",
  "icons": {
    "128": "/img/icon-128.png"
  },
  "developer": {
    "name": "Tu nombre o el de tu empresa",
    "url": "http://your-homepage-here.org"
  },
  "default_locale": "es"
}
```