# ShieldCore LA — UniFi Camera & Network Installation Website

## What's In Here

```
okyprola/
├── index.html            ← Main website (system builder, booking, contact)
├── planner.html          ← Camera Placement Planner (3D indoor + 2D outdoor)
├── download-images.sh    ← Script to download real UniFi product images
├── README.md
└── images/
    ├── products/         ← 76 product images (placeholders → replace with real)
    │   ├── g6-bullet.png
    │   ├── unvr-instant.png
    │   └── ...
    └── slides/           ← Hero slideshow (UniFi Protect screenshots)
        ├── slide1.png
        ├── slide2.png
        └── slide3.png
```

## Deploy to Cloudflare Pages

### 1. Push to GitHub
```bash
cd okyprola
git init
git add .
git commit -m "ShieldCore LA website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/okyprola.git
git push -u origin main
```

### 2. Connect to Cloudflare Pages
1. Go to dash.cloudflare.com
2. Workers & Pages → Create → Pages → Connect to Git
3. Select your okyprola repo
4. Build settings: leave everything blank
5. Deploy — live at yourname.pages.dev

### 3. Replace placeholder images
```bash
bash download-images.sh
git add . && git commit -m "Real images" && git push
```

## Test Locally
```bash
python3 -m http.server 8000
```
Open http://localhost:8000

## No build step needed. Plain HTML/CSS/JS.
