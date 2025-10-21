# P2P-VTON
# Environment
## Run the following code to install the runtime environment.
```
conda env create -f environment/environment.yaml
conda activate p2p_vton
```
## Note: Torch 1.11.0 corresponds to CUDA version 11.3. If you cannot run Torch 1.11.0 after direct installation, try installing torch 1.11.0+cu113 instead.
```
pip install torch==1.11.0+cu113
```
# Input
Place the input clothing image and person image in ```input_directory/images```, and name them ```R``` and ```T``` respectively. Place their corresponding mask images in ```input_directory/masks```, and also name them ```R``` and ```T```.
# Inference
```
python main.py \
--data.input_dir ./input_directory \
--data.output_dir ./out \
--data.device 0 \
--data.save_stg1_debug_image False \
--mea.mea_scale 15.0 \
--mea.mea_enhance 1.25 \
```
## The running results can be found in ```out/stg_2```
