# Estudio de caso XAI — Sitios de anidación de la tórtola senegalesa

Asignatura *Explicar no es entender: IA explicativa y sus límites causales* (Universidad Santo Tomás).

## Correcciones aplicadas a la entrega original

1. **Diagnóstico de proxies incompleto**: el código de correlaciones detecta 5 pares de
   variables con |r| > 0.15 (`HEIGHT↔CEILING`, `HEIGHT↔H_CEILING`, `HEIGHT↔BUILD_DIST`,
   `HEIGHT↔NEST_DIST`, `TREE_DIST↔BUILD_DIST`), pero el informe original solo discutía
   uno de ellos. Se corrigió el texto (notebook e informe) para reportar los 5 pares y
   se comparó explícitamente con el ejemplo de la guía (`TREE_DIST`↔`GREEN_DIST`, que
   en estos datos resulta poco relevante, r = 0.075).
2. **Gráfico de resumen SHAP faltante**: la guía pide "ranking por la media de |SHAP| y
   gráfico de resumen"; solo existía el ranking en barras. Se añadió el *beeswarm plot*
   (`shap.summary_plot`), que muestra dirección y dispersión del efecto por sitio.
3. **ALE no utilizado**: `PyALE` estaba instalado pero nunca se usaba, pese a que la
   dependencia entre HEIGHT y otras variables (punto 1) justifica el gráfico ALE que
   pide la guía como complemento del PDP/ICE. Se añadió el ALE de HEIGHT.
4. **Enlace reproducible**: se sube el cuaderno ejecutado de extremo a extremo, el
   informe técnico y los datos a este repositorio para cumplir con el requisito de
   entrega de un enlace reproducible (GitHub).

## Contenido

- `IAExplicativayLimites_LauraMedina.ipynb`: cuaderno ejecutado de extremo a extremo.
- `InformeIA-Limites_LauraMedina.pdf`: informe técnico (APA 7, Arial 11, 6 páginas).
- `Sitios_anidacion_tortola.xlsx`: datos originales (Banisaffar y Alizadeh Shabani, 2024).
