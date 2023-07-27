# LinuxWorks
linux tasks and projects repo

Install Kernel Headers on linux system:
#yum install kernel-devel kernel-headers -y

Install the git software first then 
#yum install git -y

Clone LiME from GitHub: Download and compile the LiME source code:
#git clone https://github.com/504ensicsLabs/LiME.git 

Go to src directory 
#cd LiME/src 

Compile the src code 
#make


Load LiME Kernel Object: Load the LiME kernel object to initiate RAM data dumping:

#insmod ./lime-6.1.38-59.109.amzn2.x86_64.ko "path=./ramdata.mem format=raw"

Note: Replace the file name "lime-4.14.198–152.320.amzn2.x86_64.ko" with the actual kernel object generated during compilation.

Verify RAM Data: Confirm that the desired data resides in RAM by using the following command:

#cat ramdata.mem | strings | grep "chaitanya"

This example looks for the string and integer values for "chaitanya" and "checkcode" variables in the RAM data .
