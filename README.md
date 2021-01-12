# SREFPN

This is the official repository for Super Resolution via Enchanced Feature Pyramid Network (SREFPN).

## Requriments

- Python 3.8.5
- Pytorch 1.6.0
- Windows 10

## Testing

* Run training x2, x3, x4 model
```bash
python train.py --root training_data/ --depth=48 --scale 2 --pretrained pretrained/48/epoch_730_x2.pth
python train.py --root training_data/ --depth=48 --scale 3 --pretrained pretrained/48/epoch_786_x3.pth
python train.py --root training_data/ --depth=48 --scale 4 --pretrained pretrained/48/epoch_772_x4.pth
```

## Training

The training dataset can be downloaded from [Training dataset DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/).
* Run testing x2, x3, x4 models on Set5, Set14, BSDS100, Urban100 and Manga109. The models will produce the accuracies equivalent to mentioned in the paper.
```bash
python test.py --upscale_factor 2 --depth 48 --checkpoint pretrained/48/epoch_730_x2.pth
python test.py --upscale_factor 3 --depth 48 --checkpoint pretrained/48/epoch_786_x3.pth
python test.py --upscale_factor 4 --depth 48 --checkpoint pretrained/48/epoch_772_x4.pth
```

## Citation

If you find SREFPN useful in your research, please consider citing:

```
@inproceedings{SREFPN,
  title={Super Resolution via Enchanced Feature Pyramid Network},
  author={Raza, Muhammad and Ketsoi, Vachiraporn and Haopeng, Chen and Xubo, Yang},
  booktitle={IEEE Transaction on Multimedia},
  pages={1--12},
  year={2021}
}
```
