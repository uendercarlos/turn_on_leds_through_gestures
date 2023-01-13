<h1 align="center">:file_cabinet: Classification project to turn on leds through gestures</h1>

## :memo: Description
The objective of this project is to demonstrate the physical control of components through gestures.

## :books: Project features
* <b>Feature 1</b>: Light up LEDs according to the number of fingers presented to the camera.

## :wrench: Technologies used
* Tecnologia; 
* Jetson nano;
* Python;
* GPIO;
* JupyterLab;
* Docker;
* Container;
* Pytorch.


## :rocket: Startup
Initialization will be done through Docker that is installed in the JetPack package of jetson nano. It is necessary to connect a windows notebook to the jetson nano through the network, remembering that both must be on the same network.

On the notebook with Windows, open a PowerShell window in administrator mode.

Connect to the Jetson Nano using the ssh protocol with the following command:
```
<ssh <username_jetsonnano>@<ip_jetsonnano>>
```
Example:
```
<ssh uender@192.168.1.8>

When inside jetson nano via terminal, create a file and run this file after initializing the container:

# create a reusable script
echo "sudo docker run --runtime nvidia -it --rm --network host --privileged\
    --volume ~/nvdli-data:/nvdli-nano/data \
    --device /dev/video0 \
    nvcr.io/nvidia/dli/dli-nano-ai:v2.0.2-r32.7.1" > docker_dli_run.sh

# make the script executable
<chmod +x docker_dli_run.sh>


# run the script
<./docker_dli_run.sh>

After initializing the container, open the browser and type the jetson nano ip followed by a colon and 8888. Example:

<192.168.1.8:8888>

Once this is done, you will be inside JupyterLab.
```
## :soon: Future Implementations
* The next implementations of this project will be to control machines through real-time camera images.



## :dart: Project Status
* Concluded