# Ejercicios Finales de Repaso

**1) Explica, en tus propias palabras, por qué es necesario que las computadoras representen los datos en binario.**

    Las computadoras necesitan representar los datos en binario porque el **binario** es su **idioma natural** y su funcionamiento interno está basado en componentes electrónicos que solo pueden distinguir entre dos estados físicos muy claros: **encendido/apagado o presencia/ausencia de corriente.**

**2) Convierte el número binario 10011011 a decimal y a hexadecimal.Convierte el número binario 10011011 a decimal y a hexadecimal.**

    128+16+8+2+1 = 155
    
    En decimal: 155

    Agrupamos el binario en bloques de 4 bits:

    1001 = 9

    1011 = B

    En hexadecimal: 9B

**3) Investiga y describe cómo se representa una imagen en formato PNG en el disco.**

    Una imagen en formato PNG (Portable Network Graphics) se guarda en el disco siguiendo una estructura muy organizada que garantiza compresión sin pérdida y soporte para transparencia.

 **Un archivo PNG está compuesto por:**

 **Firma (Signature):**

    Los primeros 8 bytes identifican el archivo como PNG.
    
    En hexadecimal: 89 50 4E 47 0D 0A 1A 0A.

**Chunks (bloques de datos):**

    El resto del archivo se divide en secciones llamadas chunks. Cada chunk tiene:

**Longitud (4 bytes)**: 

    tamaño del bloque de datos.

    Tipo (4 bytes): código que indica qué tipo de información contiene (ej. IHDR, IDAT).

    Datos: contenido específico del bloque.

    CRC (4 bytes): verificación de integridad.

**los chunk más importantes son**

    IHDR: Encabezado con dimensiones, profundidad de color, tipo de color, método de compresión.

    PLTE: Paleta de colores (si se usa).

    IDAT: Datos de la imagen comprimidos con zlib/deflate.

    IEND: Marca el final del archivo.

    Otros opcionales: tEXt (texto), tIME (fecha), gAMA (gamma), etc.


**Compresión:**
    
    Los píxeles se almacenan en los chunks IDAT, comprimidos con el algoritmo DEFLATE.

    Esto permite que el archivo sea más pequeño sin perder calidad.

**Transparencia:**

    PNG soporta canal alfa (transparencia) de 8 bits, lo que lo hace ideal para gráficos en la web.

**4) Analiza la siguiente situación: ¿Qué sucede si intentas almacenar un número mayor al que puede representar un byte (por ejemplo, 300)? ¿Cómo lo maneja Python?**

    En Python int: no hay problema, 300 se guarda tal cual.

    En Python bytes: da error porque excede el rango permitido.

    En lenguajes de bajo nivel: se produce un desbordamiento y el número se ajusta automáticamente.