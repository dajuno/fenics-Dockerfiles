# fenics stable:current build
# extended by:  
#   - zsh + config
#   - python: scipy (update), pyyaml, matplotlib2tikz
FROM quay.io/fenicsproject/stable:current
USER root
RUN apt-get update && apt-get install -y zsh && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN pip install scipy pyyaml matplotlib2tikz --upgrade
USER fenics
RUN wget -O ~/.zshrc https://raw.githubusercontent.com/grml/grml-etc-core/master/etc/zsh/zshrc 
RUN echo "source ~/.profile" > ~/.zshrc.local
USER root
