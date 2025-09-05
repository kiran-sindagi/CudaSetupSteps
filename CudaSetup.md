# STEPS FOR RUNNING MODELS ON GPU

## Links for installation

- https://visualstudio.microsoft.com/
- https://www.nvidia.com/en-us/drivers/
- https://developer.nvidia.com/cuda-toolkit
- https://developer.nvidia.com/cudnn-downloads?target_os=Windows&target_arch=x86_64&target_version=11&target_type=exe_local


## After Installation

- Copy all the files from this location

	```
		C:\Program Files\NVIDIA\CUDNN\v9.11\bin\12.9
	```

- And paste it here

	```
		C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.9\bin
	```

### Similarly

- Copy all the files from this location

	```
		C:\Program Files\NVIDIA\CUDNN\v9.11\include\12.9
	```

- And paste it here

	```
		C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.9\include
	```

### And again

- Copy all the files from this location

	```
		C:\Program Files\NVIDIA\CUDNN\v9.11\lib\12.9\x64
	```

- And paste it here

	```
		C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v12.9\lib\x64
	```

## Starting a project

#### Steps:
- Create a folder in your desired location
- Open the terminal and paste this command
	```
	python -m venv .v
	```
- Activate the virtual environment (AVOID USING POWERSHELL, USE COMMAND PROMPT/ GIT BASH TERMINAL INSTEAD)
	```
	cd .v/Scripts
	```
	```
	./activate
	```
	```
	cd ../..
	```

## Installing Libraries

- Go to https://pytorch.org/
- Select the appropriate options and download the torch library
- The command usually looks like this:
	```
	pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu129
	```
	
- After this you can go on and install the other required libraries using the command
- E.g
	
	```
	pip install numpy
	```

## To test 

					
	import torch
	print(torch.__version__)
	print(torch.cuda.is_available())
	print(torch.version.cuda)

#### The above code should produce this type of output

```
2.8.0+cu129
True
12.9

```
