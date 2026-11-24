# Vibe Generate Clip

ระบบสร้างวิดีโอสั้นแนวตั้ง 1080x1920 แบบอัตโนมัติจากไฟล์สคริปต์ JSON ด้วยภาษา Python ทำงานครบทั้งกระบวนการ ตั้งแต่การดึงภาพประกอบ การสังเคราะห์เสียงพากย์ภาษาไทย ไปจนถึงการตัดต่อใส่เอฟเฟกต์ซูมภาพและรวมไฟล์เป็น MP4

## Main Features
- **JSON-Driven Script:** กำหนดบทพากย์และคำค้นหารูปภาพแยกตามซีนได้ง่ายผ่านไฟล์ JSON
- **Smart Image Fetching:** สกัดคีย์เวิร์ดอัตโนมัติจาก Prompt เพื่อค้นหารูปภาพแนวตั้ง (1080x1920) พร้อมระบบ Retry และสร้างภาพพื้นหลังสำรองหากดึงรูปไม่สำเร็จ
- **Thai Text-to-Speech:** สร้างเสียงพากย์ภาษาไทยที่เป็นธรรมชาติด้วย `edge-tts` รองรับเสียง `th-TH-NiwatNeural` และ `th-TH-PremwadeeNeural`
- **Dynamic Ken Burns Effect:** ใส่เอฟเฟกต์ซูมภาพเคลื่อนไหว เพื่อตัดขอบลายน้ำ และจัดกึ่งกลางอัตโนมัติ
- **Asset Caching:** ตรวจสอบไฟล์ภาพและเสียงที่มีอยู่แล้ว เพื่อข้ามการสร้างซ้ำ ช่วยประหยัดเวลาเมื่อรันแก้ไขงาน

## Tech Stack
- **Language:** Python 3.10+
- **Video Editing:** MoviePy, Pillow, NumPy
- **Text-to-Speech:** Edge-TTS (`edge-tts`)
- **HTTP Client:** Requests

## Project Structure
```text
Vibe-Auto-Generate-Clip/
├── assets/
│   ├── audio/
│   └── images/
├── modules/
│   ├── audio_gen.py
│   ├── image_gen.py
│   └── video_engine.py
├── output/
├── scripts/
│   └── story_01.json
├── main.py
├── requirements.txt
└── README.md
