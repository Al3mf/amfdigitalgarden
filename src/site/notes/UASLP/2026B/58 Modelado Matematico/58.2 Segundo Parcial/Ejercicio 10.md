---
{"dg-publish":true,"permalink":"/uaslp/2026-b/58-modelado-matematico/58-2-segundo-parcial/ejercicio-10/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

Janders Company vende varios productos para oficina y de ingeniería. Actualmente, Janders esta preparando la introducción de dos nuevas calculadoras: una para el mercado de oficinas , llamada Financial Manager, y otra para el mercado de ingeniería conocida como Technician. Cada calculadora tiene tres componentes: una base, un cartucho electrónico y una caratula o parte superior. En ambas se utiliza la misma base, pero los cartuchos y las caratulas son diferentes. La empresa puede fabricar todos los componentes, o puede adquirirlos de proveedores externos. Los costos de manufactura y los precios de adquisición de los componentes se resumen en la Tabla 1

Los encargados de pronósticos en Janders indican que serán necesarias 3000 calculadoras Financial Manager y 2000 Technician. Sin embargo, la capacidad de producción esta limitada. La empresa cuenta con 200 horas de tiempo normal de fabricación y 50 horas de tiempo extra que pueden utilizarse para la fabricación de calculadoras. El tiempo extra implica nu sobrecosto, a un costo adicional de 9 dólares la hora (tabla 2) muestra los tiempos de fabricación (en minutos) de dichos componentes


| <br>Componente      | Costo <br>Manufactura<br>(Tiempo Normal) | Costo<br>Adquisicion |
| ------------------- | ---------------------------------------- | -------------------- |
| Base                | $0.5                                     | $0.6                 |
| Cartucho Financial  | 3.75                                     | 4                    |
| Cartucho Technician | 3.3                                      | 3.9                  |
| Caratula Financial  | 0.6                                      | 0.65                 |
| Caratula Technician | 0.75                                     | 0.78                 |

| Componente          | Tiempo de<br>Manufactura |
| ------------------- | ------------------------ |
| Base                | 1                        |
| Cartucho Financial  | 3                        |
| Cartucho Technician | 2.5                      |
| Caratula Financial  | 1                        |
| Caratula Technician | 1.5                      |

MIN 0.5bm + 0.6bp +3.75fcm +4fcp + 3.3tcm +3.9tcp + 0.6ftm + 0.65ftp + 0.75ttm + 0.78ttp + 9ot
ST
bases) bm+bp=5000
carfin) fcm + fcp = 3000
cartec) tcm + tcp = 2000
carafin) ttm + ttp = 2000
hor_ext) ot <= 50
totman) bm + 3fcm + 2.5tcm + ftm + 1.5ttm - 0.6ot <= 12000
END

GINT 11

![Pasted image 20260924091831.png](/img/user/Pasted%20image%2020260924091831.png)