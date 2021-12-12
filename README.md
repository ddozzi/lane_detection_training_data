# lane_detection_training_data
Training data for my lane detection CNN. Made for my STEM fair project.


## Things to note
- `360px_labels` refers to training data with size `614x360`, while `180px_labels` refers to training data with size `307x180`.
- All of the 1800 peices of training and validation data was all hand-made and manually labeled. The whole process took about ~10.7 hours.
- The training data is just resized versions of the original dataset which was `1228x720`. The original dataset was too large and inefficient to be used for training data so I just resized them to make it smaller. The original dataset made by me is still available: here.

## Format
All of the training data follow the same dictionary format, shown below.

```
{
  'img': [image in saved as a numpy array],
  'right_lane': [6 coordinates that make up the right lane],
  'left_lane': [6 coordinates that make up the left lane]
}
```
this training data was made for a fully-supervised machine learning model. The Google Colab notebook is available: here.
