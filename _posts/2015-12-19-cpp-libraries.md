---
title: C++ libraries for robotics projects
updated: 2015-09-06 15:56
---

Working on a robotics project means facing challenges in the software development part of the project, challenges that can be tackled effortless if you use the right tools for the right job. Some C++ libraries that I have used (and some that I haven't) are listed here, in order to be able to decide which library is the right one to use as your project's base.

* **[ROS](http://www.ros.org)**: is not exactly a library, is rather a component framework that works as a communication layer between these components. It provides functionalities for the integration of multiple systems. For instance, if you have a project with an arm, a gripper and a RGBD camera you can use ROS for the communication of these systems. You can have a node that controls the arm, a node that controls the gripper, a node that controls the camera, a node for running motion planning algorithms and asks for the poses of the objects from the node of the camera, etc...

* **[KDL](http://www.orocos.org/kdl)**: is a library providing powerful tools if you have to deal with tasks involving kinematics of chains, e.g. find the inverse kinematics or calculate the jacobian in real time).

* **[Drake](https://github.com/RobotLocomotion/drake/wiki)**:  is a collection of tools for analyzing the dynamics of robotic systems. Although, is mostly written in MATLAB.

* **[Odeint](http://headmyshoulder.github.io/odeint-v2/)**: a boost library for solving Ordinary Differential Equations (ODEs). Useful for evaluating complex controllers in your robot.

Linear algebra applications are prominent in robotics, computer vision etc. So the following are some of the most widely used libraries for linear algebra:

* **[Eigen](http://eigen.tuxfamily.org/index.php?title=Main_Page)**: is a library for linear algebra (metrices, vectors, numerical solvers etc).

* **[Armadillo](http://arma.sourceforge.net/)**: library for linear algebra. Its API is very similar to the MATLAB syntax.

I will try to keep this list up-to-date with new tools, or more information about their use.

