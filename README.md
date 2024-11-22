# codigo

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


**salida**

![image](https://github.com/user-attachments/assets/d249377b-9ecb-4465-bb88-ede0dbd4d21b)
