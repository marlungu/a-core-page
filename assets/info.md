# 🎨 Archetype Core Design System

**Tagline:**  
*The Architecture of Intelligent Systems.*

**Essence:**  
Technical clarity + calm precision + architectural rhythm.  
Blueprint meets education — engineers who think like architects.

---

## 🧱 1. Core Layout
| Property | Value |
|-----------|-------|
| Max Width | 1120 px |
| Grid Gaps | 24 px (cards) |
| Section Padding | 64 px (default) / 120 px (hero) |
| Border Radius | 12 – 14 px |
| Box Shadow | `0 10px 25px rgba(15,23,42,0.06)` |
| Divider Color | `#E5E7EB` (slate-200) |

---

## 🎨 2. Color System
| Role | Color | Notes |
|------|--------|-------|
| **Background Light** | `#F8FAFC` | main surface (slate-50) |
| **Panel / Card** | `#FFFFFF` | elevated elements |
| **Text Primary** | `#0F172A` | slate-900 |
| **Text Muted** | `#475569` | slate-600 |
| **Accent Primary** | `#2563EB` | blue-600 |
| **Accent Hover** | `#1E40AF` | blue-800 |
| **Accent Cyan** | `#06B6D4` | tech highlight |
| **Accent Amber** | `#F59E0B` | emphasis / warmth |
| **Footer BG** | `#0F172A` | dark grounding |
| **Footer Text** | `#CBD5E1` | slate-300–400 |

---

## ✍️ 3. Typography
**Primary Font:** *Plus Jakarta Sans* (400–800)  
**Fallback:** system-ui, Inter, Segoe UI  

| Element | Font Weight | Size | Line Height | Notes |
|----------|-------------|------|-------------|-------|
| H1 | 800 | 44 px (3.2 vw clamp) | 1.15 | Hero / headline |
| H2 | 700 | 28 – 32 px | 1.25 | Section titles |
| H3 | 600 | 20 – 22 px | 1.4 | Card headings |
| Body | 400 / 500 | 17 – 18 px | 1.65 | Default text |
| Small / Caption | 500 | 14 px | 1.4 | Tags, footers |

**Letter-spacing:** −0.01 em for headings.  
**Color:** `#0F172A` (main), `#475569` (subtext).

---

## 🧭 4. Navigation
| Element | Style |
|----------|--------|
| Header BG | `rgba(248,250,252,0.86)` with blur(6 px) |
| Logo Height | 80 px (desktop), 60 px (mobile) |
| Nav Link Active | bold + bottom border 2 px #0F172A |
| CTA Button | “Join the Blueprint” — Blue #3B82F6, 8 px radius, 0 4 12 shadow |
| CTA Hover | #2563EB + translateY(−1 px) |

---

## 🧩 5. Components

### Card
```css
.card {
  background:#fff;
  border:1px solid #E5E7EB;
  border-radius:12px;
  padding:22px;
  transition:all .2s ease;
}
.card:hover {
  border-left:2px solid #06B6D4;
  box-shadow:0 8px 22px rgba(0,0,0,.05);
}

---
 ##### Button (Primary + Ghost)
.btn.primary {
  background:#3B82F6;
  color:#fff;
  padding:8px 16px;
  border-radius:8px;
  font-weight:600;
  transition:all .3s ease;
}
.btn.primary:hover {
  background:#2563EB;
  box-shadow:0 6px 18px rgba(59,130,246,0.3);
}
.btn.ghost {
  border:1px solid #E5E7EB;
  color:#0F172A;
  background:transparent;
}
.btn.ghost:hover {
  border-color:#06B6D4;
  color:#06B6D4;
}

##### Form Input
input[type="email"] {
  padding:12px 14px;
  border:1px solid #E5E7EB;
  border-radius:12px;
  background:#fff;
  min-width:300px;
}
input::placeholder {
  color:#94A3B8;
  content:"Enter your email";
}
#####Hero Section
.hero {
  background:linear-gradient(135deg,#1E293B 0%,#334155 100%);
  color:white;
  padding:120px 24px 60px;
  background-image:
    linear-gradient(90deg,rgba(255,255,255,0.03) 1px,transparent 1px),
    linear-gradient(180deg,rgba(255,255,255,0.03) 1px,transparent 1px);
  background-size:40px 40px; /* blueprint grid */
}
