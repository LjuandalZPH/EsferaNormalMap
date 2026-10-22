<div align="center">

# Esferita: Normal Map en Unity

**Una esfera roja, un mapa de normales con mi nombre y luces de colores.**

![Unity](https://img.shields.io/badge/Unity-2022.3.62f3-black?logo=unity&logoColor=white)
![Render Pipeline](https://img.shields.io/badge/Render%20Pipeline-URP-blue)
![Estado](https://img.shields.io/badge/Estado-Completado-brightgreen)

</div>

---

## Sobre el proyecto

Este proyecto es una práctica de **Unity** sobre texturizado e iluminación. Se construyó una escena 3D con una esfera a la que se le aplicó un material con una textura con mi nombre, importada como **mapa de normales (Normal map)**, y se iluminó con luces puntuales de colores.

Cada etapa del trabajo quedó registrada en un commit de git, siguiendo el orden pedido en la tarea.

## Qué contiene la escena

| Objeto | Descripción |
|---|---|
| **Esferita** | Esfera 3D en el centro de la escena (posición `0, 0, 0`). Lleva el material `DavMaterial`. |
| **Main Camera** | Cámara que enfoca la esfera. |
| **Directional Light** | Luz direccional blanca (intensidad 2) que actúa como luz general. |
| **Point Light (verde)** | Luz puntual verde, intensidad 10 y rango 3, colocada junto a la esfera. |
| **Point Light (morada)** | Luz puntual morada, intensidad 10 y rango 10, colocada junto a la esfera. |

## Material y textura

- **Material:** `DavMaterial`, con shader *Universal Render Pipeline/Lit*.
- **Color base:** rojo. La esfera se ve roja y conserva la textura por encima.
- **Textura:** `DavidMap.png` (1013 × 470 px), una imagen con mi nombre.
- **Importación:** la textura está configurada con *Texture Type = Normal map*, que es lo que permite que Unity la interprete como vectores de superficie y no como una foto de color.

> **¿Qué es un mapa de normales?**
> Es una imagen cuyos canales de color (RGB) guardan la dirección de la normal de la superficie en cada píxel. Al iluminar, Unity usa esas normales en lugar de las del polígono, de modo que la superficie parece tener relieve **sin agregar geometría**. La forma real de la esfera no cambia, solo su respuesta a la luz.

## Historial de commits

El trabajo se hizo en este orden:

| # | Commit | Qué se hizo |
|:-:|---|---|
| 1 | `creacion de la esfera` | Se creó el proyecto y se agregó la esfera a la escena. |
| 2 | `texturizando esfera` | Se importó la textura con mi nombre, se creó el material y se aplicó a la esfera. |
| 3 | `agregando luz` | Se agregó una luz puntual de color junto a la esfera. |
| 4 | `coloreando esfera de rojo` | Se cambió el color del material a rojo. |

## Cómo abrir el proyecto

1. Instala **Unity 2022.3.62f3** (LTS) desde Unity Hub.
2. Clona el repositorio:
   ```bash
   git clone https://github.com/LjuandalZPH/EsferaNormalMap.git
   ```
3. En Unity Hub pulsa **Add** y selecciona la carpeta clonada.
4. Abre la escena `Assets/Scenes/SampleScene.unity`.

La primera vez Unity tarda unos minutos en importar los paquetes y generar la carpeta `Library`, que no se sube a git.

## Estructura del proyecto

```
Assets/
├── Assets/
│   ├── DavidMap.png        # Textura con mi nombre (Normal map)
│   └── DavMaterial.mat     # Material rojo de la esfera
├── Materials/              # Materiales adicionales de prueba
├── Scenes/
│   └── SampleScene.unity   # Escena principal
└── Settings/               # Configuración de URP
```

## Herramientas usadas

- **Unity 2022.3.62f3** con *Universal Render Pipeline (URP)*
- **Git** y **GitHub** para el control de versiones

## Autor

**David Pinto**
