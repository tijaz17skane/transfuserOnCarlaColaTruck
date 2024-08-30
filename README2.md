# Follow These to Build Towards the task of running transfuser on Truck-Trailer
  1.  Turn on debugging
  2.  Change vehicle type
  3.  Fix path issues
  4.  Change sensor positions

## 1.  Turn on debugging

Edit the `transfuser/team_code_transfuser/submission_agent.py`

Changed SAVE_PATH to, `SAVE_PATH = os.environ.get('SAVE_PATH', '/home/tijp4b/transfuser/debugView')`

In the arguments of `forward_ego`, I set, `debug=True`


## 2.  Change Vehicle Model

Edit `leaderboard/leaderboard/scenarios/route_scenario_local.py` line 250 for vehicle model change.

change ego_vehicle attributes.

## 3.  Fix Carla ROOT and Work ROOT Path

Edit `leaderboard/scripts/local_evaluation.sh`, to fix path in line 1 and line 2

## 4.  Change Sensor Positions

In `team_code_transfuser/submission_agent.py`
go to line 122+
Look for

`'x': self.config.camera_pos[0], 'y': self.config.camera_pos[1], 'z':self.config.camera_pos[2]`
and so on for configs of the 3 cameras and

`'x': self.lidar_pos[0], 'y': self.lidar_pos[1], 'z': self.lidar_pos[2]`
for lidar configs.

Remember: x axis is along the vehicle, y is to the left, z is upwards.
