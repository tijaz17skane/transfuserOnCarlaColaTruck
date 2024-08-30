# Follow These to Build Towards the task of running transfuser on Truck-Trailer
  1.  Turn on debugging
  2.  Change vehicle type
  3.  Fix path issues
  4.  Change sensor positions

## 1.  Turn on debugging

Edit the 'transfuser/team_code_transfuser/submission_agent.py'

Changed SAVE_PATH to, 'SAVE_PATH = os.environ.get('SAVE_PATH', '/home/tijp4b/transfuser/debugView')'

In the arguments of forward_ego, I set, 'debug=True'
