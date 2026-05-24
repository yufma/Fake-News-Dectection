# Fake News Detection Term Project

## 개요
이 프로젝트는 Kaggle의 Fake News Detection 데이터셋을 사용해 가짜 뉴스와 진짜 뉴스를 구분하는 분류 모델을 구현한 것입니다. 텍스트 데이터를 전처리하고, 전통적 베이스라인 모델(Naive Bayes)과 사전학습 언어 모델(BERT)을 비교 평가했습니다.

## 프로젝트 구성
- `Machine_Learning_Term_Project.ipynb` : 전체 코드 노트북
- `Fake.csv`, `True.csv` : 가짜 뉴스/진짜 뉴스 원본 데이터셋 (Kaggle 제공)
- `archive.zip` : 압축된 데이터셋 파일
- `requirements.txt` : 재현에 필요한 파이썬 패키지

## 주요 내용
- 문제 정의: 뉴스 기사를 기반으로 가짜 뉴스 여부를 분류
- 데이터셋: Kaggle Fake News Detection 데이터셋
- 베이스라인 모델: TF-IDF + Multinomial Naive Bayes
- 고급 모델: Hugging Face BERT (`bert-base-uncased`)
- 평가 지표: Accuracy, Precision, Recall, F1 Score
- 추가 분석: 오분류 사례 분석, CPU→GPU 전환 경험, 배포 가능성 평가

## 재현 방법
### 1) Google Colab에서 실행
1. Colab에서 새 노트북을 엽니다.
2. 메뉴에서 `런타임` → `런타임 유형 변경` → `GPU` 선택
3. 이 저장소를 업로드하거나 GitHub에서 노트북 열기
4. 노트북 상단 코드 셀에서 라이브러리를 설치합니다:
   ```python
   %pip install -r requirements.txt
   ```
5. Google Drive를 마운트하고 `zip_path`를 실제 위치로 변경합니다.
6. 셀을 순서대로 실행합니다.

### 2) 로컬 환경에서 실행
1. 이 폴더를 로컬 컴퓨터로 복제 또는 다운로드합니다.
2. Python 3.8 이상 환경을 준비합니다.
3. 의존성 설치:
   ```bash
   pip install -r requirements.txt
   ```
4. Jupyter Notebook을 실행합니다:
   ```bash
   jupyter notebook
   ```
5. `Machine_Learning_Term_Project.ipynb`를 열어 셀을 순서대로 실행합니다.

## 데이터 준비
1. Kaggle에서 데이터셋을 다운로드합니다.
   - 데이터셋 링크: https://www.kaggle.com/datasets
   - 검색어 예시: "Fake News Detection"
2. 다운로드한 `archive.zip` 파일을 이 폴더에 저장하거나 Google Drive에 업로드합니다.
3. `Fake.csv`와 `True.csv`가 포함된 압축 파일을 해제합니다.
4. 노트북의 `zip_path` 변수를 압축 파일 위치 또는 추출 폴더 경로로 수정합니다.
5. 압축 해제 후 `Fake.csv`와 `True.csv`를 읽어옵니다.

## 필요한 패키지
- `pandas`
- `numpy`
- `scikit-learn`
- `torch`
- `transformers`
- `datasets`
- `jupyter`

## 참고
- 이 프로젝트는 전체 ML 파이프라인을 직접 경험하는 것이 목표입니다.
- GPU 환경에서 실행하는 것이 효율적입니다.
