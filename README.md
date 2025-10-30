# 🦾 LeRobot Manual (르로봇 메뉴얼)

## 📺 YouTube Link  
👉 [유튜브 바로가기](https://www.youtube.com/watch?v=GbkX5b7VFoU)

---

## 💻 OS 환경
- **운영체제:** Ubuntu  
- **터미널 열기:** `Ctrl + Alt + T`  
- **터미널 붙여넣기:** `Ctrl + Shift + V`

---

## ⚙️ Installation Steps

### 1️⃣ 기본 패키지 설치
```bash
sudo apt install python3-pip
```
👉 Python 패키지 관리자 `pip`를 설치합니다.

---

### 2️⃣ Miniconda 폴더 생성
```bash
mkdir miniconda
```
👉 Miniconda 설치 파일을 저장할 폴더를 만듭니다.

---

### 3️⃣ Miniconda 다운로드
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
👉 Miniconda 설치 스크립트를 다운로드합니다.

---

### 4️⃣ Miniconda 설치 실행
```bash
bash ~/Miniconda3-latest-Linux-x86_64.sh
```
👉 다운로드한 설치 스크립트를 실행합니다.

---

### 5️⃣ 환경 변수 업데이트
```bash
source ~/.bashrc
```
👉 새로 설치된 conda 환경을 적용합니다.

---

### 6️⃣ LeRobot용 가상환경 생성
```bash
conda create -y -n lerobot python=3.10
```
👉 Python 3.10 환경의 `lerobot` 가상환경을 만듭니다.

---

### 7️⃣ 8️⃣ Conda 약관 승인
```bash
conda tos accept --override-channel https://repo.anaconda.com/pkgs/main
conda tos accept --override-channel https://repo.anaconda.com/pkgs/r
```
👉 Conda 패키지 채널 이용 약관을 승인합니다.

---

### 9️⃣ 가상환경 재생성 (필요 시)
```bash
conda create -y -n lerobot python=3.10
```
👉 7️⃣8️⃣약관 승인을 진행한 경우, 환경 설정을 다시 재생성합니다.

---

### 🔟 가상환경 활성화
```bash
conda activate lerobot
```
👉 LeRobot 환경으로 진입합니다.

---

### 11️⃣ FFmpeg 설치
```bash
conda install ffmpeg -c conda-forge
```
👉 영상 입출력에 필요한 FFmpeg 라이브러리를 설치합니다.

---

### 12️⃣ 상위 폴더로 이동
```bash
cd ..
```
👉 상위 디렉토리로 이동합니다.

---

### 13️⃣ LeRobot 리포지토리 클론
```bash
git clone https://github.com/huggingface/lerobot.git
```
👉 Hugging Face의 LeRobot 프로젝트를 다운로드합니다.

---

### 14️⃣ 폴더 이동
```bash
cd lerobot
```
👉 LeRobot 프로젝트 폴더로 이동합니다.

---

### 15️⃣ 개발자 모드 설치
```bash
pip install -e .
```
👉 로컬 개발 환경으로 설치합니다 (소스 수정 시 즉시 반영).

---

### 16️⃣ LeRobot 설치
```bash
pip install lerobot
```
👉 기본적인 LeRobot 패키지를 설치합니다.

---

### 17️⃣ 필수 빌드 도구 설치
```bash
sudo apt-get install cmake build-essential python3-dev pkg-config libavformat-dev libavcodec-dev libavdevice-dev libavutil-dev libswscale-dev libswresample-dev libavfilter-dev pkg-config
```
👉 LeRobot 실행에 필요한 영상/오디오/빌드 관련 라이브러리들을 설치합니다.

---

### 18️⃣ Feetech 서보모터 지원 설치
```bash
pip install -e ".[feetech]"
```
👉 Feetech STS 시리즈 서보모터를 제어하기 위한 종속 패키지를 설치합니다.

---

## ✅ 설치 완료!
이제 LeRobot을 사용할 준비가 되었습니다 🎉  
---

## 📜 참고
- 공식 GitHub: [https://github.com/huggingface/lerobot](https://github.com/huggingface/lerobot)  
- Hugging Face Install: [https://huggingface.co/docs/lerobot](https://huggingface.co/docs/lerobot/installation)
