# Laboratorio 11 · Firebase en Android
Luis Gustavo Quispe Salcedo · Programación en Móviles

## Ejecutar en un emulador Android
1. Descomprime el proyecto. En la raíz, donde está firebase.json, ejecuta con Firebase CLI y Java 21: `firebase emulators:start --only auth,firestore --project demo-lab11`. Mantén la terminal abierta.
2. Abre la carpeta **start** en Android Studio. Usa JDK 17 para Gradle y Android SDK 34. En Build Variants selecciona **devDebug**. Ejecuta en un dispositivo virtual Android. Esta variante usa el proyecto de demostración y los puertos 9099 y 8080 del equipo anfitrión.
3. Pulsa **+**, crea «Revisar inventario» y guarda. En el engranaje selecciona **Create account** y vincula un correo de prueba y una contraseña. La tarea debe seguir visible. En la interfaz de Emulator Suite comprueba que el UID del usuario coincide con el campo userId del documento de tasks.
4. Marca la tarea, edítala desde su menú y cierra sesión. La sesión anónima nueva debe mostrar su propia lista vacía. Vuelve a entrar con el correo anterior y comprueba que la tarea reaparece. Graba esta secuencia para la entrega.

## Conectar al proyecto Firebase del curso
Registra la app Android com.example.makeitso, activa Analytics y los proveedores Anonymous y Email/Password. Crea Firestore en modo producción, elige la región y publica el contenido de firestore.rules en la pestaña Reglas. Coloca el archivo oficial en **start/app/src/prod/google-services.json**, elige **prodDebug** y ejecuta. Para la vinculación de cuentas, revisa el ajuste de protección de enumeración de correo que especifica la guía para el proyecto de práctica. Para verificar Performance Monitoring, genera operaciones de guardado y actualización y consulta las trazas saveTask, updateTask y linkAccount en el proyecto conectado.

## Historial
El archivo Lab11.bundle conserva el repositorio y sus commits. Para restaurarlos: `git clone Lab11.bundle Lab11`. Para publicar en tu GitHub, crea un repositorio vacío, configura su URL como origin y sube la rama actual.
