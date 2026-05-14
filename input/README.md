# input/

Drop raw **simulator / device screenshots** here, one folder per screen.

```
input/
├── 01-pick-from-photo/
│   ├── iphone.png           ← iPhone 16 Pro Max simulator (1290×2796)
│   ├── ipad.png             ← iPad Pro 13" M4 simulator (2064×2752)
│   ├── android.png          ← Android phone (any 9:16)
│   ├── android-tablet.png   ← Android tablet (any 3:4)
│   ├── iphone-landscape.png ← iPhone rotated (2796×1290, optional)
│   └── promo.png            ← Key art for promo banners (optional)
├── 02-color-prompt-ai/
│   └── ...
└── ...
```

## Fallback chain

| Device | Looks for | Falls back to |
|---|---|---|
| `ipad` | `ipad.png` | `iphone.png` |
| `android-phone` | `android.png` | `iphone.png` |
| `android-tablet` | `android-tablet.png` → `android.png` | `iphone.png` |
| `iphone-landscape` | `iphone-landscape.png` | `iphone.png` |
| `ipad-landscape` | `ipad.png` | `iphone.png` |
| `google-play-feature` | `promo.png` | *(gradient + text only)* |
| `apple-search-ads` | `promo.png` | *(gradient + text only)* |

Missing files → renders **gradient + text only** (no device screenshot inside the mockup).

## Capture guide

| Device | Simulator | Resolution |
|---|---|---|
| iPhone | iPhone 16 Pro Max | 1290×2796 |
| iPad | iPad Pro 13" M4 | 2064×2752 |
| Android phone | Pixel 8 Pro emulator | 1344×2992 (auto-resized) |
| Android tablet | Pixel Tablet emulator | 1600×2560 (auto-resized) |

`⌘S` in Xcode simulator saves a native-resolution PNG to Desktop.
