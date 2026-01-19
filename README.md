# MusicDETR
Code for MUICDETR project.
After the paper is accepted, we will upload all the complete code.

# Getting Started
### Installation
```shell
conda create -n musicdetr python=3.11.9
conda activate musicdetr
pip install -r requirements.txt
```
### Data preparation

To train this model, you need to orgnize your dataset in the COCO format.
1. Download SSVD3.0 from [SSVD3.0]([https://opendatalab.com/OpenDataLab/COCO_2017](https://github.com/hust-itec2/SSVD3.0)).
2. Orgnize Images:
    Structure the dataset directories as follows:

    ```shell
    dataset/
    ├── images/
    │   ├── train/
    │   │   ├── image1.jpg
    │   │   ├── image2.jpg
    │   │   └── ...
    │   ├── val/
    │   │   ├── image1.jpg
    │   │   ├── image2.jpg
    │   │   └── ...
    └── annotations/
        ├── instances_train.json
        ├── instances_val.json
        └── ...
    ```

    - **`images/train/`**: Contains all training images.
    - **`images/val/`**: Contains all validation images.
    - **`annotations/`**: Contains COCO-formatted annotation files.
3. Convert Annotations to COCO Format:
   You need to convert the annotations into COCO format. The following script can serve as a reference.
   ```python
    import json

    def convert_to_coco(input_annotations, output_annotations):
        # Implement conversion logic here
        pass

    if __name__ == "__main__":
        convert_to_coco('path/to/your_annotations.json', 'dataset/annotations/instances_train.json')
    ```
4. Modify Configuration Files:
   Update the img_folder and ann_file in custom_detection.yml.
