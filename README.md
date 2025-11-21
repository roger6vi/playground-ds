# Playground Design System (Estructura inicial)

Esta base prepara un monorepo para un Design System profesional compatible con:
- Web Components y adaptadores React
- Figma Code Connect y Dev Mode
- Integración con MCP (Model Context Protocol)
- API backend en Express + MongoDB

> ⚠️ No se incluyen componentes implementados. Solo se configura la arquitectura para empezar a generarlos.

## Estructura del monorepo

```
playground-ds/
	src/
		components/           # Un directorio por componente del Design System
		adapters/
			react/              # Adaptadores Web Component → React
		styles/
			tokens.css          # Tokens de diseño (CSS vars)
		index.js              # Entry point de la librería
		index.html            # Sandbox para pruebas manuales

	ds-config/              # Tokens y configuración del DS
		typography/
		colors/
		spacing/
		radii/
		shadows/
		motion/

	api/
		server.js             # Entrypoint Express (placeholder)
		routes/
		controllers/
		models/

	app/
		src/
			pages/
			components/
			App.jsx
			main.jsx
		package.json          # App React que consumirá el DS

	figma.config.json       # Configuración inicial para Code Connect
	package.json            # Configuración raíz (Workspaces)
	README.md
	.gitignore
```

## Próximos pasos sugeridos

1. Configurar paquetes (Vite, Rollup, Storybook, etc.) según necesidades.
2. Definir tokens en `ds-config` y sincronizarlos con `src/styles/tokens.css`.
3. Implementar los primeros Web Components en `src/components/<nombre>/`.
4. Crear adaptadores React correspondientes en `src/adapters/react/`.
5. Conectar la API Express con MongoDB y MCP para exponer tokens/componentes.
6. Integrar Code Connect CLI apuntando a `figma.config.json`.
