# Periodontograma UNAN-León

Periodontograma clínico web que sigue la **Nomenclatura del Periodontograma** del Colectivo de Periodoncia, UNAN-León (mayo 2024). Es un solo archivo HTML: no requiere servidor, instalación ni base de datos.

## Funciones

- **Ficha completa por arcada** (FDI 18→28 y 48→38): margen gingival, sondaje, nivel de inserción calculado (sondaje − margen), línea mucogingival, furca vestibular/palatina, movilidad y percusión.
- **Seis sitios por diente** (D‑C‑M por vestibular y por palatino/lingual), con sangrado al sondaje y placa por sitio.
- **Dientes con anatomía por pieza**: incisivos, caninos, premolares y molares con sus raíces (tres en molares superiores, dos en inferiores) y vista oclusal con fisuras.
- **Hallazgos con el código de color del manual**:
  - Rojo: caries, borde defectuoso, endodoncia, lesión periapical, fístula, resto radicular, exudado.
  - Negro: fractura, desgaste, diastema, impactación de alimentos, gancho de removible, extracción indicada, dientes ausentes e incluidos.
  - Azul: amalgama, prótesis fija, diente de removible, implante, migración/rotación/extrusión.
  - Naranja: resina, provisional, carilla, endoposte.
  - Verde: línea mucogingival.
- Caries y restauraciones se dibujan **en la superficie elegida** (V, L/P, M, D, O/I) en la vista lateral y en la oclusal; la severidad cambia el tamaño.
- **Cuatro exámenes por paciente**: inicial, reevaluación al mes y dos mantenimientos, con opción de copiar el examen anterior.
- **Análisis**: sondaje y nivel de inserción promedio, % de sangrado, % de placa, sitios de 4–5 mm y ≥ 6 mm, evolución entre exámenes.
- **Reporte PDF** con ambas arcadas, hallazgos, simbología y evolución.
- **Exportar e importar JSON** para guardar o mover pacientes.

## Uso

1. Abre `index.html` en un navegador (o la página de GitHub Pages).
2. Toca un diente en la ficha para editarlo.
3. Registra los valores por sitio y agrega hallazgos eligiendo tipo, superficies y severidad.
4. Genera el PDF o exporta el JSON del paciente.

La app arranca con un **paciente de ejemplo**; el botón «Vaciar examen» lo borra.

## Datos y privacidad

Los datos se guardan solo en el navegador de quien usa la página (`localStorage`). Nada se envía a ningún servidor. Para respaldar o pasar un paciente a otro equipo, usa **Exportar JSON** e **Importar JSON**. Borrar los datos del navegador borra los pacientes no exportados.

## Publicar con GitHub Pages

1. Sube `index.html` y `README.md` a la raíz del repositorio.
2. En el repositorio: **Settings → Pages → Build and deployment**, elige *Deploy from a branch*, rama `main` y carpeta `/ (root)`.
3. La página quedará en `https://<usuario>.github.io/<repositorio>/`.

## Dependencias

Se cargan desde CDN, por lo que se necesita conexión a internet la primera vez:

- [jsPDF 2.5.1](https://github.com/parallax/jsPDF) (cdnjs) para el reporte PDF.
- Fuentes Atkinson Hyperlegible y JetBrains Mono (Google Fonts).

## Referencias

- Barahona J., Espinoza E., Ximénez A., Juárez G., Guevara Y. *Nomenclatura del Periodontograma*. Colectivo de Periodoncia, UNAN-León, 2024.
- Newman y Carranza. *Periodontología Clínica Esencial*. Elsevier, 2023.
