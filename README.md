# StableVideo: Text-driven Consistency-aware Diffusion Video Editing

https://github.com/rese1f/StableVideo/assets/58205475/558555f1-711c-46f0-85bc-9c229ff1f511

https://github.com/rese1f/StableVideo/assets/58205475/c152d0fa-16d3-4528-b9c2-ad2ec53944b9

https://github.com/rese1f/StableVideo/assets/58205475/0edbefdd-9b5f-4868-842c-9bf3156a54d3


## Installation
```
git clone https://github.com/rese1f/StableVideo.git
conda create -n stablevideo python=3.11
pip install -r requirements.txt
```

## Download Pretrained Model

All models and detectors can be downloaded from ControlNet Hugging Face page at [Download Link](https://huggingface.co/lllyasviel/ControlNet).


## Download example videos
Download the example atlas for car-turn, boat, libby, blackswa, bear, bicycle_tali, giraffe, kite-surf, lucia and motorbike at [Download Link](https://www.dropbox.com/s/oiyhbiqdws2p6r1/nla_share.zip?dl=0) shared by [Text2LIVE](https://github.com/omerbt/Text2LIVE) authors.

You can also train on your own video following [NLA](https://github.com/ykasten/layered-neural-atlases).

And it will create a folder data:
```
StableVideo
├── ...
├── ckpt
│   ├── cldm_v15.yaml
|   ├── dpt_hybrid-midas-501f0c75.pt
│   ├── control_sd15_canny.pth
│   └── control_sd15_depth.pth
├── data
│   └── car-turn
│       ├── checkpoint # NLA models are stored here
│       ├── car-turn # contains video frames
│       ├── ...
│   ├── blackswan
│   ├── ...
└── ...
```

## Run and Play!
Run the following command to start. We provide some [prompt template](prompt_template.md) to help you achieve better result.
```
python app.py
```
the result `.mp4` video and keyframe will be stored in the directory `./log` after clicking `render` button.

## Acknowledgement

This implementation is built partly on [Text2LIVE](https://github.com/omerbt/Text2LIVE) and [ControlNet](https://github.com/lllyasviel/ControlNet).

<!-- ## Citation -->
