ARG VARIANT="14"
# ARG USERNAME=max
# ARG USER_UID=1000
# ARG USER_GID=${USER_UID}
FROM node:${VARIANT}

# install zsh
RUN apt-get update && apt-get install -y zsh
# install oh-my-zsh
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
# set zsh plugins and theme
RUN sed -i 's/robbyrussell/mortalscumbag/' ~/.zshrc && sed -i 's/plugins=(git)/plugins=(git systemd npm ng node vscode)/' ~/.zshrc



# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# RUN groupadd --gid ${USER_UID} ${USERNAME} \
#     && useradd --uid ${USER_UID} --gid ${USERNAME} -m ${USERNAME}

# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"

# [Optional] Uncomment if you want to install more global node packages 
# RUN sudo -u node npm install -g <your-package-list -here>
