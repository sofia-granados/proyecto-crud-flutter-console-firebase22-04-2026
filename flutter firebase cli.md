¡Excelente elección! Integrar Flutter con Firebase es una de las combinaciones más potentes para el desarrollo móvil moderno. Para lograr que todo funcione correctamente desde tu terminal en Windows, vamos a seguir un camino estructurado.

---

## 1. Instalación de Node.js y npm (Global) en Windows

Para manejar las herramientas de Firebase, necesitas **Node.js**, el cual incluye automáticamente **npm** (Node Package Manager).

### Software necesario
No necesitas herramientas complejas, solo el instalador oficial:
* **Instalador MSI de Node.js:** Descárgalo desde [nodejs.org](https://nodejs.org/). Se recomienda la versión **LTS** (Long Term Support) por su estabilidad.

### Procedimiento paso a paso
1.  **Ejecuta el instalador:** Haz doble clic en el archivo `.msi` descargado.
2.  **Asistente de instalación:** Haz clic en "Next", acepta los términos y elige la ruta por defecto (normalmente `C:\Program Files\nodejs\`).
3.  **Custom Setup:** Asegúrate de que la opción **"Add to PATH"** esté seleccionada (esto es lo que permite que sea "global").
4.  **Herramientas adicionales:** Verás una casilla para instalar "Tools for Native Modules" (Chocolatey). Generalmente no es obligatoria para Firebase, pero es recomendable si planeas hacer desarrollo web avanzado.
5.  **Finalizar:** Haz clic en "Install" y luego en "Finish".

---

## 2. Verificación de la instalación

Para confirmar que Windows reconoce los comandos, abre una terminal (**CMD** o **PowerShell**) y escribe:

* **Para Node.js:** `node -v`
* **Para npm:** `npm -v`

> [!TIP]
> Si recibes un error de "comando no reconocido", reinicia tu terminal o incluso tu PC para que las variables de entorno se actualicen.

---

## 3. Instalación de Firebase CLI y FlutterFire

Aquí es donde conectamos tu entorno local con la consola de Firebase.

### Instalar firebase-tools (Global)
Para instalar las herramientas de Firebase de forma global en tu sistema, usa el siguiente comando en tu terminal:

```bash
npm install -g firebase-tools
```

### Cómo acceder a Firebase con tu cuenta de Google
Una vez instaladas las herramientas, debes vincular tu terminal con tu cuenta:

1.  En la terminal, escribe:
    ```bash
    firebase login
    ```
2.  Se abrirá automáticamente una ventana en tu **navegador web**.
3.  Selecciona tu cuenta de Google y otorga los permisos necesarios.
4.  Al finalizar, verás un mensaje de éxito en la terminal: *✔  Success! Logged in as [tu-correo@gmail.com]*

---

## 4. Instalación de Flutter CLI (FlutterFire CLI)

En el ecosistema Flutter, existe una herramienta específica llamada **FlutterFire CLI** que automatiza la configuración de Firebase en tu proyecto.

### Requisitos previos
Debes tener el SDK de Flutter ya instalado y configurado en tu PATH.

### Procedimiento de instalación
Ejecuta el siguiente comando para activar la CLI de FlutterFire de manera global:

```bash
dart pub global activate flutterfire_cli
```

### Uso básico en un proyecto
Una vez activado, sitúate en la carpeta raíz de tu aplicación Flutter y ejecuta:

```bash
flutterfire configure
```
Este comando te permitirá seleccionar tus proyectos existentes en Firebase Console y generará automáticamente el archivo `firebase_options.dart`, configurando Android, iOS y Web de una sola vez.



---

### Resumen de comandos útiles

| Acción | Comando |
| :--- | :--- |
| **Actualizar npm** | `npm install -g npm@latest` |
| **Verificar login Firebase** | `firebase login:list` |
| **Cerrar sesión** | `firebase logout` |
| **Verificar SDK Flutter** | `flutter doctor` |

¿Ya tienes creado tu proyecto en la consola web de Firebase o necesitas ayuda para vincularlo con el comando `configure`?
