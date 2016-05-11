DionaeaFR
=========

Front Web to Dionaea low-interaction honeypot.

Home DionaeaFR: http://rubenespadas.github.io/DionaeaFR/

Home Dionaea:   http://dionaea.carnivore.it/

[*] Technologies:

  - Python 2.7.3
  - Django 1.4 (1.8.11 tested working)
  - Jquery 1.7.2
  - Bootstrap Framework 2.1.1
  - jVectorMap 1.0
  - Kendo-UI v2011.3.1129
  - SQLite3

[*] Requirements:

	pip install Django
	pip install pygeoip
	pip install django-pagination
	pip install django-tables2
	pip install django-compressor
	pip install django-htmlmin
	pip install django-filter
	
	django-tables2-simplefilter:
		https://github.com/benjiec/django-tables2-simplefilter
		python setup.py install
	
	SubnetTree:
		git clone git://git.bro-ids.org/pysubnettree.git
		python setup.py install
	
	nodejs:
		sudo apt-get install nodejs
		sudo ln -s "$(which nodejs)" /usr/bin/node
	
	npm install -g less
	npm install -g promise
	apt-get install python-netaddr

[*] Install

  Download GeoIP and GeoLiteCity:
  
    wget http://geolite.maxmind.com/download/geoip/database/GeoLiteCity.dat.gz
    wget http://geolite.maxmind.com/download/geoip/database/GeoLiteCountry/GeoIP.dat.gz

  Decompress GeoIP and GeoLiteCity:
  
    gunzip GeoLiteCity.dat.gz
    gunzip GeoIP.dat.gz

  Move GeoIP and GeoLiteCity to DionaeaFR/DionaeaFR/static:
  
    mv GeoIP.dat DionaeaFR/DionaeaFR/static
	mv GeoLiteCity.dat DionaeaFR/DionaeaFR/static

  Run server:
  
	python manage.py collectstatic
	python manage.py runserver 0.0.0.0:8000

  Access to http://YOUR_IP:8000 in browser.

[*] Changelog

  - Add transport, type and protocol filters in connections table.
  - Add Attacks graph last 7 days.
  
  29/11/2012
	- Add less support
	- Add HTML minify
	- Add menu icons
	- Other visuals changes
	
  18/12/2012
	- Add home panel

  20/12/2012
	- Add country name in tooltips
	- Add Top 10 Ports Graph
	- Add ANTIVIRUS_VIRUSTOTAL variable in settings.py
	- Deactive minify by default
	- Restructure directories
	- Fixed Graphs
  
  15/05/2013
    - Refactoring Code
	- New filters system

  16/05/2013
    - Fixed mysql_command.
    - Add refresh interval in graphs.

[*] Suggestions?

Designed by @rubenespadas
