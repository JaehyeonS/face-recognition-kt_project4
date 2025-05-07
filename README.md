# 🧑‍💻 얼굴 인식 시스템 (Face Recognition with YOLO & FaceNet)

## 📌 프로젝트 개요

본 프로젝트는 실시간 웹캠 영상으로부터 얼굴을 탐지하고,  
탐지된 얼굴이 **타깃 인물(내 얼굴)**인지 여부를 판단하는 **AI 기반 얼굴 인식 시스템**입니다.

YOLO 모델을 활용한 객체 검출(Object Detection)과  
FaceNet 또는 YOLO-CLS 모델을 활용한 **인물 분류(Classification)** 방식으로 구현되었습니다.

---

## 🎯 주요 기능

- 실시간 웹캠 스트리밍에서 얼굴 영역 탐지 (YOLO 기반)
- 탐지된 얼굴에 대해 **타인인지/본인인지 분류**
- 다양한 분류 방식 테스트:
  - ✅ YOLO + FaceNet
  - ✅ YOLO + YOLO-CLS (Classifying face regions)
- 결과를 이미지 위에 **확률 수치 및 바운딩 박스**로 시각화

---

## 🖼️ 시스템 구조

[Webcam] → [YOLO 얼굴 탐지] → [분류기 (FaceNet 또는 YOLO-CLS)] → [시각화/결과 출력]

---

## 🔍 사용 예시

| 모델        | 기능 설명                       |
|-------------|-------------------------------|
| YOLO        | 얼굴 탐지 (Bounding Box 출력)  |
| YOLO-CLS    | YOLO 결과 내 얼굴 여부 분류    |
| FaceNet     | 얼굴 임베딩을 비교하여 본인 판단 |

---

## 💾 사용 데이터셋

- Kaggle 유명인 얼굴 이미지
- Roboflow Universe 기반 얼굴 객체 검출 학습용 데이터
- 자체 웹캠 이미지로 Fine-Tuning

---

## 🛠️ 적용 기술

| 항목        | 내용 |
|-------------|------|
| Language    | Python |
| Datasets    | Kaggle, Roboflow, Custom Captures |
| Framework   | OpenCV, NumPy |
| 모델        | YOLOv5, YOLO-CLS, FaceNet |
| IDE         | Google Colab, VS Code |

---

## ▶️ 실행 방법

```bash
# 패키지 설치
pip install opencv-python numpy

# 웹캠 기반 얼굴 인식 실행
python run_face_recognition.py
