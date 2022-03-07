# 1. Tableau 기본 구조

## 1-1 Tableau 제품 구성
- Tableau는 기능별로 데이터 전처리 / 시각화/ 공유 및 관리 총 3가지 제품으로 구성.
- Tableau Prep을 사용하여 전처리된 데이터를 Tableau Desktop으로 시각화하여 Tableau Server / Online에 대시보드 형태로 공유.
- 데이터 시각화를 다루기 위해 Tableau Desktop을 사용.


## 1-2 Tableau Public 설치하기
- 설치 완료.


## 1-3 Tableau Public 살펴보기
- Tableau Public은 시작 페이지 / 데이터 원본 / 워크시트 / 대시보드 / 스토리 총 5가지로 구분.

### 1-3-1 시작 페이지
- 연결 -> 파일에 연결 -> 원하는 파일 열기

### 1-3-2 데이터 원본
![image](https://user-images.githubusercontent.com/75361137/155474841-07f82cc9-586b-4b51-b648-d4c793ccdb5d.png)

- A. 왼쪽 패널 : 연결된 데이터 원본과 시트(테이블)명이 표시.
- B. 캔버스 : 데이터 원본 설정 방법 및 결합 옵션에 대한 정보 표시.
- C. 데이터 그리드 : 캔버스에서 설정한 데이터가 첫 100개 행까지 표시.
- D. 메타데이터 그리드 : 캔버스에서 설정한 데이터의 필드(컬럼) 표시.

![image](https://user-images.githubusercontent.com/75361137/155475337-15be5510-c2fc-4027-a988-307716832615.png)
- Tableau에서의 테이블 결합(JOIN)은 SQL 테이블 결합과 동일한 개념.

### 1-3-3 워크시트

![image](https://user-images.githubusercontent.com/75361137/155475800-9fcd5d15-6d37-45e4-896a-174b6e3c2c81.png)

- A. 시작페이지 이동.
- B. 사이드바 : 데이터 및 분석 패널로 구성.
- B-1. 데이터 패널 : 데이터 원본 필드(컬럼) * 계산된 필드, 집합, 매개 변수 추가 가능.
- B-2. 분석 패널 : 총계, 추세선, 참조선 등 고급 분석 * 상단 분석 탭 클릭.
- C. 시트 탭 : 데이터 원본 보기 및 워크시트, 대시보드, 스토리 추가.
- D. 페이지 및 필터 : 사이드바(B)의 데이터 패널의 값 필터하여 시각화.
- E. 마크 카드 : 사이드바(B)의 데이터 패널의 값 추가하여 시각화.
- F. 행과 열 : 사이드바(B)의 데이터 패널의 값 추가하여 시각화.
- G. 뷰 : 데이터 시각화 표시 공간.

![image](https://user-images.githubusercontent.com/75361137/155533165-0798c138-640e-4bda-ac05-9436a61d3b30.png)
- 계산된 필드 만들기로 새로운 필드 생성. (ex. 매출액 = [Price]*[Quantity])

![image](https://user-images.githubusercontent.com/75361137/155533447-aa74208a-26bc-4445-8c72-0c8873061b03.png)
- 행과 열에 필드를 넣고, 넣은 필드를 마크의 색상 또는 레이블에 Ctrl 누른 상태로 드래그 하여 시각화.

# *중요) 마크에 넣을 때에는 Ctrl을 누른 상태로* 

![image](https://user-images.githubusercontent.com/75361137/155533635-87225a1c-f8ac-44e0-a6c5-efd2c31728a4.png)
- 툴바를 통해 내림차순 또는 오름차순으로 변경.


### 1-3-4 대시보드

![image](https://user-images.githubusercontent.com/75361137/155534828-adb92746-25a7-4d1e-9423-7bf5e330a94f.png)

- A. 미리보기 : 기기(데스크톱, 태블릿, 모바일)별 대시보드 미리보기
- B. 크기 : 대시보드 크기 조정
- C. 시트 : 워크시트 리스트
- D. 개체 : 새로운 개체 생성
- E. 대시보드 : 시트 및 개체 대시보드 표시 공간
- F. 레이아웃 : 대시보드 레이아웃 조정
----------------------------------------------------------------------
- B에서 대시보드 크기를 설정하고, D에서 대시보드 제목 표시를 클릭하여 제목 설정.
- 대시보드에 시트 및 가로 개체(다른 개체도 가능)을 추가할 때는 Shift를 누른 상태로 드래그하여 추가.

# *중요) 대시보드에 넣을 때에는 Shift를 누른 상태로* 

![image](https://user-images.githubusercontent.com/75361137/155537415-f5896a93-0c74-4f4e-b1fd-7124e4f415bb.png)

- Tableau 대시보드는 워크시트를 추가하기 전 가로 및 세로 개체로 틀을 만들어 놓는 것이 좋음. -> 안 만들어두면 워크시트가 많아질수록 대시보드를 구성하기 어려움.

![image](https://user-images.githubusercontent.com/75361137/155537638-d2684ffb-993b-4376-a105-3e7ad3852791.png)

- 콘텐츠 균등 분할하여 위치를 맞춰줌.

![image](https://user-images.githubusercontent.com/75361137/155537813-95dd4128-00ef-49c0-b946-a7e2d28cfe27.png)

- 필터로 사용을 눌러 브랜드명으로 필터된 성별 매출액 확인 가능. 즉, 브랜드를 클릭하면 해당 브랜드의 성별 매출액이 바뀜.
- 필터는 SQL의 WHERE와 동일한 개념이지만, 마우스만으로 SQL보다 유연하게 필터를 사용 가능. -> 워크시트 간 상호작용.
- 레이아웃을 사용하여 기호에 맞게 대시보드 수정.


### 1-3-5 스토리
- 실무에서는 주로 스토리 보다 대시보드로 데이터 시각화를 공유하므로 이러한 기능이 있는지만 이해.

![image](https://user-images.githubusercontent.com/75361137/155564783-16623188-2801-4ec5-b4b3-de7bfcd84160.png)
- A. 새 스토리 포인트 : 스토리 포인트(캡션) 추가 및 복제
- B. 시트 및 대시보드 : 시트 및 대시보드 리스트
- C. 텍스트를 끌어와서 추가 : 새로운 텍스트 추가
- D. 제목 표시 : 스토리 제목 표시
- E. 크기 : 스토리 크기 조정
- F. 스토리 : 시트 및 대시보드 표시 공간
- G. 레이아웃 : 스토리 탐색 스타일 조정

![image](https://user-images.githubusercontent.com/75361137/155565744-3a6bde9a-7436-4e58-9e7a-84600aeed754.png)
- 스토리를 선택한 후, 캡션의 이름을 바꿔줌.


# 2. Tableau 기본 개념

## 2-1 차원 vs 측정값
- 데이터는 [차원] 및 [측정값] 필드로 나뉘게 됨.
- 차원 : 분류적인 데이터(ex. Gender, Brand, Store Addr 등)
- 측정값 : 집계적인 데이터(ex. Quantity, Price 등)

![image](https://user-images.githubusercontent.com/75361137/155567060-8dd4d37d-32ea-4c5e-aca1-971c7fcfe617.png)
- 윗 부분이 차원이고, 아래가 측정값.
- 자동으로 Tableau에서 사용자의 편의성을 위해 테이블의 열(Column)을 차원과 측정값으로 나눔.
- 그러나 연령(Age)같은 열(Column)은 숫자형이기 때문에 Tableau에서 집계적인 데이터로 인식해 측정값에 위치. -> 차원으로 변경해 주어야함.

![image](https://user-images.githubusercontent.com/75361137/155568793-37b3111c-fe5e-4ed7-8ab4-0b873ccf8a71.png)


## 2-2 연속형 vs 불연속형
- [차원] 및 [측정값] 형식은 연속형 및 불연속형으로 나뉨.
- A. 연속형 : 무한한 값인 측정값의 기본 형식(ex. Quantity, Price 등)
- B. 불연속형 : 유한한 값인 차원의 기본 형식(ex. Gender, Brand, Store Addr 등)

![image](https://user-images.githubusercontent.com/75361137/155569391-b7e6950e-ba4c-42d6-b8f6-157a71eac240.png)
- 연속형은 데이터가 없어도 선으로 연결되지만, 불연속형은 데이터가 없으면 표시되지 않음.
- 연속형일 때는 축 간격이 동일하고, 불연속형이면 축 간격이 동일하지 않음.


## 2-3 Tableau Desktop(유료) 살펴보기
- 유료버전에만 있는 기능은 서버 연결 / 라이브 vs 추출 / 공유 크게 3가지.
- 서버 연결 : Tableau Server 및 Microsoft SQL Server / MySQL / Oracle 등 다양한 서버로 연결이 가능.
- 라이브 vs 추출 : 라이브는 실시간으로 데이터가 업데이트 되는 것이고, 추출은 특정 시점마다 데이터가 업데이트 되는 것인데 유료 버전에서는 둘다 가능.
- 공유 : Tableau Server/Online으로 공유가 가능.


# 3. 정리

## 3-1 Tableau 시각화 기능보단 개념 이해
- Tableau 시각화 기능보다 Tableau에 적용되는 SQL 개념을 되짚어 보는 것이 중요. (테이블 구조 및 데이터 형식, 결합 등)
- Tableau 원본 테이블 연결 및 테이블 간의 결합(JOIN)에서 SQL 개념이 그대로 적용되기 때문.


## 3-2 Tableau 데이터 시각화 작업 순서
- Tableau 데이터 시각화 작업 순서는
1. 데이터 원본 연결
2. 워크시트 작업
3. 대시보드 구성
4. 스토리 만들기
- 이 중 2. 워크시트 작업에 많은 데이터 시각화 기능이 있으며 가장 중요한 단계.


