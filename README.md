# caugh_improvement

## To do task
* roughness 측정코드 완성
* sharpness 측정코드 완성

위 sound quality prameter는 Zwicker parameter라고 불리는 표준에 의해 측정되었고
직접 짠 코드로 측정했을 때 기존에 있는 데이터(전문 프로그램-아르테미스로 측정)와 모양이 많이 달라서 개선해야하는 상황입니다.

비교할 수 있는 기존 데이터들을 따로 폴더에 넣어뒀으니 비슷한 모양이 나올 수 있게 개선해주시면 됩니다.
기존 csv 데이터 이미지로 만들기 전에 코드의 결과로 나온 데이터와 얼마나 비슷한지 확인해보고 비슷하면 이미지로 변환해서 사용할 것입니다.

기존 아르테미스는 딜레이 문제 때문에 0.03~0.05초 간격으로 음원이 나뉘었지만 저희는 코드로 0.03초 간격으로 나눠뒀습니다. (./multi_waves 폴더 안에 저장해뒀습니다)

## loudness 예시
예를 들어 loudness를 측정했던 코드와 과정을 설명해드리자면(./loudness 예시 폴더 참고)
into_multi_waves.py 에 있는 과정으로 음원을 나눈 뒤 Loudness.py에서 각 음원마다의 loudness를 측정하고 Artemis의 결과에 맞게 보정했습니다. loudness 값이 저장된 리스트로 to_image.py에서 이미지로(result.png) 만들었고 아르테미스와 비슷한 결과(원본데이터.png)를 내기 위해서 총 음원 52개 중 40개까지만 이용했습니다.
이렇게 loudness로 나온 이미지처럼 sharpness와 roughness도 만들어주시면 됩니다.

## reference
기존에 timbral_models 로 구현했던 sharpness와 roughness 코드를 넣어뒀는데 이 값들과 Artemis로 측정한 값들을 비교해서 비슷하게 조정해주시거나 다른 방법으로 구현하셔도 됩니다!
서버에 올린 코드는 https://github.com/kimseongah/caugh 에서 확인하실 수 있습니다.