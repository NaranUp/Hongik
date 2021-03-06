# Color Space
## Color Model
색상 모델은 색상이 숫자 튜플로 표현될 수 있는 방법을 설명하는 추상적인 수학 모델이며, 일반적으로 3, 4개의 값이나 색상 구성요소로 표현된다.    
 이 모델이 성분이 어떻게 설명될 수 있는지에 관한 정확한 해석 방법과 연관되어 있을 때, 결과적인 색상 세트를 "색상 공간"이라고 한다. 

## Color space
컬러가 담긴 공간.    
색의 특정한 조직으로 다양한 물리적 장치에 의해 지원되는 색상 프로파일링과 결합하여, 재현 가능한 색의 표현을 나타낸다.
Color Space은 임의로, 즉 물리적으로 실현된 색상이 부여된 색상 이름(임의의 넘버링 포함)과 함께 물리적 색상 견본에 할당되거나(예시-Pantone 컬렉션) 수학적으로 구조화된다.(예-NCS 시스템, Adobe RGB, sRGB)
    
    
예시    
감산 원색(사이안, 마젠타, 노랑, 검정)을 사용하는 CMYK 색상 모델을 기반으로 색 공간의 경우. 
주어진 색 공간의 3차원 표현을 만들기 위해 표현 X축을 마젠타 색의 양, Y축을 청록의 양, Z축을 황색의 양으로 설정하면 . 이 3D 공간은 세 가지 색소를 결합함으로써 생성될 수 있는 모든 가능한 색상에 대한 고유한 위치를 제공한다.    
많은 Color Space가 이런 식으로 3차원 값으로 표현될 수 있지만 어떤 것은 더 많거나 적은 면적을 가지고, 팬톤같은 것은 이런 식으로 표현될 수 없다.
    
    
+ RGB     
 가산혼합. 가장 기본적인 색상 모델로 색을 광원인 Red, Green, Blue의 3가지 성분을 조합으로 보는 것이다. 검은색은 R=G=B=0이다.    
 각 색마다 8bit으로 표현되어 (2^8)^3 = 16,777,216가지 색으로 표현되며, 모든 색은 길이가 1인 3차원 정육면체내의 한 점과 대응시킬 수 있다.
 
+ CMYK    
 감산혼합. C=cyan M=magenta Y=yellow K=black
 
+ lab    
<img src="https://sensing.konicaminolta.asia/wp-content/uploads/2018/09/3D-LAB.jpg" width="400px" height="400px" title="px(픽셀) 크기 설정" alt="lab"></img><br/>
lightness, a”red-green”, b”yellow-blue”    
Lab 색 공간은 RGB나 CMYK가 표현할 수 있는 모든 색역을 포함하며, 인간이 지각할 수 없는 색깔도 포함하고 있다.

+ YUV    
![https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/YUV_UV_plane.svg/300px-YUV_UV_plane.svg.png)](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/YUV_UV_plane.svg/300px-YUV_UV_plane.svg.png)

UV 평면의 Color Space    
Y=밝기    
인간의 눈이 밝기차에비해 색차에는 비교적 둔하다는 점을 이용해서 Y에 많은 비트(해상도)를 할당하고 U(Cb), V(Cr)에는 적게 할당하여 압축한다.
YCbCr/YPbPy 등이 이 Color Space를 사용. 

+ HSL, HSV    
Hue(색상), Saturation(채도), Intensity=Value(명도)로 구성된 컬러모델.
물감을 사용하는 전통적인 색 혼합법과 비슷한 원리로 직관적이다.

+ 먼셀 색 체계    
 20세기 초 Albert Muncell에 의해 개발. 물감, 크레용 등의 색상지정에 사용
![https://upload.wikimedia.org/wikipedia/commons/thumb/c/ce/Munsell_1943_color_solid_cylindrical_coordinates.png/510px-Munsell_1943_color_solid_cylindrical_coordinates.png)](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ce/Munsell_1943_color_solid_cylindrical_coordinates.png/510px-Munsell_1943_color_solid_cylindrical_coordinates.png)

+ NCS    
 유럽에서 널리 사용된다. 노랑,빨강,초록,파랑을 한 평면에 강제로 넣기때문에 lightness dimention이 인식된 lightness가 다르다
     
     
# Color Gamut
컴퓨터 그래픽과 사진을 포함한 색상 재현에서 gamut는 색의 완전한 부분집합이다.
    
중요한 이유: 사진을 디지털화하거나, 디지털화된 이미지를 다른 색 공간으로 변환하거나, 특정 출력 장치를 사용하여 지정된 매체에 출력하면 일반적으로 gamut가 변경되는데, 그 과정에서 원본의 색상의 일부가 손실될 수 있다.
     
![https://docs.arnoldrenderer.com/download/attachments/88736289/image001.jpg?version=1&modificationDate=1560750710000&api=v2)](https://docs.arnoldrenderer.com/download/attachments/88736289/image001.jpg?version=1&modificationDate=1560750710000&api=v2)
    
### ACES 
(Academy Color Encoding System).   
영화나 TV를 제작하는 과정에서 색상 관리를 위한 업계 표준으로서, 디지털카메라 및 여러 촬영 방식의 사용이 증가함에 따라 발생하는 많은 소스마다 다른 색 공간을 통일시켜 제작, 포스트 프로덕션에서 야기될 수 있는 문제점을 보완하는 방법으로 제시된 색상 관리 및 이미지 교환 시스템이다.
ACES는 16bit, 32bit, 25stop 이상의 규격을 가지고 있어 현존하는 모든 카메라의 다이내믹 레인지와 컬러 영역을 커버할 수 있다. 넓은 color gamut가 특징이자 장점.
    
# Gamma
감마는 디스플레이에 입력되는 신호의 밝기(Gray Level)와 화면상에 나타나는 영상의 휘도 간 상관 관계를 결정하는 수치이다. 감마값에 따라 같은 화면이라도 표현되는 밝기 톤의 차이가 느껴질 수 있다. 감마값이 1인 경우는 입력과 출력의 밝기가 같지만, 1보다 크면 중·저계조 영역에서 화면이 좀 더 어둡게 표현이 되고, 반대로 1보다 작으면 밝게 표현이 된다.
    
![https://2.bp.blogspot.com/-uhV7ylirKL8/Wgf9Ta5bJzI/AAAAAAAAB3g/IvU_KiqvtSs96jOA81liHWgvAq5Kb-57gCK4BGAYYCw/s1600/image002-736561.png)](https://2.bp.blogspot.com/-uhV7ylirKL8/Wgf9Ta5bJzI/AAAAAAAAB3g/IvU_KiqvtSs96jOA81liHWgvAq5Kb-57gCK4BGAYYCw/s1600/image002-736561.png)

# LUT
Look-Up Table(LUT)란 비디오에 적용하여 룩을 변경할 수 있는 색상 사전 설정이다.      
간단히 말하자면 색상hue, 채도saturation, 조도brightness를 "수학적으로 정확하게" 조정하여 촬영된 원본 이미지의 색상 값을 새로운 값으로 만들어주는 방법이다.    이미지의 대비 또는 색상을 변경하거나 둘 다 변경할 수 있다.    
1D LUT는 입력값과 출력값이 1:1로 매칭되는 가장 간단한 테이블인 반면, 3D LUT는 훨씬 더 복잡하고 색상의 좌표값으로 표현할 수 있다.
    
LUT의 종류
    
1) Technical LUTs:

테크니컬 LUT는 이미지를 하나의 색공간(color space 또는 gamut)에서 다른 색공간으로 옮기기 위해 만들어졌다.  해당 LUT의 최종 목표는 두 가지 다른 시청 환경에서 똑같은 결과물을 만들어내는 것이다. 예를 들면, (똑같은 소스를) TV에서 보는 것과 잉크젯 프린터로 출력해서 보는 결과를 똑같이 맞춰주는 것이다.    
    
2) Creative LUTs:

크리에이티브 LUT는 다른 소프트웨어에서도 늘 한결같이 LUT가 가진 하나의 룩look을 표현할 수 있게 해준다.

*우리가 creative LUT를 technical LUT라고 생각하고 사용할 때 문제가 발생한다.  실제로 다양한 컬러 보정 LUT들이 이런 오해를 받고 있다.
    
3) Camera LUTs:

카메라 LUT의 좋은 예- ARRI Alexa의 Rec709 LUT    
이런 종류의 LUT는 technical LUT와 creative LUT를 합친 결과물이라고 할 수 있다.  그러나 카메라 노출에 의한 광량때문에 해당 LUT를 사용할 때마다 정확하게 작동하진 않는다.
  
# Log Space
Log (logarithmic)
로그 색상 곡선을 사용하는 가장 큰 이유는 카메라 센서(또는 필름)으로부터 동적인 정보 범위를 유지하는 방법이다. 그것은 비디오 화면을 캡처하는 것보다 가능한 한 많은 데이터를 저장하기 때문에 표준 비디오 곡선보다 더 많은 센서 정보를 이용한다. 이를 통해 후반 작업에 사용할 수 있는 훨씬 더 많은 컬러 데이터를 제공할 수 있다.

<img src="https://assets.rocketstock.com/uploads/2017/05/Log-Curve.jpg" width="570px" height="350px" title="px(픽셀) 크기 설정" alt="log"></img><br/>

위는 Linear color curve와 LOG color curve 사이의 차이를 나타낸 것이다.    
곡선에 익숙하다면, 곡선의 왼쪽 아래가 검정과 그림자를 나타낸다는 것을 알 수 있다. 그리고 곡선의 오른쪽 위로 이동할 때, 하이라이트와 화이트를 볼 수 있다. 보다시피 로그 곡선은 그림자를 유지하기 위해 이미지의 어두운 부분을 위로 민다. 하이라이트를 유지하기 위해 곡선의 상단이 아래로 이동시킨다. 따라서 각 색상 곡선의 측면에서 더 많은 데이터를 보존할 수 있다.

Linear 색상 공간은 장면에서 정확한 수학적 값에 부합하게 일정하고 변하지 않는 휘도 값을 가진다. 우리의 눈이 색을 정확한 휘도 값과 다르게  보고 있고 밝고 어두운 영역에서 더 많은 디테일을 볼 수 있기 때문에, 특정 영역에서는 매우 어둡고 질퍽하게 보일 것이다. 따라서 우리는 색 정보를 좀 더 미적으로 보기 위해 다른 색 공간을 적용해야 하고, 디스플레이와 모니터의 색 값을 표준화해야 한다.

--------
참조    

https://en.wikipedia.org/wiki/Color_model#CMYK_color_model
http://journal.kobeta.com/참관기-aces-시스템/
https://programminggiraffe.tistory.com/2
https://m.blog.naver.com/PostView.nhn?blogId=dwater1&logNo=220810673551&proxyReferer=https:%2F%2Fwww.google.com%2F
https://news.samsungdisplay.com/1869
https://mixinglight.com/portfolio/understanding-luts/
http://www.tv4u.co.kr/guide/content.asp?idx=1483
https://www.artstation.com/tiberius-viris/blog/3ZBO/color-space-management-srgb-linear-and-log
https://www.rocketstock.com/blog/tips-for-log-color-space-compositing/


    
