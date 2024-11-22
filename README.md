# codigo

```
function procesarArchivo(nombre) {
  return new Promise((resolve) => {
    console.log(`Procesando archivo: ${nombre}`);
    setTimeout(() => {
      console.log(`Archivo procesado: ${nombre}`);
      resolve(); // Marca la promesa como resuelta
    }, 2000); // Simula el tiempo de procesamiento
  });
}

const archivos = ["archivo1.txt", "archivo2.txt", "archivo3.txt"];

Promise.all(archivos.map(procesarArchivo))
  .then(() => console.log("Todos los archivos han sido procesados."));

```

**salida**

```
Producción:

Procesando archivo: archivo1.txt
Procesando archivo: archivo2.txt
Procesando archivo: archivo3.txt
Archivo procesado: archivo1.txt
Archivo procesado: archivo2.txt
Archivo procesado: archivo3.txt
Todos los archivos han sido procesados.
```
