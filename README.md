If you are using [Digital Ocean](digitalocean.com/), just copy the content from the files and paste in the **User Data** field.

![](https://i.imgur.com/P4Z3up0.png)

This is the same as manually putting it in 
`/var/lib/coreos-install/user_data`

But if you want, you can use [wget](https://en.wikipedia.org/wiki/Wget) to download the [raw content](https://raw.githubusercontent.com/Kuchiriel/coreos-configs/master/docker-compose.cloud-config) from GitHub. Then, using **ssh** shell, execute the following commands. Each one located in the respective file with correct file names.

![](https://i.imgur.com/ED7rtHz.png)


