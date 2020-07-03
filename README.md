# Super Kitty Piano (Pink Sky) 

#### This project is for A/B testing purpose. Go to the original project https://github.com/CloudemyTV/super-kitty-piano

This is the Super Kitty Piano - Pink Sky version created by our cat at Clooudemy. 

We often demo this website as class material in Cloudemy online classes, and occasionally play it in the parties.

For grandmasters like you, this is your new world-class instrument. 

You can play [Super Kitty Piano](http://superkittypiano.com)  at superkittypiano.com


![Super Kitty](/images/super-kitty.gif)


#### Super Kitty Piano - Copyright 2020 Cloudemy.tv



### Note:

The sound of kitty piano is generated using Web Audio API.

Go to: https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API for more details.

The Super Kitty Piano works on most recent browsers (not IE). We recommend you to play it on Firefox or Chrome.



## Option 1: Deploy to AWS EC2 using user data.

Copy & paste the Shell Script below onto the EC2 User Data, when you launch an EC2 instance. EC2 will automatically run commands and deploy the Super Kitty Piano website during launch:

    #!/bin/bash
    yum update -y
    yum install git -y
    yum install httpd -y
    systemctl start httpd
    systemctl enable httpd
    git clone https://github.com/CloudemyTV/super-kitty-piano-pink-sky.git /var/www/html/
    
