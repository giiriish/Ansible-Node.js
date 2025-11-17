🚀 Deploy Node.js Application on AWS EC2 Using Ansible

steps:

🛠 Step 1 — Configure AWS EC2

Create an EC2 instance (Ubuntu 22.04 recommended) and make sure it has a public IP.



🔧 Open Port 3000 in Security Group


Go to:

AWS Console → EC2 → Instances → Security → Security Groups → Inbound Rules

Add a rule:


Type	            Port	        Source     
Custom TCP	      3000	       0.0.0.0/0


Commamnds for ec2 connect to playbooks:


step 2 : check your ec2 connect to keypiar - ssh -i /home/girish/aws-2/my-key-2.pem ubuntu@13.201.173.250


Now run the ping test:

ansible -i inventory.ini ec2 -m ping


▶️ Step 7 — Run the Deployment

Use the following command:

ansible-playbook -i inventory.ini playbook.yml


<img width="1616" height="715" alt="Screenshot 2025-11-17 165026" src="https://github.com/user-attachments/assets/777f1004-2f20-4f0a-b27e-d82ba21c3605" />


Final step : Check for run successfully nodejs application on aws ec2 server


open browser:  http://<EC2_Public-ip>node port  ---------->  http://13.201.173.250:3000



<img width="1719" height="489" alt="Screenshot 2025-11-17 164720" src="https://github.com/user-attachments/assets/e4eaa32b-2933-4517-bdfd-13cf9b94e3c6" />
