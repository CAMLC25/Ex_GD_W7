# Ex_GD_W7 — Unity Animation Exercise (Week 7)

Bài tập thực hành môn **Game Development** — Tuần 7.  
Dự án tập trung vào hệ thống **Animation** trong Unity, sử dụng **Animator Controller** với character **Xbot** từ Mixamo.

---

## 🎯 Mục tiêu bài tập

- Làm quen với **Unity Animator Controller** và **Animation State Machine**
- Import và sử dụng animation từ **Mixamo** (`.fbx`)
- Thiết lập **Transition** giữa các animation states
- Áp dụng **Universal Render Pipeline (URP)** trong dự án 3D

---

## 🗂️ Cấu trúc dự án

```
Ex_GD_W7/
├── Assets/
│   ├── Animations/
│   │   └── Xbot/
│   │       ├── Happy Idle.fbx          # Animation đứng yên vui vẻ
│   │       ├── Swing Dancing.fbx       # Animation nhảy múa
│   │       └── XBotController.controller  # Animator Controller
│   ├── Scenes/
│   │   └── SampleScene.unity           # Scene chính
│   ├── Settings/                        # Cài đặt URP (PC & Mobile)
│   └── InputSystem_Actions.inputactions # Input System config
├── Packages/
│   └── manifest.json
└── ProjectSettings/
```

---

## ✨ Nội dung chính

### 🕺 Character & Animation
- **Character**: Xbot (Mixamo rigged humanoid character)
- **Animations** (từ Mixamo):
  - `Happy Idle` — trạng thái đứng yên mặc định
  - `Swing Dancing` — animation nhảy múa
- **Animator Controller**: `XBotController`
  - State mặc định: **Happy Idle**
  - Transition từ **Happy Idle → Swing Dancing** (dựa trên Exit Time)

### 🎬 Scene Setup
| GameObject | Mô tả |
|---|---|
| `Main Camera` | Camera chính với URP Camera data, Post Processing bật |
| `Directional Light` | Ánh sáng hướng (Intensity: 2, Realtime) |
| `Global Volume` | URP Post Processing volume |
| `Swing Dancing` | Prefab Xbot character với Animator Controller |

---

## 🛠️ Yêu cầu cài đặt

| Công cụ | Phiên bản |
|---|---|
| Unity Editor | **6000.3.26f1** (Unity 6) |
| Render Pipeline | Universal Render Pipeline (URP) **17.3.0** |
| Input System | **1.20.0** |
| AI Navigation | **2.0.15** |

---

## 🚀 Hướng dẫn chạy dự án

1. **Clone repository:**
   ```bash
   git clone <repository-url>
   ```

2. **Mở project bằng Unity Hub:**
   - Chọn **Open > Add project from disk**
   - Trỏ đến thư mục `Ex_GD_W7`
   - Unity phiên bản **6000.3.26f1** (Unity 6)

3. **Mở Scene:**
   - Vào `Assets/Scenes/SampleScene.unity`

4. **Nhấn Play** để chạy và xem animation.

---

## 📦 Packages sử dụng

| Package | Phiên bản | Mục đích |
|---|---|---|
| `com.unity.render-pipelines.universal` | 17.3.0 | Render Pipeline URP |
| `com.unity.inputsystem` | 1.20.0 | New Input System |
| `com.unity.ai.navigation` | 2.0.15 | NavMesh AI Navigation |
| `com.unity.timeline` | 1.8.13 | Timeline animation |
| `com.unity.visualscripting` | 1.9.12 | Visual Scripting |

---

## 📝 Ghi chú

- Thư mục `Library/`, `Temp/`, `obj/`, `Logs/` đã được loại trừ khỏi Git (xem `.gitignore`)
- Asset animation Xbot lấy từ [Mixamo](https://www.mixamo.com/) (cần tài khoản Adobe để tải)

---

*Bài tập tuần 7 — Game Development Course*

