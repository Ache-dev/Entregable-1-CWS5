# LoginHome

Aplicación móvil desarrollada con [Expo](https://docs.expo.dev/versions/v57.0.0/) (React Native) que implementa un flujo de autenticación básico: **Login**, **Registro** y **Home**.

## Stack

- Expo ~57.0.21
- React 19 / React Native 0.86
- React Navigation (native-stack) para el enrutado entre pantallas
- TypeScript

## Estructura del proyecto

```
LoginHome/
├── App.tsx                # Navegador raíz (Stack: Login, Register, Home)
├── index.ts                # Punto de entrada de Expo
├── app.json                 # Configuración de Expo (nombre, iconos, splash)
├── assets/                  # Íconos y recursos gráficos
└── src/
    ├── theme/
    │   └── colors.ts         # Paleta de colores compartida por las vistas
    └── views/
        ├── Login.tsx         # Pantalla de inicio de sesión
        ├── Register.tsx      # Pantalla de registro
        └── Home.tsx          # Pantalla posterior al login
```

## Flujo de la app

1. **Login** (`src/views/Login.tsx`): valida que se ingresen correo y contraseña, y navega a `Home`. Incluye enlace a `Register`.
2. **Register** (`src/views/Register.tsx`): valida que se completen nombre, correo y contraseña, y navega a `Home`. Incluye enlace de regreso a `Login`.
3. **Home** (`src/views/Home.tsx`): pantalla de bienvenida con botón de "Cerrar sesión" que regresa a `Login`.

> Nota: la validación es solo de formulario (campos no vacíos); no hay backend ni persistencia de usuarios conectados todavía.

## Requisitos previos

- Node.js LTS
- npm
- App [Expo Go](https://expo.dev/go) en el celular, o un emulador Android/iOS configurado

## Instalación

```bash
npm install
```

## Ejecución

```bash
npm start        # abre el Metro Bundler / Expo Dev Tools
npm run android   # ejecutar en emulador/dispositivo Android
npm run ios       # ejecutar en simulador/dispositivo iOS
npm run web       # ejecutar en el navegador
```

Escanea el código QR con Expo Go (Android) o la app de Cámara (iOS) para abrir el proyecto en un dispositivo físico.
