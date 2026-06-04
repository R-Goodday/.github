<div align="center">

<img src="YOUR_LOGO_URL" alt="꿈틀 로고" width="200"/>

# 꿈틀 (Kkumteul)

아이가 직접 만드는 AI 맞춤형 동화로 상상력, 어휘력, 사고력을 함께 키우는 유아 동화 서비스
</div>

<br/>

---

## 🎬 Service Preview

교훈, 등장인물, 배경을 선택하면 AI가 동화와 삽화를 자동으로 생성하고, 부모 목소리를 학습한 TTS로 동화를 읽어줍니다.

- 🎨 **교훈 · 등장인물 · 배경** 선택 → AI가 나만의 동화 + 삽화 자동 생성
- 🎙️ **부모 목소리**를 학습한 TTS로 친숙하고 안정적인 독서 경험 제공
- 🎮 **3단계 지식그래프 게임**으로 분석적 · 종합적 · 추리적 사고력 향상
- 📝 **핵심 어휘 자동 추출** 단어장 + 동화 공유 기능

---

## ✨ What We Build

- 교훈 · 등장인물 · 배경 선택 기반 AI 맞춤형 동화 자동 생성
- 동화 도메인 특화 품사 순환 생성 구조(FP-Tree) + Propp 민담 구조론 적용
- FLUX.2-klein-4B 기반 페이지별 삽화 자동 생성
- 부모 목소리 1분 녹음으로 Voice Cloning TTS 구현 (GPT-SoVITS)
- Kafka + Redis + SSE 기반 동화 · 삽화 · TTS 비동기 병렬 스트리밍
- 3단계 지식그래프 게임 — 바구니 분류 → 별자리 조립 → 관계도 탐험
- 페이지 단위 어휘 자동 추출 단어장 및 동화 공유 기능

---

## 📱 Screenshots

<div align="center">
  
| <img src="https://github.com/user-attachments/assets/3b6daa18-f1ee-4d05-91d2-2e7c86fc1a60" width="200"/> | <img src="https://github.com/user-attachments/assets/75c8c827-23d6-4e36-9e2c-2f1d84a88eca" width="200"/> | <img src="https://github.com/user-attachments/assets/bee7cce6-91fb-4646-a2e6-d61f81224e58" width="200"/> |
|:---:|:---:|:---:|
| **동화 생성** | **동화 읽기** | **동화 목록** |

| <img src="https://github.com/user-attachments/assets/873f54f6-5cb7-4193-bb79-b01de00a5fc2" width="190"/> | <img src="https://github.com/user-attachments/assets/406dc8ab-40d3-4a33-8a1a-e073befd5b8f" width="190"/> | <img src="https://github.com/user-attachments/assets/dda972c1-9733-4b2c-9bc0-e4a2eaad514d" width="190"/> | <img src="https://github.com/user-attachments/assets/514ac8da-6721-4104-bc9d-17edb8186402" width="190"/> |
|:---:|:---:|:---:|:---:|
| **1단계 — 바구니 분류** | **2단계 — 별자리 조립** | **3단계 — 관계도 탐험** | **Voice Cloning** |

</div>


---

## 🏗️ Architecture

<div align="center">
<img src="https://github.com/user-attachments/assets/d031f542-90b0-43bf-82f7-96b366c76f31" alt="아키텍처" width="100%"/>
</div>

- **SSE 실시간 스트리밍** — 텍스트 · 삽화 완성 즉시 클라이언트 전송, 3페이지 누적 시 화면 노출
- **Kafka + Redis 비동기 파이프라인** — 동화 · 삽화 · 단어 추출 병렬 처리
- **하이브리드 인프라** — GPU 전용 서버(FLUX, GPT-SoVITS) 분리 운영
- **CI/CD** — GitHub Actions + Docker + AWS EC2

---

## 🛠️ Tech Stack

### Frontend
[![React Native](https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)](https://expo.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)](https://axios-http.com/)

### Backend
[![Java 21](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)](https://kafka.apache.org/)
[![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)](https://redis.io/)
[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)](https://www.mysql.com/)

### AI / ML
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)](https://openai.com/)
[![GPT-SoVITS](https://img.shields.io/badge/GPT--SoVITS-412991?style=flat-square&logo=github&logoColor=white)](https://github.com/RVC-Boss/GPT-SoVITS)
[![FLUX](https://img.shields.io/badge/FLUX.2--klein--4B-000000?style=flat-square&logo=github&logoColor=white)](https://github.com/black-forest-labs/flux)

### Infra
[![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square&logo=amazonec2&logoColor=white)](https://aws.amazon.com/ec2/)
[![AWS S3](https://img.shields.io/badge/AWS_S3-569A31?style=flat-square&logo=amazons3&logoColor=white)](https://aws.amazon.com/s3/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)](https://nginx.org/)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions)

---

## 📂 Repositories

| Repository | Role |
|---|---|
| [R-Goodday/Front](https://github.com/R-Goodday/Front) | React Native 프론트엔드 앱 |
| [R-Goodday/Back](https://github.com/R-Goodday/Back) | Spring Boot 메인 API 서버 |
| [R-Goodday/AI](https://github.com/R-Goodday/AI) | FastAPI AI 서버 — 동화 생성 · 삽화 · TTS |

---

## 👥 Team

**참 좋은데이** | 지도교수: 정인환 교수님

<table>
  <tr>
    <td align="center" width="140px">
      <img src="https://github.com/dkfjslrks19.png" width="80" style="border-radius:50%"/><br/>
      <b>선우영민</b><br/>
      Frontend<br/>
      <a href="https://github.com/dkfjslrks19">@dkfjslrks19</a>
    </td>
    <td align="center" width="140px">
      <img src="https://github.com/tpdus.png" width="80" style="border-radius:50%"/><br/>
      <b>윤세연</b><br/>
      Frontend<br/>
      <a href="https://github.com/tpdus">@tpdus</a>
    </td>
    <td align="center" width="140px">
      <img src="https://github.com/LgE02.png" width="80" style="border-radius:50%"/><br/>
      <b>이가은</b><br/>
      Backend<br/>
      <a href="https://github.com/LgE02">@LgE02</a>
    </td>
    <td align="center" width="140px">
      <img src="https://github.com/Joonseok-Lee.png" width="80" style="border-radius:50%"/><br/>
      <b>이준석</b><br/>
      Backend<br/>
      <a href="https://github.com/Joonseok-Lee">@Joonseok-Lee</a>
    </td>
    <td align="center" width="140px">
      <img src="https://github.com/zzuhannn.png" width="80" style="border-radius:50%"/><br/>
      <b>조주한</b><br/>
      Backend<br/>
      <a href="https://github.com/zzuhannn">@zzuhannn</a>
    </td>
  </tr>
</table>
