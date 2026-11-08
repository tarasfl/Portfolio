# Portfolio media

The homepage uses a portrait and project cover images; project galleries support images and MP4 videos. Edit the homepage image paths in `src/pages/index.astro` and the gallery entries in `src/pages/projects/[id].astro`.

Each gallery entry uses `src`, `alt` and `caption`. Videos also use `type: "video"` and `poster`. Play controls are native, playback is user-initiated, and changing slides pauses a hidden video. Videos have no audio and do not preload their full files. Full-size still images open in a separate tab.

## Sources and prepared assets

- `IMG_6384.HEIC`: portrait, converted to `taras-portrait.jpg`.
- `IMG_7477.HEIC`: drone hardware photograph, converted to `drone-hardware.jpg`.
- `IMG_5473.JPG`: rover component CAD view, `rover-arm-cad.jpg`.
- `IMG_5474.JPG`: structural study total displacement view, `rover-arm-displacement.jpg`. Its legend says displacement in mm; do not describe it as a stress or factor-of-safety result.
- `photo_2026-11-08_21-27-46.jpg`: `drone-concept.jpg`. Caption explicitly identifies this as a conceptual exploded illustration.
- `photo_2026-11-08_21-27-49.jpg`: `drone-dashboard.jpg`.
- `IMG_0419.MOV`: 20-second excerpt from 00:02–00:22, `drone-outdoor-test.mp4`. Caption does not claim an autonomous or GNSS-denied flight mode.
- `Screen Recording 2026-10-16 191324.mp4`: 30-second excerpt from 02:20–02:50, `drone-navigation-screen.mp4`.
- `Video Project 2.mp4`: complete approximately 5.83-second levitation demonstration, `ball-levitation-demo.mp4`. Original circular framing retained.
- Previously reviewed cube repository figures `static/FULL_TEST.png` and `static/optimised flywheel .png`: `cube-simulation-example.jpg` and `cube-flywheel-simulation.jpg`. These are different saved simulation cases, not physical tests or final specifications.

Images are resized for web use. Videos are H.264 MP4 with fast-start metadata and no audio. The source files are unchanged. Poster frames are taken from the prepared videos.

## Smartbreadboard and ball report additions

- `1787423579235.jpeg`: `smartbreadboard-pcb-render.jpg`, also used as the homepage cover. This is a 3D design render.
- `1787423579319.jpeg`: `smartbreadboard-pcb-layout.jpg`, routed PCB layout.
- `1787423579586.jpeg`: `smartbreadboard-assembled-pcb.jpg`, physical assembled board.
- `1787423579498.jpeg`: `smartbreadboard-prototype.jpg`, breadboard development setup.
- `Report_Patrick_Project.docx`, embedded `word/media/image2.png`: `ball-mechanical-iterations.png` (report figure 2).
- The same report, `word/media/image3.png`: `ball-assembly-cad.png` (report figure 3). The source is only 146 × 320 pixels; it is retained without upscaling or invented detail.
- The same report, `word/media/image6.png`: `ball-system-connections.png` (report figure 6).
- The same report, `word/media/image4.png`: `ball-hmi-screen.png` (report figures 4 and 16).

The report illustrations are CAD renders, a system diagram and an HMI design screenshot, not photographs of the physical apparatus. Captions credit the team report. The existing physical demonstration video and its poster remain in the ball gallery. The report's student identifiers and full document are not published. No new performance claims were inferred from these images.

Every project now has supplied media in its homepage preview and gallery. The old placeholder SVG files remain unused in `public/images`.

