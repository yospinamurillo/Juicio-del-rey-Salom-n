# 👑 El Juicio de Salomón

> *"Escucha a ambos con el corazón, y la verdad se revelará"*

Una aplicación web que juzga conflictos con la sabiduría del Rey Salomón — escuchando lo que las palabras dicen y lo que el corazón calla. Impulsada por Claude AI (Anthropic).

---

## ¿Qué hace?

El usuario presenta un conflicto entre dos partes. La app analiza ambas voces con inteligencia emocional y emite un juicio sabio: no busca quién "tiene razón", sino qué es verdadero, justo y sanador para ambos.

**Casos de uso:**
- Conflictos entre personas (socios, familia, pareja, compañeros)
- Dilemas éticos o morales
- Decisiones difíciles con múltiples perspectivas
- Ejercicios de empatía y perspectiva

---

## Tecnología

| Elemento | Detalle |
|---|---|
| Frontend | HTML5 + CSS3 + JavaScript vanilla |
| IA | Claude Sonnet 4 via Anthropic API |
| Dependencias | Google Fonts (Cinzel + Lora) — solo para tipografía |
| Backend | Ninguno — corre directo en el navegador |

---

## Inicio rápido

### 1. Obtén tu API Key

Crea una cuenta en [console.anthropic.com](https://console.anthropic.com) y genera una API key.

### 2. Configura el archivo

Abre `salomon.html` en cualquier editor de texto y busca esta línea cerca del final:

```js
const ANTHROPIC_API_KEY = 'YOUR_API_KEY_HERE';
```

Reemplaza `YOUR_API_KEY_HERE` con tu clave real:

```js
const ANTHROPIC_API_KEY = 'sk-ant-api03-...';
```

### 3. Abre en el navegador

Doble clic sobre `salomon.html` — no necesita servidor local ni instalación.

---

## Estructura del proyecto

```
salomon.html      ← App completa (un solo archivo)
README.md         ← Este documento
```

---

## Cómo funciona

```
Paso I   → El usuario describe la posición de cada parte (A y B)
Paso II  → Agrega contexto adicional opcional (historia, emociones, lo que está en juego)
Paso III → La IA juzga como Salomón: en prosa fluida, con corazón y sabiduría
```

El prompt del sistema instruye al modelo a:

- Leer lo que se dice **y** lo que no se dice
- No buscar "quién gana" sino qué es justo y sanador
- Reconocer cuando ambas partes tienen razón, o ambas se equivocan
- Hablar en primera persona como Salomón, con voz serena
- Terminar con una frase de sabiduría o bendición

---

## Despliegue en producción

> ⚠️ Si despliegas esta app públicamente, **nunca expongas tu API key en el frontend**. Usa un backend como proxy.

### Opción A — Netlify Drop (más rápido)

1. Ve a [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arrastra `salomon.html` al navegador
3. Listo — URL pública en segundos

### Opción B — GitHub Pages

```bash
git init
git add salomon.html README.md
git commit -m "El Juicio de Salomón"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/salomon.git
git push -u origin main
```

Activa GitHub Pages en Settings → Pages → rama `main`.

### Opción C — Backend proxy (recomendado para producción pública)

Crea un servidor Node.js/Express en Railway o Render que reciba las peticiones del frontend y llame a la API de Anthropic desde el servidor, sin exponer la key al cliente.

---

## Personalización

| Qué cambiar | Dónde |
|---|---|
| Tono del juicio | Variable `systemPrompt` en el `<script>` |
| Longitud de respuesta | `max_tokens: 1000` y el prompt |
| Colores y tipografía | Variables CSS en `:root` |
| Idioma | Textos del HTML + prompt del sistema |
| Modelo de IA | `model: 'claude-sonnet-4-20250514'` |

---

## Funciones de la app

- Flujo de 3 pasos guiado
- Soporte para contexto adicional opcional
- Copiar juicio al portapapeles
- Imprimir juicio (diseño limpio para impresión)
- Reiniciar para un nuevo caso
- Diseño responsive (móvil y escritorio)

---

## Autor

Desarrollado por **Yesit Ospina** — [github.com/yesitospina](https://github.com/yesitospina)

---

## Licencia

MIT — libre para usar, modificar y distribuir.
