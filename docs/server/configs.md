---
sidebar_position: 2
---

# Конфиги

## server.properties
```dotenv
difficulty=hard
allow-flight=true
view-distance=8
simulation-distance=4
```

## bukkit.yml
Подробнее о каждом параметре https://bukkit.fandom.com/wiki/Bukkit.yml/ru
```YML
spawn-limits: # Количество мобов на игрока
  monsters: 40 # Монстры 
  animals: 5 # Животные
  water-animals: 2 # Водные животные (Дельфины, спруты, ...) 
  water-ambient: 3 # Водные животные (Рыбы)
  water-underground-creature: 2 # Водные животные (Светящийся спрут)
  axolotls: 2 # Оксылотл 
  ambient: 4 # Окружение (Летучие мыши)
ticks-per: # Количество тиков на спавн моба
  animal-spawns: 300 # 15 сек
  monster-spawns: 10 # 0,5 сек
  water-spawns: 300 # 15 сек
  water-ambient-spawns: 300 # 15 сек
  water-underground-creature-spawns: 300 # 15 сек
  axolotl-spawns: 300 # 15 сек
  ambient-spawns: 300 # 15 сек
chunk-gc:
  period-in-ticks: 400
```

## spigot.yml
Подробнее о каждом параметре https://www.spigotmc.org/wiki/spigot-configuration/
```YML
settings:
  moved-wrongly-threshold: 0.0625
  moved-too-quickly-multiplier: 10.0
  netty-threads: 4
world-settings:
  default:
    merge-radius:
      item: 2.5
      exp: 3.0
    hanging-tick-frequency: 200 # Время проверки декоративных сущностей (стойки/рамки/картины и т.д.)
    item-despawn-rate: 6000
    arrow-despawn-rate: 300 # 15 секунд на даспавн
    trident-despawn-rate: 1200 # 60 секунд на даспавн
    mob-spawn-range: 3 # Радиус в чанках от игрока, где будут спавнится мобы
    entity-activation-range: # Радиус в котором ентити будут активничать
      animals: 32
      monsters: 32
      raiders: 48
      misc: 16
      water: 16
      villagers: 32
      flying-monsters: 32
    tick-inactive-villagers: false # Инактивные жители не тикают
    entity-tracking-range: # Радиус в котором ентити будут видны
      players: 128 # Игрок
      animals: 48 # Жители, обычные/водные животные
      monsters: 48 # Монстры, рейдеры и фантомы
      misc: 32  # Таблички, картины, рамки, дроп итемов, опыт
      display: 128
      other: 64 # Все остальное (Например: Стойки для брони)
```

## paper-global.yml
Подробнее о каждом параметре https://docs.papermc.io/paper/reference/global-configuration
```YML
block-updates:
  disable-chorus-plant-updates: false
  disable-mushroom-block-updates: false
  disable-noteblock-updates: false
  disable-tripwire-updates: false
chunk-loading-advanced:
  auto-config-send-distance: true
  player-max-concurrent-chunk-generates: 0
  player-max-concurrent-chunk-loads: 0
chunk-loading-basic:
  player-max-chunk-generate-rate: -1.0
  player-max-chunk-load-rate: 100.0
  player-max-chunk-send-rate: 75.0
chunk-system:
  gen-parallelism: default
  io-threads: 12
  worker-threads: 6
item-validation: 
  book-size:
    page-max: 1280 # Ограничение в байтах на резмер книг
unsupported-settings:
  allow-grindstone-overstacking: true
  allow-headless-pistons: true
  allow-permanent-block-break-exploits: true
  allow-piston-duplication: true
  compression-format: ZLIB
  perform-username-validation: true
```

## paper-world-defaults.yml
Подробнее о каждом параметре https://docs.papermc.io/paper/reference/world-configuration
```YML
chunks:
  delay-chunk-unloads-by: 10s # Время через которое выгружаются неактивные чанки из ОЗУ сервера
  entity-per-chunk-save-limit:
    area_effect_cloud: 8
    arrow: 16
    dragon_fireball: 3
    egg: 8
    ender_pearl: 8
    experience_bottle: 3
    experience_orb: 16
    eye_of_ender: 8
    fireball: 8
    firework_rocket: 8
    llama_spit: 3
    potion: 8
    shulker_bullet: 8
    small_fireball: 8
    snowball: 8
    spectral_arrow: 16
    trident: 16
    wither_skull: 4
  max-auto-save-chunks-per-tick: 16
  prevent-moving-into-unloaded-chunks: true
entities:
  behavior:
    nerf-pigmen-from-nether-portals: false
  spawning:
    creative-arrow-despawn-rate: 400
    despawn-ranges:
      ambient:
        hard: 54
        soft: 32
      axolotls:
        hard: 54
        soft: 32
      creature:
        hard: 54
        soft: 32
      misc:
        hard: 54
        soft: 32
      monster:
        hard: 54
        soft: 32
      underground_water_creature:
        hard: 54
        soft: 32
      water_ambient:
        hard: 54
        soft: 32
      water_creature:
        hard: 54
        soft: 32
    duplicate-uuid:
      mode: SAFE_REGEN
      safe-regen-delete-range: 32
    iron-golems-can-spawn-in-air: false
environment:
  optimize-explosions: true
fixes:
  fix-items-merging-through-walls: true
  disable-unloaded-chunk-enderpearl-exploit: true
  fix-curing-zombie-villager-discount-exploit: true
  split-overstacked-loot: true
hopper:
  cooldown-when-full: true
  ignore-occluding-blocks: true
misc:
  redstone-implementation: ALTERNATE_CURRENT # Достаточно ванильное поведение редстоуна, но могут быть отличия
  update-pathfinding-on-block-update: false
tick-rates:
  behavior:
    villager:
      acquirepoi: 120
      validatenearbypoi: 60
  container-update: 1
  dry-farmland: 1
  grass-spread: 4
  mob-spawner: 4
  sensor:
    villager:
      nearestbedsensor: 80
      nearestlivingentitysensor: 40
      playersensor: 40
      secondarypoisensor: 80
      villagerbabiessensor: 40
unsupported-settings:
  fix-invulnerable-end-crystal-exploit: true
```