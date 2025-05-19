# 🧠 YOLOv8 기반 실시간 객체 인식 웹 애플리케이션 (Flask + OpenCV)

이 프로젝트는 **Ultralytics YOLOv8 모델**과 **Flask 웹 프레임워크**를 이용해, 웹캠을 통해 실시간으로 촬영한 영상에서 **객체를 탐지하고 화면에 시각화**하는 **웹 애플리케이션**입니다.  
Flask 서버를 통해 MJPEG 스트림으로 실시간 결과를 클라이언트에 전달하며, **Colab 환경에서도 실행이 가능**하도록 **Ngrok 연동**을 제공합니다.

---

## 📷 데모 화면

> 객체 인식 결과를 시각화한 예시 캡처

<img width="700" alt="demo" src="https://github.com/user-attachments/assets/3eb2ecbe-4f40-483c-87a9-87a845c79682" />
---

## 🚀 실행 방법

### 1. 로컬 환경에서 실행
```bash
# 패키지 설치
pip install flask flask-cors flask-sock opencv-python pyngrok ultralytics

# YOLOv8 모델 다운로드는 코드 실행 시 자동 진행됩니다

# 서버 실행
python app.py
```

### 2. 구글 코랩에서 실행
```bash
# Ngrok 토큰 등록
!ngrok authtoken <your_token>

# run_server.py 실행
!python run_server.py
```

---

## 💡 핵심 기능
### 📸 웹캠 프레임을 실시간 캡처 (OpenCV)
### 🤖 YOLOv8 모델로 객체 인식 및 바운딩 박스 시각화
### 🛰 MJPEG 스트림 방식으로 인식 결과 실시간 전달
### 🌍 웹 페이지에서 실시간 객체 탐지 화면 확인
### 🔗 Ngrok을 통한 외부 접속 및 시연 가능


---
## 🧩 기술 스택
| 영역     | 사용 기술                                     |
| ------ | ----------------------------------------- |
| 백엔드    | Python, Flask, flask-sock, flask-cors     |
| 영상 처리  | OpenCV, Ultralytics YOLOv8                |
| 프론트엔드  | HTML5 (`<img src=\"/video_feed\">` 기반 시청) |
| 외부 연동  | Ngrok, pyngrok                            |
| 테스트 환경 | Google Colab                              |


---
## 📁 디렉토리 구조
```bash
.
├── app.py
├── run_server.py
├── sample_data
│   ├── anscombe.json
│   ├── california_housing_test.csv
│   ├── california_housing_train.csv
│   ├── mnist_test.csv
│   ├── mnist_train_small.csv
│   └── README.md
├── uploads
│   ├── image_example1.jpg
│   ├── image_example2.jpg
|
├── www
│   ├── index.html
│   └── js
│       └── app.js
└── yolov8n.pt
```

---
## 🛠 향후 개선 방향
### YOLOv8 모델의 정확도 향상을 위한 custom 데이터셋 적용
### 모델 처리 속도 향상을 위한 GPU 최적화
### 모바일/저사양 디바이스에서도 작동하도록 프레임 압축 방식 도입
### 인식 결과를 텍스트로 로그 저장 및 다운로드 기능 추가

---
## 🧑‍💻 개발자
### 👤 최기영
### 고급 웹 프로그래밍 과제 프로젝트
