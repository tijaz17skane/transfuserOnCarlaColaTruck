In team_code_transfuser/submission_agent.py

go to line 122+

Look for 

'x': self.config.camera_pos[0], 'y': self.config.camera_pos[1], 'z':self.config.camera_pos[2],

and so on for configs of the 3 cameras and 

'x': self.lidar_pos[0], 'y': self.lidar_pos[1], 'z': self.lidar_pos[2],

for lidar configs.

Remember: x axis is along the vehicle, y is to the left, z is upwards.
