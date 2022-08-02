# Usage Notes

To perform transfer learning with frozen layers, call `train.py` setting the `--freeze` argument to the number of layers to be frozen. For example, to freeze the backbone while training on the Sealing dataset, do:

    python train.py --data sealing.yaml --weights yolov5s.pt --epochs 100 --img 640 --device cpu --freeze 10

The `val.py` script has been updated to record detection result data to file `detections.txt` alongside other validation artifacts. This can be used to compute the ROC-AUC plot for the detector.

To run validation on the Sealing dataset. enter:

    python val.py --data sealing.yaml --weights runs/train/exp/weights/best.pt --img 640 --device cpu

## References

* [Transfer Learning with Frozen Layers](https://docs.ultralytics.com/tutorials/transfer-learning-froze-layers/)
