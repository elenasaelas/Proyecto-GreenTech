# 🌿 Proyecto GreenTech MVP Sostenibilidad
---

## ¿Qué había en el `index.html` original?

Una web que pero cargaba medio megabyte de librerías para hacer cosas mínimas: un botón verde, un icono de hoja y el año en el footer.

Bootstrap, jQuery, Font Awesome, Moment.js, Google Fonts. Cinco dependencias, siendo ninguna necesaria.

---

## ¿Qué se refactorizó en el código?

Se eliminó todo lo que sobraba y se reemplazó con lo que el navegador ya sabe realizar por defecto:

- El botón y el layout → CSS nativo
- El icono de hoja → emoji 🌿, sin librería
- Las fuentes → las que ya tiene instaladas el teléfono del usuario
- El año en el footer → escrito directamente en el HTML
- La imagen → se sirve en el tamaño justo según el dispositivo, y solo se descarga cuando el usuario la va a ver (`loading="lazy"` + `srcset`)

Resultado: de ~570 KB de dependencias externas a 0.

---

## ¿Por qué estos cambios son importantes?

Cada byte que una web transfiere consume energía: en el servidor, en la red y en el dispositivo del usuario. Una web pesada calienta la CPU, agota la batería y hace que los móviles de gama media se queden cortos antes de tiempo. Eso acelera que la gente compre un móvil nuevo, y el viejo acaba en la basura.
Hacer software ligero es una forma concreta de reducir ese ciclo.

---

## Estructura del proyecto
```
GreenTech-MVP-Sostenible/
├── index.html
├── style.css
└── README.md
```

---
## Referencias (IEEE)

[1] W3C, "Web Sustainability Guidelines (WSG) 1.0," World Wide Web Consortium, 2023. [Online]. Available: https://www.w3.org/TR/wsgl/

[2] Green Software Foundation, "Green Software Practitioner Course," 2024. [Online]. Available: https://learn.greensoftware.foundation/

[3] R. Verdecchia, P. Lago, I. Malavolta, y G. Procaccianti, "Green IT and Green Software Engineering: A Systematic Mapping Study," arXiv preprint arXiv:2102.04945, 2021. [Online]. Available: https://arxiv.org/abs/2102.04945
