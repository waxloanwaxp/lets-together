# Let's Together (ทางเดียวกัน ไปด้วยกัน)

> แพลตฟอร์มร่วมเดินทางแบบไม่แสวงหากำไร (Peer-to-Peer Carpooling) แห่งแรกของไทย

[![Next.js](https://img.shields.io/badge/Next.js-14-black?logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![React](https://img.shields.io/badge/React-18-61DAFB?logo=react)](https://reactjs.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 🌟 ภาพรวมโครงการ

**Let's Together** เป็นแพลตฟอร์มร่วมเดินทาง (Carpooling) แบบ Peer-to-Peer ที่เชื่อมต่อผู้ขับขี่และผู้โดยสารเพื่อแบ่งปันค่าใช้จ่ายอย่างยุติธรรม ตามแนวคิด **"ทางเดียวกัน ไปด้วยกัน"**

### 🎯 จุดเด่นหลัก

| คุณสมบัติ | รายละเอียด |
|------------|-------------|
| **💰 แบ่งปันค่าใช้จ่ายยุติธรรม** | คำนวณจากค่าน้ำมัน + ค่าทางด่วนจริง หารเท่ากัน ไม่มีค่าคอมมิชชันแพลตฟอร์ม (0%) |
| **🛡️ ความปลอดภัยสูงสุด** | ยืนยันตัวตน 4 ระดับ | ปุ่ม SOS 3 วินาทีเชื่อม Police I Lert U | ติดตาม GPS เรียลไทม์ |
| **🤝 ชุมชนที่เชื่อถือได้** | ระบบคะแนน 2 ทิศทาง | ผู้ใช้คะแนน < 4.0 ถูกระงับ | e-KYC และตรวจสอบใบขับขี่/ป้ายภาษี |
| **🗺️ จับคู่เส้นทางอัจฉริยะ** | AI จับคู่เส้นทาง | จุดแวะพักหลายจุด | คำนวณระยะทางแวะรับอัตโนมัติ |
| **🌱 เป็นมิตรสิ่งแวดล้อม** | ลดจำนวนรถ | ลดมลพิษ | ลดความแออัดจราจร |

## 🏗️ สถาปัตยกรรมระบบ

```
lets-together-web/
├── src/
│   ├── app/                    # Next.js App Router
│   │   ├── (auth)/             # หน้าล็อกอิน/สมัครสมาชิก
│   │   ├── (dashboard)/        # หน้าหลักหลังล็อกอิน
│   │   │   ├── driver/         # ฟีเจอร์ผู้ขับขี่
│   │   │   └── passenger/      # ฟีเจอร์ผู้โดยสาร
│   │   ├── api/                # API Routes
│   │   ├── layout.tsx          # Root Layout
│   │   ├── page.tsx            # Landing Page
│   │   └── globals.css         # Global Styles
│   ├── components/
│   │   ├── ui/                 # Base UI Components
│   │   ├── layout/             # Layout Components
│   │   ├── driver/             # Driver Components
│   │   ├── passenger/          # Passenger Components
│   │   ├── shared/             # Shared Components
│   │   └── map/                # Map Components
│   ├── lib/
│   │   ├── api/                # API Client
│   │   ├── hooks/              # Custom React Hooks
│   │   ├── store/              # Zustand Stores
│   │   ├── types/              # TypeScript Types
│   │   ├── utils/              # Utility Functions
│   │   └── config/             # Configuration
│   └── middleware.ts           # Auth Middleware
├── public/                     # Static Assets
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── next.config.js
└── README.md
```

## 🚀 เริ่มต้นใช้งาน

### ข้อกำหนดเบื้องต้น

- Node.js 18.17+
- npm/yarn/pnpm
- Git

### การติดตั้ง

```bash
# Clone repository
git clone https://github.com/your-org/lets-together.git
cd lets-together

# ติดตั้ง dependencies
npm install

# คัดลอก environment variables
cp .env.example .env.local

# เริ่ม development server
npm run dev
```

เปิดเบราว์เซอร์ที่ `http://localhost:3000`

### สคริปต์ที่ใช้งานได้

```bash
npm run dev          # เริ่ม development server
npm run build        # Build สำหรับ production
npm run start        # เริ่ม production server
npm run lint         # ตรวจสอบโค้ดด้วย ESLint
npm run type-check   # ตรวจสอบ TypeScript
npm run test         # รัน tests
npm run test:watch   # รัน tests ในโหมด watch
```

## 🎨 Design System

### สีธีม (Themes)

#### 🟢 Passenger Mode (Default)
- **Primary**: Emerald Green (`#16a34a`)
- **Secondary**: Ocean Blue (`#0284c7`)
- **Background**: Emerald 50 (`#f0fdf4`)

#### 🔵 Driver Mode
- **Primary**: Deep Navy (`#1e3a5f`)
- **Accent**: Orange (`#ea580c`)
- **Background**: Slate 50 (`#f8fafc`)

### ฟอนต์ (Typography)
- **Thai**: Sarabun (รองรับภาษาไทยอย่างสมบูรณ์)
- **Heading**: Plus Jakarta Sans
- **Body**: Inter

### คอมโพเนนต์หลัก

| หมวดหมู่ | คอมโพเนนต์ |
|-----------|------------|
| **Base UI** | Button, Input, Card, Badge, Avatar, Modal, Toast, Rating, Skeleton |
| **Layout** | Header, RoleToggle, Footer, Navigation |
| **Driver** | RouteForm, RequestCard, ActiveRouteMap, VehicleInfo |
| **Passenger** | SearchForm, RouteCard, RouteResults, BookingForm, LiveTripMap |
| **Shared** | CostBreakdown, DriverProfile, PassengerProfile, TripCard, SOSEmergencyButton, VerificationBadge |
| **Map** | TripMap, RoutePolyline, VehicleMarker, WaypointMarker |

## 🔐 การยืนยันตัวตน (Authentication)

### ระดับการยืนยัน 4 ระดับ

| ระดับ | ไอคอน | คำอธิบาย |
|--------|--------|------------|
| **UNVERIFIED** | ❌ | ยังไม่ได้ยืนยัน |
| **PHONE_VERIFIED** | 📱 | ยืนยันเบอร์โทรด้วย OTP |
| **KYC_VERIFIED** | 🆔 | สแกนใบหน้าจับคู่บัตรประชาชน (e-KYC) |
| **FULL_VERIFIED** | ✅ | ครบทุกขั้นตอน รวมใบขับขี่และป้ายภาษี |

### Flow การสมัครสมาชิก

1. **เบอร์โทรศัพท์** → รับ OTP 6 หลัก
2. **ยืนยัน OTP** → ไปขั้นตอนข้อมูลส่วนตัว
3. **ข้อมูลส่วนตัว** → ชื่อ-นามสกุล
4. **เลือกบทบาท** → ผู้โดยสาร / ผู้ขับขี่ (ต้อง FULL_VERIFIED)
5. **ยอมรับเงื่อนไข** → เสร็จสิ้น

## 🗺️ ฟีเจอร์หลัก

### 👨‍✈️ ผู้ขับขี่ (Driver)
- **ประกาศเส้นทาง** - กำหนดจุดเริ่มต้น/จุดหมาย/จุดแวะพัก/เวลา/ที่นั่งว่าง
- **จัดการคำขอ** - ดูโปรไฟล์ผู้โดยสาร ยอมรับ/ปฏิเสธคำขอ
- **นำทางเรียลไทม์** - GPS tracking, จุดรับ-ส่ง, ปุ่ม SOS
- **สถิติรายได้** - ดูรายได้ ค่าใช้จ่าย กราฟแนวโน้ม

### 🧍‍♂️ ผู้โดยสาร (Passenger)
- **ค้นหาเส้นทาง** - กรองตามจุดเริ่มต้น/ปลายทาง/วันที่/ราคา/คะแนน
- **ส่งคำขอ** - เลือกจุดขึ้น-ลง/จำนวนสัมภาระ/ข้อความเพิ่มเติม
- **ติดตามการเดินทาง** - GPS แบบเรียลไทม์ ปุ่ม SOS แชร์ตำแหน่ง
- **ประวัติการเดินทาง** - ดูรายละเอียด ให้คะแนน ดาวน์โหลดใบเสร็จ

### 🛡️ ความปลอดภัย (Safety)
- **ปุ่ม SOS** - กดค้าง 3 วินาที → นับถอยหลัง → ส่ง Police I Lert U
- **ติดตาม GPS** - แชร์ตำแหน่งให้คนใกล้ชิค ตรวจจับเบี่ยงเบนเส้นทาง
- **ระบบคะแนน 2 ทิศทาง** - ให้คะแนนกัน และกัน คะแนน < 4.0 = ระงับชั่ว่วคราว
- **ยืนยันตัวตน 4 ระดับ** - OTP → e-KYC → ใบขับขี่/ป้ายภาษี → คะแนนรีวิว

### 💰 การคำนวณค่าใช้จ่าย (透明透明)

```typescript
// สูตรคำนวณค่าโดยสารต่อคน
C_passenger = (C_fuel + C_tolls) / (N_driver + N_passengers)

// เพดานราคาต่อที่นั่ง (ป้องกันการตั้งราคาเกิน)
C_seat = (R_rate × D) / N_seats
```

**ตัวอย่าง:**
- ค่าน้ำมัน: 120 บาท
- ค่าทางด่วน: 50 บาท
- ผู้โดยสาร: 3 คน + คนขับ 1 คน = 4 คน
- **ค่าโดยสารต่อคน = (120 + 50) / 4 = 42.50 บาท**

## 📱 PWA (Progressive Web App)

- ✅ ติดตั้งได้บนหน้าจอหลัก (Installable)
- ✅ ทำงานออฟไลน์ได้ (Offline Support)
- ✅ Push Notifications
- ✅ App Shortcuts (ค้นหา/ประกาศ/การเดินทาง)
- ✅ Splash Screens & App Icons

## 🧪 Testing

```bash
# รัน unit tests
npm run test

# รัน tests พร้อม coverage
npm run test:coverage

# รัน E2E tests (ถ้ามี)
npm run test:e2e
```

### Test Coverage Targets
- Unit Tests: > 80%
- Integration Tests: > 70%
- E2E Tests: Critical paths only

## 🚢 Deployment

### Vercel (แนะนำ)
```bash
# Connect GitHub repo to Vercel
# Set environment variables in Vercel dashboard
# Deploy automatically on push to main
```

### Docker
```dockerfile
# Build
docker build -t lets-together .

# Run
docker run -p 3000:3000 --env-file .env.production lets-together
```

### Environment Variables สำหรับ Production
```env
NEXT_PUBLIC_API_URL=https://api.letsgotogether.com/api/v1
NEXT_PUBLIC_WS_URL=wss://api.letsgotogether.com
JWT_SECRET=super-secure-random-string
NEXT_PUBLIC_MOCK_API=false
```

## 🤝 Contributing

1. Fork repository
2. สร้าง feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
4. เปิด Pull Request

### Code Style
- ใช้ TypeScript strict mode
- Follow ESLint + Prettier config
- เขียน tests สำหรับฟีเจอร์ใหม่
- Update documentation

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📞 Contact & Support

- **Website**: https://letsgotogether.com
- **Email**: support@letsgotogether.com
- **GitHub Issues**: [Report Bug/Request Feature](https://github.com/your-org/lets-together/issues)

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - React Framework
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [Radix UI](https://www.radix-ui.com/) - Accessible UI Components
- [Zustand](https://github.com/pmndrs/zustand) - State Management
- [Leaflet](https://leafletjs.com/) - Interactive Maps
- [Lucide Icons](https://lucide.dev/) - Beautiful Icons
- [date-fns](https://date-fns.org/) - Date Utility

---

<p align="center">
  Made with ❤️ for Thai Community<br>
  <strong>ทางเดียวกัน ไปด้วยกัน</strong>
</p>