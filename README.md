- clovis-sample-apps

There are three sample applications. A running instance of Mero such as singlenode Mero is a prerequisite for compiling, building and running these Clovis applications. 
1. c0cp
2. c0cat
3. c0del

- install build dependencies
>> sudo ./install-build-deps

- compile, build and run applications
>> make
>> make test

- clean
>> make clean

- Clean install mero
The clean install mero script stops currently running m0singlenode, uninstall mero and mero-devel packages, removes all configuration and storage disks. It then installs the new version pointed by directory path, configuraes it as a m0singlenode and starts services.
>> ./clean_install_mero
illegal number of parameters
clean_install_mero <rpms directory path>
>> ./clean_install_mero ./rpms/jenkins-OSAINT_mero-1400-29-g7a51cbd/

- clovis apps resource file <.cappsrc>
Clovis applications require a .cappsrc file residing in the same directory where the application is executed. This resource file contains all clovis related resource parameters for running a clovis application on that particular client machine. The this file can be generated using the cappsrcgen utility.
>>./cappsrcgen > .cappsrc
[sudo] password for seagate: 
>>cat .cappsrc
10.0.2.15@tcp:12345:44:101
10.0.2.15@tcp:12345:45:1
<0x7000000000000001:0>
<0x7200000000000000:0>
/tmp/
