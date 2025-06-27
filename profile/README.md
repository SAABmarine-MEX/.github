# SAABmarine-MEX
<!-- ## *Deep Reinforcement Learning and Residual Dynamic Modelling with ROS2 integration for BlueROV2* -->
## *Reducing the sim-to-real gap of a BlueROV2*

<img src="../real_mocap_sim.gif"/>

This gif shows the setup that have enabled this whole project. Underwater mocap system (buttom left video), SMaRC's water tank at KTH (middle video) and simulation of the BlueROV2 ( buttom right video). With this setup, we are able to capture the real BlueROV2's exact motion and compare it against the simulated one. 

Being able to measure the sim-to-real gap, this project explores a solution to reduce this gap, **Residual Dymamics Modelling**, by learning the residual. This method seeks to increase the realism of the simulation of the BlueROV2 while emphazaing computational efficiency to ensure real-time simulation capability.

This is then used for training a **Deep Reinforcement Learning** control policy with the purpose of enabling better sim-to-real transfer than the nominal simulation.

## Implementation

The implementation of this work can be divded into four main parts:

* ROS2
  * ROS2 based Ground Control Station (GCS) using Mavros for the BlueROV2
  * Repo: [saabmarineMEX_ros2](https://github.com/SAABmarine-MEX/saabmarineMEX_ros2)
* Simulation
  * BlueROV2 Unity-based simulation in SMaRCSim
  * Repos: [SMARCUnityStandardRL](https://github.com/SAABmarine-MEX/SMARCUnityStandardRL), [SMARCUnityAssetsRL](https://github.com/SAABmarine-MEX/SMARCUnityAssetsRL) (both required, check respective readme for installation guide) 
* Residual Dynamic Modelling
  * Training and inference pipeline for enhancing the realism of simulated BlueROV2 dynamics
  * Repo: [saabmarineMEX_learning](https://github.com/SAABmarine-MEX/DRL-Python)
* Deep Reinforcement Learning
  * Training and ROS2 inference pipeline for Deep Rienforcement Learning (DRL) control policy of BlueROV2
  * Repos:
    * Training: [saabmarineMEX_learning](https://github.com/SAABmarine-MEX/DRL-Python)
    * Inference: [saabmarineMEX_ros2](https://github.com/SAABmarine-MEX/saabmarineMEX_ros2)

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
