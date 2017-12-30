## What is this?

This is some tested _.cloud-config_ files I made to make managing [CoreOS](https://coreos.com/why/) less cryptic.

## How to install?

If you are using [Digital Ocean](https://www.digitalocean.com/products/), just copy the content from the files and paste in the _User Data_ field.

![](https://i.imgur.com/0X3jF5t.png)

If you have already installed CoreOS in a VM or Vagrant. This is the same as manually putting the files in: `/var/lib/coreos-install/user_data` before installation.

But if you want, you can use [wget](https://en.wikipedia.org/wiki/Wget) or [curl](https://pt.wikipedia.org/wiki/Curl_(Unix)) to download the [raw content](https://raw.githubusercontent.com/Kuchiriel/coreos-configs/master/docker-compose.cloud-config) from GitHub.

Then, using a ssh shell (supposing you are running through a VPS), execute the following command: `sudo coreos-cloudinit --from-file` _your-file_`.cloud-config`, otherwise just use a vanilla terminal instead.

You can install direct from the URL as well: `sudo coreos-cloudinit --from-url https://github.com/Kuchiriel/coreos-configs/raw/master/`_your-file_`.cloud-config`

Every _.cloud-config_ file in this repository has some example commands approaching different ways to install, which you can just copy and paste in the terminal:

![](https://i.imgur.com/ko9kUGu.png)

## Which ones are available now?

By now, the following files are available:

### [docker-compose](https://github.com/Kuchiriel/coreos-configs/blob/master/docker-compose.cloud-config)
Installs docker-compose.

| CoreOS Version | Working? |
| :------------: | :------: |
| [1478.0.0 (alpha)](https://coreos.com/releases/#1478.0.0) | Yes |
| [1465.2.0 (beta)](https://coreos.com/releases/#1465.2.0)  | No  |
| [1409.7.0 (stable)](https://coreos.com/releases/#1409.7.0)| No  |

If you want to make docker-compose work with previous versions of CoreOS, you need to edit this selected part of the file. It will alllow you to download an appropriate version of docker-compose which's target the compatible version of docker engine.

![](https://i.imgur.com/JZbKTnE.png)

[See this](https://github.com/docker/compose/releases) for more details on how to do this.

# Security

Piping commands from internet to shell is considered bad practice, 
and there is lot of discussion on the internet:

* [Hacker News Discussion](https://news.ycombinator.com/item?id=12766049)
* [Don't Pipe to your Shell](https://www.seancassidy.me/dont-pipe-to-your-shell.html)
* [The Truth About Curl and Installing Software Securely on Linux](https://medium.com/@esotericmeans/the-truth-about-curl-and-installing-software-securely-on-linux-63cd12e7befd)

But this was done anyway because of the convenience factor (there is no way to be more straightforward than this),
please, feel free to review and open an Issue.

This security tip was given to me by a friend after I saw his repo of termux tools.
https://github.com/onlurking/termux

<a target='_blank' rel='nofollow' href='https://app.codesponsor.io/link/fs3bBt7nP9jn4VLgZERmuNMy/Kuchiriel/coreos-configs'>
  <img alt='Sponsor' width='888' height='68' src='https://app.codesponsor.io/embed/fs3bBt7nP9jn4VLgZERmuNMy/Kuchiriel/coreos-configs.svg' />
</a>
