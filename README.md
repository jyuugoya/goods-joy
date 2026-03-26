[Goods & Joy 3D Product Viewer Demo.md](https://github.com/user-attachments/files/26261448/Goods.Joy.3D.Product.Viewer.Demo.md)
# **Goods \& Joy 3D Product Viewer Demo**

#### SHOPIFY 기반으로 제작된 K-POP 굿즈 쇼핑몰의 상품 상세 페이지에

#### 3D 뷰어를 적용한 데모 프로젝트입니다.

#### A demo project implementing a 3D product viewer 

#### for a K-POP goods shopping mall.



#### **Live Demo** : https://jyuugoya.github.io/goods-joy/shop-landing.html



##### **OVERVIEW**

###### 기존 쇼핑몰의 2D 상품 이미지를 넘어, 고객이 상품을 360° 회전하며 입체적으로 확인할 수 있는 3D 뷰어를 구현했습니다.

###### Beyond traditional 2D product images, this project allows customers to explore products interactively in 360° 3D before purchasing.



##### **TECH STACK**

###### Google Model Viewer

###### Kiri Engine Pro (3DGS mode)

###### TRELLIS (Hugging Face)

###### Blender

###### HTML / CSS / JavaScript



##### **3D Object제작 과정**



|**앤톤 인형 (Meongryongi)**|**보이넥스트도어 공식 응원봉 (wonder stick)**|**엑소 응원봉 (eridibong)**|
|-|-|-|
|Kiri Engine으로 실물 촬영<br />→ GLB export<br />→ 상품 페이지 연결|투명 구체 소재로 스캔 난이도 높음<br />→ 구체 분리 후 TRELLIS AI로 이미지를 3D 변환<br />→ Blender에서 투명 UV Sphere 추가<br />→ Texture Paint로 텍스처 수정<br />→ GLB export<br />→ 상품페이지 연결|Kiri Engine의 3DGS모드(Gaussian Splatting)로 실물 촬영 <br />→ PLY export|

###### 

##### **File Structure**

###### goods-joy/

###### ├── shop-landing.html       # 메인 쇼핑몰 페이지

###### ├── 앤톤3d.glb              # 앤톤 인형 3D 모델

###### ├── 앤톤\_앞.png             # 앤톤 인형 정면 사진

###### ├── 앤톤\_뒤.png             # 앤톤 인형 후면 사진

###### ├── trellis\_wonderstick.glb # 원더스틱 3D 모델

###### ├── Exo\_Gaussian Splatting.ply # 에리디봉 3D 모델

###### └── 보이넥스트도어응원봉.jpg  # 원더스틱 실물 사진



##### **Key Challenges**

###### 투명/광택 소재의 3D 스캔 문제

###### 응원봉의 투명 구체는 빛을 투과해 3D 스캔이 어려웠습니다.

###### Featureless Object Scan, Gaussian Splatting, AI 생성 등 다양한 방법을 시도한 끝에

###### 구체 분리 → 3D 오브젝트를 이미지 AI로 생성 → Blender로 구체 합성 방식으로 해결했습니다.

