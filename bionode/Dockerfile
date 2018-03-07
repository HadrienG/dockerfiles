FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# nvm and node
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash && \
    export NVM_DIR="$HOME/.nvm" && \
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" && \
    nvm install --lts && \
    npm i -g bionode-ncbi  && \
    npm i bionode-sra && \
    mv node_modules/bionode-sra/ .nvm/versions/node/v?.?.?/lib/node_modules/ && \
    cd .nvm/versions/node/v?.?.?/bin/ && \
    ln -s ../lib/node_modules/bionode-sra/cli.js bionode-sra

ENV PATH /root/.nvm/versions/node/v8.9.4/bin/:$PATH
