Here are the compatibility issues and challenges in running transfuser on Truck-Trailer in CARLA:


1.  The truck-trailer model was built with carla 0.9.13 and unreal engine 4.26. https://github.com/frankeng/CarlaSemiTruckTrailer
2.  The transfuser code is written for carla 0.9.10.1 and for leaderboard 1.0. https://github.com/autonomousvision/transfuser/issues/218.
3.  When trying to edit uasset files in carla 0.9.10.1 using a newer version of unreal engine,UE says .uasset too old.  
4.  They upgraded to unreal engine 4.26 in carla 0.9.12, and I could not find an older version of unreal engine elsewhere. I wanted to use the fbx in unreal to generate a model in unreal engine < 4.26, one that would be compatible with carla 0.9.10.1. But didn't find any.



