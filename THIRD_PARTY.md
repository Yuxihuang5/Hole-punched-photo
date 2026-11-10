# Third-party components

- ONNX Runtime Web 1.20.1: https://github.com/microsoft/onnxruntime (MIT). Runtime files are bundled under assets/runtime; license included.
- YOLOv5n v7.0: https://github.com/ultralytics/yolov5/tree/v7.0 (GPL-3.0). The released ONNX model is converted from FP16 to FP32 for browser compatibility; model and license included under assets/models.
- U-2-Net / u2netp: https://github.com/xuebinqin/U-2-Net (Apache-2.0). Model distributed through https://github.com/danielgatis/rembg/releases/tag/v0.0.0 ; preprocessing adapted from rembg (MIT): https://github.com/danielgatis/rembg .
- heic2any 0.0.4: https://github.com/alexcorvi/heic2any (MIT). Includes the project's prebuilt browser conversion bundle, based on libheif. License included under assets/runtime.

All runtime and model requests are relative to the site, including GitHub Pages repository subpaths. Photo input is processed locally in the browser.
