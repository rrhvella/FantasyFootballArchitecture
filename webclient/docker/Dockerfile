FROM nginx
RUN apt-get update -y && apt-get install -y git-core && \
git clone https://github.com/jmaaanu/FantasyFootballWebView.git /tmp/fantasy && \
cp -R /tmp/fantasy/NodeServer/public/* /usr/share/nginx/html/ && \
rm -fr /tmp/fantasy && \ 
apt-get autoremove -y git-core
EXPOSE 80
COPY adapt_from_env.sh /root/adapt_from_env.sh
CMD ["/bin/sh","/root/adapt_from_env.sh"]
