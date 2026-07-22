# 🤖 Limpiador de Instagram (Unfollow Bot)

¡Bienvenido! Este script automatiza la tediosa tarea de cruzar tus listas de Instagram para descubrir quién no te sigue de vuelta y deja de seguirlos por ti.

El proceso simula clics reales en un navegador oculto, por lo que es la forma más segura de limpiar tu cuenta sin usar aplicaciones de terceros dudosas.

---

## ⚙️ Requisito Previo (Obligatorio)

Para que el programa funcione, tu computadora necesita el entorno de ejecución **Node.js**.
Si no lo tienes, descárgalo e instálalo (es gratis y toma un minuto):
👉 **[https://nodejs.org/](https://nodejs.org/)** _(Descarga la versión "LTS")._

---

## 📥 Paso 1: Descargar tus datos (Los JSON)

El bot no adivina tus seguidores; necesita que le des tus listas oficiales. Tienes que descargar tu información desde Meta:

1. Abre Instagram y entra a **Configuración** > **Centro de cuentas**.
2. Ve a **Tu información y tus permisos** > **Descargar tu información**.
3. Selecciona **Descargar o transferir información** y elige tu cuenta.
4. Elige **Parte de tu información** y selecciona ÚNICAMENTE la sección de **Seguidores y seguidos**.
5. **¡MUY IMPORTANTE!** En la configuración final asegúrate de marcar:
   - **Intervalo de fechas:** Desde el principio (Todo el tiempo).
   - **Formato:** Selecciona **JSON** (Si lo dejas en HTML, el bot fallará).
6. Haz clic en "Crear archivo". Instagram tardará un rato en procesarlo y te avisará cuando esté listo para descargar.
7. Cuando lo descargues, extrae el archivo. Busca adentro los documentos llamados exactamente `followers.json` y `following.json`, es importante que tenga el mismo nombre que se señala aqui, de no ser asi renombralos, OJO cuando los descargas ya son .json, no es necesario que les pongas .json para el renombre, solo verefica que se llamen exactamente followers y following.
8. Pega esos dos archivos en esta misma carpeta, junto al bot.

---

## 🚀 Paso 2: Ejecutar el Bot

Una vez que tengas Node.js instalado y tus dos archivos JSON listos en la carpeta:

1. Haz doble clic en el archivo **`Iniciar_Bot.bat`**.
2. Se abrirá una terminal negra. La primera vez, descargará automáticamente el navegador interno (Playwright) que necesita para funcionar.
3. Se abrirá una ventana de Instagram. **Tienes 60 segundos para iniciar sesión MANUAlMENTE** (Puedes modifcar el tiempo de inicio en el codigo "unfollow.js" linea 66, 60=60000). Ingresa tu usuario, contraseña y pasa la autenticación de dos pasos si la tienes.
   En caso de fallar en meter tus datos pero se genero el archivo "Auth.json" solo borralo y repite el proceso
4. Una vez logueado, el bot guardará tu sesión de forma local y segura en tu propia máquina.
5. El bot tomará el control de esa ventana, comparará las listas y comenzará a limpiar tu cuenta.

---

## ⚠️ Reglas de Supervivencia

- **Paciencia absoluta:** El bot está programado con pausas intencionales entre cada persona que deja de seguir. Esto es vital para engañar al sistema anti-spam de Meta. Si lo aceleras, te pueden bloquear la cuenta. Déjalo corriendo de fondo mientras haces otra cosa.
- **No toques la ventana de Chromium:** Deja que el bot controle esa ventana específica. Puedes usar tu navegador normal (Chrome, Edge) para otras cosas sin problema.
- **NO COMPARTAR LOS ARCHIVOS J.SON** En caso de querer compartir el bot, unicamente comparte el archivo .bat, el .js y el .txt que recibiste, es sumamente importante que nadie mas tenga tus archivos "followers.json", "following.json" y "auth.json" dado que es tu información privada y tus credenciales de acceso.

## 🖋️ Créditos y Distribución

Este proyecto fue desarrollado originalmente por **Cehort.gl**.

Eres libre de utilizar, estudiar o compartir esta herramienta. Sin embargo, como única condición para su uso y distribución, se solicita mantener los créditos correspondientes al autor original, conservando intactas las referencias a las siguientes cuentas:

- **GitHub:** [Eve Z Rey](https://github.com/evezrey)
- **Instagram:** [@cehort.gl](https://instagram.com/cehort.gl)

## ⚖️ Descargo de Responsabilidad y Derechos

Este script es un proyecto de software puramente **experimental** y educativo. Al ejecutarlo, aceptas las siguientes condiciones:

- **Uso bajo tu propio riesgo:** Este código interactúa con plataformas de terceros mediante automatización de interfaz. Las políticas de uso y los algoritmos de detección de Meta cambian constantemente.
- **Cero Responsabilidad:** El desarrollador y creador de esta herramienta **no se hace responsable** por suspensiones, bloqueos temporales (_Action Blocks_), _shadowbans_, eliminación de cuentas, pérdida de datos o cualquier otro daño directo o indirecto que resulte del uso de este software.
- **Privacidad:** El script se ejecuta 100% de manera local en tu computadora. Tus credenciales y archivos JSON JAMAS se envían a ningún servidor externo.
- **Propiedad Intelectual:** Este proyecto es independiente y no está afiliado, asociado, autorizado, respaldado ni patrocinado de ninguna manera por Instagram, Meta Platforms, Inc., ni ninguna de sus filiales o subsidiarias.
