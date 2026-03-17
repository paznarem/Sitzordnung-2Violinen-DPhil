# 🎻 Sitzordnung — Segundos Violines

Generador de distribución de atriles para secciones de orquesta. Evita que siempre se sienten los mismos juntos.

## Funcionalidades

- **Plantilla flexible**: Añade/edita miembros con código numérico. Marca líderes (van siempre en atriles delanteros).
- **Generación inteligente**: Selecciona quién toca cada semana → genera atriles evitando repetir parejas recientes.
- **Historial**: Guarda cada semana. Consulta quién tocó con quién y cuándo.
- **Estadísticas**: Frecuencia de emparejamientos y participación de cada miembro.
- **Exportar/Importar**: Backup en JSON para no perder datos.
- **Imprimir**: Vista optimizada para imprimir y poner en el atril.

## Cómo funciona el algoritmo

1. Los **líderes** se asignan a los atriles delanteros (por orden de código).
2. A cada líder se le asigna el compañero con **menor coincidencia** en las últimas 4 semanas.
3. El resto se empareja aleatoriamente, **priorizando parejas nuevas** (greedy matching minimizando repeticiones recientes).
4. Los atriles traseros se barajan para mayor variedad.

## Despliegue en GitHub Pages

1. Clona este repo
2. Ve a **Settings → Pages → Source: main branch**
3. Listo — tu URL será `https://tu-usuario.github.io/sitzordnung/`

## Uso local

Simplemente abre `index.html` en un navegador. No requiere servidor, dependencias ni instalación.

## Datos

Todo se guarda en `localStorage` del navegador. Usa **Exportar JSON** para hacer backups.
