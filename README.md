# Body_Morphometry-Chest
[**MOAI 2022 Body Morphometry AI Segmentation Online Challenge**](https://www.kaggle.com/competitions/body-morphometry-chest/overview)  

![](CT-Segmentation-Guide.png)

# Summary
## Environment  
- **GPU**: NVIDIA RTX 4090
- **OS**: Windows 11
- **Libraries**
    - python 3.7.15
    - PyTorch 1.11.0
    - albumentations 1.3.0

## Models  
- UNet based (https://github.com/qubvel/segmentation_models.pytorch)

|Encoder|Params, M|LB|
|------|---|---|  
|efficientnet-b0|4M|0.9642|  
|efficientnet-b7|63M|0.96411|  
|timm-mobilenetv3_large_100|2.97M|0.95877|  
|**timm-resnest269e**|**108M**|**0.9651**|
|resnext101_32x16d|191M|0.96075|
|Ensembles (efficientnet-b7 + timm-resnest269e)||0.96362|

## Data processing
- Pre processing
    - albumentation  
- Post processing
    - bfs

# Description

## 개요  
  MOAI 2022 Body Morphometry AI Segmentation Online Challenge는 원광대학교병원과 서울아산병원의 공동 연구 주제인 Body Morphometry 중 하나로, CT 영상에서 근육과 지방에 대하여 인공지능 기술을 기반으로 자동 Segmentation 기술 개발 및 정량적 평가 수행을 통한 의료 인공지능 연구 개발 활성화를 목표로 하고 있습니다.

## Body Morphometry란?
  모든 의료 및 건강증진의 근본이 되는 데이터로 Body Morphometry 관련 질환은 모든 질환 중 가장 높은 유병률을 나타내며 성인 인구의 1/3 이상의 사회적 문제입니다. 특히, 근육, 지방, 뼈의 변화는 많은 질병과 건강악화의 원인이자 결과로 그 중요성은 나날이 증가하고 있습니다.



## Body Morphometry 중요성
  세계 각국 질병구조가 만성병 구조로 바뀌고 고령화 사회로 진전됨에 따라 예방과 관리에 대한 중요성이 재인식 되고 있습니다. 이러한 만성질환은 발병원인이 복합적으로, 진단 및 치료의 어려움이 발생합니다. 이는 완치의 한계 발생과 오진율 증가의 원인이 되기도 합니다. 최근 이러한 문제점을 개선하기 위해 개인의료기록과 다양한 의료 데이터의 통합 분석을 통한 정밀 진단 및 치료, 예후예측을 통한 예방과 관리에 대한 연구가 급진전하고 있습니다. 특히, 비만, 근감소증, 골다공증과 같은 Body Morphometry 정보와 질병 간의 유의성에 관한 연구들이 보고되면서 다양한 의료 정보의 융합 연구에 대한 중요성과 필요성은 더욱 가중되고 있습니다.

## 대회목적
MOAI 2022 Body Morphometry AI Segmentation Challenge는 의료 인공지능 연구 개발 활성화를 목적으로 인공지능 학습 분위기 조성 및 확산, 혁신성장의 기회 마련을 위해 연구자 및 대학생들과 함께 아이디어 발굴을 위한 다음과 같은 세부 목표들을 가지고 있습니다.

## 의료 데이터
  의료 데이터는 관련 규정으로 인해 공유가 어려우며, 이해를 위한 추가적인 지식, Ground Truth 제작의 어려움 등의 특성으로 인해 접근성이 매우 떨어지는 데이터 중 한 가지입니다. 각 분야의 전문가들이 직접 선별하고 가공한 익명화(Anonymization)된 의료 데이터와 이에 해당하는 연구주제를 공유하여 관심 있는 연구자들이 의료 데이터와 해당 연구주제에 대한 접근을 용이하게 하고자 합니다.

## 교류 활성화
  의료 인공지능은 다양한 요소 기술들의 통합이 필요한 융합 기술 및 학제 간 연구입니다. 이러한 의료와 공학의 학제 간 연구는 다양한 전문지식이 필요하기 때문에 각 분야의 전문가 및 연구자들의 활발한 교류가 필수입니다. 본 대회는 해당 주제에 대한 정보/지식/데이터 공유에 한정되지 않고, 각 분야의 전문가와 연구자들 간의 교류를 지향하고 있습니다. 이를 통해 의료 인공지능 연구 활성화 계기를 만들고자 합니다.

## 인공지능 인력 양성
  현재 국내외 인공지능 전문가 및 연구자는 현저히 부족한 상황입니다. 본 대회는 전문 분야와 지식을 통한 실용적인 연구개발 주제를 다룸으로써 실무형 인공지능 인력 육성에 기여하고자 합니다. 또한, 의료 인공지능과 관련된 전처리, Augmentation, 후처리 등 기본적인 지식과 노하우를 공유하는 계기 마련을 통해 전문 인력의 질적·양적 양성의 가속화를 기반으로 국제 경쟁력 확보를 목표로 하고 있습니다.  

  
## 참가자격
  국내 대학(원)생, 일반인, 산학연 콘소시엄 등 (빅데이터에 관심 있는 모든 사람)
  외국인의 경우, 국내 팀 소속으로 참여 가능
