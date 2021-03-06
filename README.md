# Vagrant Sensu Development VM

## About

This vagrant configuration will boot up a working [Sensu](https://github.com/sensu/sensu) server to facilities development/testing.

## Requirements

  * [Vagrant](http://www.vagrantup.com/) - Recommended version 1.4.X
  * [VirtualBox](https://www.virtualbox.org/) - Recommended version 4.3.X
  * Internet access :))

## Installation

Boot image
<pre>
$ git clone https://github.com/ruben-nieva/vagrant-sensu.git 
$ cd vagrant-sensu
$ vagrant up
</pre>

`Note:` server IP is predefined with 10.170.0.2

Start the services you need

<pre>
$ vagrant ssh
$ service sensu-server start
$ service sensu-api start
$ service sensu-client start
$ service uchiwa start
</pre>

For example to access the Uchiwa dashboard open
http://10.170.0.2:3000/ in a browser.

## License

Apache License Version 2.0
