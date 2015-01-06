sinatra-script
==============

sinatraをSysVinitやらSystemdやらUpstartで動かすもの  

## Dependencies  

vagrant上でubutnu14.04を動くようにしておいて下さい。  

vagrant ssh で vagrant に login し  
`$ sudo apt-get install ruby`  
`$ sudo gem install sinatra`  
を実行し ruby と sinatra を installしておいて下さい。  

## Usage  

sinatra.sysvinit を /etc/init.d/sinatra にrenameして配置  
`sudo /etc/ini.d/sinatra start|stop|restart|status`  
  
sinatra.conf.upstart を /etc/init/sinatra.conf にrenameして配置  
`sudo initctl start|stop|restart|status sinatra`  
  
sinatra.service.systemd を /etc/systemd/system/sinatra.service にrenameして配置  
`sudo systemctl start|stop|restart|status sinatra`  
＊ubuntu14.0.4で systemd を動かす場合は package の install と grub の書き換えが必要（？）  
  
  
## Structure  
  
* sinatra.sysvinit  
* sinatra.conf.upstart  
* sinatra.service.systemd（気が向いたら）  
  
