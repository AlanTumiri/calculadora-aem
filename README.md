# Calculadora de AEM

Calculadora de **árbol de expansión mínima / máxima** (Kruskal y Prim) con grafo en 3D, tabla de pasos, matriz de adyacencia y lectura de grafos desde una foto.

App web instalable en el celular (PWA). Hecha para la materia, funciona con cualquier grafo.

## Usar

Abrir la página publicada en GitHub Pages. En el celular: menú del navegador → **Agregar a pantalla de inicio** para usarla como app.

Flujo paso a paso:
1. Nodos — cuántos tiene el grafo.
2. Aristas — conectar nodos con su peso (a mano) o **📷 escanear una foto**.
3. Objetivo (mínimo/máximo) y método (Kruskal/Prim).
4. Resultado — grafo 3D animado, peso total, pasos y matriz.

## Leer fotos (API de Claude)

La lectura de fotos usa la API de Anthropic con **tu propia API key**:

- Se crea en https://console.anthropic.com/settings/keys
- Se pega en la app en **⚙ Ajustes**. Se guarda **solo en tu dispositivo** (localStorage), nunca en este repositorio.
- Cada foto analizada consume saldo de tu cuenta de Anthropic.

> No subas nunca tu API key a este repositorio ni la compartas: es pública y cualquiera podría gastar tu saldo.

## Archivos

- `index.html` — la app completa (lógica, 3D y lectura de foto).
- `manifest.webmanifest`, `sw.js`, `icon-*.png` — soporte PWA (instalación y uso offline del cálculo manual).

El cálculo (Kruskal/Prim) y el visor 3D funcionan sin internet una vez instalada; solo la lectura de fotos necesita conexión y la API key.
