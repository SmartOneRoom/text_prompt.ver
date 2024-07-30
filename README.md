# 택배 안전 CCTV
이번 프로젝트는 스마트원룸 프로젝트의 사이드 프로젝트로 진행되었습니다.    

## 팀 소개
[손명호](https://github.com/thsaudgh8) | 팀장   
[이상준](https://github.com/eru2) | 팀원   
[김윤정](https://github.com/kingodjerry) | 팀원   

## 문제 정의
[택배기사와 소비자의 직접적인 접촉과 갈등]   

1. 소비자의 관점 - 택배 훼손 및 분실, 컴플레인 후 기사와의 갈등, 혼자 사는 1인 가구의 두려움(대면 및 사건사고)   
2. 택배기사의 관점 - 배송 업무 이외에도 직접적인(direct) 연락망으로 고객관리   

## 해결책 : 비대면 배송을 위한 택배 안전 CCTV
실시간 Segmentation을 통해 택배가 왔는지 확인하고, 대면 접촉을 최소화하세요!   
<img width="687" alt="스크린샷 2024-07-30 15 00 53" src="https://github.com/user-attachments/assets/4177b74d-3155-4540-9945-a01d7a0d0749">
<img width="684" alt="스크린샷 2024-07-30 15 01 20" src="https://github.com/user-attachments/assets/7fd0fd4d-f4be-401e-beee-d76c580409c1">

## 사용한 AI Model
**Segment Anything by Meta → Grouded SAM by IdeaReaserch → FastSAM by Ultralytics**     
1. 이번 프로젝트에서는 총 3가지 모델을 사용했으며, 최종적으로는 FastSAM을 사용했습니다.
2. 사용한 모든 모델은 Meta에서 제작한 Segmentation 모델인 SegmentAnything을 기초로 하고 있습니다. 모두 Zero-shot Learning을 기초로 하기 때문에 따로 Fine-tuning을 진행하지 않아도 기존에 학습되지 않은 객체를 인식할 수 있습니다. 
3. GroundedSAM 사용 시, 1 Frame에 80초 정도 걸리는 **이미지 처리 시간의 한계**로 인해 실시간성이 강한 Ultralytics의 FastSAM을 사용하기로 했습니다.
4. 최종 산출물로는 Text prompt와 Image를 입력받아 FastSAM으로 Segmentation을 수행하는 CCTV를 제작했습니다.
   
<img width="685" alt="스크린샷 2024-07-30 15 01 55" src="https://github.com/user-attachments/assets/a04cb600-a9e6-4dcd-bd79-da05868f8340">
<img width="684" alt="스크린샷 2024-07-30 15 09 02" src="https://github.com/user-attachments/assets/2c08db81-1228-42e1-98cc-40f825130214">
<img width="682" alt="스크린샷 2024-07-30 15 09 19" src="https://github.com/user-attachments/assets/cf9180a5-4c72-4aaf-9057-f2db267d3c6e">
<img width="683" alt="스크린샷 2024-07-30 15 09 32" src="https://github.com/user-attachments/assets/b6239c3c-5a42-4c90-b97e-374036923501">

최종 output의 이미지는 첨부된 ppt 자료에 올려두었습니다.    
[PPT 보러가기](https://www.canva.com/design/DAGLGN4d-aY/qWzT5F_FydbTBlKngVBoWA/view?utm_content=DAGLGN4d-aY&utm_campaign=designshare&utm_medium=link&utm_source=editor)
