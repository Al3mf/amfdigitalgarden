---
{"dg-publish":true,"permalink":"/uaslp/2026-b/58-modelado-matematico/58-2-segundo-parcial/ejercicio-11/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

La principal sucursal del Burlington Bank en Vermont requiere de 8 a 15 cajeros de servicio, dependiento de la hora del dia, como se indica en la tabla. Los cajeros de tiempo ocmpleto trabajan 8 horas consecutivas a $15 la hora, comenzando a las 8am, 10am y 12pm. Las regunlaciones sindicales requieren que a toda hora al menos 60% de los cajeros sean de tiempo completo. Como gerente del departamento personal, haga una recomendacion respecto al numero de empleados de tiempo completo y de tiempo parcial requeridos a lo largo del dia para minimizar el costo diario total

| Periodo   | Numero minimo de<br>Cajeros |
| --------- | --------------------------- |
| 8am-10am  | 8                           |
| 10am-12pm | 10                          |
| 12pm-2pm  | 15                          |
| 2pm-4pm   | 12                          |

MIN 15xt + 8x1 + 8x2 + 8x3
->
MIN 120xt + 32x1 +32x2 + 32x3
ST
xt+x1>=8
xt+x2+x2>=10
xt+x2+x3>=15
xt+x3>=12

0.4xt - 0.6x1 >= 0
0.4xt - 0.6x1 - 0.6x2 >= 0
0.4xt - 0.6x2 - 0.6x3 >= 0
	0.4xt - 0.6x3 >= 0

![Pasted image 20260924093838.png](/img/user/Pasted%20image%2020260924093838.png)