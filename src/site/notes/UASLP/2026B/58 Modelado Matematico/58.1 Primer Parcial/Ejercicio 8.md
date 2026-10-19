---
{"dg-publish":true,"permalink":"/uaslp/2026-b/58-modelado-matematico/58-1-primer-parcial/ejercicio-8/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

La refineria Azteca produce dos tipos de gasolina sin plomo: regular y extra, los cuales vende a su cadena de estaciones de servicio en $12 y $14 por barril respectivamente. Ambos tipos se preparan del inventario de la azteca de petroleo nacional refinado y de petroleo importado refinado, y deben cumplir con las siguientes especificaciones:

|         | Presion maxima<br>de vapor | Octanaje<br>minimo | Demanda maxima<br>de barriles/semana | Entregas minimas<br>barriles/semana |     |
| ------- | -------------------------- | ------------------ | ------------------------------------ | ----------------------------------- | --- |
| Regular | 23                         | 88                 | 100 000                              | 50 000                              | $12 |
| Extra   | 23                         | 93                 | 20 000                               | 5 000                               | $14 |

Las características del inventario de petróleos refinados son las siguientes:

|           | Presion de <br>vapor | Octanaje | Inventario<br>barriles | Costo<br>$ / barril |
| --------- | -------------------- | -------- | ---------------------- | ------------------- |
| Nacional  | 25                   | 87       | 40 000                 | $8                  |
| Importado | 15                   | 98       | 60 000                 | $15                 |


Que cantidades de los dos petróleos (nacional e importado) deberá mezclar la Azteca en ambas gasolinas, a fin de maximizar la ganancia semanal?

Los componentes de una mezcla contribuyen al octanaje general, según sus porcentajes por peso, asimismo para la presión de vapor

12(x1+x2) + 14(x3+x4) - 8(x1+x3) - 15(x2+x4)
12x1+12x2+14x3+14x4-8x1-8x3-15x2-15x4
MAX 4x1-3x2+6x3-x4

RESTRICCIONES
(87x1+98x2)/(x1+x2)>=88
87x1+98x2 >= 88x1+88x2
-x1+10x2>=0

87x3+98x4)/(x3+x4)>=93
-6x3+5x4>=0

(25x1+15x2)/(x1+x2)<=23
2x1-8x2<=0
2x3-8x4<=0

x1+x2 <= 100 000
x3+x4 <= 20 000
x1+x2>= 50 000
x3+x4>=5 000
x1+x2<=40 000
x3+x4<=60000
x1+x2+x3+x4>=0

![Pasted image 20260917094850.png](/img/user/Pasted%20image%2020260917094850.png)