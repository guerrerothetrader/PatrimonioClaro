# Patrimonio Claro - APK para Android

Este proyecto empaqueta la app dentro de un APK: los archivos van en el propio móvil
(funciona sin conexión y sin alojar nada). Tus datos se guardan solo en ese teléfono.

## Cómo obtener el APK (sin instalar nada en tu ordenador)
1. Crea una cuenta gratuita en https://github.com y un repositorio **privado** nuevo.
2. Sube TODO el contenido de esta carpeta (arrastra los archivos y carpetas a la página del repositorio).
   Si no aparece la carpeta `.github`, crea el archivo a mano: "Add file > Create new file",
   nombre `.github/workflows/build-apk.yml`, y pega el contenido de `build-apk.yml.txt`.
3. Abre la pestaña **Actions** > "Compilar APK" > **Run workflow**. Tarda unos 5-10 minutos.
4. Al terminar, entra en esa ejecución y descarga el archivo `patrimonio-claro-apk` (un zip con `app-debug.apk`).

## Instalar en el móvil
1. Pasa `app-debug.apk` al teléfono (cable, Drive, correo...).
2. Ábrelo y permite "Instalar apps desconocidas" para la app desde la que lo abres.
3. Si Play Protect avisa, pulsa "Instalar de todos modos" (es tu propia app, no está en Play Store).

## Importante
- Todas las compilaciones se firman con la misma clave (`android/app/patrimonio.keystore`),
  así que puedes actualizar la app instalada sin perder los datos. Mantén el repositorio privado.
- Si desinstalas la app, se borran sus datos: haz antes una copia desde Ajustes.
- Para actualizar la app web: sustituye `www/index.html` y vuelve a ejecutar el workflow.
