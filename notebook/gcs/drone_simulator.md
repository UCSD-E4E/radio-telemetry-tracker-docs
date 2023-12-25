# Drone Simulator

Our drone sim is meant to help test the GCS without having to connect to our physical system in Sealab. If the on-board computer (OBC) is not on or you are not explicitly testing the GCS's connection to the system, you may use this simulator to test. To do so, follow these steps:

1. Run gcs and set mode to drone/tower as needed
2. If in tower mode:
	1. Set up connection on GCS (click on System: No Connection > Connection Settings and specify connector)
	2. Run sim using `ipython -I droneSimulator.py -- --protocol tcp` (optionally, specify number of clients by adding `--clients x`, where x is the number of clients with which you want to test)
	3. Start sim using `sim.start()`
3. If in drone mode:
	1. Run sim using `ipython -I droneSimulator.py -- --protocol tcp`
	2. Start sim using `sim.start()`
	3. Set up connection on GCS (click on System: No Connection > Connection Settings and specify connector)
4. Run any tests; as a simple test to start, I'd recommend:
	1. Open map on GCS UI and zoom in on the U.S. > Southern California > La Jolla > UCSD > Warren
	2. Run `sim.do_mission()` and ensure simulated flight appears on map (should be a triangular path near Warren)
5. Stop sims with `sim.stop()`
