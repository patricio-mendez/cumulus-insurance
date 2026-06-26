# Cumulus Seguros — Demo Web

Sitio web ficticio de Cumulus Seguros (insurance multi-ramo: auto, hogar, vida, salud), preparado para demos de **Agentforce** en industria de seguros. Hermano del sitio Cumulus Bank.

## Stack

- HTML/CSS/JS estático — sin build, sin dependencias.
- Paleta magenta (`#6B1F4D`) + coral (`#FF6B6B`) — diferenciada del azul/teal de Cumulus Bank.
- Calculadora de prima interactiva por tipo de seguro.

## Estructura

```
.
├── index.html      # Página única
├── .nojekyll       # Evita procesamiento Jekyll en GitHub Pages
├── .gitignore
└── README.md
```

## Publicación en GitHub Pages

1. Crear el repo en GitHub: `cumulus-insurance`
2. Desde esta carpeta:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Cumulus Seguros demo site"
   git branch -M main
   gh repo create cumulus-insurance --public --source=. --remote=origin --push --description "Cumulus Seguros - Insurance demo site (Cumulus Bank sibling)"
   gh api -X POST repos/patricio-mendez/cumulus-insurance/pages \
     -f "source[branch]=main" -f "source[path]=/"
   ```
3. URL final: `https://patricio-mendez.github.io/cumulus-insurance/`

## Diferencias visuales vs Cumulus Bank

| Asset | Cumulus Bank | Cumulus Insurance |
|---|---|---|
| Color primario | Azul `#0d3b6e` | Magenta `#6B1F4D` |
| Color CTA | Teal `#1ab8a0` | Coral `#FF6B6B` |
| Logo gradient | Azul → Teal | Magenta → Magenta Vibrante |
| Hero card | Tarjeta de crédito 3D | Escudo de protección 3D |
| Productos | Cuentas, Tarjetas, Préstamos, Inversiones | Auto, Hogar, Vida, Salud |
| Calculadora | Cuota de préstamo | Prima de seguro |

## MIAW Agent (pendiente)

El sitio NO incluye widget MIAW todavía. Se agregará el agente de seguros en la siguiente fase.

## Disclaimer

Cumulus Seguros es una marca ficticia creada exclusivamente para demos de Salesforce. Todos los datos, logos, métricas, testimonios y productos son inventados con fines ilustrativos.
