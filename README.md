# lane_detection_training_data
- Training data for my lane detection CNN. Made for my STEM fair project. 
- The following text explains the training data. An in-depth explanation for my project is available: here.
- If you're here from O2 wondering who I am, im ddozzi


## Things to note
- `360px_labels` refers to training data with size `614x360`, while `180px_labels` refers to training data with size `307x180`.
- All of the 1800 peices of training and validation data was all hand-made and manually labeled. The whole process took about ~10.7 hours.
- The training data is just resized versions of the original dataset which was `1228x720`. The original dataset was too large and inefficient to be used for training data so I just resized them to make it smaller. The original dataset made by me is still available: here.

## Format
All of the training data is saved as a pickle file for ease of use (`.p`). They follow the same dictionary format, shown below.

```
{
  'img': [image of a lane saved as a numpy array],
  'right_lane': [6 coordinates that make up the right lane],
  'left_lane': [6 coordinates that make up the left lane]
}
```
this training data was made for a fully-supervised machine learning model. The Google Colab notebook is available: here.

## Naming
You might notice the pickle files being named with the prefixes:
- `lsc`
- `msc`
- `dsr`

these prefixes are abbreviations of:

- `light straight curved`
- `medium straight curved`
- `dark straight rain`

they are named as such due to the kind of videos the images for the training dataset are derived from.

  When creating the dataset, I realized that I would need a lot of images in order to train it properly. What's the best source for lots of images? That's right, videos. Videos are made up of thousands of images, which when combined, created the illusion of moving objects, and animation. I got 3 videos from youtube, each of varying difficulty. 
  - The first was in broad daylight where lane lines were clearly visible, hence the name `light straight curved`. 
  - The next was in fairly rainy weather with a bit of bumpiness - `medium straight curved`. 
  - The last one was named `dark straight rain` as it was pitch black, with barely any lane visibility, rainy weather, and lots of road bumpiness.

## License 
GNU General Public License v3.0
