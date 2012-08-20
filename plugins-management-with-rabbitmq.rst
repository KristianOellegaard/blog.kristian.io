Plugins (management) with RabbitMQ
##################################
:date: 2011-08-05 15:11
:category: Sysadm

Today i spent quite some time investigating why i could make the plugin
"management" run with RabbitMQ. I was running ubuntu 10.04 (LTS) and did
sudo apt-get install rabbitmq-server.

First of all, it was a mystery how to enable the plugins. There were no
default plugin directory existing, but thats solved by adding it
yourself. You can find your rabbitmq directory with whereis, e.g.
"whereis rabbitmq". Then you just create a folder called "plugins"
inside the folder called rabbitmq\_version, in my case:
/usr/lib/rabbitmq/lib/rabbitmq\_server-1.7.2/

In the above case, i didnt get it working, as the management interface
isn't compatible with 1.7.2, which is bundled with the LTS. So now I'm
investigating the possibility to upgrade it via their custom apt-get
repository available from their website.

However, the reason why im writing this, is that i spent a lot of time
not beeing able to enable the plugins.

You have to run a script inside the bin folder in /usr/lib/rabbitmq/ -
both for enabling and disabling plugins
