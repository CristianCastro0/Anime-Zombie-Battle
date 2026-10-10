<p align="center">
  <img src="Marketing/Steam/AnimeZombieBattleBanner.png" alt="Anime Zombie Battle" width="100%">
</p>

<p align="center">
  <strong>Sobrevive a la horda. Derrota a los jefes. Supera tu récord.</strong>
</p>

<p align="center">
  <img alt="Unity 6000.3.22f1" src="https://img.shields.io/badge/Unity-6000.3.22f1-222c37?logo=unity&logoColor=white">
  <img alt="Plataforma: Windows" src="https://img.shields.io/badge/plataforma-Windows-0078d4?logo=windows&logoColor=white">
  <img alt="Estado: en desarrollo" src="https://img.shields.io/badge/estado-en%20desarrollo-f59e0b">
</p>

# Anime Zombie Battle

Juego de acción 2D (*beat 'em up*) para PC en el que resistes oleadas interminables de zombis y te enfrentas a jefes en una arena. Es un proyecto independiente, hecho con Unity y pensado para publicarse en Steam.

> **Estado: desarrollo temprano** (actualizado el 10 de octubre de 2026). Ya existen el menú principal y la base técnica del proyecto; el jugador, los enemigos y la arena de juego son lo que sigue. El detalle está en [Estado actual](#estado-actual).

## Contenido

- [Cómo nace la idea](#cómo-nace-la-idea)
- [El planteamiento](#el-planteamiento)
- [Qué buscamos](#qué-buscamos)
- [Estado actual](#estado-actual)
- [Hoja de ruta](#hoja-de-ruta)
- [Tecnologías](#tecnologías)
- [Cómo abrir el proyecto](#cómo-abrir-el-proyecto)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Cómo se trabaja](#cómo-se-trabaja)
- [Preguntas frecuentes](#preguntas-frecuentes)
- [Licencia y créditos](#licencia-y-créditos)

## Cómo nace la idea

Todo empieza con un tipo de juego que nunca pasa de moda: aguantar oleadas. Un personaje, una arena, zombis que no dejan de llegar y jefes que obligan a aprender sus movimientos. Juegos como *Crazy Zombie* lo resumen bien: un modo para un jugador y otro cooperativo, reglas que se entienden en segundos y las ganas de intentarlo una vez más para mejorar el puntaje.

La otra mitad de la historia es personal. *Anime Zombie Battle* es el primer proyecto de Cristian con un motor de videojuegos: viene del mundo de C# y .NET, pero nunca había construido un juego. En lugar de aprender con ejercicios sueltos, decidió hacerlo de la manera más directa: levantar un juego completo, desde la primera línea de código hasta una página en Steam, trabajando a tiempo parcial durante los fines de semana.

La identidad llegó antes que el código. El logo y el banner existían antes de que el repositorio tuviera su primer commit y fijaron un tono: ciudad en blanco y negro, explosiones, letras agrietadas y destellos. Qué tan oscuro o qué tan brillante será el arte de los personajes todavía se está decidiendo.

<p align="center">
  <img src="Marketing/Steam/AnimeZombieBattleLogo.png" alt="Logo de Anime Zombie Battle" width="280">
</p>

## El planteamiento

### La pregunta de partida

Un solo desarrollador, pocas horas a la semana y un motor nuevo: ¿qué se puede terminar de verdad? Anime Zombie Battle parte de esa restricción y no de una lista de deseos. La meta no es el juego más grande, sino un juego **completo**: que se pueda jugar de principio a fin, que se sienta bien y que llegue a Steam.

### La propuesta

Un jugador, una arena y oleadas sin fin. Las oleadas no terminan y, en el camino, aparece un jefe intermedio con un ataque fuerte que avisa antes de golpear. Cuanto más aguantas, más puntos: el mejor puntaje se guarda y es la razón para volver a intentarlo.

### Principios de diseño

1. **Terminar antes que ampliar.** El alcance de la versión 1.0 está cerrado. Lo que puede esperar, como el cooperativo local o el jefe con fases, espera a la 1.1.
2. **Que se sienta bien antes que se vea bien.** Primero un prototipo jugable con figuras simples; solo cuando moverse y golpear es satisfactorio se invierte en el arte final.
3. **Técnica sólida desde el inicio.** El nuevo Input System de Unity y *object pooling* para los enemigos, en lugar de crear y destruir objetos sin control.
4. **Publicar de verdad.** El destino es una venta única en Steam, sin anuncios ni contenido de pago adicional en la 1.0.

### Alcance

| Versión 1.0 (la meta) | Después de la 1.0 | Fuera de alcance |
|---|---|---|
| Un jugador, con movimiento y ataque con detección de golpes | Cooperativo local para dos jugadores | Multijugador en red |
| Varios tipos de zombis comunes y un jefe intermedio simplificado | Jefe con cambio de fase a mitad de vida | Anuncios y contenido de pago (DLC) en la 1.0 |
| Oleadas de enemigos en una arena | Ranking en línea y logros (opcional) | Más de una arena en la 1.0 |
| Vida y puntaje en pantalla, con el mejor puntaje guardado | | |
| Menú principal y menú de pausa | | |
| Música y efectos de sonido | | |

## Qué buscamos

- **Un juego terminado y publicado.** Una versión 1.0 jugable de principio a fin y disponible en Steam, con venta única.
- **Partidas que se entienden en segundos y se repiten por el puntaje.** Acción directa y fácil de entender, con el récord como razón para volver.
- **Aprender el ciclo completo de hacer un juego.** Del prototipo al lanzamiento: entrada, animación 2D por huesos, oleadas con *pooling*, interfaz, audio, pruebas, build y publicación.
- **Un proceso ordenado y visible.** Alcance controlado, ramas y Pull Requests, documentación y un estado público que se actualiza a medida que avanza el desarrollo.
- **Una base que pueda crecer.** Que la 1.0 deje la estructura lista para el cooperativo local y las mejoras de la 1.1.

## Estado actual

*Última actualización: 10 de octubre de 2026.*

| Área | Estado | Detalle |
|---|---|---|
| Base del proyecto | ✅ Hecho | Unity 6 (6000.3.22f1) con Git, GitHub y Git LFS configurados; nuevo Input System |
| Diseño | ✅ Hecho | Documento de diseño técnico v1.0.0: alcance, arquitectura y plan de trabajo |
| Identidad visual | ✅ Hecho | Logo cuadrado, banner y logo transparente para usar dentro del juego |
| Arte de interfaz | ✅ Base lista | Botones en cuatro estados (normal, resaltado, presionado y deshabilitado) e íconos de ajustes, atrás, pausa y sonido |
| Menú principal | 🔨 En curso | Escena con fondo, logo y botones. **Jugar** carga la arena y **Salir** cierra el juego; Opciones, Ajustes y Música todavía no hacen nada |
| Arena | ⏳ Pendiente | La escena `Arena01` existe, pero solo tiene la cámara |
| Jugador | ⏳ Pendiente | Movimiento, ataque y detección de golpes |
| Enemigos y jefe | ⏳ Pendiente | Zombis, oleadas con *pooling* y jefe intermedio |
| Interfaz de juego | ⏳ Pendiente | Vida, puntaje, pausa y pantallas de victoria y derrota |
| Audio | ⏳ Pendiente | Música y efectos de sonido |
| Publicación | ⏳ Pendiente | Página de Steam, build final y lanzamiento |

### Decisiones pendientes

- **Dirección de arte de los personajes:** mantener el tono oscuro y crudo del logo o ir hacia algo más brillante.
- **Ranking en línea:** si llegará y con qué servicio (es opcional y no bloquea la 1.0).
- **Precio y fecha de lanzamiento.**

## Hoja de ruta

1. [ ] **Menú y base:** pulir el menú principal y dejar el proyecto ordenado. *(en curso)*
2. [ ] **Prototipo jugable:** jugador, ataque, primer zombi, cámara y vida con figuras simples, y la prueba de "¿se siente bien jugarlo?".
3. [ ] **Sistemas de juego:** estados y pausa, oleadas con *object pooling*, tipos de zombi, jefe, puntaje y guardado.
4. [ ] **Arte y animación:** jugador, zombis, jefe y arena, con animación por huesos.
5. [ ] **Audio y pulido:** música, efectos, partículas y sacudida de pantalla.
6. [ ] **Pruebas:** playtesting, corrección de errores, rendimiento y build de Windows.
7. [ ] **Publicación:** página en Steam, subida del build y lanzamiento de la 1.0.
8. [ ] **Versión 1.1:** cooperativo local y jefe con cambio de fase.

El ritmo es de fin de semana, así que las fechas se publicarán aquí cuando sean firmes.

## Tecnologías

| | |
|---|---|
| Motor | Unity 6 (6000.3.22f1) |
| Lenguaje | C# |
| Interfaz | uGUI + TextMeshPro |
| Entrada | Input System (nuevo) |
| Animación 2D | 2D Animation Package (previsto) |
| Control de versiones | Git + GitHub + Git LFS |
| Arte y audio | Krita y Audacity (previstos) |

## Cómo abrir el proyecto

Necesitas:

- [Unity Hub](https://unity.com/download) con Unity **6000.3.22f1**.
- [Git](https://git-scm.com/) y [Git LFS](https://git-lfs.com/): las imágenes, el audio, las fuentes y los modelos se guardan con LFS.

```bash
git lfs install
git clone https://github.com/CristianCastro0/Anime-Zombie-Battle.git
```

Después:

1. En Unity Hub elige **Add > Add project from disk** (Agregar > Agregar proyecto desde el disco) y selecciona la carpeta clonada.
2. Espera a que Unity importe los assets; la primera vez tarda unos minutos.
3. Abre `Assets/Scenes/MainMenu.unity` y pulsa **Play**.

Para generar un ejecutable de Windows: **File > Build Profiles**, plataforma Windows y **Build**. Las escenas `MainMenu` y `Arena01` ya están en la lista.

## Estructura del repositorio

```
Assets/
├── Art/          Arte de la interfaz (botones, logos y fondos)
├── Audio/        Música y efectos de sonido (pendiente)
├── Plugins/      Librerías de terceros
├── Prefabs/
├── Resources/
├── Scenes/       MainMenu y Arena01
└── Scripts/      Código del juego (Managers, Player, Enemies, UI)
Docs/             Documentación de diseño (pendiente)
Marketing/Steam/  Logo y banner para la tienda de Steam
Packages/         Paquetes de Unity
ProjectSettings/  Configuración del proyecto
```

## Cómo se trabaja

- Desarrollo individual y a tiempo parcial, durante los fines de semana.
- Cada rama de trabajo se nombra con la fecha y las iniciales (por ejemplo `10102026CC`) y se integra por Pull Request a `Developer` y, de ahí, a `main`.
- Las imágenes, el audio, las fuentes y los modelos viajan por Git LFS.

## Preguntas frecuentes

**¿Cuándo sale?**
Todavía no hay fecha. El estado y la hoja de ruta se actualizan en este README.

**¿Puedo jugarlo ya?**
Aún no: por ahora solo existe el menú principal y no hay una versión jugable.

**¿En qué plataformas estará?**
En PC con Windows, a través de Steam.

**¿Tendrá cooperativo?**
Está planeado como cooperativo local para dos jugadores en la versión 1.1. La 1.0 es para un jugador.

**¿Cuánto costará?**
Será de pago único, sin anuncios ni DLC en la 1.0. El precio todavía no está definido.

## Licencia y créditos

### Licencia

Por ahora el código y los assets propios del proyecto no tienen una licencia abierta definida: todos los derechos están reservados. Las fuentes y los paquetes de terceros conservan sus propias licencias.

### Créditos

- Inspirado en *Crazy Zombie*. Este proyecto es independiente y no tiene relación con ese juego ni con sus creadores.
- Tipografía del menú: [Anton](https://fonts.google.com/specimen/Anton), bajo licencia SIL Open Font License.
- Hecho con [Unity](https://unity.com/) y TextMeshPro.
- Desarrollo: Cristian ([@CristianCastro0](https://github.com/CristianCastro0)).
