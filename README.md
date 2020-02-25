# magireco-autofun
## Overview
Autopatcher for [Magia Record](https://play.google.com/store/apps/details?id=com.aniplex.magireco.en), works for all version/region. The provided tool will automatically unpack the APK, then insert smali files and code which required to load the provided native library.

By using this tool and distributes the generated modified APK on the internet, you're helping me to kill android modders, even if by small percentage. Thank you.

### Features
- Player's attack, buff rate and disc damage rate multiplier
- Enemy's attack, buff rate, disc damage rate and defense reducement
- Always autoplay, always turn, magia/doppel always active

The following features are configurable by editing `koaConf.ini`:
- Player's attack, buff rate and disc damage rate multiplier
- Enemy's attack, disc damage rate and defense reducement

The following features are configurable by configuring in-game's combat auto setting (In-game Combat > Menu > Auto Settings):
- Magia/doppel always active: Use Magia > On for enable, off for disable
- Always turn: Use Connect > On for enable, off for disable
- Always autoplay: Use Skills > On for enable, off for disable

### Longevity
The provided tool and native library will works even when the game is officially updated, unless there are major changes which affect entire functionality. So, this tool will probably works until the game dies or until another layer of security being added into the game.

### Device support
32-bit ARM and x86, at the moment.

## Requirements
- JRE/JDK 11.02 or newer

## Download
You can download it on [Releases](https://github.com/k0np4ku/magireco-autofun/releases) page.

## Usage
```
$ auto <apk-file>
```

## Configuration
You can find the configuration file on the application's data path.
- **English version:** /mnt/sdcard/com.aniplex.magireco.en/koaConf.ini or /storage/emulated/0/com.aniplex.magireco.en/koaConf.ini
- **Japan version:** /mnt/sdcard/com.aniplex.magireco/koaConf.ini or /storage/emulated/0/com.aniplex.magireco/koaConf.ini
- **Taiwan version:** /mnt/sdcard/com.komoe.madokagp/koaConf.ini or /storage/emulated/0/com.komoe.madokagp/koaConf.ini

In case you fucked up, you can delete the existing koaConf.ini and then a new configuration will be generated, or you can copy the following text:
```# Note
## Types
# - Boolean: Only accept true & false as its value, and true means enabled, while false means disabled
# - Float: Fractional value, e.g., 1.0, 10.0, 100.0
# - Int: Integrer, or in idiot's language, a number

[main]
# Boolean | Setting this to false will disables entire functionality
enabled=true

[player]
# Float | Player's attack will be multiplied by the specified value
attackMultiplier=10.0

# Float | Player's buff rate will be multiplied by the specified value
buffRateMultiplier=5.0

# Float | Player's disc damage rate will be multiplied by the specified value
discDamageRate=5.0

[enemy]
# Float | Enemy's attack will be divided by the specified value
attackReducement=10.0

# Float | Enemy's disc damage rate will be divided by the specified value
discDamageRateReducement=10.0

# Boolean | Reduce enemy's defense to zero
reduceEnemyDef=true
```
