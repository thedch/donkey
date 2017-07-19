# Donkey: a self driving library and control platform for small scale DIY vehicles.

Donkey is minimalist and modular self driving library written in Python. It is developed for hobbiests with a focus on allowing fast experimentation and easy community contributions.  

---------------------------
**REFACTOR IN PROGRESS**

*We've learned a lot in the past couple months and working to implement many of those changes in a new version Donkey 2.1. This version will make it easy for users to contribe new pilots, sensors, controllers, and actuators rather than needing to rewrite the the whole code base. This new ROS'ish version lives in the [dev branch](https://github.com/wroscoe/donkey/tree/dev) and will be merged into master on July 16th. All the hardware in the standard build will be supported and most of the funcationality for driving/training will remain.*


---------------------------


### [Build a Donkey Car.](http://www.donkeycar.com) ($200 + 2 hours)

#### Use Donkey if you want to:
* Make an RC car drive its self.
* Compete in self driving races like [DIY Robocars](diyrobocars.com)
* Use existing autopilots to drive your car.
* Use community datasets to create, improve and test autopilots that other people can use.  


#### Features:
* Data logging of image, steering angle, & throttle outputs.
* Wifi car controls (a virtual joystic).
* Community contributed driving data and autopilots.
* Hardware CAD designs for optional upgrades.


### Drive your car
Once you have built your car and it's connected to the same wifi as your computer.

1. Open a terminal and clone the donkey repo: `git clone https://github.com/wroscoe/donkey`
1. Start the default pilot server using docker: `bash start-server.sh`
1. Open a new terminal and find your car's Raspberry Pi's IP address: `python scripts/find_car.py`
1. SSH to your car's Raspberry Pi: `ssh pi@<your pi's ip address>` (default password = raspberry)
1. Clone the donkey repo on the Pi: `git clone https://github.com/wroscoe/donkey`
1. Start your car's driver loop: `python scripts/drive.py  --remote http://<your computers ip address>:8887`
1. Turn on your car.
1. Go to `<your_pilot_server_ip>:8887` on your phone or computer to start driving your car.
