# 🌍 INFINIGEN Explorer

### Procedural Infinite World Generator for Game Developers

> **Generate worlds. Explore them. Customize everything. Build your game.**

**INFINIGEN Explorer** is a browser-based procedural world-generation prototype created for game developers who want a fast way to generate, explore, customize, and export **large-scale low-poly game environments**.

## It combines **infinite-style procedural chunk streaming**, Earth-inspired biomes, seasonal environments, weather, procedural vegetation, custom GLB/GLTF assets, online asset discovery, HDRI environments, character models, object replacement, AI-assisted world generation, configuration import/export, and engine-oriented exports into one experimental world-building toolkit.

## 🚀 Live Demo

### 🎮 **[▶ Explore INFINIGEN Explorer](https://punitpritam788.github.io/INFINIGEN-Explorer---Procedural-Infinite-World-Generator/)**

Open the prototype directly in your browser and explore the procedural world.

> **No map editor. No empty scene. Start with a generated world and make it your own.**

---

## 🧠 The Idea

Creating an environment for a game can take a huge amount of time.

Terrain has to be created.
Trees have to be placed.
Rocks have to be distributed.
Biomes need visual identity.
Weather needs atmosphere.
Seasons need variation.
Assets need to be integrated.
And after all of that, the world still needs to be exported into the actual development workflow.

**INFINIGEN Explorer is an experiment around solving that first step.**

Instead of starting from an empty scene, developers start with a **procedurally generated world** that they can continuously explore and modify.

The long-term concept is to make world creation feel closer to:

```text
IDEA
 ↓
GENERATE
 ↓
EXPLORE
 ↓
CUSTOMIZE
 ↓
ADD YOUR ASSETS
 ↓
EXPORT
 ↓
BUILD YOUR GAME
```

---

# ✨ Core Features

## ♾️ Infinite-Style Procedural World

The world is generated using a **deterministic chunk-based system**.

Rather than attempting to keep one giant environment permanently loaded, the prototype generates nearby chunks around the player and streams the world as exploration continues.

That makes the system suitable as a foundation for large procedural environments while keeping the browser runtime focused on the area around the player.

### World generation controls

* 🌍 Seed-based procedural generation
* 🔄 Regenerate current world
* 🎲 Random Regenerate
* 📏 World scale control
* 🌿 Density control
* 👁️ Render-distance control
* 💨 Wind intensity
* 🕑 Time-of-day control
* 📊 Chunk and FPS monitoring
* 🐞 Debug mode

The prototype also exposes explicit **Regenerate World** and **Random Regenerate** controls for quickly rebuilding the environment or creating a new seed.

---

# 🌎 Earth-Inspired Biomes

INFINIGEN Explorer is not designed around a single generic landscape.

The prototype includes multiple biome definitions based on real-world environmental patterns, with different terrain parameters, vegetation styles, environmental colors, water behavior, seasonality, and special features.

### 🌴 Tropical

* Tropical Rainforest
* Tropical Dry Forest
* Tropical Savanna
* Mangrove

### 🌲 Temperate

* Temperate Broadleaf Forest
* Birch & Aspen Woodland
* Cherry Woodland
* Temperate Rainforest
* Mediterranean Scrub
* Temperate Grassland
* Flooded Grassland & Swamp

### ❄️ Boreal & Polar

* Boreal Forest / Taiga
* Arctic Tundra
* Ice Sheet & Polar Desert

### 🏜️ Arid

* Hot Desert
* Cold Desert & Steppe

### 🏔️ Montane & Coastal

* Alpine & Montane
* Coastal Dune & Shore

### 🌋 Volcanic

* Active Volcanic Field

## The underlying biome library stores environmental characteristics such as terrain height, mountain strength, vegetation density, canopy behavior, seasonality, snow behavior, and biome-specific flora/special features.

# 🌿 Procedural Flora & Landforms

One of the main ideas behind INFINIGEN Explorer is that **different environments should actually feel different**.

The procedural flora library is structured around recognizable growth forms from different environments.

Examples include:

🌴 Tropical emergent vegetation
🌱 Mangrove prop roots
🌳 African-style savanna trees
🌲 Boreal spruce forms
🏔️ Wind-shaped alpine vegetation
🌵 Columnar desert cactus
🌾 Dryland grasses and shrubs
❄️ Arctic dwarf vegetation

The prototype also includes environmental details such as:

* Grass
* Plants
* Flowers
* Ferns
* Trees
* Rocks
* Logs
* Mushrooms
* Water features
* Tide-pool elements
* Wetland vegetation
* Volcanic rocks
* Lava-related elements

The goal is for the generated environment to communicate the identity of its biome rather than simply changing terrain colors.

---

# 🍂 Real-World-Inspired Seasonal System

The environment includes four seasons:

| Season | Icon |
| ------ | ---- |
| Spring | 🌸   |
| Summer | ☀️   |
| Autumn | 🍂   |
| Winter | ❄️   |

Seasonal behavior can influence the appearance of vegetation and environmental conditions.

The biome system differentiates between **deciduous and evergreen environments**, allowing foliage behavior to vary between biomes rather than applying one global seasonal effect.

Developers can manually select a season or use seasonal progression inside the world.

---

# 🌦️ Dynamic Weather

The environment includes a weather override system with multiple atmospheric states.

### Available weather modes

☀️ Clear
🌧️ Rain
🌊 Monsoon Rain
⛈️ Thunderstorm
❄️ Snow
🌬️ Blizzard
🌨️ Sleet
🧊 Hail
🌫️ Fog
🏜️ Dust Storm
🔥 Wildfire Haze
🌋 Ash & Embers

Weather can be manually overridden or driven by the seasonal environment.

---

# 🧩 Custom Biome Builder

Don't want to use one of the predefined biomes?

Create your own.

The **Custom Biome** interface allows developers to experiment with:

* Custom biome name
* Terrain height
* Mountain strength
* Procedural terrain
* Optional ground texture
* Texture tile size

A custom biome can also use a **Poly Haven ground material** rather than relying only on procedural terrain coloring.

This makes the built-in biomes starting points rather than limitations.

---

# 🌐 Online Asset Connector

This is one of the biggest parts of the prototype.

INFINIGEN Explorer can search an online asset library and integrate available 3D content into the generated environment.

The prototype connects to **Poly Haven** for asset discovery and loading.

### Asset categories

🌲 Trees
🥥 Palms
🌲 Conifers
🌸 Flowers & Blossoms
🌿 Plants
🌿 Ferns & Groundcover
🪨 Rocks
⛰️ Boulders & Cliffs
🪵 Logs & Stumps
🍄 Mushrooms
📦 Props
🏛️ Architecture
🪑 Furniture
⚙️ Industrial

This makes the procedural generator much more flexible because developers are not limited to the geometry built directly into the prototype.

---

# 🧱 Procedural + Online GLB Worlds

You can decide how online assets participate in world generation.

### Three available modes

**Procedural Only**

Use the built-in procedural environment.

**Mixed**

Combine procedural generation with imported GLB assets.

**GLB Only**

Prefer loaded online assets where an appropriate asset is available.

The system also exposes separate mix controls for:

* 🌲 Trees
* 🪨 Rocks
* 🌿 Plants
* 📦 Props

So a developer can build a world where some object types remain procedural while others come from custom assets.

---

# 🎚️ Object Population Controls

Developers can control how many objects are generated within each loaded chunk.

Population controls are available for:

* Trees
* Rocks
* Plants
* Props

Each category can either use:

**AUTO**

or a manually chosen object budget.

The implementation supports a configurable per-chunk population range up to 50 objects per category.

This gives developers another way to find the balance between:

**visual richness ↔ runtime performance**

---

# 📦 Bring Your Own GLB / GLTF

Have your own game assets?

Load them.

INFINIGEN Explorer supports custom `.glb` and `.gltf` models through:

* 🌐 Online URL
* 📁 Local file

Assets can be organized into categories such as:

* Tree
* Rock
* Plant
* Prop

They can then be stored in the **Asset Pool** and used by the procedural world system.

---

# ⚙️ GLB Quality & Performance Controls

3D assets can become expensive very quickly.

That is why the prototype includes configurable delivery quality.

### GLB / GLTF

* 1K
* 2K
* 4K
* 8K

### Ground Textures

* 1K
* 2K
* 4K
* 8K

### HDRI

* 1K
* 2K
* 4K
* 8K

### Realtime Renderer

* Low
* Medium
* High

The low rendering mode is intended to reduce the cost of large worlds by using smaller online deliveries, reducing shadow workload for online assets, and using a lower renderer pixel ratio.

---

# 📐 Natural Asset Scaling

Different GLB models can arrive with completely different dimensions.

A tree might be imported tiny.

A rock might arrive enormous.

A prop might use another unit scale entirely.

The prototype therefore includes a **Natural Size Fit** workflow that normalizes models using their actual bounding-box dimensions and fits them according to their category.

This helps maintain more believable proportions between:

```text
TREE
   ↓
PLANT
   ↓
ROCK
   ↓
PROP
```

instead of simply applying the same scale to every asset.

---

# 🔄 Object Connector

Want to manually replace something inside the generated world?

Use **Object Connector**.

### Workflow

```text
LOAD GLB
   ↓
SELECT ASSET
   ↓
ENTER REPLACE MODE
   ↓
AIM AT OBJECT
   ↓
PRESS E / CLICK
   ↓
OBJECT REPLACED
```

The selected asset can replace generated trees, rocks, plants, or props directly in the world.

The connector also provides controls for attachment offset and scale.

This is particularly useful when procedural generation gets you **90% of the way there** and you want to manually customize the final environment.

---

# 🧑 Character Connector

Characters are also treated as configurable world assets.

The prototype supports:

* Procedural character
* GLB character
* Character disabled

Custom character models can be loaded from:

* URLs
* Local `.glb`
* Local `.gltf`

The loader also detects animation clips and can create an animation mixer when an animated model is provided.

Character visuals can also be hidden completely, which is useful when the tool is being used purely as a map/environment generator.

---

# 🎥 First-Person & Third-Person Exploration

The world is designed to be explored rather than simply viewed.

### Controls

| Input     | Action           |
| --------- | ---------------- |
| `W A S D` | Move             |
| `Mouse`   | Look             |
| `SPACE`   | Jump / movement  |
| `CTRL`    | Movement control |
| `SHIFT`   | Speed            |
| `V`       | Switch camera    |
| `H`       | Toggle panel     |
| `F3`      | Debug            |
| `E`       | Replace object   |

The prototype supports pointer-lock exploration and both first-person and third-person camera presentation.

---

# 🌅 HDRI Environment System

The environment can also use external HDRI environments.

Developers can:

* Search HDRIs
* Preview HDRI results
* Load an HDRI
* Adjust HDRI intensity
* Use the HDRI as the background
* Fall back to procedural sky lighting

## The prototype uses RGBE/HDRI loading and exposes HDRI quality and strength controls.

# 🤖 AI Architect

The prototype includes an experimental **AI Architect** interface.

Instead of manually configuring a biome, developers can describe the world they want.

For example:

```text
Volcanic hellscape with lava rivers...
```

The current implementation interprets keywords from the description and adjusts supported world settings accordingly.

This is intentionally an early prototype of a larger idea:

> **Describe a world → let the system configure the world.**

The AI layer is currently lightweight, but it provides the foundation for expanding toward more advanced natural-language world generation.

---

# 💾 World Configuration System

Generated worlds can be represented as configuration data.

The prototype supports **World Code / IGX configuration export and import**, allowing settings to be saved and recreated.

Configuration can include information such as:

* Seed
* Biome
* Weather
* World scale
* Density
* Wind
* Time of day
* Render distance
* Season
* Online asset settings
* Asset pools
* Custom biome settings
* HDRI configuration
* Runtime quality configuration

This allows the generated world setup to be treated as something that can be **saved, shared, and reconstructed** rather than being a temporary scene only.

---

# 📤 Export Your World

INFINIGEN Explorer includes two different export directions.

## 📦 GLB Snapshot

A finite snapshot of the currently loaded world can be exported as a `.glb`.

Export controls include:

* Snapshot radius
* Character inclusion
* Texture size cap
* Binary GLB output

The prototype explicitly positions this snapshot workflow for importing generated content into workflows such as **Unity / Unreal**.

---

## ⚙️ Infinite World JavaScript Export

The project can also export JavaScript containing the world configuration for an infinite browser runtime.

The exported configuration can include:

```text
SEED
BIOME
WEATHER
WORLD SCALE
DENSITY
WIND
TIME OF DAY
SEASON
RENDER DISTANCE
ONLINE ASSETS
ASSET MIX
CUSTOM BIOME
HDRI SETTINGS
```

This is useful when the goal is not simply to export one static map, but to reproduce the procedural world-generation configuration itself.

---

# 🧬 Deterministic Worlds

One of the fundamental ideas of the project is **seed-based generation**.

A seed controls procedural generation so the same world configuration can be reproduced.

That makes deterministic generation useful for:

* Game prototypes
* Level-design experiments
* Testing
* Procedural game concepts
* Reproducible environments
* Sharing world configurations

And when you want something completely different:

```text
🎲 RANDOM REGENERATE
```

creates a new world seed and rebuilds the environment.

---

# 🛠️ Technology Stack

INFINIGEN Explorer is currently built around web-native 3D technology.

### Core

* **HTML5**
* **CSS3**
* **JavaScript**
* **WebGL**

### 3D

* **Three.js**
* `GLTFLoader`
* `GLTFExporter`
* `DRACOLoader`
* `KTX2Loader`
* `RGBELoader`

### Rendering

* Three.js post-processing
* Effect Composer
* Render Pass
* Bloom
* Output Pass

### Online Assets

* Poly Haven API
* Poly Haven models
* Poly Haven HDRIs
* Poly Haven materials

The prototype configures both Draco and KTX2 support for imported GLTF/GLB content.

---

# 🎮 Who Is This For?

INFINIGEN Explorer is aimed at developers and creators experimenting with:

**🎮 Indie Game Development**
Create an environment foundation before building gameplay.

**🌍 Procedural Games**
Use deterministic generation to create large environments.

**🧪 Game Prototyping**
Generate something playable without first building an entire level manually.

**🎨 Technical Art**
Experiment with procedural vegetation and custom asset placement.

**🗺️ Level Design**
Generate a starting world and then manually customize important areas.

**💡 Creative Experiments**
Use the world as a playground for ideas.

---

# 🔥 What You Can Build On Top of It

INFINIGEN Explorer is intentionally designed as a **foundation**, not the final destination.

A future game could use it as the starting point for:

```text
OPEN WORLD
SURVIVAL GAME
EXPLORATION GAME
RPG
SANDBOX
SIMULATION
PROCEDURAL ADVENTURE
ENVIRONMENT GENERATOR
LEVEL DESIGN TOOL
WORLD-BUILDING TOOL
```

The generated environment can become the canvas on which gameplay systems are added.

---

# ⚡ Example Workflow

Imagine you want to prototype a survival game.

### Step 1

Generate a world.

### Step 2

Choose:

```text
Biome → Mangrove
Season → Monsoon/Summer
Weather → Rain
Density → High
```

### Step 3

Search for online assets.

```text
Trees
Rocks
Plants
Props
```

### Step 4

Add your own GLB assets.

### Step 5

Adjust the GLB/procedural mix.

### Step 6

Replace important generated objects manually.

### Step 7

Add a character.

### Step 8

Explore the environment in first-person or third-person.

### Step 9

Export the world snapshot.

### Step 10

Continue development in your game workflow.

---

# 🎯 Project Philosophy

INFINIGEN Explorer is built around a simple idea:

> **Procedural generation should give developers more creative freedom, not less.**

The generator provides the starting point.

The developer decides what happens next.

You can:

**keep everything procedural**

or

**mix procedural generation with real assets**

or

**replace generated objects**

or

**create a custom biome**

or

**build an environment around your own assets**

or

**export the result and continue elsewhere.**

The more systems are added, the more the generated world becomes a creative playground instead of a fixed template.

---

# 🔮 Future Direction

This project is still evolving.

The current prototype is a foundation for much larger ideas, including potential future work around:

* More detailed biome transitions
* More environmental systems
* Better terrain generation
* More vegetation types
* Improved water systems
* Rivers and larger hydrological features
* Advanced erosion
* Wildlife
* NPCs
* More intelligent AI world generation
* Better procedural asset distribution
* Additional online asset providers
* More import/export formats
* Game-engine integrations
* Larger world persistence systems
* More advanced world editing
* Multiplayer-compatible procedural worlds
* More detailed environmental simulation

The goal is to gradually move from a **procedural exploration prototype** toward a much more complete **world-building toolkit**.

---

# ⚠️ Prototype Status

> **INFINIGEN Explorer is currently a prototype.**

It is not intended to replace a complete game engine, terrain editor, or production-ready world pipeline yet.

Some systems are experimental and may change significantly during future development.

Performance can vary depending on:

* GPU
* Browser
* World size
* Render distance
* Asset complexity
* Texture resolution
* Number of loaded models
* Procedural density

For heavier scenes, the prototype provides lower-quality GLB, texture, HDRI, and realtime rendering options intended to help reduce rendering cost.

---

# 📜 Third-Party Assets

INFINIGEN Explorer can retrieve third-party assets from external services such as **Poly Haven**.

The prototype is designed around Poly Haven's CC0 asset ecosystem, but developers should always verify the current license associated with any third-party content before using it in a shipped commercial project.

INFINIGEN Explorer does not claim ownership of third-party models, textures, HDRIs, or other external assets.

---

# 🤝 Contributing

The project is currently experimental, but the long-term goal is to make it increasingly useful for developers experimenting with procedural worlds.

Ideas and contributions around:

* Procedural generation
* Biome systems
* Performance optimization
* Asset integration
* Terrain generation
* World simulation
* Rendering
* Game-engine export
* AI-assisted world creation

are especially relevant to the project's direction.

---

# ⭐ Support the Project

If you like the idea of generating game worlds instead of manually building every environment from scratch:

⭐ **Star the repository**
🍴 **Fork the project**
🐛 **Report bugs**
💡 **Share ideas**
🧩 **Experiment with the generator**

---

# 🌍 INFINIGEN Explorer

### **Generate Infinite-Style Worlds. Add Your Assets. Shape Your Environment.**

**Live Demo:**

### 👉 https://punitpritam788.github.io/INFINIGEN-Explorer---Procedural-Infinite-World-Generator/

---

## 🧭 The Vision

The current project is only a prototype.

But the direction is bigger:

> **A developer should be able to open a world generator, describe the environment they imagine, explore it immediately, bring in their own assets, shape the world however they want, and then take that world into their game-development workflow.**

**INFINIGEN Explorer is the beginning of that idea.**
