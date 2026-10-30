# 0192210-leonardo-geney-iac-aws

Despliegue automático de una instancia EC2 con Apache en AWS usando **CloudFormation** (Infraestructura como Código) y **GitHub Actions**.

- **Estudiante:** Leonardo Geney — 0192210
- **Programa:** Ingeniería de Sistemas — UFPSO Ocaña
- **Asignatura:** Cloud Computing
- **Docente:** Wilder Andrés Duarte Neira

## Estructura

```
.
├── .github/
│   └── workflows/
│       └── deploy.yml      # Flujo de GitHub Actions
├── templates/
│   └── template.yaml       # Plantilla CloudFormation (EC2 + Security Group + User Data)
└── README.md
```

## Funcionamiento

1. Cada `push` a `main` ejecuta el workflow `deploy.yml`.
2. GitHub Actions se autentica en AWS con los secretos del repositorio.
3. Se despliega el stack `proyecto-web-iac` con la plantilla `templates/template.yaml`.
4. La instancia EC2 instala Apache vía User Data y publica `index.html`.

## Sitio web

URL: http://IP_PUBLICA  <!-- reemplazar con el valor WebsiteURL del stack -->
