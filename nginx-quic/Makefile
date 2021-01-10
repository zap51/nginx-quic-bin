
default:	build

clean:
	rm -rf Makefile nginx-quic-zap

build:
	$(MAKE) -f nginx-quic-zap/Makefile

install:
	$(MAKE) -f nginx-quic-zap/Makefile install

modules:
	$(MAKE) -f nginx-quic-zap/Makefile modules

upgrade:
	/usr/sbin/nginx -t

	kill -USR2 `cat /var/run/nginx.pid`
	sleep 1
	test -f /var/run/nginx.pid.oldbin

	kill -QUIT `cat /var/run/nginx.pid.oldbin`
