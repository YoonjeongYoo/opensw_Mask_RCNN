# opensw_Mask_RCNN
오픈소스SW실습 과제1 : Mask RCNN 환경구축

<진행과정 및 문제상황>

1. https://ultrakid.tistory.com/21 해당 링크에 나와있는 방법을 따라 cuda 및 cudnn를 설치
2. https://reyrei.tistory.com/21 해당 링크에 나와있는 대로 balloon.py 파일을 이용하여 훈련 진행 시도
-> ImportError: Could not find 'nvcuda.dll' 발생 (문제상황 발생)

![스크린샷 2023-11-24 033826](https://github.com/YoonjeongYoo/opensw_Mask_RCNN/assets/145105916/a82b9b39-b91b-4e6d-a49e-b18f84593776)

3. https://github.com/matterport/Mask_RCNN.git에 제공된 mask_rcnn_ballon.h5 파일을 사용하기로함
4. https://hansonminlearning.tistory.com/16를 따라서 jupyter notebook 파일을 수정 (경로 수정)
![스크린샷 2023-11-24 031955](https://github.com/YoonjeongYoo/opensw_Mask_RCNN/assets/145105916/bfa8424a-346a-430d-9c82-75242d391ee1)

(ROOT_DIR 경로수정, BALLON_WEIGHTS_PATH 경로수정)

![스크린샷 2023-11-24 032005](https://github.com/YoonjeongYoo/opensw_Mask_RCNN/assets/145105916/083316f6-cf57-44fa-a5ed-1a4680aa69c2)

(BALLOON_DIR 경로수정)

![스크린샷 2023-11-24 032015](https://github.com/YoonjeongYoo/opensw_Mask_RCNN/assets/145105916/fa950e7b-a417-4b86-940e-4664442100c8)

(DEVICE = "/gpu:0" 으로 수정)

5. jupyter notebook 수정 후 run(실행) 시도 시 오류 발생
![스크린샷 2023-11-24 033927](https://github.com/YoonjeongYoo/opensw_Mask_RCNN/assets/145105916/0ab93144-981a-47e0-a714-36cf72fe6715)

->ImportError: Could not find 'nvcuda.dll' 발생(문제상황 발생)

<정리>

ImportError: Could not find 'nvcuda.dll'에러가 계속 발생하는 걸로 보아 'nvcuda.dll'이 제대로 설치가 되지 않았거나 경로설정이 잘 안되있는 것으로 보임

해당 부분을 해결해보려고 시도했지만 해결하지 못함

실습시 사용한 파일은 master branch에 업로드 하였음
