# AI-SCHOOL 9기 Final Project
AI 스쿨 9기 Final Project 기록
------------
# 프로젝트 개요
Kaggle에 올라온 공모전에 참가하는 방향으로 프로젝트를 결정
![image](https://github.com/Seongjin1225/AI_School_9th_Final_Project_TEAM_3/assets/114036940/3d08ca36-7039-4b0d-bf45-9c0da51955e9)
https://www.kaggle.com/competitions/blood-vessel-segmentation/overview
- 신장 CT 사진에서 혈관을 찾아내는 Image Segmentation 작업 프로젝트
-----------
# 데이터 소개
-------------
- train 데이터와 test 데이터로 구성
- train 데이터는 총 5개의 하위 폴더로 구성(kidney_1_dense, kidney_1_sparse, kidney_2, kidney_3_dense, kidney_3_sparse)
- 각각의 하위 폴더마다 images, labels로 구성되어 있으며 kidney_3_dense의 경우 images만 존재(labels는 kidney_3_sparse에서 가져와야 함)
- train data의 경우 images 6,928장 labels 7,429장으로 구성
- test data는 labels는 없이 images 6장으로 구성
# 기본 모델
Medical Image Segmentation 분야에서 뛰어난 성능을 보인 U-Net Architecture를 프로젝트의 기본 모델로 선정
![image](https://github.com/Seongjin1225/AI_School_9th_Final_Project_TEAM_3/assets/114036940/732bb591-d07b-4dfa-a40e-830f25b86b4c)
- U-Net은 수축경로(encoder)와 확장경로(decoder)가 U자 형태로 구성된 구조를 가지고 있다
- 두 경로는 서로 대칭적이며 이 부분을 연결하는 역할을 하는 것이 브릿지(Bridge)
- 인코더와 디코더 모두 3X3 Convolution을 사용
