## 1) Verificación de peso de despegue

**En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.**

**Variables de entrada**
    
    Peso_maximo
    peso_combustible
    peso_carga

**Variables de salida**

    peso_total_Aeronave


**INICIO**

    Imprimir: Cual es el peso maximo que puede tener la a eronave

    Leer: Peso_Maximo

    Imprimir: Cual es el peso del combustible que hay en la aeronave

    Leer: peso_combustible

    Imprimir: Cual es el peso de la carga que lleva la aeronave

    Leer: peso_carga

    peso_total_aeronave = peso_combustible + peso_carga

**SI** (peso_total_aeronave ≤ peso_maximo)

    Imprimir: La aeronave puede volar

**SINO** 

    Imprimir: La aeornave no puede volar

**FIN**

## 3) Registro de altitudes de vuelo

Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.

**Variables de entrada**

Altitudes= 6
tiempo = 0
Altitud

**Variables de salida**

Medicion_final


    INCIO
        
        Imprimir: cual es la altitud en el momento

        mientras (Altitudes < 6)
        
            leer: altitud

            altitudes = altitud
            
            tiempo = tiempo + 10
            
        fin mientras

        medicion_final = altitutdes

        Imprimir: medición_final



## 6) Control de temperatura en cabina

Un sistema mide cada 5 minutos la temperatura en cabina durante una hora. Si en algún momento se detecta una temperatura mayor a 27°C o menor a 18°C, debe indicar que se active el sistema de climatización.

**Variables de entrada**
    
    temperatura
    temperatura_cabina

**variables de salida**


    INICIO

        




