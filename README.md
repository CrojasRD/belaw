# Belaw Ec - Proyecto Completo

Proyecto de plataforma de suscripción para abogados independientes con Firebase Auth y Firestore.

## Estructura

- `index.html` - Landing page principal con todos los servicios
- `login.html` - Página de login con Firebase Auth
- `app.html` - Dashboard privado de suscriptores
- `suscripciones.html` - Página de planes de suscripción
- `img/` - Carpeta de imágenes (equipo.avif)

## Cómo ejecutar localmente

### Opción 1: Python (recomendado - sin instalaciones)

```bash
cd belaw-proyecto
python -m http.server 8000
```

Luego abre tu navegador: **http://localhost:8000**

### Opción 2: Node.js (http-server)

```bash
npm install -g http-server
cd belaw-proyecto
http-server -p 8000
```

Luego abre: **http://localhost:8000**

### Opción 3: VS Code Live Server

1. Abre la carpeta en VS Code
2. Click derecho en `index.html`
3. Selecciona "Open with Live Server"

## Firebase Configuración

Los archivos ya incluyen las credenciales de Firebase:
- **Project ID:** belaw-ec
- **Database:** Firestore con 6 colecciones (users, consultas, clientes, casos, seguimiento, facturacion)
- **Authentication:** Email/Password
- **Security Rules:** Ya configuradas

## Cómo probar

1. **Landing page:** http://localhost:8000/index.html
2. **Popup de planes:** Debería aparecer a los 8 segundos automáticamente
3. **Botón Planes:** En la navbar (arriba a la derecha)
4. **Login:** http://localhost:8000/login.html
   - Email: admin@belaw-ec.com
   - Password: La que configuraste en Firebase
5. **Dashboard:** http://localhost:8000/app.html

## Notas importantes

- Las URLs limpias (sin .html) funcionan SOLO en Vercel con rewrite rules
- Localmente debes acceder con las extensiones .html
- Los estilos están en línea dentro de cada HTML para evitar problemas de carga
- Firebase Auth funciona en localhost también
- El tema claro/oscuro se guarda en localStorage

## Solución de problemas

**¿No se ve el popup?**
- Abre la consola (F12) y ve si hay errores de Firebase
- Espera 8+ segundos después de cargar la página

**¿No aparecen los botones?**
- Presiona Ctrl+F5 para borrar cache
- Verifica que index.html esté cargando correctamente

**¿Firebase no conecta?**
- Verifica que tienes internet
- Comprueba que las reglas de seguridad de Firestore permiten lectura

## Próximos pasos

Una vez que todo funcione localmente:
1. Volvemos a Vercel con confianza
2. Configuramos URLs limpias (rewrite rules)
3. El sitio estará listo para producción
