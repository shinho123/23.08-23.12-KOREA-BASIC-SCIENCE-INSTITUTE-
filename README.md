# 23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-
기관 협업 공동 연구 - 한국기초과학지원연구원(Korea Basic Science Institute)

기간 : 23.08 ~ 23.12

참여인원 : 8명

# 연구 배경
+ 한국기초과학지원연구원 (이하 KBSI) 가 보유한 분석 장비를 대상으로 12대 국가전략기술에 해당하는 기술 및 관련 산업을 지원하고, 장비 활용도를 극대화하기 위한 신규 분석장비 개발 및 기존 분석장비 활용도 요구가 커지고 있음
+ 이에 KBSI가 보유한 분석장비 관련 기술의 경쟁력을 파악하고, 전략산업과 연관된 분석장비의 특성을 반영하여 분석장비 활용도를 높이고 자원 활용도를 극대화하는 것이 필요함
+ 특허는 기술의 중요한 대용지표로 활용될 수 있으므로, 특허분석을 바탕으로 해당기술의 경쟁력 및 관련 전략기술과의 유사성 및 적합성 등을 파악하는 것이 요구됨 


# 연구 목적
+ KBSI(Korea Basic Science Institute) 보유 분석장비 관련 기술의 경쟁력을 파악하고, 전략산업과 연관된 적용가능 유망기술을 도출하고자 함
+ 이러한 과정을 시스템적이고 체계적으로 수행하기 위한 특허분석 방법론을 제시하고 이를 개발·적용하는 데 목적이 있음

# 프레임워크

![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/4026b77a-ca3c-4d91-a390-e795af04cd62)

# 수행 역할
+ 특허 데이터 수집(Google Patents), 데이터 필터링, 데이터 전처리, LDA 토픽 모델링, 네트워크 분석

+ 데이터 수집 : Goole Patents에서 수집

## Ⅰ. KBSI 연구 개요에서 기술 관련 키워드 추출 → 기술 키워드 조합 → 검색 조건으로 설정 후 해외(국내 제외) 특허 검색 및 저장

### 기술 키워드 조합 순서 및 조건 : 
+ 연구개요에서 기술적인 의미를 내포하는 키워드의 조합
+ 단일 키워드지만 키워드 길이 자체가 매우 긴 키워드(키워드 자체만으로 기술적인 의미를 내포하고 있음)
+ 다른 키워드와 함께 조합하면 검색되지 않으나 단일 키워드 검색만으로 많은 특허가 검색되는 키워드

#### 1. 연구개요에서 기술적인 의미를 내포하는 키워드의 조합
+ "극저온 전도냉각형 다축 자기장환경 프로브 스테이션 개발", "자성 메모리 소자의 특성", "메모리 소자 성능 개선 및 신소자 개발",
"맴리스터 소자", "온도의존성", "웨이퍼 레벨의 검사 및 진단용", "전력반도체", "차량용반도체", "우주항공산업", "온도변화 내구성", "프로브스테이션", "냉각수단", "고온 분석 수단", "웨이퍼 레벨"의 "물성평가", "성능향상"


#### 2. 1에서 수집한 기술 키워드를 영문으로 변경 후 키워드 조합 수행

##### 시스템 관련 키워드

+ 다축자기장(multi-axis magnetic field or vector field), 전도냉각(conduction-cooled or conduction-cooling), 열스위치(heat switch), 전류도입선(or 전류인입선, current lead), 극저온 프로브 스테이션(cryogenic probe station), (다축)자기장 보정(multi-axis shim), 자기장 집속(flux focusing), 양산용 반도체 검사장비(Semiconductor inspection equipment for mass production), wafer level 검사장비(wafer inspection equipment)
 
##### 시스템을 이용한 분석 관련 키워드

+ 자기메모리(MRAM) / 멤리스터(memristor) / 전력반도체(power semiconductor) / 우주항공(aerospace) / 차량용반도체(automotive semiconductors) / 심해탐사(deep sea exploration)+물성측정장비(physical property measurement system), 스핀(spin), 스핀토크(spin torque), MTJ(magnetic tunneling junction), 초전도 마그넷(superconducting magnet), 스핀분극(spin polarization), 자기이방성(magnetic anisotropy), 열-전기물성(열전물성, thermoelectric physical property), magnetic switching phase diagram, 고속 스위칭(fast switching), MRAM 상용화 공정 기술(MRAM-commercialization process technology)


#### 3. 동일한 성격의 기술 분야로 키워드를 분류

##### 자기장 및 냉각 관련 키워드 : 
 
+ 다축자기장(multi-axis magnetic field or vector field) - 시스템 관련 키워드
+ 전도냉각(conduction-cooled or conduction-cooling) - 시스템 관련 키워드
+ 열스위치(heat switch) - 시스템 관련 키워드
+ 극저온 프로브 스테이션(cryogenic probe station) - 시스템 관련 키워드
+ (다축)자기장 보정(multi-axis shim) - 시스템 관련 키워드

##### 전력반도체 및 반도체 검사장비 관련 키워드 : 
 
+ 양산용 반도체 검사장비 (semiconductor inspection equipment for mass production) - 시스템 관련 키워드
+ wafer level 검사장비 (wafer inspection equipment) - 시스템 관련 키워드
+ 자기메모리 (MRAM) / 멤리스터 (memristor) - 시스템을 이용한 분석 관련 키워드
+ 전류도입선 (or 전류인입선, current lead) - 시스템 관련 키워드

##### 분석 및 실험 관련 키워드 : 
 
+ 물성측정장비 (physical property measurement system) - 시스템을 이용한 분석 관련 키워드
+ 스핀 (spin) - 시스템을 이용한 분석 관련 키워드
+ 스핀토크 (spin torque) - 시스템을 이용한 분석 관련 키워드
+ MTJ (magnetic tunneling junction) - 시스템을 이용한 분석 관련 키워드
+ 초전도 마그넷 (superconducting magnet) - 시스템을 이용한 분석 관련 키워드
+ 스핀분극 (spin polarization) - 시스템을 이용한 분석 관련 키워드
+ 자기이방성 (magnetic anisotropy) - 시스템을 이용한 분석 관련 키워드
+ 열-전기물성 (열전물성, thermoelectric physical property) - 시스템을 이용한 분석 관련 키워드
+ magnetic switching phase diagram - 시스템을 이용한 분석 관련 키워드
+ 고속 스위칭 (fast switching) - 시스템을 이용한 분석 관련 키워드

##### 응용 분야와 관련된 키워드 :
 
+ 전력반도체 (power semiconductor) - 시스템을 이용한 분석 관련 키워드
+ 우주항공 (aerospace) - 시스템을 이용한 분석 관련 키워드
+ 차량용반도체 (automotive semiconductors) - 시스템을 이용한 분석 관련 키워드
+ 심해탐사 (deep sea exploration) - 시스템을 이용한 분석 관련 키워드

##### MRAM 상용화 및 공정 기술 관련 키워드 :
 
+ MRAM 상용화 공정 기술 (MRAM-commercialization process technology) - 시스템을 이용한 분석 관련 키워드

#### 5. 기술 키워드 조합 후 해외 특허 검색

##### 특허 검색 조건

![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/63dee37e-cec6-4b94-8369-269ab7abe5fd)

#### 6. 검색 결과(총 40,052건)

![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/26dc0ab1-b737-45f7-9b46-f263036747c1)

## Ⅱ.토픽별 주제 선정 및 키워드(Semiconductor) 도출

# 분석 방법
+ LDA 분석 결과 - 수집된 해외 특허 데이터중 MRAM(Magnetoresistive Random Access Memory)과 Semiconductor를 포함하고 있는 160개의 데이터 세트를 분석
+ 특허의 'abstract'속성과 'title' 부분의 데이터를 결합 후 LDA 토픽 분석을 수행
+ MRAM과 연관되어 있는 특허에서 주로 중요한 관점으로 도출 되는 기술 키워드들을 분석
  
```python
ldamodel = gensim.models.ldamodel.LdaModel(corpus, num_topics = 6, id2word = dictionary, random_state = 3)
ldamodel.print_topics(num_words = 10)
```

# 분석 결과
### Topic 1 : 절연 소재 및 제조 과정(Insulating Material & Manufacturing Process)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/0cac3017-0612-4fb7-85c3-0daedc66a9cd)

+ Topic 1은 박막 및 회로 구조에서 바닥 부분에 위치한 절연 소재와 소재의 제조 과정에 관한 키워드로 구성되어 있음
+ insulating, dielectric - 절연소재, element, material - 소재, 성분, bottom, area - 위치, barrier - 경계, ferromagnetic - 자성 소재 

### Topic 2 : 유전체 표면 및 에칭(Dielectric & Etching)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/906dc55c-73c7-4a6c-9099-08b663701da0)

+ Topic 2는 유전체 표면과 에칭 과정과 관련된 키워드로 구성되어 있음
+ dielectric - 유전체(전기가 잘 안통하는), etch - 에칭(etching), magnetoresistive - 자기저항

### Topic 3 : 자기저항 구조체 및 데이터 저장(Magnetoresistive Structures & Data Storage)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/7141f972-a513-4119-8645-e87c904f4fb2)

+ Topic 3는 자기저항을 가지는 구조체와 데이터 저장에 관련된 키워드로 구성되어 있음
+ magnetoresistive - 자기저항, structures - 구조체, data - 데이터, dielectric - 유전체(전기가 잘 통하지 않는 물질) 

### Topic 4 : 소재 스택 및 스페이서(Material Stack & Spacer)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/9405809b-938d-4b73-bc01-cf18e95c7623)

+ Topic 4는 다양한 소재에서 쌓인 스택과 스페이서를 통해 자기저항을 가지는 트랜지스터와 관련된 키워드로 구성되어 있음
+ material - 소재, stack - 쌓다, magnetoresistive - 자기저항, spacer - 스페이서(게이트 단자의 사면을 Side Wall 형태로 둘러싼 절연막)

### Topic 5 : 회로 전압 및 전류 특성(Circuit Voltage & Current Characteristics)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/efa27428-632b-4930-854a-b3402c17d1a0)

+ Topic 5는 회로의 전압과 전류 특성에 대한 키워드로 구성되어 있음 특히 다수의 구조체를 통합하여 형성된 회로의 특성을 설명하고 있음
+ voltage, current - 전류/전압, circuit - 회로, plurality, integrated - 다수의 통합된, structures - 구조체

### Topic 6 : 트랜지스터 데이터 유형 & 자화 특성(Transistor Type & Magnetization Characteristics)
![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/94a54052-0d86-45cb-8730-397785c1a35e)

+ Topic 6는 트랜지스터의 다양한 데이터 유형과 자화 특성에 관한 키워드로 구성되어 있음
+ transistor - 트랜지스터, data - 데이터, magnetization - 자화(자계 중에 놓여진 물체가 자성을 띄는 것)

## Ⅲ. 네트워크 분석

### 분석 데이터 : Mram + Semiconductor(160개 데이터세트)
### 분석 사용 프로그램 : Gephi

## 분석 결과

![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/b4ab1810-50a8-4ff8-b108-d7515bcadbb2)

#### 에너지 및 물리

![image](https://github.com/shinho123/23.08-23.12-KOREA-BASIC-SCIENCE-INSTITUTE-/assets/105840783/8a893bc0-a0c7-4d99-a4ef-f230182aee39)

+ 관련 단어
   + 전기 및 전자공학 : Voltage, Power, Electromagnetic, Frequency
   + 물리학 및 열역학 : Wave, Pressure
   + 플라즈마 : Plasma
   + 기계공학 : Surface, Pipe, Housing
   + 기타 공학 및 설계과정 : Generating, Injection, Supply, Locate, Water



