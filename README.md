<h1 align="center">
  <sub>
    <img src="src/main/resources/assets/cameramod/textures/item/camera_item.png" width="150" alt="CameraMod icon">
  </sub>
  <br>
  Minecraft Virtualcam
</h1>

<p align="center">
  A Fabric 26.1.2 port of <a href="https://github.com/TGGamesYT/cameramod">Minecraft Virtualcam by TGGamesYT</a>.
</p>

This mod lets you place a camera in Minecraft and stream its view to other applications. On Linux, use the local MJPEG stream with OBS. On Windows, the original [SoftCam](https://github.com/tshino/softcam) virtual-camera support is retained.

> **Experimental port:** Tested in-game on Linux. The Windows virtual-camera driver has not yet been tested with this port.

## Requirements

- Minecraft **26.1.2**
- Fabric Loader and Fabric API for 26.1.2
- Java 25

## Setup

1. Put the mod JAR and Fabric API in your Minecraft profile’s `mods` folder.
2. Start the game, enter a world, place a camera, and activate it with the camera activator.

### Linux: OBS

Add a **Browser Source** in OBS with this URL:

```text
http://127.0.0.1:7236/
```

The direct MJPEG stream is available at `http://127.0.0.1:7236/stream`. You can then start OBS Virtual Camera if you want to use the output in another application.

### Windows

The port includes the original SoftCam files. Windows virtual-camera registration and output still need testing. The OBS browser-source method above is also available.

## Camera FPS

The stream defaults to 30 FPS. To change its limit in-game, use:

```text
/cm streamfps 60
```

The limit can be set from 1 to 240 FPS; actual performance depends on Minecraft and your computer.

## Credits

- **Original mod:** [TGGamesYT/cameramod](https://github.com/TGGamesYT/cameramod) by TGGamesYT
- **Windows virtual-camera library:** [softcam](https://github.com/tshino/softcam)
- The original project was inspired by [Flashz](https://youtube.com/@flashzyt).

This repository is an unofficial port of TGGamesYT’s mod, not a replacement for the original project. The original GPL-2.0 license is retained.

## Building

Run `./gradlew build` with Java 25. The JAR will be in `build/libs/`.
