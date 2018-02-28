# PFMN

![main_figure](assets/PFMN.png)

This project hosts the PyTorch implementation code for our **CVPR 2018** paper.

- Sangho Lee, Jinyoung Seong, Youngjae Yu and Gunhee Kim. A Memory Network Approach for Story-based Temporal Summarization of 360&deg; Videos. In *CVPR*, 2018. [[arxiv]]()

We propose a novel memory network model named *Past-Future Memory Network* (PFMN) for story-based temporal summarization of 360&deg; videos.
PFMN first computes the score of 81 normal field of view (NFOV) region proposals cropped from the input 360&deg; video, and then recovers latent, collective storyline using a memory network that involves two external memories to store the embeddings of previously selected subshots and future candidate subshots.
We empirically validated that the proposed memory network approach outperformed other state-of-the-art methods, not only for view selection but also for story-based temporal summarization in both 360 videos and photostreams.

Skipping the view selection step, our PFMN is also applicable to conventional video summarization with no modification.
**Because of lincensing issues, here we present only the memory network component and our newly collected conventional video dataset from YouTube.**

## Dataset
The subset of Yahoo Flickr 100M used in our work will be available soon,
and this contains res5c and pool5 features of ResNet-152 in the format used by the code.

## Dependencies
Our implementation requires the following dependencies:
- [CUDA 8.0](https://developer.nvidia.com/cuda-downloads)
- [PyTorch 0.3.1](http://pytorch.org/)

## Setup
We highly recommend using python2 & virtualenv (our_tmp_sum : our dataset directory, which will be available soon):
```
git clone https://github.com/sangho-vision/CVPR2018_PFMN.git
cd CVPR2018_PFMN & ln -s ${our_tmp_sum} tmp_sum
pip install -r requirements.txt
pip install 'requests[security]'
```

If SSL InsecurePlatformWarning occurs when installing requests package:
```
sudo apt-get install libffi-dev libssl-dev
```

## Acknowledgement

We appreciate Joonil Na, Jaemin Cho and [Juyong Kim](http://juyongkim.com/) for helpful comments and discussions.

## Authors

Sangho Lee, Jinyoung Sung, [Youngjae Yu](https://yj-yu.github.io/home/) and [Gunhee Kim](http://vision.snu.ac.kr/~gunhee/)
[Vision and Learning Lab](http://vision.snu.ac.kr/) @ Computer Science and Engineering, Seoul National University, Seoul, Republic of Korea

## Reference

If you use this code or dataset as part of any published research, please refer the following paper.
```
@inproceedings{PFMN:2018:CVPR,
    author    = {Sangho Lee and Jinyoung Sung and Youngjae Yu and Gunhee Kim},
    title     = "{A Memory Network Approach for Story-based Temporal Summarization of 360\deg~Videos}"
    booktitle = {CVPR},
    year      = 2018
}
```

## License

MIT license
