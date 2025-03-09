# LBA-Net
Lightweight Band-Adaptive Hyperspectral Image Compression with Feature Decouple and Recurrent Model

## Dataset Preparation and Model Training Instructions

### 1. Dataset Preparation
1. Download the dataset from the link provided in our paper.
2. Process the dataset following the method described by Guo et al. [1].
3. Convert the processed data into `.txt` format.
4. Split the dataset into training and testing sets.
5. Ensure that both the processed data and the `.txt` files for the training and testing sets are placed in the same directory (e.g., `total_data`).

### 2. Updating Paths
1. Modify `root_dir = ""` in `dataset.py` to the path of the `total_data` directory.
2. Create three directories to store logs, test results, and model checkpoints:
   - `out_dir_train` (for training logs)
   - `out_dir_test` (for test results)
   - `checkpoint_dir` (for model weights)
3. Set `train_path` and `test_path` in the `train.py` command to the paths of the prepared training and testing sets.
4. Configure the lambda value according to the instructions in our paper.

### 3. Running the Training Script
1. Use the `cd` command to navigate to the project directory.
2. Run the following command in the terminal:

   ```sh
   python train.py


[1] Guo, Y., Tao, Y., Chong, Y., Pan, S., & Liu, M. (2023). "Edge-Guided Hyperspectral Image Compression With Interactive Dual Attention." IEEE Transactions on Geoscience and Remote Sensing, vol. 61, pp. 1-17.
DOI: 10.1109/TGRS.2022.3233375.
