Dev setup for Node.js with MongoDB. Based on VirtualBox, Ubuntu 12.04, Vagrant and Chef

## Literature & Pre-requisite
Please go thru the following links and setup these tools before proceeding
  * [VirtualBox from Oracle](http://virtualbox.org)
  * [Vagrant](http://vagrantup.com)

## Setup
```bash
vagrant box add precise64 http://files.vagrantup.com/precise64.box
git clone https://github.com/truepattern/nodejs-dev-vbox.git mynodejs
cd mynodejs
vagrant up
```

### Packages
Following softwares are installed to the vbox
  * git
  * nodejs
  * nginx
  * mongodb

### Console
  * vagrant ssh 

### Start
  * vagrant up
  
### Stop
  * vagrant halt

### Node.js App
  * The sample app is in 'app' directory 
  * ssh to virtualbox
  
```bash
# node is automatically started by upstart and should be running already
ps -aef | grep node
```

  * go to your host box, browser and try http://localhost:8080
  * nginx runs on port 80 and forwards the site to port 3000 where app runs


## Notes
You can use this to bootstrap your node development, or copy the cookbooks and Vagrantfile to your existing node.js setup

## License & References
  * Please refer to the cookbooks for their respective licenses (mostly Apache). 
  * http://blog.semmy.me/post/17222183802/node-js-getting-started-with-vagrant
  * https://github.com/opscode-cookbooks
