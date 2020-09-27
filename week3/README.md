## Color Model
색상 모델은 색상이 숫자 튜플로 표현될 수 있는 방법을 설명하는 추상적인 수학 모델이며, 일반적으로 3, 4개의 값이나 색상 구성요소로 표현된다.
 이 모델이 성분이 어떻게 설명될 수 있는지에 관한 정확한 해석 방법과 연관되어 있을 때, 결과적인 색상 세트를 "색상 공간"이라고 한다. 

## Color space
컬러가 담긴 공간.
Color Space은 임의로, 즉 물리적으로 실현된 색상이 부여된 색상 이름(임의의 넘버링 포함)과 함께 물리적 색상 견본에 할당되거나(예시-Pantone 컬렉션) 수학적으로 구조화된다.(예-NCS 시스템, Adobe RGB, sRGB)

예시    
감산 원색(사이안, 마젠타, 노랑, 검정)을 사용하는 CMYK 색상 모델을 기반으로 색 공간의 경우. 
주어진 색 공간의 3차원 표현을 만들기 위해 표현 X축을 마젠타 색의 양, Y축을 청록의 양, Z축을 황색의 양으로 설정하면 . 이 3D 공간은 세 가지 색소를 결합함으로써 생성될 수 있는 모든 가능한 색상에 대한 고유한 위치를 제공한다.
많은 Color Space가 이런 식으로 3차원 값으로 표현될 수 있지만 어떤 것은 더 많거나 적은 면적을 가지고, 팬톤같은 것은 이런 식으로 표현될 수 없다.


+ RGB     
 가산혼합. 가장 기본적인 색상 모델로 색을 광원인 Red, Green, Blue의 3가지 성분을 조합으로 보는 것이다. 검은색은 R=G=B=0이다. 각 색마다 8bit으로 표현되어 (2^8)^3 = 16,777,216가지 색으로 표현되며, 모든 색은 길이가 1인 3차원 정육면체내의 한 점과 대응시킬 수 있다.
-CMYK
 감산혼합. C=cyan M=magenta Y=yellow K=black
+CIE 
+YUV
UV 평면의 Color Space
 Y=밝기
 YCbCr/YPbPy 등이 이 Color Space를 사용. 

# 원통형 좌표 컬러 모델
+HSL, HSV
+먼셀 색 체계
 20세기 초 Albert Muncell에 의해 개발. 물감, 크레용 등의 색상지정에 사용
![ https://en.wikipedia.org/wiki/File:Munsell_1943_color_solid_cylindrical_coordinates.png)] ( https://en.wikipedia.org/wiki/File:Munsell_1943_color_solid_cylindrical_coordinates.png)


+NCS
 유럽에서 널리 사용된다. 노랑,빨강,초록,파랑을 한 평면에 강제로 넣기때문에 lightness dimention이 인식된 lightness가 다르다
