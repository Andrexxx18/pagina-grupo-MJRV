# Página del equipo

Proyecto realizado como parte de la práctica **Git, GitHub, Tailscale y Gitea en equipos de 4**.

Una mini web estática donde cada integrante del equipo tiene su propia sección.

## Equipo

| Integrante | Rol | Sección |
|---|---|---|
| Nombre Apellido | Líder / Integrador | [`nombre.html`](./nombre.html) |
| Nombre Apellido | Anfitrión del servidor | [`nombre.html`](./nombre.html) |
| Nombre Apellido | Desarrollador / Revisor | [`nombre.html`](./nombre.html) |
| Nombre Apellido | Desarrollador / Documentador | [`nombre.html`](./nombre.html) |

## Estructura del proyecto

```
├── index.html        # Página principal con enlaces a cada sección
├── nombre1.html       # Sección individual de cada integrante
├── nombre2.html
├── nombre3.html
├── nombre4.html
└── README.md
```

Cada archivo `nombre.html` incluye: nombre, carrera, un hobby y una foto o emoji representativo. Además, cada integrante agrega en `index.html` un enlace a su propia sección.

## Cómo clonar y contribuir

```bash
git clone https://github.com/USUARIO-LIDER/pagina-equipo-N.git
cd pagina-equipo-N
git switch main
git pull
git switch -c feature/mi-seccion
# hacer los cambios...
git add .
git commit -m "Agrega sección de <nombre>"
git push -u origin feature/mi-seccion
```

Luego abrir un **Pull Request** hacia `main` y esperar la revisión de un compañero antes de fusionar.

## Flujo de trabajo

- La rama `main` está protegida: no se permiten cambios directos, todo pasa por Pull Request con al menos 1 aprobación.
- Cada tarea se desarrolla en su propia rama `feature/<descripción>`.
- Los conflictos de *merge* se resuelven localmente antes de continuar.

## Remotos

Este proyecto también se replica en un servidor **Gitea** propio, accesible mediante **Tailscale**:

```bash
git remote -v
# origin  -> https://github.com/USUARIO-LIDER/pagina-equipo-N.git
# gitea   -> http://<IP-tailscale-anfitrion>:3000/equipo-N/pagina-equipo-N.git
```

