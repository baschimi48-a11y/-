BuildCalc TH - Android project

แอปนี้เป็น WebView ที่ฝังหน้าเครื่องคำนวณวัสดุก่อสร้างไว้ในแอป และใช้งานออฟไลน์ได้

หมายเหตุสำคัญ:
- ZIP นี้เป็นซอร์สโปรเจกต์ ไม่ใช่ APK ที่คอมไพล์แล้ว
- เพิ่ม GitHub Actions workflow ไว้ที่ .github/workflows/build-apk.yml เพื่อให้ GitHub สร้าง APK บนคลาวด์ได้

สร้าง APK โดยใช้มือถือ Android อย่างเดียว (ต้องมีบัญชี GitHub):
1. แตก ZIP นี้ในมือถือ
2. เปิด github.com ใน Chrome แล้วเข้าสู่ระบบ
3. สร้าง repository ใหม่ (แนะนำ Public หากต้องการใช้ GitHub Actions ฟรีได้ง่ายขึ้น) ตั้งชื่อ BuildCalcTH และสร้าง repository ว่าง
4. อัปโหลด “เนื้อหาทั้งหมดภายในโฟลเดอร์ BuildCalcTH_Android” ไปไว้ที่ root ของ repository โดยต้องรวมโฟลเดอร์ .github ด้วย
   - ตรวจสอบว่า build.gradle, settings.gradle, app/ และ .github/workflows/build-apk.yml อยู่ระดับบนสุดของ repository
   - ถ้าอัปโหลดผ่านมือถือไม่เห็นโฟลเดอร์ .github ให้เปิด “Desktop site” ใน Chrome หรือใช้ GitHub app/เครื่องมืออัปโหลดที่รองรับโฟลเดอร์ซ่อน
5. เปิดแท็บ Actions ของ repository แล้วเลือก workflow “Build BuildCalcTH APK”
6. กด Run workflow แล้วรอให้สถานะเป็นสีเขียว
7. เปิดงานที่เสร็จแล้ว เลื่อนลงไปที่ Artifacts แล้วดาวน์โหลด BuildCalcTH-debug-APK
8. แตก ZIP ของ artifact จะได้ app-debug.apk จากนั้นแตะไฟล์ APK เพื่อติดตั้ง หาก Android ขอสิทธิ์ติดตั้งจากแหล่งนี้ ให้เปิดเฉพาะเบราว์เซอร์/แอปที่คุณใช้ดาวน์โหลดและเชื่อถือ

หาก workflow ล้มเหลว ให้เปิด log ของงาน Build debug APK แล้วใช้ข้อความผิดพลาดเพื่อตรวจสอบ

หมายเหตุ: APK นี้เป็น debug build สำหรับติดตั้ง/ทดสอบ ไม่ใช่ signed release สำหรับเผยแพร่ใน Play Store
