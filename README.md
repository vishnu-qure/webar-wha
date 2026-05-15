# qure.ai WebAR - Setup Guide

## Folder structure

```
webar/
├── index.html
├── targets.mind        <- generated from the single target image
├── README.md
├── images/
│   └── target.png      <- the one marker image to scan
└── videos/
    └── ar-video.mp4    <- the one video shown in AR
```

## Step 1 - Add the target image

Place the single image you want people to scan at:

```
images/target.png
```

## Step 2 - Generate `targets.mind`

The AR page uses `targets.mind`, so this file must be regenerated from the single image.

1. Go to: https://hiukim.github.io/mind-ar-js-doc/tools/compile
2. Upload only `images/target.png`
3. Click Compile
4. Download the file
5. Rename it to `targets.mind`
6. Place it in the root `webar/` folder, replacing the old `targets.mind`

## Step 3 - Add the video

Place the single MP4 video at:

```
videos/ar-video.mp4
```

## Step 4 - Deploy

Deploy the entire `webar/` folder to a static host that supports HTTPS, such as Netlify or Vercel.

Camera access requires HTTPS on phones.

## Step 5 - Test

1. Open the hosted HTTPS URL on your phone
2. Tap Begin Experience
3. Allow camera access
4. Point the camera at the printed target image
5. The video should play on top of the image

## Video specs

- Format: MP4, H.264
- Resolution: 1280x720 or higher
- Muted playback is already configured
- The video loops automatically
