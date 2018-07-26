# USDZerve
This project aims to use an open source and modern pipeline to create Web-based 3D product configurators, capable of presenting the customized product in AR.

## W.I.P.  This project is still in concept phase.

There's currently no line of source code available. 
For feature requests, please create an **Issue**.
For direct feedback, please contact me on **[Twitter](https://twitter.com/pixelpartner)**.

## Roadmap

- [x] Describe purpose, roadmap and dependencies.
- [ ] Develop tornado server for customized USD scene archives
  - [ ] respond to urlParameters
  - [ ] respond to JSON parameters
  - [ ] accept only parameters supported in the loaded USD scene
  - [ ] configure and write flattened .usdc and textures
  - [ ] use ZipFile.py to create .usdz archive (or wait for Pixar to directly support this)
  - [ ] support frontend UI updates for long running USD creation processes
  - [ ] serve archive
- [ ] Combine USDZ creation with 2D SVG UI
- [ ] Create sample order details PDF on the server with PNG or SVG
- [ ] Create .blend scenes with Armory3D extensions
- [ ] Add infrastructure to automatically create interfacing **elm** and **haxe** code to connect the WebGL scene with the HTML UI.
  - [ ] Create 2D thumbnails for **variants** to register and later show in UI.
  - [ ] Create 2D thumbnails for **variant groups** to register and later show in UI.

## Supporting

- [ ] Desktop and mobile web browsers capable of WebGL1 or WebGL2.
- [ ] An interactive 3D presentation of the product.
- [ ] Automatic creation of HTML/CSS-based UI to choose a variant and configure the product with predefined parameters.
- [ ] **[optional]** Server-side creation of customized **3D scene files** to download/serve for presenting the final configuration in **AR** on modern SmartPhones. 
  - [ ] **.usdz** on modern Apple products, using **AR-QuickLook**
  - [ ] **.gltf** on others, using **WebXR** with an Mozilla App.
- [ ] Server-side creation of PDFs describing the configured product.

## Dependencies

##### For Development

- [**Blender3D**](https://www.blender.org), the open source 3D modelling, animation and rendering tool (with lots of more features)
  (is included in the **Armory3D** install)
- [**Armory3D**](https://armory3d.org/), the open source cross platform game engine using **Blender3D** as editor, [**Haxe**](https://haxe.org/) as cross platform language and [**Kha**](http://kha.tech/) as graphics framework.
- **[elm](http://elm-lang.org/)**, a functional programming language that produces error-free Javascript for frontend UIs.

##### Extra On the Server

- **[Pixar's OpenUSD](https://graphics.pixar.com/usd/docs/index.html)** (on [Linux](https://github.com/PixarAnimationStudios/USD/#3-run-the-script), [macOS](https://github.com/vfxpro99/usd-build-club/wiki/USD-on-macOS) and [Windows](https://github.com/vfxpro99/usd-build-club/wiki/Using-Pixar's-build-script-on-Windows)) to produce [USDZ 3D scene archives](https://developer.apple.com/videos/play/wwdc2018/603/) for [AR Quicklook on iOS12 devices and macOS10.14](https://developer.apple.com/arkit/gallery/)
- **[tornado](http://www.tornadoweb.org)**, the **python** web framework for asynch processes
