# Use the human voice website template

## How it works

This site is completely static and only uses HTML and CSS. It depends on copy & paste and is inspired by the [manual until it hurts](https://indieweb.org/manual_until_it_hurts)  developement practice.

## Using this website as a template for your own

This website is free and open source. You are welcome to use it and customize it however you wish.

## Deploying the website to your server

It is up to you how you deploy your site but here is one method you could use in case you are curious...

If you have a server with SSH enabled you can use the following [rsync](https://en.wikipedia.org/wiki/Rsync) command to upload the site to the appropriate directory on your server. You will need to replace the folder path and server IP address with the info for your specific server. Make sure to run this command inside your site folder!

```
rsync -avP $(pwd)/ username@XXX.XXX.XXX.XXX:/var/www/youwebsite.net/ --exclude={'.DS_Store','.vscode','README.md'} --chmod=Du=rwx,Dgo=rx,Fu=rw,Fog=r --delete
```

username = SSH username on your server
XXX.XXX.XXX.XXX = Your servers IP address
--exclude={'.DS_Store','.vscode','README.md'} = directories and files you want to exclude from the live site

## About

This website template was created by Elliott Cost for Giles Turnbull's company, [Use the human voice](https://www.usethehumanvoice.com/). Giles suggested that we open source the template for others to use.