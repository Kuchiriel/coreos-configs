## How to install?

If you are using [Digital Ocean](digitalocean.com/), just copy the content from the files and paste in the User Data field.

![](https://i.imgur.com/0X3jF5t.png)

If you have already installed CoreOS in a VM or Vagrant. This is the same as manually putting the files in: `/var/lib/coreos-install/user_data`

But if you want, you can use [wget](https://en.wikipedia.org/wiki/Wget) to download the [raw content](https://raw.githubusercontent.com/Kuchiriel/coreos-configs/master/docker-compose.cloud-config) from GitHub. 

Then, using a ssh shell, execute the following command: `sudo coreos-cloudinit --from-file` _your-file_`.cloud-config`

You can install direct from the URL as well: `sudo coreos-cloudinit --from-url https://github.com/Kuchiriel/coreos-configs/raw/master/`_your-file_`.cloud-config`

Every _.cloud-config_ file has some example commands:

![](https://i.imgur.com/ko9kUGu.png)


