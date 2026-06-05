# AppM Flutter Números Primos

Aplicación desarrollada en Flutter que muestra números primos de forma secuencial cada vez que el usuario presiona el botón de incremento.

## Requisitos

Antes de ejecutar el proyecto, es necesario tener instaladas las siguientes herramientas:

* Flutter SDK
* Android Studio
* Android SDK
* Git
* Visual Studio Community (opcional, para aplicaciones Windows)
* Google Chrome o Microsoft Edge (opcional, para Flutter Web)

---

# Instalación de Flutter en Windows

## 1. Descargar Flutter

Descargar Flutter desde el sitio oficial:

https://flutter.dev/docs/get-started/install/windows

Extraer el contenido en una carpeta, por ejemplo:

```text
C:\Flutter\flutter
```

---

## 2. Configurar las Variables de Entorno

Agregar la siguiente ruta al PATH de Windows:

```text
C:\Flutter\flutter\bin
```

Pasos:

1. Buscar "Variables de entorno" en Windows.
2. Seleccionar "Editar las variables de entorno del sistema".
3. Abrir "Variables de entorno".
4. Editar la variable Path.
5. Agregar:

```text
C:\Flutter\flutter\bin
```

6. Guardar los cambios.
7. Reiniciar la terminal.

---

## 3. Verificar la Instalación

Ejecutar:

```bash
flutter --version
```

o

```bash
flutter doctor
```

Si aparece:

```text
"flutter" no se reconoce como un comando interno o externo
```

significa que Flutter no se encuentra agregado correctamente al PATH.

---

# Solución de Problemas Encontrados

## Error: Could not find a Flutter SDK

Mensaje:

```text
Could not find a Flutter SDK.
Please download, or, if already downloaded, click 'Locate SDK'.
```

### Solución

Configurar Android Studio:

File → Settings → Languages & Frameworks → Flutter

Seleccionar la ruta:

```text
C:\Flutter\flutter
```

No seleccionar:

```text
C:\Flutter\flutter\bin
```

---

## Error: Flutter no se reconoce como comando

Mensaje:

```text
flutter no se reconoce como un comando interno o externo
```

### Solución

Agregar al PATH:

```text
C:\Flutter\flutter\bin
```

Verificar:

```bash
where flutter
```

Resultado esperado:

```text
C:\Flutter\flutter\bin\flutter.bat
```

---

## Error: Visual Studio not installed

Mensaje:

```text
Visual Studio not installed; this is necessary to develop Windows apps.
```

### Solución

Instalar Visual Studio Community.

Durante la instalación seleccionar:

```text
Desarrollo de escritorio con C++
```

(Desktop Development with C++)

Este requisito es únicamente para aplicaciones Windows.

---

## Error: Cannot find Chrome executable

Mensaje:

```text
Cannot find Chrome executable
```

### Solución

Instalar Google Chrome o utilizar Microsoft Edge.

Para ejecutar con Edge:

```bash
flutter run -d edge
```

Si el proyecto es únicamente para Android, este error puede ignorarse.

---

# Inicializar Git en el Proyecto

Al intentar conectar GitHub apareció:

```text
fatal: not a git repository
```

### Causa

El proyecto no tenía inicializado Git.

### Solución

```bash
git init
```

Agregar archivos:

```bash
git add .
```

Crear commit:

```bash
git commit -m "Primer commit"
```

Conectar con GitHub:

```bash
git remote add origin https://github.com/Roger-grff/AppM_flutter_NPrimos-.git
```

Subir el proyecto:

```bash
git branch -M main
git push -u origin main
```

---

# Funcionalidad de la Aplicación

La aplicación genera números primos de forma consecutiva.

Cada vez que el usuario presiona el botón:

```text
2
3
5
7
11
13
17
19
...
```

### Lógica utilizada

```dart
bool esPrimo(int n) {
  if (n < 2) return false;

  for (int i = 2; i <= n ~/ 2; i++) {
    if (n % i == 0) {
      return false;
    }
  }

  return true;
}

void _incrementCounter() {
  setState(() {
    do {
      _counter++;
    } while (!esPrimo(_counter));
  });
}
```

---

# Ejecución del Proyecto

Obtener dependencias:

```bash
flutter pub get
```

Ejecutar en Android:

```bash
flutter run
```

Verificar dispositivos:

```bash
flutter devices
```

Diagnóstico general:

```bash
flutter doctor
```

---

# Autor

Roger Greff

Tecnologías utilizadas:

* Flutter
* Dart
* Android Studio
* Git
* GitHub

