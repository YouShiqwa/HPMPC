# HPMPC: Robotic Imitation Learning via Hybrid Perception Model
This is the Official PyTorch implementation of "HPMPC: Robotic Imitation Learning via Hybrid Perception Model"  
Our code is coming soon!  
# Architecture 
![image](https://github.com/YouShiqwa/HPMPC/blob/main/pic/1.png)
# Environment
Make sure you have the following dependencies installed:
* Pytorch>=2.0.1
* Numpy
* CUDA>=11.7
# Demo
This is a demo of our work！  
![demo of our work](https://github.com/YouShiqwa/HPMPC/blob/main/video_gif.gif)
# DataSets
You can generate the dataset for training using the following statement：  
```
python3 record_sim_episodes.py \
    --task_name sim_transfer_cube_scripted \
    --dataset_dir <data save dir> \
    --num_episodes 100
```
To can add the flag --onscreen_render to see real-time rendering. To visualize the episode after it is collected, run  
```
python3 visualize_episodes.py --dataset_dir <data save dir> --episode_idx 0
```
# Simulated experiments
To train HPMPC:  
```
python -u imitate_episodes_v2.py  \
--gpu 0 \
--ckpt_dir <ckpt dir> \
--task_name "sim_transfer_cube_scripted" 
```
If you want to evaluate the training results，run  
```
--gpu 0 \
--ckpt_dir <ckpt dir> \
--task_name "sim_transfer_cube_scripted"  --eval
```
To enable temporal ensembling, add flag ```--temporal_agg```.



