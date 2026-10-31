# Libro de cuentas

Registro personal de ingresos, gastos, casos por cobrar e inversiones.
Cada persona crea su cuenta con correo y contraseña y solo ve su propio libro.
Los datos se guardan en Firebase (Firestore) y se sincronizan entre el celular y la computadora.
Funciona sin internet por ratos: los cambios se guardan en el dispositivo y se suben al reconectar.

## Archivos
- `index.html`: la aplicación completa.
- `firestore.rules`: reglas de seguridad de la base de datos (cada usuario solo accede a `users/<su id>`).

## Puesta en marcha
1. En `index.html`, reemplaza el bloque `firebaseConfig` con la configuración de tu proyecto de Firebase.
2. En Firebase: activa Authentication con "Correo electrónico/contraseña" y crea Firestore en modo producción.
3. En Firestore → Reglas, pega el contenido de `firestore.rules` y publica.
4. En Authentication → Configuración → Dominios autorizados, agrega el dominio donde publiques la app (por ejemplo `usuario.github.io`).
5. Publica el repositorio con GitHub Pages (Settings → Pages → Deploy from branch → `main`, carpeta raíz).

## Usar en el iPhone como app
Abre la dirección en Safari → botón Compartir → "Agregar a pantalla de inicio".
