# robust-detection-benchmark

General project repo, starting point for users & hosting benchmark table:
https://github.com/bethgelab/robust-detection-benchmark (this repo)

Stylize arbitrary datasets:
https://github.com/bethgelab/stylize-datasets

Corrupt arbitrary datasets:
https://github.com/bethgelab/add-common-image-corruptions

Object detection:
https://github.com/bethgelab/robust_object_detection

## Workflow

1. clone
2. get data (COCO, Pascal) & MMdetect
3. stylize.sh
4. train object detector
5. corrupt datasets & evaluate

## Benchmark

Coco: Results are evaluated on COCO 2017val.
Cityscapes: Results are evaluated on Cityscapes val.
Pascal: Results are evaluated on Pascal VOC 2007 test.

Results are sorted by their absolute performance under corruption.

### Coco

#### Object detection:

Model  | Backbone  | box AP clean | box AP corr. | box % |
:-----:|:---------:|:------------:|:------------:|:-----:|
Hybrid Task Cascade | X-101-64x4d-FPN-DCN | 50.6 | 32.7 | 64.7  |    
Faster R-CNN Combined | R-50-FPN | 34.6   | 20.4 | 58.9  |
Mask R-CNN   | R-50-FPN          | 37.3   | 18.7 | 50.1  |
Faster R-CNN | R-50-FPN          | 36.3   | 18.2 | 50.2  |
RetinaNet    | R-50-FPN          | 35.6   | 17.8 | 50.1  |

#### Instance Segmentation:

Model  | Backbone  | mask AP clean | mask AP corr. | mask % |
:-----:|:---------:|:-------------:|:-------------:|:------:|
Hybrid Task Cascade | X-101-64x4d-FPN-DCN | 43.8 | 28.1 | 64.0  | 
Mask R-CNN Combined | R-50-FPN | 32.9  | 19.0      | 57.7   |
Mask R-CNN          | R-50-FPN | 34.2  | 16.8      | 49.1   |


### Pascal VOC

#### Object detection:

Model  | Backbone  | box AP50 clean | box AP50 corr. | box % |
:-----:|:---------:|:--------------:|:--------------:|:-----:|
Faster R-CNN Combined | R-50-FPN | 80.4 | 56.2       | 69.9  |
Faster R-CNN | R-50-FPN          | 80.5 | 48.6       | 60.4  |


### Cityscapes

#### Object detection:

Model  | Backbone  | box AP clean | box AP corr. | box % |
:-----:|:---------:|:------------:|:------------:|:-----:|
Faster R-CNN Combined | R-50-FPN | 36.3 | 17.2   | 47.4  |
Faster R-CNN | R-50-FPN  | 36.4   | 12.2         | 33.4  |
Mask R-CNN   | R-50-FPN  | 37.5   | 11.7         | 31.1  |



#### Instance Segmentation:

Model  | Backbone  | mask AP clean | mask AP corr. | mask % |
:-----:|:---------:|:-------------:|:-------------:|:------:|
Mask R-CNN Combined  | R-50-FPN | 32.1  | 14.9     | 46.3   |
Mask R-CNN   | R-50-FPN  | 32.7    | 10.0          | 30.5   |


## Citation

If you use our code or the benchmark, please cite:
```
@article{xyz2019,
  title={xxx},
  author={xyz},
  journal={arXiv:},
  year={2019}
}
```
