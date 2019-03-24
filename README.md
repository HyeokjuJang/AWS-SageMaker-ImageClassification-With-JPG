# AWS-SageMaker-ImageClassification-With-JPG
Using MXNet
## 이 리포는 [AWS 튜토리얼을 약간 수정](https://github.com/awslabs/amazon-sagemaker-examples/tree/master/introduction_to_amazon_algorithms/imageclassification_caltech)한 것입니다.  
원 글은 위 링크를 따라가셔서 참고해주세요!  
## 무엇을 수정하였는가?  
원래 있던 튜토리얼에는 Caltech 101 파일을 기반으로 학습합니다. (.rec) 확장자를 다운받아서 그것을 AWS SageMaker로 학습하고 배포하는 과정을 거칩니다.  
하지만 제가 하고싶었던 것은 jpg파일을 기반으로 처음부터 학습하는 것이었습니다. 추가적인 하드웨어 없이 노트북만으로요.  
그래서 기존 튜토리얼에 약간 추가와 수정을 통해 하나의 주피터 노트북 프로젝트로 AWS SageMaker를 이용해 학습, 배포를 가능하게 작성해봤습니다.  
정말 별거 없는 리포지토리입니다.  
## 준비물  
1. 학습하고 싶은 jpg 이미지.  
2. 크롬이 동작 가능한 기기.  
3. 당신의 아마존웹서비스 계정을 이용가능하게 해줄 Visa카드.
## 사전준비
가장 먼저 해야할 일은 jpg 이미지 파일을 분류하는 것입니다. 당신이 구분하고 싶은대로 폴더를 만들고 그 안에 넣어주세요.  
한 이미지 안에 여러개의 분류하고 싶은 것이 있다면 이 리포지토리는 적합하지 않습니다. 당신이 따로 수정을 하셔야해요!  
이 리포지토리는 하나의 이미지에 하나의 라벨만 존재해야합니다.  
## 아마존웹서비스 준비
아마존웹서비스 계정이 필요합니다. 돈이 청구될 수도 있어요! 그리고 아래의 것들을 준비해주세요.
1. S3 버킷(버킷의 이름에는 sagemaker가 들어가게 지어주세요 sagemaker의 권한에 S3 버킷중 sagemaker라는 텍스트가 들어가있으면 접속을 허가하는 역할이 있어요.)
2. Sagemaker 새 노트북 인스턴스(생성하면서 역할을 선택할 때 1번에 있는 항목이 되어있는지 확인해주세요!)
## 다음으로 해야할 것
이 리포지토리에 있는 주피터 노트북파일(.ipynb)을 Sagemaker 노트북 안으로 넣어주셔야해요.
넣는 방법은 간단해요. Sagemaker 주피터 노트북으로 접속해주시고 New - Terminal에서 cd SageMaker로 가셔서 git clone https://github.com/HyeokjuJang/AWS-SageMaker-ImageClassification-With-JPG/ 을 해주세요. 그러면 클론이 이루어집니다! 
넣는 것까지 다 하셨다면 이제 ipynb파일을 여시고 해당 내용을 따라가주세요!
