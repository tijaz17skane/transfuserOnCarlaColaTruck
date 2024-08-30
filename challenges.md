
## Compatibility Issues and Challenges in running transfuser on Truck-Trailer in CARLA:

1.  Transfuser code was written for CARLA 0.9.10.1, hence the codebase is compatible with this version of CARLA only (if you use it out of the box). Refer to this link for more: https://github.com/autonomousvision/transfuser/issues/218.
2.  I found CARLA 0.9.10.1 to crash much less than CARLA 0.9.12 and 0.9.13.
3.  Transfuser was made to work with Carla leaderboard 1.0, and the evaluation code runs on a route similar to the longest6 route provided by CARLA leaderboard.
4.  Each CARLA version comes with a compatible Scenario Runner, which can be downloaded from: https://github.com/carla-simulator/scenario_runner
5.  The way CARLA responds to different queries is slightly different in all versions, which is why we get these compatibility issues. (e.g. upon inquiring for town01, CARLA 0.9.10.1 return TOWN01, whereas CARLA 0.9.13 returns carla/towns/town01)
6.  The Truck-Trailer model was built with carla 0.9.13 and unreal engine 4.26. https://github.com/frankeng/CarlaSemiTruckTrailer 

8.  When trying to edit uasset files in carla 0.9.10.1 using a newer version of unreal engine (4.26+), UE says .uasset too old.  
9.  They upgraded to unreal engine 4.26 in carla 0.9.12, and I could not find an older version of unreal engine elsewhere. I wanted to use the fbx in unreal to generate a model in unreal engine < 4.26, one that would be compatible with carla 0.9.10.1. But didn't find any.


## The Way Forward:

1.  Fix the compatibility issues outside of docker
2.  Put the edited transfuser code, scenario runner and carla files in the docker container Oscar created.
3.  Run transfuser on Truck-Trailer inside the docker container. 



