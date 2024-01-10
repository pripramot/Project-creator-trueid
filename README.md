# Project-creator-trueid
พื้นที่เก็บงานเขียนของพี่มิว-น้องมิ้น



<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" height="200px" srcset="https://github.com/jmorganca/ollama/assets/3325447/56ea1849-1284-4645-8970-956de6e51c3c">
    <img alt="logo" height="200px" src="https://github.com/jmorganca/ollama/assets/3325447/0d0b44e2-8f4a-4e99-9b52-a5c1c741c8f7">
  </picture>
</div>

# Ollama

[![Discord](https://dcbadge.vercel.app/api/server/ollama?style=flat&compact=true)](https://discord.gg/ollama)

Get up and running with large language models locally.

### macOS

[Download](https://ollama.ai/download/Ollama-darwin.zip)

### Windows

Coming soon! For now, you can install Ollama on Windows via WSL2.

### Linux & WSL2

```
curl https://ollama.ai/install.sh | sh
```

[Manual install instructions](https://github.com/jmorganca/ollama/blob/main/docs/linux.md)

### Docker

The official [Ollama Docker image](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` is available on Docker Hub.

## Quickstart

To run and chat with [Llama 2](https://ollama.ai/library/llama2):

```
ollama run llama2
```

## Model library

Ollama supports a list of open-source models available on [ollama.ai/library](https://ollama.ai/library 'ollama model library')

Here are some example open-source models that can be downloaded:

| Model              | Parameters | Size  | Download                       |
| ------------------ | ---------- | ----- | ------------------------------ |
| Llama 2            | 7B         | 3.8GB | `ollama run llama2`            |
| Mistral            | 7B         | 4.1GB | `ollama run mistral`           |
| Dolphin Phi        | 2.7B       | 1.6GB | `ollama run dolphin-phi`       |
| Phi-2              | 2.7B       | 1.7GB | `ollama run phi`               |
| Neural Chat        | 7B         | 4.1GB | `ollama run neural-chat`       |
| Starling           | 7B         | 4.1GB | `ollama run starling-lm`       |
| Code Llama         | 7B         | 3.8GB | `ollama run codellama`         |
| Llama 2 Uncensored | 7B         | 3.8GB | `ollama run llama2-uncensored` |
| Llama 2 13B        | 13B        | 7.3GB | `ollama run llama2:13b`        |
| Llama 2 70B        | 70B        | 39GB  | `ollama run llama2:70b`        |
| Orca Mini          | 3B         | 1.9GB | `ollama run orca-mini`         |
| Vicuna             | 7B         | 3.8GB | `ollama run vicuna`            |
| LLaVA              | 7B         | 4.5GB | `ollama run llava`             |

> Note: You should have at least 8 GB of RAM available to run the 7B models, 16 GB to run the 13B models, and 32 GB to run the 33B models.

## Customize a model

คู่มือการเรียนรู้ทีละขั้นตอนโดยใช้ Python และ Google Gemini AI เพื่อสร้าง Chatbots
คุณพร้อมที่จะสำรวจโลกแห่งปัญญาประดิษฐ์แล้วหรือยัง? มาร่วมเดินทางเพื่อสร้างแชทบอทโดยใช้ Python และโมเดล Gemini AI ของ Google กันเถอะ! คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการจัดการ generative AI และ Gemini AI ของ Google เพื่อสร้างแชทบอท นอกจากนี้เรายังจะใช้ประโยชน์จากเครื่องมืออันทรงพลังของ Google Cloud สำหรับการพัฒนาโปรแกรมและการแชร์ข้อมูล

ส่วนที่ 1: ทำความเข้าใจ Generative AI ของ Google
Gemini ของ Google คือชุดโมเดล AI ที่สร้างหลายรูปแบบซึ่งพัฒนาโดยห้องปฏิบัติการวิจัย AI ของ Google, DeepMind และ Google Research โมเดลเหล่านี้สามารถรับอินพุตข้อความและรูปภาพได้ ขึ้นอยู่กับว่ารูปแบบโมเดลรองรับอะไรบ้าง ได้รับการออกแบบมาเพื่อตีความรูปภาพและข้อความ ทำให้เป็นตัวเลือกที่ยอดเยี่ยมสำหรับการสร้างแชทบอท ( Google AI Dev )

ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม Python
ในการเริ่มต้น คุณจะต้องตั้งค่าสภาพแวดล้อม Python Python เป็นภาษาการเขียนโปรแกรมระดับสูงที่มีการตีความซึ่งง่ายต่อการอ่านและเขียน มีการใช้กันอย่างแพร่หลายในด้านวิทยาศาสตร์ข้อมูล การเรียนรู้ของเครื่อง และการพัฒนา AI คุณสามารถติดตั้ง Python ได้โดยใช้เว็บไซต์อย่างเป็นทางการหรือผ่านตัวจัดการแพ็คเกจของระบบ

ขั้นตอนที่ 2: การติดตั้ง SDK ของ Google
เมื่อคุณตั้งค่า Python แล้ว คุณจะติดตั้ง SDK ของ Google ได้ SDK จัดเตรียมอินเทอร์เฟซ Python ให้กับโมเดล AI เจนเนอเรชั่นของ Google คุณสามารถติดตั้งได้โดยใช้ pip ซึ่งเป็นตัวติดตั้งแพ็คเกจของ Python นี่คือวิธีการ:


pip install google-cloud-aiplatform
ขั้นตอนที่ 3: รับคีย์ API
หากต้องการใช้ SDK คุณจะต้องมีคีย์ API คุณสามารถรับสิ่งนี้ได้จาก Google Cloud Console ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่ คอนโซล Google Cloud
คลิกตัวเลือก "โครงการ" ทางด้านซ้ายมือ
คลิกที่ "สร้างโครงการ"
ตั้งชื่อโครงการของคุณแล้วคลิก "สร้าง"
คลิกที่ตัวเลือก "API & Services" ทางด้านซ้ายมือ
คลิกที่ "แดชบอร์ด"
คลิกที่ "เปิดใช้งาน API และบริการ"
ในแถบค้นหา พิมพ์ "Cloud AI Platform" และคลิกที่ "Cloud AI Platform"
คลิกที่ "เปิดใช้งาน"
คลิกที่ "ข้อมูลรับรอง"
คลิกที่ "สร้างข้อมูลรับรอง"
คลิกที่ "คีย์ API"
คลิกที่ "สร้าง"
ขั้นตอนที่ 4: เรียกใช้แอปพลิเคชันราศีเมถุน
เมื่อคุณมีคีย์ API แล้ว คุณก็สามารถเรียกใช้สคริปต์ Python ได้ นี่คือตัวอย่างวิธีที่คุณสามารถทำได้:

```
python gemini_app.py
```

### ส่วนที่ 2: การสร้าง Chatbots ด้วย Google Gemini AI
แชทบอทเป็นโปรแกรมคอมพิวเตอร์ที่ออกแบบมาเพื่อโต้ตอบกับผู้ใช้ในเวลาเดียวกัน สามารถใช้เพื่อวัตถุประสงค์ที่หลากหลาย 
เช่น การตอบคำถามของลูกค้า การนัดหมาย และอื่นๆ

### ขั้นตอนที่ 1: การตั้งค่าแอปพลิเคชัน Flask

#### Flask เป็นเฟรมเวิร์ก Python บนเว็บน้ำหนักเบาที่ใช้สำหรับสร้างเว็บแอปพลิเคชัน คุณสามารถตั้งค่าแอปพลิเคชัน Flask ได้โดยใช้รหัสต่อไปนี้:

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
    return 'Hello, world!'

if __name__ == '__main__':
    app.run(debug=True)
ขั้นตอนที่ 2: บูรณาการ SDK ของ Google
เมื่อคุณตั้งค่าแอปพลิเคชัน Flask แล้ว คุณก็สามารถผสานรวม SDK ของ Google ได้ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:


from google.cloud import aiplatform

# Instantiate the AI Platform client
client = aiplatform.AIPlatformServiceClient()

# Load the model
model = client.load_model('projects/[PROJECT_ID]/locations/[LOCATION]'
                           '/models/[MODEL_ID]')


# Make a prediction
response = model.predict(inputs=[[input]])

# Print the response
print(response)
```

ส่วนที่ 3: การใช้ประโยชน์จากเครื่องมือของ Google Cloud สำหรับการพัฒนาโปรแกรมและการแชร์ข้อมูล
Google Cloud มีชุดเครื่องมือที่ช่วยให้นักพัฒนาสามารถเรียกใช้แอปพลิเคชันบนโครงสร้างพื้นฐานสาธารณะหรือส่วนตัวได้ 
นอกจากนี้ยังมีเครื่องมือสำหรับนักพัฒนาที่มีประสิทธิภาพสำหรับการพัฒนาโปรแกรมและการแบ่งปันข้อมูล

ขั้นตอนที่ 1: การตั้งค่าบัญชี Google Cloud
หากต้องการใช้เครื่องมือของ Google Cloud คุณจะต้องตั้งค่าบัญชี Google Cloud ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่ คอนโซล Google Cloud
คลิกที่ปุ่ม "สร้างบัญชี"
ทำตามคำแนะนำบนหน้าจอเพื่อสร้างบัญชีของคุณ
ขั้นตอนที่ 2: การตั้งค่าโครงการ
เมื่อคุณตั้งค่าบัญชี Google Cloud แล้ว คุณสามารถสร้างโปรเจ็กต์ใหม่ได้ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่ คอนโซล Google Cloud
คลิกตัวเลือก "โครงการ" ทางด้านซ้ายมือ
คลิกที่ "สร้างโครงการ"
ตั้งชื่อโครงการของคุณแล้วคลิก "สร้าง"
ขั้นตอนที่ 3: การตั้งค่าการเรียกเก็บเงิน
ก่อนเริ่มใช้เครื่องมือของ Google Cloud คุณจะต้องตั้งค่าการเรียกเก็บเงินก่อน ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่ คอนโซล Google Cloud
คลิกตัวเลือก "การเรียกเก็บเงิน" ทางด้านซ้ายมือ
คลิกที่ "เพิ่มบัญชีสำหรับการเรียกเก็บเงิน"
ทำตามคำแนะนำบนหน้าจอเพื่อเพิ่มบัญชีสำหรับการเรียกเก็บเงินของคุณ
ขั้นตอนที่ 4: การใช้เครื่องมือของ Google Cloud
เมื่อคุณตั้งค่าบัญชี Google Cloud แล้ว คุณสามารถเริ่มใช้เครื่องมือของ Google Cloud ได้ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่ คอนโซล Google Cloud
คลิกที่ตัวเลือก "Cloud Shell" ทางด้านซ้ายมือ
คลิกที่ปุ่ม "เริ่ม Cloud Shell"
ทำตามคำแนะนำบนหน้าจอเพื่อเริ่มเซสชัน Cloud Shell
ส่วนที่ 4: การแชร์ข้อมูลกับ Google Cloud
Google Cloud ช่วยให้คุณแบ่งปันข้อมูลกับผู้ใช้หรือบริการอื่น ๆ สิ่งนี้มีประโยชน์สำหรับการทำงานร่วมกันในโครงการ การแชร์ข้อมูลระหว่างบริการต่างๆ และอื่นๆ

ขั้นตอนที่ 1: การแชร์ข้อมูลกับบริการ Google Cloud
คุณสามารถแชร์ข้อมูลกับบริการของ Google Cloud ได้โดยใช้คอนโซลผู้ดูแลระบบ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่คอนโซลผู้ดูแลระบบ
คลิกที่ตัวเลือก "การแบ่งปันข้อมูล" ทางด้านซ้ายมือ
คลิกที่ "แบ่งปันข้อมูลกับบริการ Google Cloud"
ปฏิบัติตามคำแนะนำบนหน้าจอเพื่อแชร์ข้อมูลของคุณ
ขั้นตอนที่ 2: การแบ่งปันข้อมูลกับผู้ใช้รายอื่น
คุณยังสามารถแบ่งปันข้อมูลกับผู้ใช้รายอื่นได้ ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

ไปที่คอนโซลผู้ดูแลระบบ
คลิกที่ตัวเลือก "การแบ่งปันข้อมูล" ที่ด้านข้างมือ
คลิกที่ "แบ่งปันข้อมูลกับผู้ใช้รายอื่น"
ปฏิบัติตามคำแนะนำบนหน้าจอเพื่อแชร์ข้อมูลของคุณ
บทสรุป
เมื่อปฏิบัติตามคำแนะนำนี้ คุณจะมีความเข้าใจอย่างถ่องแท้เกี่ยวกับวิธีการใช้ Python และโมเดล Gemini AI ของ Google เพื่อสร้างแชทบอท นอกจากนี้คุณยังจะได้เรียนรู้วิธีใช้ประโยชน์จากเครื่องมือของ Google Cloud สำหรับการพัฒนาโปรแกรมและการแชร์ข้อมูล ขอให้มีความสุขในการเขียนโค้ด!

โปรดจำไว้ว่า Google มีเครื่องมือสำหรับนักพัฒนาบนเว็บฟรี นั่นคือ Google AI Studio ซึ่งช่วยให้คุณพัฒนาข้อความแจ้งได้อย่างรวดเร็ว จากนั้นจึงรับคีย์ API เพื่อใช้ในแอปของคุณ ( Google AI Blog ) ดังนั้น หากคุณเพิ่งเริ่มต้นใช้งานเครื่องมือ AI ของ Google นี่เป็นจุดเริ่มต้นที่ดี!

หมายเหตุ: อย่าลืมเคารพความเป็นส่วนตัวของผู้ใช้และความปลอดภัยของข้อมูลเสมอเมื่อสร้างแอปพลิเคชันด้วย AI


