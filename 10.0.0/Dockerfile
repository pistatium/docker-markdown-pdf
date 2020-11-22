FROM node
RUN apt-get update\
 && apt-get install -y --no-install-recommends fonts-noto-cjk\
 && rm -rf /var/lib/apt/lists/*
RUN npm install --silent -g markdown-pdf@10.0.0\
 && rm -rf ~/.npm/cache/*\
 && mkdir -p /opt/docs
WORKDIR /opt/docs
COPY fonts.conf /etc/fonts/conf.d/99-local.conf
ENV NODE_PATH /usr/local/lib/node_modules
CMD ["/bin/bash"]
