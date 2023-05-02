# 📀음악 리뷰 감성분석📀 수정이 아직...

<div align=center>
MobileBert를 활용한 긍부정 예측 딥러닝 프로젝트
  
음악 리뷰에는 보통 긍정적인 리뷰가 많지만, 일부 부정적인 리뷰도 있다. 이를 이진 분류 문제로 정의하여 MobileBERT 모델을 훈련시킨다. 

<img src="https://img.shields.io/badge/PyTorch-E34F26?style=flat-square&logo=PyTorch&logoColor=white"/></a>

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/></a>
</div>

# 1. 문제 정의
## 1.1 영향력

  전 세계의 수많은 사람들이 스트리밍 플랫폼을 통해 인터넷 상에서 음악이나 비디오를 스트리밍하는 서비스를 제공받고 있다. 사용자들은 인터넷에 연결된 장치에서 음악을 듣고, 저장 및 다운로드 없이 해당 음악에 대한 액세스 권한을 얻을 수 있기 때문에 다양한 음악에 대한 접근이 쉬워졌으며, 이러한 플랫폼들은 인터넷의 보급과 함께 급속도로 성장하고 있다. 대표적인 스트리밍 플랫폼으로 Spotify가 있는데, Spotify에만 2023년 3월 31일 기준으로 5억 1,500만 명이 오디오 스트리밍 서비스를 이용하고 있고 Spotify는 거의 모든 연령대 뿐만 아니라 선진국과 개발도상국 시장 모두에서 이용자 수에 대한 큰 성장을 보였다. [[1]](https://www.engadget.com/spotify-reaches-more-than-half-a-billion-users-for-the-first-time-142818686.html) 이를 미루어 보아 사람들의 음악 컨텐츠에 대한 관심이 날로 증가함을 알 수 있다.

  음악 시장의 성장과 더불어 발전하는 IT기술이 스트리밍 플랫폼의 시장을 성장시키고 있다. 음악 스트리밍 플랫폼은 기존에는 음악을 스트리밍하기 위한 단순한 플랫폼이었지만, 지금은 매우 다양한 기능을 제공하며 기본적으로 대부분의 스트리밍 플랫폼에는 댓글과 평점과 같이 청취자가 실제로 앨범에 대해 피드백을 줄 수 있는 환경이 마련되어 있다. 그리고 스트리밍 플랫폼 외에도 AllMusic, Pitchfork, Rolling Stone, NME와 같은 음악 관련 웹사이트나 앱에서도 앨범에 대한 리뷰와 평점을 남길 수 있는 기능이 제공되고 있고 이러한 서비스들이 많아지고 있다. 

스트리밍 플랫폼의 시장의 성장률을 미루어 보아 시간인 지남에 따라 데이터의 


## 1.2 문제 정의

(수정사향: 음악 리뷰 감성분석 모델은 음악 산업에서 예측력과 시장 파악력을 높임으로 다양한 산업역량을 강화할 수 있다.

음악 추천 시스템_ 음악 리뷰 감성분석 모델을 활용하여 사용자의 취향에 맞는 음악을 추천하는 시스템을 구축할 수 있다.

마케팅 분석_
  
음악 리뷰 감성분석 모델을 활용하여 마케팅의 성과를 분석, 평가하여 다음 상품의 마케팅에 참조할 수 있다.
    
음악 리뷰 감성분석 모델을 활용하여 음악 장르, 아티스트, 앨범 등의 정보를 추출하여 음악 산업에서의 시장 동향과 인기도를 파악할 수 있다.
    
아티스트 평가_ 음악 리뷰 감성분석 모델을 활용하여 아티스트의 평가를 수행할 수 있다.

이 데이터를 사용해서 긍부정 프로젝트를 해볼 예정이다.

음악 추천/마케팅 분석... 
시장조사 설문조사 실태조사 

이것이 의미있는 일이다!!->문제정의

첫걸음으로 긍부정을 해보겠다.)
  

# 2.데이터
## 2.1 원시 데이터 현황

(수정사향: >총건수, 라벨의 분포(평점, 긍부정, 긍부정중), 부가정보>>파이차트 내가 데이터 시각화하기)

- 출처: https://www.kaggle.com/datasets/michaelbryantds/78k-music-album-reviews
![그림1](https://user-images.githubusercontent.com/104000117/232916528-72d8be0a-6ca6-4ce3-bc63-49e4563d659b.png)
![그림2](https://user-images.githubusercontent.com/104000117/232916534-04b41e98-89d7-4401-98c7-36d431c76512.png)

## 2.2 데이터 가공

(수정사향: 임계값 구한 방법 설명.....
이진분류 (출력)/파이차트, 제거 데이터, 입력 데이터에 대한 설명/문장 데이터=>길이 분포 len(str)/도수분표, 최종 데이터 (f_data, ,csv, 엑셀, 제이쓴..), raw_data.csv 가공 source.py 이력들 기록, <데이터 접근> )

- 임계값(threshold)을 정의하고, 이 임계값을 기준으로 위의 데이터를 0 또는 1로 분류한 결과
![그림3](https://user-images.githubusercontent.com/104000117/232919132-60083ffb-0de6-443d-9b2f-f32a8d3ad646.png)


# 딥러닝 모델링

# Reference

[1]https://www.engadget.com/spotify-reaches-more-than-half-a-billion-users-for-the-first-time-142818686.html


(수정사항: 신문기사 인용 주의
보고서를 통해서 작성되었을 경우, 출처작성)
