# Household Finances in Spain: Income, Consumption & Wealth Distribution

<table align="center" style="width: 100%; border: none; border-collapse: collapse;">
  <tr>
    <td align="center" style="width: 33.3%; border: none; padding: 5px;">
      <img src="https://github.com/user-attachments/assets/9396b4d6-0a05-43b3-950c-daa757d7ae63" style="width: 100%; height: auto;" />
    </td>
    <td align="center" style="width: 33.3%; border: none; padding: 5px;">
      <img src="https://github.com/user-attachments/assets/a2115e74-02e6-43cc-8f36-2bb1e93bf90b"; height: auto;" />
    </td>
    <td align="center" style="width: 33.3%; border: none; padding: 5px;">
      <img src="https://github.com/user-attachments/assets/ea923d9f-ee0e-408a-894e-dbccff676e3f" style="width: 100%; height: auto;" />
    </td>
  </tr>
</table>




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
