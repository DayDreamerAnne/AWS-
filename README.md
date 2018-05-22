# AWS-
Start a jupyter notebook on AWS EC2 instance

Step 1: SSH to your EC2 instance.
  ssh -i myPemFile.pem ec2-user@ec2-35-183-5-235.ca-central-1.compute.amazonaws.com

Step 2:Install Anaconda on EC2. 
  
  1)wget https://repo.continuum.io/archive/Anaconda2-4.1.1-Linux-x86_64.sh
  
  2)bash /path/of/the/sh/file/https://repo.continuum.io/archive/Anaconda2-4.1.1-Linux-x86_64.sh
  
  3)source .bashrc
  
  4) try anaconda: conda list

Step 3: jupyter notebook --no-browser --port=8888

Step 4: SSH to Jupyter Notebook Server
  
  ssh -i myPemFile.pem -L 8000:localhost:8888 ec2-user@ec2-35-183-5-235.ca-central-1.compute.amazonaws.com

Step 5: Open local broser and go to localhost:8000
