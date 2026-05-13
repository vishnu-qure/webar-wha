# qure.ai WebAR — Setup Guide

## Your folder structure should look like this:

```
webar/
├── index.html          ← the AR page (already built)
├── targets.mind        ← generated from the 4 target images
├── README.md
├── images/
│   ├── act1-clinic.png       ← your B&W sketch (Act 1)
│   ├── act2-detection.png    ← your B&W sketch (Act 2)
│   ├── act3-school.png       ← your B&W sketch (Act 3)
│   └── act4-stadium.png      ← your B&W sketch (Act 4)
└── videos/
    ├── act1-clinic.mp4       ← your animated video (Act 1)
    ├── act2-detection.mp4    ← your animated video (Act 2)
    ├── act3-school.mp4       ← your animated video (Act 3)
    └── act4-stadium.mp4      ← your animated video (Act 4)
```

---

## Step 1 — Generate your targets.mind file

This file has already been generated as `targets.mind`. If you need to regenerate it, this is the file that teaches the AR system what each sketch looks like.

1. Go to: https://hiukim.github.io/mind-ar-js-doc/tools/compile
2. Upload all 4 sketch images IN ORDER:
   - First: images/act1-clinic.png
   - Second: images/act2-detection.png
   - Third: images/act3-school.png
   - Fourth: images/act4-stadium.png
3. Click Compile
4. Download the file — rename it to targets.mind
5. Place it in your webar/ folder

---

## Step 2 — Add your videos

Place your 4 MP4 files from Runway into the videos/ folder.
Name them exactly:
- act1-clinic.mp4
- act2-detection.mp4
- act3-school.mp4
- act4-stadium.mp4

Current note: `videos/act1-clinic.mp4` is currently a copy of `videos/act2-detection.mp4`. Replace it later if Act 1 needs a unique video.

---

## Step 3 — Deploy to Netlify (free, 2 minutes)

1. Go to netlify.com — sign up free
2. Drag and drop your entire webar/ folder onto the Netlify dashboard
3. Netlify gives you a live HTTPS URL instantly
   Example: https://your-site-name.netlify.app

---

## Step 4 — Generate your QR code

1. Go to qr-code-generator.com
2. Enter your Netlify URL
3. Download as high-res PNG
4. Print it on your banner or on a small card next to the banner

---

## Step 5 — Test before the event

1. Print one of your sketch images on A4
2. Open the QR on your phone
3. Tap Begin Experience
4. Point at the printed sketch
5. The video should play on top of it

---

## Tips for the banner

- Each sketch zone should be at least 30x20cm on the printed banner
- Sketches should have good contrast and detail for reliable tracking
- Make sure the printed banner is well lit at the event (no harsh glare)
- Test in the actual venue lighting before the event

---

## Video specs (for Runway exports)

- Format: MP4 (H.264)
- Resolution: 1280x720 or higher
- Duration: 8 seconds, looping
- No audio needed (videos are muted in the AR experience)
