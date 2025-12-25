# 🛠️ Guía de Mantenimiento del Modpack

Este repositorio aloja los archivos de tu modpack. Aquí tienes los pasos para actualizarlo.

## ✅ Requisito Previo: Activar GitHub Pages
Para que los archivos se puedan descargar, ve a:
1.  **Settings** (Pestaña arriba) -> **Pages** (Menú izquierda).
2.  En **Source** elige `Deploy from a branch`.
3.  En **Branch** selecciona `main` y carpeta `/ (root)`.
4.  Dale a **Save**.
5.  Espera 1-2 minutos. Arriba aparecerá tu URL: `https://fabiannavarroo.github.io/modpack/`.

---

## 📦 Cómo Actualizar Mods (Añadir o Quitar)

1.  **En tu PC**: Ve a la carpeta `MyPack`.
2.  **Cambios**:
    *   Mete los nuevos `.jar` en `mods/`.
    *   Borra los que no quieras.
    *   *(Opcional)* Añade configs en `config/`.
3.  **Regenerar Manifest**:
    Abre una terminal en `C:\Users\faby\Downloads\mine_launch` (un nivel arriba) y ejecuta:
    ```powershell
    python server/gen_manifest.py --base-url "https://fabiannavarroo.github.io/modpack" --input-dir "MyPack" --pack-version "1.1.0" --neoforge-url "https://fabiannavarroo.github.io/modpack/launcher/neoforge-installer.jar"
    ```
    *(Cambia "1.1.0" por el número de versión que quieras).*
4.  **Subir Cambios**:
    ```powershell
    cd MyPack
    git add .
    git commit -m "Actualizando mods"
    git push
    ```

---

## ☕ Cómo Cambiar la Versión de NeoForge

1.  **Descargar**: Baja el nuevo instalador de la web oficial de NeoForge.
2.  **Reemplazar**:
    *   Ve a `MyPack/launcher/`.
    *   Borra el viejo.
    *   Pega el nuevo y **renómbralo** a `neoforge-installer.jar` (así no tienes que cambiar el comando).
3.  **Regenerar y Subir**:
    Igual que con los mods (pasos 3 y 4 de arriba).

---

## 🚀 Cómo Jugar (Para tus amigos)

1.  Descarga el **Launcher** (.exe) que te enviaré.
2.  Ábrelo.
3.  Si es la primera vez, dale a **"Install NeoForge"**.
4.  Dale a **"Update Mods"** (se bajarán solos).
5.  Dale a **"OPEN MINECRAFT LAUNCHER"**.
6.  Juega con el perfil **neoforge**.
