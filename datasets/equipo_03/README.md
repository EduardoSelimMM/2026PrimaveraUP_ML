# Equipo

+ García Ortiz Gustavo Isaí
+ Téllez Paniagua Gael
+ Carreiro Muradas Rodrigo
+ Martínez De la Parra Félix Emiliano

## Fecha de exposición:
22 de mayo de 2026. 25 minutos.

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

ticker_ipc = "^MXX"

fecha_inicio = "2022-01-01"
fecha_final = "2026-03-31"

datos_acciones = yf.download(lista_tickers_ipc, start = fecha_inicio, end = fecha_final,
                             group_by='ticker', auto_adjust = True, progress = False)

datos_ipc = yf.download(ticker_ipc, start = fecha_inicio, end = fecha_final, group_by='ticker',
                        auto_adjust = True, progress = False)
```
