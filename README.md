# PAtt-Lite: Lightweight Patch and Attention MobileNet for Challenging Facial Expression Recognition
This is the official implementation for our paper [PAtt-Lite: Lightweight Patch and Attention MobileNet for Challenging Facial Expression Recognition](https://arxiv.org/pdf/2306.09626.pdf). 

## Notice
Thanks to @heomyeongboem for [pointing out](https://github.com/JLREx/PAtt-Lite/issues/6#issuecomment-2044500189) the implementation error around our proposed Attention Classifier. We had a massive overlook on how TensorFlow treats and assumes its input, thus the current model can be seen somewhat as a "few-shot" model. This error, along with the performance comparison with SOTA under this setting are not intentional and we intend to solve this as soon as possible. 

We are working on it to solve it while retaining the reported performance and the proposed architecture as much as we can. The fixed architecture and its experimental results will be updated here in the coming weeks. 

Meanwhile, the dataset compilation code has been uploaded and is available [here](data-compile.ipynb). 

## To Do
- [x] Update architecture figure for more details
- [x] Upload dataset compilation codes
- [ ] Fix implementation error around attention

## Abstract
![architecture](architecture.png)

Facial Expression Recognition (FER) is a machine learning problem that deals with recognizing human facial expressions. While existing work has achieved performance improvements in recent years, FER in the wild and under challenging conditions remains a challenge. In this paper, a lightweight patch and attention network based on MobileNetV1, referred to as PAtt-Lite, is proposed to improve FER performance under challenging conditions. A truncated ImageNet-pre-trained MobileNetV1 is utilized as the backbone feature extractor of the proposed method. In place of the truncated layers is a patch extraction block that is proposed for extracting significant local facial features to enhance the representation from MobileNetV1, especially under challenging conditions. An attention classifier is also proposed to improve the learning of these patched feature maps from the extremely lightweight feature extractor. The experimental results on public benchmark databases proved the effectiveness of the proposed method. PAtt-Lite achieved state-of-the-art results on CK+, RAF-DB, FER2013, FERPlus, and the challenging conditions subsets for RAF-DB and FERPlus. 

## Notebook
The [training notebook](patt-lite-notebook.ipynb) and the [dataset compilation codes](data-compile.ipynb) can be found in this repository. 

## License
PAtt-Lite is available under the MIT license. See [LICENSE](LICENSE) for details. 

## Citation
If you find our work useful in your research, please consider citing our paper. 
```bibtex
@article{le2024patt,
  title={PAtt-Lite: lightweight patch and attention MobileNet for challenging facial expression recognition},
  author={Le Ngwe, Jia and Lim, Kian Ming and Lee, Chin Poo and Ong, Thian Song and Alqahtani, Ali},
  journal={IEEE Access},
  year={2024},
  publisher={IEEE}
}
```
