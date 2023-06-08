## Stable-diffusion을 사용하기 위해 반드시 알아야 하는 내용

- txt2img란?
  - text to image 를 의미합니다. 태그를 입력해서 그림을 생성하겠다는 말입니다. (태그 추천이 필요하다면 [여기](https://novelai.app)를 참고해주세요.)
  - 글씨를 넣을 수 있는 부분이 총 2개 있는데 위쪽부터 각각 원하는 태그, 원하지 않는 태그입니다.
- Stable Diffusion checkpoint란?
  - 원하는 화풍을 만들기 위한 모델입니다. 인터넷에서 다운받아 쓰면 됩니다.
- Sampling Steps란?
  - 생성 과정에서의 단계 수를 의미합니다. 이 단계가 높을 수록 더 높은 품질의 이미지를 생성하며, 필요한 리소스가 늘어납니다. (보통 20~30을 많이 사용합니다.)
- Restore faces(얼굴 복원)란?
  - 이미지 내 인물 얼굴의 세부 사항과 특징을 복구하거나 향상시키는 과정을 말합니다. 얼굴을 이쁘게 출력해준다고 보면 됩니다.
- Tiling(타일링)이란?
  - 이미지를 반복되는 패턴 모양으로 출력합니다.
- Hires. fix(고해상도 보정)란?
  - 고해상도로 그림을 뽑아줍니다. 고화질로 출력할 때 체크합니다.
- Width/Height(가로/세로)란?
  - 그림의 가로/세로 크기를 의미합니다. (주로 정사각형은 512 x 512, 직사각형은 512 x 768, 768 x 512를 많이 사용합니다.)
- Batch count(배치 수)란?
  - 출력할 그림의 개수입니다.
- CFG Scale(CFG 스케일)이란?
  - 내가 적은 내용을 얼마나 그림에 반영할지를 나타내는 값입니다. 이 낮을 수록 창의적인 그림이 많이 나옵니다. (주로 7~12를 많이 사용합니다.)
- Seed(시드)란?
  - 그림의 고유번호입니다. -1`🎲️`은 랜덤이고 재활용 마크`♻️`는 내가 이전에 뽑은 그림을 불러옵니다.

## Quick Start

1. https://civitai.com 에서 본인이 원하는 화풍의 `*.safetensors` 파일을 다운로드 받은 후, 해당 파일을 `/models/Stable-diffusion` 폴더에 넣습니다.
   1. 해당 `*.safetensors`파일을 우리는 Stable Diffusion checkpoint, 줄여서 checkpoint라고 부릅니다.
2. 터미널에 `./webui.sh`를 실행해서 webui를 실행합니다. (윈도우라면 `./webui.bat`을 실행해주세요)
3. http://localhost:7860 에 접속해서 webui를 확인하고 Generate 버튼 근처 `🎴` 이모지를 클릭합니다.
4. Checkpoints를 선택하고 본인이 추가한 모델을 선택합니다. (만약 없을 시 새로고침 해주세요.)
5. `🎴` 이모지를 다시 클릭해서 메인 화면으로 돌아갑니다.
6. 본인이 원하는 태그를 넣고 이미지를 Generate 합니다.
