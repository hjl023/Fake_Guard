

## Fake_Guard

## 프로젝트 개요
최근 생성형 AI 기술의 급격한 발전으로 인해, 그에 따른 사회적 문제가 대두되고 있습니다. 
특히, 유명인이나 일반인의 얼굴을 이용한 딥페이크 영상이 큰 이슈가 되고 있습니다. 
이러한 딥페이크 영상은 사회적으로 매우 위험한 영향을 미칠 수 있기 때문에 이를 탐지하고 대응할 수 있는 시스템이 필요합니다.


https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/b1a3c5cc-9aa5-4f1f-8387-5449167907a5


이 프로젝트에서는 AI를 활용한 자동 딥페이크 탐지 시스템을 개발하여, 이미지, 오디오, 동영상에서 발생할 수 있는 변조를 효과적으로 탐지할 수 있는 방법을 모색했습니다. 
다양한 변조 유형에 대한 대응력을 갖춘 시스템을 설계했습니다.

## 추론 방식

- 동영상 업로드
사용자가 동영상을 업로드하면, FastAPI를 사용하여 동영상의 URL과 이름을 MySQL 데이터베이스에 저장합니다.

- 프레임 분석
동영상에서 각 프레임을 추출하여, TALL++ 모델을 사용하여 딥페이크 여부를 판단합니다.

- 이미지 분석
동영상 내 이미지가 변조되었는지 판단하기 위해 EfficientNet 모델을 활용하여 이미지의 변조 여부를 분석합니다.

- 오디오 분석
동영상에 포함된 오디오가 변조되었는지 확인하기 위해 SpecRNet 모델을 사용하여 오디오의 변조 여부를 분석합니다.

## 작업 흐름도(전처리)

[이미지]
   
![이미지 전처리](https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/50aa15b9-a095-420c-8c5a-b5b0bb8ae515)

[오디오]
   
![오디오 전처리](https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/65edb264-7413-4415-b9dc-3c497f52afb5)

## 작업 흐름도(모델)

[동영상]

![동영상처리](https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/5f73961e-c2ec-4edc-9a2d-3d318c7d5d56)

[이미지]

![이미지 처리](https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/727732e7-2d98-4a63-ba79-1bdb3304deb3)

## 시연 영상


https://github.com/lee-hyeon-gu/Fake_Guard/assets/149747454/e0c94a14-bf9b-4482-83c3-e237ae93a3df


## Reference 

## Related and additional tools
1. TALL++ https://github.com/rainy-xu/TALL4Deepfake
