



# Strapi คืออะไร
Strapi คือระบบ **Content Management System (CMS)** แบบ **Headless** ที่ถูกพัฒนาโดยใช้ JavaScript และ Node.js ซึ่งมีความยืดหยุ่นสูง ผู้ใช้สามารถสร้างและจัดการเนื้อหาต่างๆ ผ่าน API ได้อย่างง่ายดายโดยไม่ต้องผูกพันกับรูปแบบการแสดงผลเฉพาะแพลตฟอร์มใดๆ
# สารบัญ
 - [รายละเอียดของ Strapi](#%E0%B8%A3%E0%B8%B2%E0%B8%A2%E0%B8%A5%E0%B8%B0%E0%B9%80%E0%B8%AD%E0%B8%B5%E0%B8%A2%E0%B8%94%E0%B8%82%E0%B8%AD%E0%B8%87%20Strapi)
 - [ขั้นตอนการติดตั้ง](#%E0%B8%82%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B8%95%E0%B8%AD%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%95%E0%B8%B4%E0%B8%94%E0%B8%95%E0%B8%B1%E0%B9%89%E0%B8%87)
 - [กรณีการใช้งาน](#%E0%B8%81%E0%B8%A3%E0%B8%93%E0%B8%B5%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99)
 - [.gitignore](#.gitignore)
 - [Deployment](#Deployment)
## รายละเอียดของ Strapi
CMS หรือ **Content Management System** คือระบบที่ช่วยในการจัดการเนื้อหาเว็บไซต์หรือแอปพลิเคชันโดยไม่จำเป็นต้องมีความรู้ทางการเขียนโค้ดมากนัก ผู้ใช้สามารถสร้าง, แก้ไข, และจัดการเนื้อหาผ่านอินเทอร์เฟซที่ใช้งานง่าย เช่น แดชบอร์ดหรือแผงควบคุม ซึ่งช่วยให้การจัดการเนื้อหาสะดวกและรวดเร็วขึ้น

**Strapi** เป็นหนึ่งใน CMS ที่ได้รับความนิยม โดย Strapi เป็น CMS แบบ Headless ซึ่งหมายความว่า มันแยกส่วนของการจัดการเนื้อหาออกจากส่วนของการแสดงผล ทำให้สามารถเชื่อมต่อกับ Frontend หรือแอปพลิเคชันใด ๆ ผ่าน API เช่น REST หรือ GraphQL ได้อย่างยืดหยุ่น นอกจากนี้ Strapi ยังเป็น Open Source ซึ่งหมายความว่าผู้ใช้สามารถปรับแต่งและขยายการทำงานได้ตามความต้องการ

### องค์ประกอบของ Strapi
องค์ประกอบของ Strapi สามารถเเบ่งย่อยออกเป็น 2 ส่วนได้เเก่ `Content Manager` และ `Content Type-builder` โดย Content Type-builder เป็นตั้วสร้างและจัดการ `Content Type `ซึ่งสามารถแบ่งออกเป็น 2 ประเภทได้เเก่ 

 1. **Collection Type**  เป็นประเภทของเนื้อหาที่สามารถมีหลายรายการได้ เช่น บทความ (Articles), ผลิตภัณฑ์ (Products), หรือโพสต์ในบล็อก (Blog Posts) ซึ่งเหมาะสำหรับข้อมูลที่มีหลายรายการหรือรายการที่มีลักษณะเหมือนกัน
	-   ตัวอย่างการใช้งาน: คุณอาจมี Collection Type สำหรับโพสต์ในบล็อกซึ่งแต่ละโพสต์จะมีข้อมูลเช่น ชื่อเรื่อง, เนื้อหา, และวันที่โพสต์
 2. **Single Type** เป็นประเภทของเนื้อหาที่มีเพียงรายการเดียวเท่านั้น เช่น หน้าแรก (Homepage), การตั้งค่าระบบ (Site Settings), หรือข้อมูลเกี่ยวกับเรา (About Us) ซึ่งเหมาะสำหรับข้อมูลที่ไม่ต้องมีหลายรายการและมีเพียงชุดข้อมูลเดียวที่ใช้ทั่วทั้งเว็บไซต์
	-   ตัวอย่างการใช้งาน: คุณอาจมี Single Type สำหรับหน้าแรกของเว็บไซต์ซึ่งมีข้อมูลเช่น หัวข้อหลัก, ข้อความต้อนรับ, และภาพใหญ่


	![Content-type Builder interface](https://docs.strapi.io/img/assets/content-type-builder/content-types-builder.png) 
Reference: [https://docs.strapi.io/user-docs/content-type-builder](https://docs.strapi.io/user-docs/content-type-builder)


โดยมีประเภทข้อมูลดังนี้
![Fields selection](https://docs.strapi.io/img/assets/content-type-builder/fields-selection.png)
Reference: https://docs.strapi.io/user-docs/content-type-builder/configuring-fields-content-type


**Content Manager** เป็นเครื่องมือที่สำคัญสำหรับการจัดการเนื้อหาใน Strapi ซึ่งช่วยให้ผู้ใช้สามารถจัดการข้อมูลได้อย่างมีประสิทธิภาพและเป็นระเบียบ 
#### ประเภทของ Content Types

1.  **Collection Type**:
    
    -   **Collection Type** คือประเภทของข้อมูลที่สามารถมีหลายรายการ เช่น ฐานข้อมูลที่มีหลายระเบียนที่มีโครงสร้างเดียวกัน
    -   ตัวอย่าง: **User** (Collection Type) ที่มีหลายตัวอย่างของผู้ใช้ โดยแต่ละตัวอย่างมีข้อมูลเช่น ชื่อผู้ใช้, อีเมล, รหัสผ่าน, และบทบาท
    -   ข้อมูลตัวอย่าง:
        -   **Username**: Jennifer
        -   **Email**: Jennifer@dome.tu.ac.th.com
        -   **Password**: Jlaw123
        -   **Role**: Student
2.  **Single Type**:
    
    -   **Single Type** คือประเภทของข้อมูลที่มีเพียงหนึ่งรายการเดียวเท่านั้น โดยใช้สำหรับข้อมูลที่ไม่ต้องการหลายรายการ
    -   ตัวอย่าง: **Contact** (Single Type) ที่มีข้อมูลเพียงชุดเดียวสำหรับข้อมูลติดต่อ เช่น FacebookID, โทรศัพท์, และที่อยู่
    -   ข้อมูลตัวอย่าง:
        -   **LineID**: Jennifer Lawrence
        -   **Phone**: +66 986704012
        -   **Address**: 168/980 etc.

#### ฟังก์ชันการทำงานของ Content Manager

-   **การจัดการ Collection Types**:
    
    -   สามารถดู, สร้าง, แก้ไข, และลบรายการที่อยู่ใน Collection Type
    -   แสดงรายการทั้งหมดในมุมมอง List View และอนุญาตให้ทำการค้นหาและกรองข้อมูล
-   **การจัดการ Single Types**:
    
    -   แสดงข้อมูลทั้งหมดของ Single Type ในมุมมอง Edit View เนื่องจากมีเพียงรายการเดียว
-   **การค้นหาและการกรอง**:
    
    -   ใช้เครื่องมือค้นหาและกรองเพื่อค้นหาหรือกรองรายการที่ต้องการภายใน Collection Type
-   **การเพิ่มและแก้ไขข้อมูล**:
    
    -   เพิ่มข้อมูลใหม่หรือแก้ไขข้อมูลที่มีอยู่ใน Content Manager

Content Manager จึงเป็นเครื่องมือสำคัญที่ช่วยให้การจัดการเนื้อหาภายใน Strapi เป็นไปอย่างมีประสิทธิภาพและเป็นระเบียบตามที่กำหนดไว้ใน Content-Type Builder.

นอกจากนี้ยังมีฟีเจอร์อื่นๆเช่น  `Media Library`, `Documentation`, `Plugins`, `Marketplace` เป็นต้น
## ขั้นตอนการติดตั้ง
ความต้องการขั้นต่ำของระบบ

 -  **NodeJS**  v.18 upto v.20
 - **npm**  < v.6

ขั้นตอน
 1. สร้าง folder ที่ต้องการเก็บ Strapi
 2. กด `Win + R` บนแป้นพิมพ์ แล้วพิมพ์ `cmd` จากนั้นกด Enter เพื่อเปิด Command Prompt
 3. นำทางไปยังโฟลเดอร์ที่สร้างไว้โดย `cd` เข้าไปใน folder ที่สร้างไว้
 4. ทำการ Download และติดตั้ง Strapi ตามคำสั่งดังนี้ 
```
npx create-strapi-app@latest my-project --quickstart
#เมื่อรันจะขึ้นข้อความให้เลือก Login/Sign up หรือ Skip แนะนำให้เลือก Login
```

5. `cd` เข้าไปใน `my-project` จากนั้นทำการตรวจสอบ version ด้วยคำสั่ง`npm -v`
6. เริ่มต้นใช้งาน Strapi ด้วยคำสั่ง `npm run develop` จะเด้งเข้าสู่หน้าสมัคร admin `localhost:1337/admin/register` อัตโนมัติ

![image](https://github.com/user-attachments/assets/f301945f-3591-435b-9297-f60fae73a832)

7. สามารถทำการ Register เพื่อเข้าใช้งานไปยังหน้า `Interface`ของ Strapi

## กรณีการใช้งาน

1.  **เว็บไซต์และบล็อก**: ใช้ Strapi เพื่อจัดการเนื้อหา เช่น บทความ, ข่าวสาร, และโพสต์บล็อก โดยเชื่อมต่อกับ Frontend ที่สร้างด้วยเทคโนโลยีต่าง ๆ เช่น `React`, `Vue`, หรือ `Angular`
    
2.  **แอปพลิเคชันมือถือ**: Strapi สามารถให้บริการเนื้อหาผ่าน API สำหรับแอปพลิเคชันมือถือ (iOS หรือ Android) ทำให้สามารถจัดการข้อมูลที่แสดงในแอปได้ง่าย
    
3.  **ระบบจัดการเนื้อหา eCommerce**: ใช้ Strapi เพื่อจัดการข้อมูลผลิตภัณฑ์, หมวดหมู่, คำสั่งซื้อ, และข้อมูลลูกค้า สำหรับเว็บไซต์หรือแอปพลิเคชัน eCommerce
    
4.  **แพลตฟอร์มการเรียนรู้**: สร้างและจัดการเนื้อหาเกี่ยวกับหลักสูตร, บทเรียน, และข้อสอบ โดย Strapi สามารถเชื่อมต่อกับ Frontend ที่ใช้ในการสอนและเรียนรู้
    
5.  **ระบบการจัดการเนื้อหาภายในองค์กร**: ใช้ Strapi เพื่อจัดการข้อมูลที่ต้องการแบ่งปันภายในองค์กร เช่น เอกสาร, ข่าวสารภายใน, และฐานข้อมูลทรัพยากร
    
6.  **โปรเจกต์ที่ต้องการ API ที่กำหนดเอง**: Strapi ช่วยในการสร้าง API ที่กำหนดเองตามความต้องการของโปรเจกต์ ทำให้สามารถจัดการและให้บริการเนื้อหาได้อย่างยืดหยุ่น

## .gitignore

**`.gitignore` หรือ ไฟล์ที่ไม่ต้องการติดตามใน Git** มีจุดประสงค์และความสำคัญดังนี้

ไฟล์ `.gitignore` เป็นส่วนสำคัญของระบบควบคุมเวอร์ชัน Git โดยใช้ในการ**ระบุไฟล์หรือโฟลเดอร์ที่เราไม่ต้องการให้ Git ติดตามหรือบันทึกใน repository** เช่น ไฟล์ที่สร้างขึ้นโดยเครื่องมือพัฒนาซอฟต์แวร์ ไฟล์ที่เก็บข้อมูลลับ หรือไฟล์ที่เป็นผลลัพธ์จากการคอมไพล์
การกำหนด `.gitignore` ช่วยลดความเสี่ยงในการแชร์ข้อมูลที่ไม่จำเป็นหรือข้อมูลลับ เช่น คีย์ API รหัสผ่าน หรือไฟล์การตั้งค่าเฉพาะท้องถิ่น นอกจากนี้ยังช่วยให้ repository ของคุณมีขนาดเล็กลงและสะอาดขึ้น โดยการละเว้นไฟล์ที่ไม่จำเป็น ตัวอย่างเช่น โฟลเดอร์ที่มี `ข้อมูลส่วนตัว` เป็นต้น

ในกรณีข้างต้นการเพิ่ม `node_modules` และ `.env` ลงใน `.gitignore` เป็นแนวทางปฏิบัติที่ดีเมื่อใช้ Git เพราะเหตุผลดังนี้:
### 1. **node_modules:**

-   **ขนาดใหญ่**: โฟลเดอร์ `node_modules` มักมีขนาดใหญ่มากเนื่องจากประกอบด้วยไฟล์จำนวนมากที่ถูกติดตั้งจากแพ็คเกจที่โครงการของคุณต้องการ ถ้าคุณติดตาม (track) โฟลเดอร์นี้ใน Git จะทำให้ repository ของคุณมีขนาดใหญ่และอาจทำให้การ push และ pull ช้าลง
-   **ไม่จำเป็นต้องติดตาม**: ไฟล์ใน `node_modules` สามารถถูกติดตั้งใหม่ได้ตลอดเวลาจากไฟล์ `package.json` โดยใช้คำสั่ง `npm install` ดังนั้นไม่จำเป็นต้องบันทึกโฟลเดอร์นี้ในระบบควบคุมเวอร์ชัน
-   **แพลตฟอร์มที่ต่างกัน**: ไฟล์ใน `node_modules` อาจแตกต่างกันไปตามแพลตฟอร์ม (เช่น Windows, macOS, หรือ Linux) ทำให้เกิดปัญหาเมื่อพยายามแชร์โฟลเดอร์นี้ระหว่างเครื่องที่ใช้แพลตฟอร์มต่างกัน

### 2. **.env:**

-   **ข้อมูลสำคัญ**: ไฟล์ `.env` มักใช้เพื่อเก็บข้อมูลการตั้งค่าต่าง ๆ เช่น คีย์ API, ข้อมูลการเชื่อมต่อฐานข้อมูล, และตัวแปรสภาพแวดล้อม (environment variables) ซึ่งเป็นข้อมูลที่สำคัญและอาจมีความลับ การแชร์ไฟล์นี้ใน repository อาจทำให้ข้อมูลที่สำคัญเหล่านี้ถูกเปิดเผยต่อบุคคลที่ไม่ควรเห็น
-   **ความแตกต่างในสภาพแวดล้อม**: ไฟล์ `.env` มักจะมีการตั้งค่าที่แตกต่างกันไปตามสภาพแวดล้อม (เช่น การพัฒนา, การทดสอบ, หรือการใช้งานจริง) ดังนั้นแต่ละนักพัฒนาหรือเซิร์ฟเวอร์อาจมีไฟล์ `.env` ของตัวเองที่ไม่ควรถูกแชร์

ดังนั้น การเพิ่ม `node_modules` และ `.env` ลงใน `.gitignore` จะช่วยให้ repository ของคุณมีขนาดเล็กลง, ปลอดภัยมากขึ้น และจัดการได้ง่ายขึ้นในการทำงานร่วมกันในทีม
Reference: https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files

## Deployment

 1.**เตรียม `AWS EC2 Instance`**
 - **สร้าง EC2 Instance**:
	 - ไปที่ AWS Management Console และเลือก EC2
	 - กด "Launch Instance"
	 - เลือก Amazon Machine Image (AMI)  Ubuntu 22.04เลือกขนาดของ Instance  t2.medium 
	 - ตั้งค่า Security Group Rule เพื่ออนุญาตการเชื่อมต่อผ่านพอร์ตที่จำเป็นดังนี้  
		-   **Type:**  `SSH`,  **Protocol:**  `TCP`,  **Port Range**  `22`,  **Source:**  `::/0`
		-   **Type:**  `HTTPS`,  **Protocol:**  `TCP`,  **Port Range**  `443`,  **Source:**  `0.0.0.0/0, ::/0`
		-   **Type:**  `HTTP`,  **Protocol:**  `TCP`,  **Port Range**  `80`,  **Source:**  `0.0.0.0/0, ::/0`
		-   **Type:**  `Custom TCP Rule`,  **Protocol:**  `TCP`,  **Port Range**  `1337`,  **Source:**  `0.0.0.0/0`
บางครั้งการสร้าง Security Group Rule **ที่มากเกินกว่าความจำเป็นอาจนำมาซึ่งผมเสียมากกว่าผลดี** เพราะอาจมี**ความเสี่ยงด้านความปลอดภัย** และทำให้ผู้ผประสงค์ร้ายสามารถโจมตี web application ที่ทำการ deploy ได้
	 - ตรวจสอบและสร้าง Instance
 - **เชื่อมต่อกับ EC2 Instance**:
	 - ใช้ SSH เพื่อเชื่อมต่อไปยัง EC2 Instance โดยใช้ `ssh -i "Key2.pem" ubuntu@ec2-100-27-224-138.compute-1.amazonaws.com`

2.**ติดตั้ง Dependencies บน EC2**

 - **อัพเดตระบบและติดตั้ง Node.js, npm, และ Git**:
```
sudo apt update 
sudo apt upgrade -y 
sudo apt install 
nodejs npm git -y
```
- **ตรวจสอบเวอร์ชัน Node.js และ npm**:
```
node -v npm -v
```

3.**ติดตั้งและตั้งค่า Strapi**
สร้างและตั้งค่าโปรเจกต์ Strapi
	-**สร้างโฟลเดอร์สำหรับโปรเจกต์ Strapi**:
```
mkdir strapi-app
cd strapi-app
```

-**Clone โปรเจกต์จาก GitHub**
หลังจากการทดลอง `npm run develop` ผ่านเครื่องของผู้ใช้ ขั้นตอนต่อไปคือการ push code ใน local file ของเครื่องuser  เพื่อนำไปจัดเก็บใน Github แล้วทำการ Clone code เพื่อสามารถใช้งานผ่าน Server โดยมีวิธีการดังนี้
-   **ตรวจสอบไฟล์ที่ต้องการ Push**
    
    -   ใช้คำสั่ง `cd` เพื่อเปิด Terminal 
    -   ไปยัง directory ที่มีโปรเจกต์ที่ต้องการ
    -  ใช้คำสั่ง `git init` เพื่อเริ่มต้นสร้าง Git repository ใหม่ใน directory ปัจจุบันที่คุณกำลังใช้งานอยู่
    -   ใช้คำสั่ง `git status` เพื่อตรวจสอบการเปลี่ยนแปลงของไฟล์ในโปรเจกต์
-   **Add ไฟล์ที่ต้องการ Push**
    
    -   ใช้คำสั่ง `git add .` เพื่อเพิ่มไฟล์ทั้งหมดที่ต้องการจะ push ขึ้นไปยัง GitHub
    -   หรือเลือกเพิ่มไฟล์เฉพาะที่ต้องการด้วยการใช้คำสั่ง `git add <filename>`เช่น `git add Panuwat`
-   **Commit การเปลี่ยนแปลง**
    
    -   ใช้คำสั่ง `git commit -m "Your commit message"` เพื่อบันทึกการเปลี่ยนแปลงลงใน local repository
    -   ตัวอย่าง: `git commit -m "Initial commit with basic setup"`
-   **Push ไปยัง GitHub**
    
    -   ใช้คำสั่ง `git push origin main` (หรือ `master` หาก branch ชื่อ `master`) เพื่อ push การเปลี่ยนแปลงทั้งหมดจาก local ไปยัง GitHub repository
    -   หากมีการเปลี่ยนแปลงชื่อ branch หรือสร้าง branch ใหม่ ควรเปลี่ยนชื่อ branch ในคำสั่งตามความเหมาะสม
- **Clone Project จาก Github** 
```
git clone https://github.com/Panuwatkongmark6509650633/Panuwat.git
```
**เข้าไปยัง Folder ที่ทำการ Clone ด้วย `cd Panuwat`**
```
# ติดตั้ง Library เนื่องจาก node_module ติด gitignore ทำให้ต้องติดตั้งใหม่
npm install
# สร้าง Project บ่งบอกว่าโปรเจกต์นี้กำลังทำงานในสภาพแวดล้อมการผลิต
NODE_ENV=production 

# รันสคริปต์ `build` ที่กำหนดไว้ในไฟล์ `package.json` ของโปรเจกต์
npm run build
```
ตรวจสอบว่าไฟล์ `.env` มีการตั้งค่าหรือไม่
```
cat .env
```
หากไม่มีให้ทำการเพิ่ม `code` ในส่วน `.env` โดยมีขั้นตอนดังนี้
```
nano .env
```
```
## GNU nano 7.2
HOST=0.0.0.0
PORT=1337
APP_KEYS=bdelYVvqC6uuto3mIf0gwQ==,aScF3hHp8czmf5zXC0oPIQ==,GlQk78G3SfkXiDVB/s7VCQ==,ophDstDIKquV2l75U8gZAA==
API_TOKEN_SALT=3usgidVLUgjlJ7gZVbHISQ==
ADMIN_JWT_SECRET=PFgDJLQb/I1ThrIkbVCFug==
TRANSFER_TOKEN_SALT=Lu8UFgxiBlwpQuA6AvLyJg==
# Database
DATABASE_CLIENT=sqlite
DATABASE_FILENAME=.tmp/data.db
JWT_SECRET=nSrwlWBnsmVQCQZ2CP5aUA==
NODE_ENV=production
```
-   กด `Ctrl+O` เพื่อบันทึกไฟล์ จากนั้นกด `Enter` เพื่อยืนยัน
-   กด `Ctrl+X` เพื่อออกจาก `nano`
ทำการตรวจสอบอีกครั้งด้วยคำสั่ง `cat .env`


4.**เข้าใช้งาน Strapi ผ่าน Server**

หลังจากที่ได้ตั้งค่าโปรเจกต์ Strapi เรียบร้อยแล้ว ขั้นตอนต่อไปคือการรันโปรเจกต์ Strapi บนเซิร์ฟเวอร์และเข้าถึงผ่านเบราว์เซอร์ โดยทำตามขั้นตอนดังนี้:

- **รันโปรเจกต์ Strapi:**
 
    ใช้คำสั่ง `npm run develop` เพื่อเริ่มการพัฒนาโปรเจกต์ Strapi
```
npm run develop
```
-   **ตรวจสอบ Public IPv4 Address ของ Instance:**
    
    -   ทำการ `Copy Public IPv4 address` จาก Instance ที่คุณได้สร้างไว้บนแพลตฟอร์มเซิร์ฟเวอร์ เช่น AWS, DigitalOcean หรือแพลตฟอร์มอื่น ๆ ที่คุณใช้ในการโฮสต์
-   **เข้าถึง Strapi ผ่านเบราว์เซอร์:**
    
    -   เปิดเว็บเบราว์เซอร์และพิมพ์ URL โดยใช้ Public IPv4 Address ที่คุณคัดลอกมา พร้อมกับต่อท้ายด้วย Port `1337` ตัวอย่างเช่น:
```
http://100.27.224.138:1337/
```
เมื่อทำตามขั้นตอนทั้งหมดที่กล่าวมาจะสามารถเข้าถึงและใช้งาน Strapi ผ่าน Server ได้อย่างสมบูรณ์
Reference: https://docs.strapi.io/dev-docs/installation/cli
https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/
https://docs.strapi.io/dev-docs/deployment


