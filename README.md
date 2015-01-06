sinatra-script
==============
  
sinatraをSysVinitやらSystemdやらUpstartで動かすsample    
  
## Dependencies  
  
vagrant で ubutnu14.04 が動くようにしておいて下さい。  

## Usage  
  
1. repository の取得  
`git clone git@github.com:k-shin/sinatra-script.git`  
  
2. vagrant の起動   
`cd sinatra-script && vagrant up`  
  
3. sinatra の 起動  
`vagrant ssh`  
*SysVinit*  
`sudo /etc/ini.d/sinatra start|stop|restart|status`  
*Upstart*  
`sudo initctl start|stop|restart|status sinatra`  
*Systemd*  
`sudo systemctl start|stop|restart|status sinatra.service`  
＊ubuntu14.0.4では systemd は動かない模様？  
  
  
## Structure  
  
* sinatra.yml  
* sinatra.sysvinit  
* sinatra.conf.upstart  
* sinatra.service.systemd(？)  
* hello.rb  
* Vagrantfile  
