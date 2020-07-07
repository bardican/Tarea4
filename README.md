# Tarea 4

## Modulación BPSK
Se inicia con el apartado de modulación mediante una onda sinusoidal, donde para BPSK cada 1 enviado corresponde a la onda en su forma corriente, y para cada 0 que se desee enviar el inverso de esta onda. Como se puede apreciar en la siguiente figura:

![Modulación](https://github.com/bardican/Tarea4/blob/master/Modulada_BPSK.png)

Por otro lado, con respecto a la densidad espectral de potencia, se encontró lo siguiente:

![DEP](https://github.com/bardican/Tarea4/blob/master/DEP.png)

Esto quiere decir que la distribución de la potencia decae conforme el rango de frecuencias se amplía, y los picos de energía se agrupan conforme a cada periodo.

## Canal Ruidoso

Ahora bien, se desea que esta onda pase por un canal ruidoso a distintas relación señal a ruido (SNR). Para ello s e emplea la creación de vector con datos distribuidos normalmente, lo que se conoce como ruido gaussiano blanco. Con ello, se obvieron las siguientes densidades espectrales de potencia:

![DEP1](https://github.com/bardican/Tarea4/blob/master/DEP1.png) ![DEP2](https://github.com/bardican/Tarea4/blob/master/DEP2.png) ![DEP3](https://github.com/bardican/Tarea4/blob/master/DEP3.png) ![DEP4](https://github.com/bardican/Tarea4/blob/master/DEP4.png) ![DEP5](https://github.com/bardican/Tarea4/blob/master/DEP5.png) ![DEP6](https://github.com/bardican/Tarea4/blob/master/DEP6.png)

## Demodulación

Para solucionar ese apartado, se consideró que como la energía o potencia en los casos donde la onda es negativa la potencia también. Por lo que para definir cuando aparece un 1, se aplica un if para E > 0. Dando como resultado que independientemente del valor de SNR del rango dado, el decodificador funciona sin errores, tal y como se aprecia:

![DEM](https://github.com/bardican/Tarea4/blob/master/BERvsSNR.png)

## Conclusión

Se obtienen en el receptor los bits tal y como fueron enviados, la cantidad de ruido del canal a pesar de ser alta  no dificultó la labor del demodudador BPSK.

