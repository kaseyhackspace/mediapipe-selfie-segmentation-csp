# mediapipe-selfie-segmentation-csp

"Workaround" for https://github.com/google/mediapipe/issues/2799.

## Steps:
- Download all files from and host in `scripts/<folder_name>`
    - `https://cdn.jsdelivr.net/npm/@mediapipe/selfie_segmentation/`
    - `https://cdn.jsdelivr.net/npm/@mediapipe/camera_utils/`
    - `https://cdn.jsdelivr.net/npm/@mediapipe/control_utils/`
    - `https://cdn.jsdelivr.net/npm/@mediapipe/drawing_utils/`
- set CSP to `script-src 'self'`
``` html
<meta http-equiv="Content-Security-Policy" content="script-src: 'self'">
```
- Use libraries in `scripts` folder rather than CDN
``` html
<script src="scripts/camera_utils/camera_utils.js" crossorigin="anonymous"></script>
<script src="scripts/control_utils/control_utils.js" crossorigin="anonymous"></script>
<script src="scripts/drawing_utils/drawing_utils.js" crossorigin="anonymous"></script>
<script src="scripts/selfie_segmentation/selfie_segmentation.js" crossorigin="anonymous"></script>
```
