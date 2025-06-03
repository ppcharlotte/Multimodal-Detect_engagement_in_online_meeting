# Online Meeting Engagement Prediction

This repository provides a pipeline for segmenting, extracting, and analyzing features from online meeting videos to predict participant engagement using clustering methods.

## Project Structure

```
1-video_segmentation.ipynb
2-extract_reference_segments.ipynb
3-feature_extraction.ipynb
4-feature_gathering.ipynb
5-label_analysis.ipynb
6-clustering.ipynb
7-clustering_alignment.ipynb
data/
    all_features_combined.pickle
    behavior_results.zip
    dnn_feature_reference.pickle
    dnn_feature.pickle
    reference_behavior_results.zip
```

## Pipeline Overview

1. **Video Segmentation**  
   [`1-video_segmentation.ipynb`](1-video_segmentation.ipynb): Downloads the dataset and segments meeting videos into 5-second clips, filtering to extract target clips.

2. **Extract Reference Segments**  
   [`2-extract_reference_segments.ipynb`](2-extract_reference_segments.ipynb): Extracts reference segments corresponding to the segmented video clips for feature extraction and analysis.

3. **Feature Extraction**  
   [`3-feature_extraction.ipynb`](3-feature_extraction.ipynb): Extracts features (e.g., Action Units, DNN features) from video clips using tools such as OpenFace and dlib.

4. **Feature Gathering**  
   [`4-feature_gathering.ipynb`](4-feature_gathering.ipynb): Aggregates extracted features into combined datasets.

5. **Label Analysis**  
   [`5-label_analysis.ipynb`](5-label_analysis.ipynb): Analyzes behavioral labels and prepares data for clustering.

6. **Clustering**  
   [`6-clustering.ipynb`](6-clustering.ipynb): Applies clustering algorithms and analyzes features to identify patterns of engagement without using alignment features.

7. **Clustering Alignment**  
   [`7-clustering_alignment.ipynb`](7-clustering_alignment.ipynb): Applies clustering algorithms and analyzes features to identify patterns of engagement using alignment features.

## Data

- All intermediate and final data files are stored in the `data/` directory.
- Feature files:  
  - `all_features_combined.pickle`  
  - `dnn_feature_reference.pickle`  
  - `dnn_feature.pickle`
- Behavioral results:  
  - `behavior_results.zip`  
  - `reference_behavior_results.zip`

## Requirements

- Python 3.x
- Jupyter Notebook or Google Colab
- [OpenFace](https://github.com/TadasBaltrusaitis/OpenFace)
- [dlib](https://github.com/davisking/dlib)
- Python packages: numpy, pandas, scikit-learn, mediapipe, etc.

## Setup

1. Clone the repository.
2. Data will be downloaded automatically in the code, but you can also prepare your own video data and place it in the appropriate directories if needed.
3. Run the notebooks in order for a full pipeline execution.

## License

This project is intended for academic and research purposes only.

