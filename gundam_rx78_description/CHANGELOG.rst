^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package gundam_rx78_description
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.2 (2020-01-20)
------------------
* Add more examples by @Naoki-Hiraoka (`#6 <https://github.com/gundam-global-challenge/gundam_robot/issues/6>`_)

  * fix some parameters
  * use mesh for collision
  * update mesh collada model with Naoki-Hiraoka:simplify-urdf
  * Simplify URDF (simplify, scale and mergenode collada)
    - calculate mass property from convex_hull
    - fix check_position, now base_link is the center of foot

* Contributors: Kei Okada, Naoki Hiraoka

0.0.1 (2019-07-01)
------------------
* Add gundam RX-79 Description (`#1 <https://github.com/gundam-global-challenge/gundam_robot/issues/1>`_)

  * respect @Naoki-Hiraoka 's dynamics parameters on urdf (mu2/kp/kd...) https://github.com/Naoki-Hiraoka/gundam_robot/tree/gundam-walk
  * respect @Naoki-Hiraoka 's dynamics parameters  https://github.com/Naoki-Hiraoka/gundam_robot/tree/gundam-walk
  * quick hack for urdfdom_py 0.4.0
    Once https://github.com/ros/urdf_parser_py/pull/47 is merged, we can remove this block
  * pip8ify python files
  * add roslint check
  * update GGC_TestModel_rx78_20170112.urdf and gundam_rx78_control.yaml with latest ggc_dae_to_urdf.py
  * add write_mesh option, by default we do not write meshes/ files
  * update gazebo tag generation, fix legacyModeNS warning and use gundam_rx78_control/JointTrajectoryController
  * update GGC_TestModel_rx78_20170112.urdf and gundam_rx78_control.yaml with latest ggc_dae_to_urdf.py
  * add joint trajectory controllers settings for control.yaml
  * ggc_dae_to_urdf.py, set ankle back  as a fixed joint, due to mimic joint instability
  * update GGC_TestModel_rx78_20170112.urdf and gundam_rx78_control.yaml with latest ggc_dae_to_urdf.py
  * use effort controller as default
  * remove unused section
  * mimic_joint_plugin is no longer used, use updated version of effort controller
  * use default_pid for control.yaml
  * update control.yaml format for updated effort_controller, whcih supports mimic joints
  * update link CoM, center of mass and joint axis need displacement
  * increase wight(density) for crotch_p link
  * add back sole to footprint gazebo tag
  * set cover_pid for crotch covers, fix mimic_multiplier for side cover
  * calc_inertia : set origin of inertial
  * calc_inertia : increase minimum mass to 50
  * calc_inertia : add dnesity options
  * too small weight cause vibration on hand/fingers
  * update pid param of effort controller for each joints
  * small size/mass link make gazebo unstable, so add dummy collision shape
  * add only parent and child links
  * increase default effort/velocity
  * add mesh and urdf generated from GGC_TestModel_rx78_20170112
  * commit 2019/03/06 pinned & position controller version

* Contributors: Kei Okada, Naoki Hiraoka
