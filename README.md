# Robust Grasp Planning Over Uncertain Shape Completions

This repository includes code used in our work on [robust grasp planning over uncertain shape completions](https://arxiv.org/pdf/1903.00645.pdf). More specifically, all sub-modules used to run the simulated and real grasping experiment  

**Authors**: Jens Lundell\
**Maintainer**: Jens Lundell, jens.lundell@aalto.fi  
**Affiliation**: Intelligent Robotics Lab, Aalto University

## Getting Started

The code was developed for python2.7 and Ubuntu 18.04.

### Dependencies

[Graspit](https://github.com/aalto-intelligent-robotics/graspit.git) (You need to use our fork of Graspit! to make the code work.)\
[PyTorch](https://pytorch.org/)\
[Curvox](https://github.com/jsll/curvox)\
[binvox-rw-py](https://github.com/dimatura/binvox-rw-py)\
[python-pcl](https://github.com/strawlab/python-pcl)\
[Mesh_Reconstruction](https://github.com/CRLab/Mesh_Reconstruction)\
[ROS Melodic](http://wiki.ros.org/melodic)

### Sub modules

The code includes the following sub-modules that are automatically pulled in

* [graspit_commander](https://github.com/aalto-intelligent-robotics/graspit_commander)
* [graspit_interface](https://github.com/aalto-intelligent-robotics/graspit_interface)
* [graspit_msgs](https://github.com/CRLab/graspit_msgs)
* [grid_sample_plugin](https://github.com/aalto-intelligent-robotics/grid_sample_plugin)
* [shape_completion_network](https://github.com/aalto-intelligent-robotics/shape_completion_network)
* [point_cloud_segmentation](https://github.com/aalto-intelligent-robotics/point_cloud_segmentation)
* [Fast-3D-Pointcloud-Segmentation](https://github.com/fverdoja/Fast-3D-Pointcloud-Segmentation)

## ROS Installation

Clone or download the project from Github:

```
mkdir ws
cd ws
git clone --recursive git@github.com:aalto-intelligent-robotics/robust_grasp_planning_over_uncertain_shape_completions.git
catkin_make
```

## Simulation experiments

First of all, you need to download the ground-truth meshes and create some shape completed meshes. Ground-truth meshes can be downloaded from [here](https://drive.google.com/drive/u/1/folders/1ScywyPvZNoFzg8cn1i_gQ9OlYYe1lLg-) and for shape completed meshes you can either download some pre-generated ones [here](https://drive.google.com/drive/u/1/folders/128kbeCBe3W3leGJcV3fmtLMu35jHSPuD) or generate new ones as detailed [here](https://github.com/aalto-intelligent-robotics/shape_completion_network).

After you have these meshes, run

```
roslaunch graspit_interface graspit_interface.launch
```

and the following user interface will launch

![interface start](images/interface_start.png?raw=true "Interface start")

Next, click on the `Do Simulation Experiments button` and the following window will pop up

![Simulation experiments](images/simulation_experiments.png?raw=true "Simulation Experiments")

Then, click each of these buttons and give the appropriate path to the data. Once you are done, simply click on run. If everything goes as expected, you will see the following in the original GraspIt! window

GraspIt! is now generating and evaluating the grasps in the background and once it is done, it will save the results in the folder you specified earlier.

## Real-World experiments

Coming soon

# Citation

This repository contains code corresponding to our work on [robust grasp planning over uncertain shape completions](https://arxiv.org/pdf/1903.00645.pdf). If you use the code for your research, please cite

```
@article{lundell2019robust,
  title={Robust Grasp Planning Over Uncertain Shape Completions},
  author={Lundell, Jens and Verdoja, Francesco and Kyrki, Ville},
  journal={arXiv preprint arXiv:1903.00645},
  year={2019}
}

```

# License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
