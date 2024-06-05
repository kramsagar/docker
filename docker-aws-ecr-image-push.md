https://www.youtube.com/watch?v=-8_r28jJ6AM

https://www.youtube.com/watch?v=t0TXPCwcg3I

1. download aws cli to linux
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

2. configure aws

root@ram-node1:~/ecr# aws configure
AWS Access Key ID [None]: AKIATCKANPIY6FGFERAK
AWS Secret Access Key [None]: 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
Default region name [None]: us-east-1
Default output format [None]: 
root@ram-node1:~/ecr# 

3. create one IAM user and add container register access policy to it.
![alt text](image-1.png)

4. create repo in ECR
![alt text](image-2.png)


5. view push commands in ecr cloud
![alt text](image-3.png)

6. Retrieve an authentication token and authenticate your Docker client to your registry. Use the AWS CLI:

![alt text](image-4.png)

7. Build your Docker image using the following command. 

root@ram-node1:~/flask-proj/awesome-compose/flask/app# docker build -t msapps .


8. Build your Docker image using the following command.  and tag it with remote repo and host.

docker tag msapps:latest 211125369393.dkr.ecr.us-east-1.amazonaws.com/msapps:latest
![alt text](image-5.png)

9. Run the following command to push this image to your newly created AWS repository:

docker push 211125369393.dkr.ecr.us-east-1.amazonaws.com/msapps:latest










