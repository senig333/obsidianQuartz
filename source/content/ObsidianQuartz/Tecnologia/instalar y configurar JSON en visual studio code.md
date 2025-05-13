<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# instalar y configurar JSON en visual studio code

Para instalar y configurar JSON en Visual Studio Code, sigue estos pasos:

## **Creación de un archivo JSON**

1. Abre Visual Studio Code.
2. Crea una nueva carpeta para organizar tus archivos (opcional).
3. Haz clic en "New File" y nombra el archivo con la extensión `.json`, por ejemplo, `data.json`.
4. Escribe o pega el contenido JSON dentro del archivo. VS Code proporciona características como *IntelliSense* y validación para ayudarte a escribir correctamente[^1][^5].

## **Instalación de extensiones recomendadas**

- **Prettier - Code Formatter**:
    - Ve a la pestaña de extensiones en VS Code (ícono de cubo en la barra lateral izquierda).
    - Busca "Prettier - Code Formatter" e instálalo.
    - Configura Prettier como el formateador predeterminado:
        - Ve a *File > Preferences > Settings*.
        - En la configuración JSON (`settings.json`), agrega:

```json
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnSave": true
```

        - Esto permite que tu archivo JSON se formatee automáticamente al guardar[^1][^3].
- **Material Icon Theme**: Instala esta extensión para visualizar íconos personalizados según el tipo de archivo, como los de JSON[^1].


## **Configuración adicional**

- Para personalizar la configuración del editor, abre el archivo `settings.json` desde *File > Preferences > Settings > Open Settings (JSON)* y agrega configuraciones útiles como:

```json
{
    "editor.wordWrap": "on",
    "editor.tabSize": 2,
    "editor.renderWhitespace": "all"
}
```

Esto mejora la legibilidad y manejo de archivos JSON[^3][^8].


## **Uso de JSON Server**

Si necesitas un servidor para simular datos con JSON:

1. Instala Node.js desde su página oficial.
2. Abre la terminal en VS Code y ejecuta:

```bash
npm install -g json-server
```

3. Crea un archivo `db.json` con tus datos.
4. Inicia el servidor con:

```bash
json-server --watch db.json
```

Esto ejecutará un servidor local accesible desde `http://localhost:3000`[^2].

Con estos pasos, tendrás configurado Visual Studio Code para trabajar eficientemente con archivos JSON.

<div style="text-align: center">⁂</div>

[^1]: https://www.youtube.com/watch?v=QMTJ_z_EHC8

[^2]: https://www.youtube.com/watch?v=RY5jLSB2yC0

[^3]: https://jonmircha.com/vscode

[^4]: https://learn.microsoft.com/es-es/microsoft-edge/visual-studio-code/microsoft-edge-devtools-extension/launch-json

[^5]: https://code.visualstudio.com/docs/languages/json

[^6]: https://www.youtube.com/watch?v=ymY4PHGm4a8

[^7]: https://www.youtube.com/watch?v=fs9DJjvW_q4

[^8]: https://www.youtube.com/watch?v=WI3_Bh1TKj0

