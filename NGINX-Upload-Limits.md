# NGINX Upload Limits

Sometimes NGINX likes to error out when uploading large images to websites. There is an easy fix to this, simply follow the guide below:

## Step 1
Navigate to your NGINX Config File, it should be something like this: `/etc/nginx/nginx.conf`



## Step 2
Add the below line to your config file:

`client_max_body_size 10000M;`

Which should lead your config file to look something similar to this:

![example](https://cdn.discordapp.com/attachments/764688949586821151/1551245055493275658/7GiLm5e.png?ex=6ab14509&is=6aaff389&hm=7b6f9d57bf452e9f03aac1b8daf76e67a59af6c484ca16db79343f7ca13bdfdb&)

## Step 3
Restart NGINX to enable your changes with this command: `sudo systemctl restart nginx`
