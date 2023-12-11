To install RCTComms, perform the following:
1. Navigate to the base directory of your local copy of the repo (`cd path/to/directory/radio_collar_tracker_comms`)
2. Activate your environment, if installing to one (for example, `conda activate rctGCS`)
3. Run `python -m pip install .`
	1. Do not forget the . at the end, as it indicates that you want to install from the current directory, `radio_collar_tracker_comms`
	2. This will run `setup.py`, which handles other dependencies for you

Note that, if you're making changes to comms, and importing to another module using `import RCTComms`, you'll need to reinstall using these steps to reflect your new changes. Imports from RCTComms will use the most recent installation, not whatever is currently in memory in the code files. 
