# PhysiPlay 🪐 — Interactive Physics Playground & AI Solver

<p align="left">
  <strong>다른 언어로 읽기:</strong> 
  <a href="README.md">🇺🇸 English (영어)</a>
</p>

> **물리 법칙을 눈으로 보고, 손으로 체험하다.**  
> PhysiPlay는 15가지 물리 현상을 실시간으로 조작해 볼 수 있는 인터랙티브 시뮬레이터와, 물리 문제 사진을 업로드하면 AI가 단계별 풀이 및 맞춤형 시뮬레이션 애니메이션(다중 객체 결합 운동 포함)을 즉시 생성해주는 Gemini 기반 AI Solver가 결합된 융합형 웹 플랫폼입니다.

---

## 🎥 Demonstration
*(여기에 작동 화면 스크린샷이나 녹화된 GIF 이미지를 넣어주세요!)*
![PhysiPlay Main Screenshot](path/to/screenshot.png)

---

## ✨ Key Features

### 1. 15종 인터랙티브 시뮬레이터 (Interactive Canvases)
HTML5 Canvas와 정밀한 수치 해석(RK4 등)을 활용하여 물리 법칙을 실시간 가시화합니다. 각 카드에서 마우스 드래그 및 슬라이더 조절을 통해 파라미터를 조작하고 이에 즉각적으로 반응하는 물리 시뮬레이션을 탐구할 수 있습니다.
- **역학 (Mechanics):** 
  - 포물선 운동 (발사 각도와 초기 속도 조절, 궤적 & 낙하지점 시뮬레이션)
  - 충돌 (두 물체의 질량과 속도 설정, 탄성·비탄성 충돌 시 운동량 & 에너지 변화)
  - 등가속도 직선 운동 (일정한 가속도를 가진 직선 위 물리 거동 관찰)
  - 단진자 (줄 길이·감쇠·초기 각도 조절, RK4 수치 적분 적용)
- **파동 & 소리 (Waves & Acoustics):**
  - 파동 중첩 (두 파동의 진폭·진동수·위상을 독립 조절하여 보강·소멸 간섭 및 맥놀이 관찰)
- **전자기학 (Electromagnetics):**
  - 전기장선 (점전하를 마우스로 드래그 배치하여 등전위선 & 전기장선 실시간 가시화)
  - 전자기 유도 (코일 근처에서 자석을 흔들어 자기선속 변화에 따른 유도 기전력 & 렌츠의 법칙 탐구)
- **열역학 (Thermodynamics):**
  - 열전달 (경계 온도와 재료 열전도율에 따른 시간에 따른 1차원 온도 확산 컬러맵 가시화)
  - 열기관 사이클 (카르노, 오토, 디젤 사이클의 P-V 및 T-s 선도 비교 및 피스톤 실시간 거동 가시화)
- **광학 (Optics):**
  - 기하광학 (입사각과 매질의 굴절률을 조절하여 스넬의 법칙, 전반사 및 빛의 분산 레이트레이싱)
- **현대물리 & 우주 (Modern Physics & Space):**
  - 광전 효과 (빛의 진동수와 밝기에 따른 광전자 방출량을 관찰하고 빛의 입자성 탐구)
  - 케플러 궤도 (이심률과 초기 속도 조절을 통한 행성 궤도 시뮬레이션 및 면적 속도 일정 법칙 확인)
- **유체 & 진동공학 (Fluid & Vibration Mechanics):**
  - 유체 역학 (파이프 내부 단면 조절에 따른 베르누이 압력 저하 및 벤투리 효과 관찰)
  - 기계 진동 (질량·감쇠·강성 및 조화 외력 설정을 통한 고유 진동수 공진 및 과도 응답 관찰)

### 2. Gemini 2.5 Flash 기반 AI Solver & Physics Teacher
- **AI 이미지 문제 풀이:** 물리 시험지나 책의 문제 사진을 찍어 업로드하면, Gemini 2.5 Flash가 수식을 포함한 단계별 풀이 과정을 마크다운(KaTeX 수식 렌더링)으로 제공합니다.
- **실시간 애니메이션 연동:** AI가 문제에서 초기 속도, 질량, 각도 등의 물리적 파라미터를 정확하게 추출(JSON 포맷)하여, 해당 문제 상황에 맞는 **맞춤형 캔버스 애니메이션**을 즉시 화면에 재생합니다.
- **고급 다중 객체 결합 운동(Combined) 지원:** 여러 물체가 동시에 독립적으로 움직이거나 서로 마주보고 달리는 등 복잡한 복합 상황 문제를 지원합니다. 일반화된 2D 데카르트 좌표계(오른쪽/위 $+$, 왼쪽/아래 $-$, 지연 시간 포함)로 물체들의 거동 데이터를 자동 맵핑하고, 두 물체가 만나는 점(`meetPoint`)의 좌표와 시간까지 예측하여 다중 애니메이션을 동시 구동합니다.
- **AI 물리 선생님 챗봇:** 현재 탐구 중인 시뮬레이터의 컨텍스트를 이해하고 질문에 실시간 답변을 해주는 친절한 챗봇이 우측 하단에 탑재되어 있습니다.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5 Canvas, Vanilla JavaScript, Vanilla CSS, KaTeX (수식 렌더링)
- **Backend:** Python (`http.server`, `urllib`), Google Gemini API (`gemini-2.5-flash`)

---

## 🚀 Quick Start (로컬 실행 방법)

### 1. 프로젝트 다운로드 (Clone)
```bash
git clone https://github.com/사용자이름/physidogam.git
cd physidogam
```

### 2. Gemini API 키 설정 (필수 🔑)
AI Solver 및 챗봇 기능을 사용하려면 Google Gemini API 키가 필요합니다.
1. 프로젝트 루트 디렉토리에 `api_key.txt` 파일을 생성합니다.
2. [Google AI Studio](https://aistudio.google.com/)에서 발급받은 API 키를 파일 안에 텍스트로 붙여넣고 저장합니다.
   *(예: `api_key.txt` 파일 내용이 `AIzaSy...` 한 줄만 되도록 입력)*

### 3. 서버 실행
프로젝트 루트 폴더에서 파이썬 로컬 서버를 실행합니다.
```bash
python server.py
```
*Windows 환경의 경우, 루트 폴더에 있는 `PhysiPlay_실행.bat` 파일을 더블 클릭하여 실행할 수도 있습니다.*

### 4. 접속
웹 브라우저를 열고 아래 주소로 접속합니다.
> **http://localhost:7788**

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
