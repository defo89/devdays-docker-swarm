FROM ubuntu

# chain commands
# remove apt lists - wont be present in any layer
RUN apt-get update \
	&& apt-get install -y nginx \
	&& rm -rf /var/lib/apt/lists/*
EXPOSE 80
CMD ["/usr/sbin/nginx","-g","daemon off;"]
COPY default /etc/nginx/sites-available/default
COPY www/ /var/www/html/
