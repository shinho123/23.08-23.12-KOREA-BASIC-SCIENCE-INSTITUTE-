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

# 분석 결과
+ LDA 분석 결과 - 국내·외 MRAM(Magnetoresistive Random Access Memory)과 연관되어 있는 특허(총 31,148건) 중 특허의 'abstract'속성과 'title' 부분의 데이터를 결합 후 LDA 토픽 분석을 수행
+ MRAM과 연관되어 있는 특허에서 주로 중요한 관점으로 도출 되는 기술 키워드들을 분석
  
```python
ldamodel = gensim.models.ldamodel.LdaModel(corpus, num_topics = 6, id2word = dictionary, random_state = 3)
ldamodel.print_topics(num_words = 10)
```

## 토픽별 주제 선정 및 키워드 도출

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

