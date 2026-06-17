# Household Finances in Spain: Income, Consumption & Wealth Distribution
<img width="859" height="748" alt="image" src="https://github.com/user-attachments/assets/4c694356-33e3-47a7-9c23-4f7cf695e91f" />
<img width="803" height="739" alt="image" src="https://github.com/user-attachments/assets/d73a1390-8351-44fb-a6dc-70cc60458dd3" />


> **Estado: en desarrollo (work in progress).** Proyecto personal de investigación.
> Autor: Pablo Monrocle Arribas.

Análisis cuantitativo de la distribución de la **renta, la riqueza y el consumo** de los
hogares en España entre **2002 y 2020**, con un doble enfoque **intrageneracional**
(percentiles/deciles) e **intergeneracional** (grupos de edad del cabeza de familia).

## Contenido del análisis
- **Renta**: salarios por hora y mensuales, renta laboral individual y del hogar,
  renta bruta total y per cápita; descomposición por fuentes de ingreso.
- **Consumo**: consumo total y per cápita, desglose en bienes duraderos y no duraderos,
  y desigualdad entre/within grupos (descomposición de la varianza).
- **Riqueza**: riqueza bruta y neta, líquida e ilíquida; endeudamiento de los hogares
  (ratios deuda/riqueza y deuda/ingreso).
- **Movilidad social**: dinámica de percentiles para hogares jóvenes (24–34).
- **Econometría**: regresión cuantílica para la persistencia de ingresos frente a shocks
  y elasticidad consumo–renta por riqueza y edad.

## Datos
- **EFF** — Encuesta Financiera de las Familias (Banco de España), olas 2002–2020.
- **EES** — Encuesta de Estructura Salarial (INE).
- **EU-SILC** — Eurostat (comparativa europea).

> **Los microdatos NO se incluyen en el repositorio** por sus condiciones de uso.
> Proximamente se creara un file llamado `data/README.md` para las fuentes y cómo obtenerlos.

## Metodología (resumen)
- Ponderación e imputación múltiple de la EFF; deflactado por IPC (INE), base 2020.
- Descomposición de la varianza (entre grupos / dentro de grupos) siguiendo
  Krueger & Perri (2006).
- Regresión cuantílica con polinomios de Hermite para persistencia de ingresos
  (Arellano & Bonhomme, 2017) y elasticidad consumo–renta (Basso et al., 2017).
- Cálculos en **Stata 14 MP**; tablas y figuras en **LaTeX**.

## Estructura del repositorio
- `latex/`     — Documento, tablas y figuras en LaTeX (.tex)
- `figures/`   — Gráficos generados (PDF/PNG)
- `do_files/`  — Scripts de Stata (.do)
- `output/`    — Resultados intermedios (tablas exportadas, logs)
- `docs/`      — Borradores y notas
- `data/`      — **Vacío.** Microdatos no incluidos (ver `data/README.md`)

## Cómo reproducir
1. Obtener los microdatos de la EFF, EES y EU-SILC y colocarlos en `data/`.
2. Ejecutar los `.do` de `do_files/` en orden.
3. Compilar los `.tex` de `latex/` con pdfLaTeX.

## Licencia
Proyecto personal. Todos los derechos reservados © Pablo Monrocle Arribas.
