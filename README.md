## PROGRAMMING ASSIGNMENT : VERIFICATION OF CACHE COHERENCE IN FUTURBUS+ PROTOCOL

### Initial Setup & Steps

Initially clone the repository and go to the code ```main``` directory and execute the following two command to start the docker instances (make sure docker is already installed in your computer and started; [check here](https://docs.docker.com/get-docker/) for installation steps of docker.

```docker-compose build```

```docker-compose run ubuntu bash```


#### VERIFICATION OF FUTUREBUS+ PROTOCOL USING MURPHI3.1

To do the verification, go to the bash shell and follow the steps shown below,

* First go to the directory ```Murphi3.1/src``` and compile the Murphi using ```make``` command (if it not already generated). And optionally make the executable access using the command ```chmod +x Murphi3.1/src/mu```, if you in the home directory.
* Then go to the directory ```verification``` and obtain the C file for the Futurebus+ verification using ```./../Murphi3.1/src/mu futurebus.m``` command (if it not already generated). This will generate the C file ```futurebus.C```. 
* Thereafter compile the generate file using the command ```make futurebus```, this eventually generate the executable program.
* Finally run the executable using the following command ```./futurebus```.

**OR***
you can perform these entire steps by simply go to the ```verification``` directory and run the command ```sh run.sh```.

#### VERIFICATION OF FUTUREBUS+ PROTOCOL WITH THE FIX USING MURPHI3.1

I have implemented the fixing for futurebus+ protocol, to check that,

* First go to the directory ```verification``` and obtain the C file for the Futurebus+ verification using ```./../Murphi3.1/src/mu futurebus_fix.m``` command (if it not already generated). This will generate the C file ```futurebus_fix.C```. 
* Thereafter compile the generate file using the command ```make futurebus_fix```, this eventually generate the executable program.
* Finally run the executable using the following command ```./futurebus_fix```.

**OR***
you can perform these entire steps by simply go to the ```verification``` directory and run the command ```sh run_fix.sh```.
