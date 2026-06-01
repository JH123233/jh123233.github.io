# PhysiPlay 🪐 — Interactive Physics Playground & AI Solver

> **물리 법칙을 눈으로 보고, 손으로 체험하다.**  
> PhysiPlay는 9가지 물리 현상을 실시간으로 조작해 볼 수 있는 인터랙티브 시뮬레이터와, 물리 문제 사진을 업로드하면 AI가 단계별 풀이 및 맞춤형 시뮬레이션 애니메이션을 제공하는 AI Solver가 결합된 융합형 웹 플랫폼입니다.

---

## 🎥 Demonstration
*(여기에 작동 화면 스크린샷이나 녹화된 GIF 이미지를 넣어주세요!)*
![PhysiPlay Main Screenshot](path/to/screenshot.png)

---

## ✨ Key Features

### 1. 9종 인터랙티브 시뮬레이터 (Interactive Canvases)
HTML5 Canvas와 정밀한 수치 해석(RK4 등)을 활용하여 물리 법칙을 실시간 가시화합니다. 각 카드에서 마우스 드래그 및 슬라이더 조절을 통해 실시간 반응을 볼 수 있습니다.
- **역학 (Mechanics):** 포물선 운동, 탄성/비탄성 충돌, 등가속도 직선 운동, 단진자 운동 (RK4 적용)
- **전자기학 (Electromagnetics):** 실시간 등전위선 및 전기장선 가시화
- **열역학 (Thermodynamics):** 시간에 따른 1차원 열전달 및 온도 확산 컬러맵
- **구조역학 (Structural):** 보(Beam)의 하중 종류에 따른 실시간 응력 분포 및 처짐
- **파동 & 천체 (Wave & Space):** 두 파동의 중첩/간섭(맥놀이), 이심률 변화에 따른 케플러 행성 궤도

### 2. Gemini 2.5 Flash 기반 AI Solver & Physics Teacher
- **AI 이미지 문제 풀이:** 물리 시험지나 책의 문제 사진을 찍어 업로드하면, Gemini 2.5 Flash가 수식을 포함한 단계별 풀이 과정을 마크다운(KaTeX 수식 렌더링)으로 제공합니다.
- **실시간 애니메이션 연동:** AI가 문제에서 초기 속도, 질량, 각도 등의 물리적 파라미터를 정확하게 추출(JSON 포맷)하여, 해당 문제 상황에 맞는 **맞춤형 캔버스 애니메이션**을 즉시 화면에 재생합니다.
- **AI 물리 선생님 챗봇:** 현재 탐구 중인 시뮬레이터의 컨텍스트를 이해하고 질문에 실시간 답변을 해주는 친절한 챗봇이 우측 하단에 탑재되어 있습니다.

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, Vanilla JavaScript, Vanilla CSS, KaTeX (수식 렌더링)
- **Backend:** Python (`http.server`, `urllib`), Google Gemini API (`gemini-2.5-flash`)

---

## 🚀 Quick Start (로컬 실행 방법)

### 1. 프로젝트 다운로드 (Clone)
```bash
git clone https://github.com/사용자이름/physidogam.git
cd physidogam
