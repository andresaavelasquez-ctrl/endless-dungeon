# Endless Dungeon v0.2

Juego web estático: entorno 3D, personaje 2D y mazmorras procedurales por sectores. No requiere npm ni compilación.

## Probar en Termux

```bash
pkg update
pkg install python git gh unzip
cd ~/storage/downloads/dungeon-web-game-v0.2
python -m http.server 8080
```

Abre `http://127.0.0.1:8080`.

## Crear repositorio y subir

```bash
git init
git add .
git commit -m "Endless Dungeon v0.2"
git branch -M main
gh auth login
gh repo create endless-dungeon --public --source=. --remote=origin --push
```

## Activar GitHub Pages una vez

En GitHub: `Settings > Pages > Build and deployment > Source: GitHub Actions`.

Desde ese momento cada `git push` a `main` publica automáticamente la actualización.

```bash
git add .
git commit -m "Nueva actualización"
git push
```

## Controles

- WASD/flechas: movimiento.
- Q/E: girar cámara.
- Móvil: controles en pantalla.
- Al cruzar un extremo se genera un sector nuevo usando la misma semilla.
