# ENTREGA PRUEBA MF 0493: Gestor de Tareas

## URL's de backend y frontend, tanto de repositorios github como de netlify y render:
1. URL repositorio backend:
   https://github.com/jesuscaso/backend-todo-app.git
2. URL repositorio frontend:
   https://github.com/jesuscaso/frontend-todo-app.git
3. URL Netlify:
   https://gestortareasjesus.netlify.app
4. URL Render:
   https://backend-todo-app-izhu.onrender.com/api/tareas

## Pasos instalación Backend
1. Hacemos login en Render
2. Pulsamos en Añadir nuevo -> Web Service
3. Introducimos la url del repositorio de Github que contiene el código fuente del backend
4. Introducimos "npm start" en "Start Command"
5. Seleccionamos "Free" en "Instance Type"
6. En "Environment Variables" introducimos estas dos: 
   ```
   MONGO_URI=mongodb+srv://<usuario>:<password>@<cluster>.mongodb.net/tareas (cambiar usuario y password por los que correspondan)
   PORT=3000
   ```
7. Pulsamos en "Deploy Web Service"
8. Una vez que termine el despligue correctamente copiamos la url del servicio web que aparece en la parte superior del Dashboard de Render

## Pasos instalación Frontend
1. Hacemos login en Netlify
2. Pulsamos en "Add new site"
3. Seleccionamos "Import an existing project"
4. En "Let’s deploy your project with…" seleccionamos "GitHub"
5. Seleccionamos el repositorio de Github que contiene el código fuente del frontend
6. En "Site name" introducimos el nombre que queremos dar al sitio
7. En "Build command" introducimos "npm run build"
8. En "Publish directory" introducimos "dist"
9. Pulsamos "Add environment variables" y añadimos la siguiente variable:
   ```
   VITE_API_URL=https://<tu-api-backend>.onrender.com/api/tareas (será la url que copiamos en el paso 8 de la instalación del Backend)
   ```
10. Pulsamos en "Deploy <nombre-del-sitio>"