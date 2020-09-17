17 Sept 2020
============

Use NGINX as a web server + proxy server

On Windows, download nginx zip file and unzip to any folder - there is no installer, you just have to run the exe
During development, you could run ngnix and point this specific path for it to pick the conf from

# Run
pthapliy@HAW-PTHAPLIY-01 MINGW64 /C/GIT/MyPersonal/Ludo/JavascriptUI (UI)
$ /C/Prasun/Software/NGINX/nginx-1.15.6/nginx.exe -p "/C/GIT/MyPersonal/Ludo" -c "ProxyServer/nginx.conf"

# Always test before running
pthapliy@HAW-PTHAPLIY-01 MINGW64 /C/GIT/MyPersonal/Ludo/JavascriptUI (UI)
$ /C/Prasun/Software/NGINX/nginx-1.15.6/nginx.exe -p "/C/GIT/MyPersonal/Ludo" -c "ProxyServer/nginx.conf" -T

Troubleshooting:
	-T tells you that events section is required in conf file, so added some junk
	-T will also tell you that logs folder is missing .. so add it here /Ludo/logs

Troubleshooting:
	Chrome does not apply CSS, even though the file is downloaded in the browser
	Fix: The Networks tab in chrome reveals that browser made a request with Content-Type plain text instead of css. This was also coming as an error in console
		Resource interpreted as Stylesheet but transferred with MIME type text/plain: "http://localhost/style.css".
	To fix, 
	(a) add "include mime.types" in the conf
	(b) Copy the mime.types file from original nginx folder to our directory /C/GIT/MyPersonal/Ludo/ProxyServer/
	(c) Add header correction lines in conf file
		
		location ~ /.css {
			add_header  Content-Type    text/css;
		}
		
		location ~ /.js {
			add_header  Content-Type    application/x-javascript;
		}

This is the most minimal version of conf with which our HTML can be served with NGINX as a web server

Then on Google Chrome, navigate to http://localhost/