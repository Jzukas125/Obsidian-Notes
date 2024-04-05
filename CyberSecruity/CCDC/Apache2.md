#CCDC 
	To start apache we need to do 'sudo service apache2 start'

Installing a ddos rule in apache2 server
	make sure to update	
	Installing the service which is fail2ban 'sudo apt-get install fail2ban'
	Writing the rules for a new file called jail.local use 'sudo vim etc/fail2ban/jail.local'
	Add the following rules:

apache-ddos]
		enabled = true
		port = http,https
		filter = apache-ddos
		logpath = /var/log/apache2/access.log
		maxretry = 100
		findtime = 60
		bantime = 3600
		action = iptables-multiport[name=apache-ddos, port="http,https", protocol=tcp]'
	Add a new file called apache-ddos.conf in the etc/fail2ban/filter.d
	sudo vim etc/fail2ban/filter.d/apache-ddos.conf

Then add the lines 
	[Definition] 
	failregex = ^<host> -.*"(GET|POST|HEAD).*HTTP.*" (4[0-9][0-9]|5[0-9][0-9]) .*
	ignoreregex =
	
	Add the rules by restarting the server using 
	sudo systemctl restart fail2ban




