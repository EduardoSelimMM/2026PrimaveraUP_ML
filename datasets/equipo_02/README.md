# Equipo

+ Alcocer Cancino Kevin Eliuth
+ Gómez Perroni Iñaki
+ González Aguilar Diego
+ Estudiante pendiente
+ Estudiante pendiente

## Fecha de exposición:
15 de mayo de 2026. 30 minutos.

## Conjunto de datos

```
import pandas as pd
import yfinance as yf

lista_tickers_ipc = [
    "AC.MX", "ALPEKA.MX", "ALSEA.MX", "AMXB.MX", "ASURB.MX", 
    "BBAJIOO.MX", "BIMBOA.MX", "BOLSAA.MX", "CEMEXCPO.MX", "CHDRAUIB.MX", 
    "CUERVO.MX", "ELEKTRA.MX", "FEMSAUBD.MX", "GAPB.MX", "GCARSOA1.MX", 
    "GCC.MX", "GENTERA.MX", "GFNORTEO.MX", "GNP.MX", 
    "GRUMAB.MX", "ORBIA.MX", "PE&OLES.MX", "PINFRA.MX", "Q.MX", 
    "RA.MX", "TLEVISACPO.MX", "VESTA.MX", "VOLARA.MX", 
    "WALMEX.MX"
]

fecha_inicio = "2022-01-01"
fecha_final = "2026-03-31"

datos = yf.download(lista_tickers_ipc, start = fecha_inicio, end = fecha_final,
group_by='ticker', auto_adjust = True, progress = False)
```

## Instrucciones

Para el histórico de cada acción calcular:

1. Volumen promedio
2. Rendimiento diario promedio
3. Volatilidad del rendimiento diario
4. Skewness del rendimiento diario
5. Curtosis del rendimiento diario
6. Sharpe-Ratio
7. Rango intradia promedio. Promedio de cuánto varía el precio entre el máximo y el mínimo de cada día.
8. Rango horario promedio. Promedio de cuánto varía el precio entre el precio de cierre y el precio de apertura de cada día.
9. Up/Down Volume Ratio. Suma del volumen en días alcistas dividida por la suma del volumen en días bajistas.

Esto le dejará un renglón de 9 entradas por cada acción.

Con los renglones de todas las acciones, llevar a cabo clustering por k-medias, DBSCAN y clustering aglomerativo.

El objetivo es intentar entender si podemos agrupar a las acciones.

¿La ventana de tiempo de observación tiene algún efecto?

