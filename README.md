# DotCS-Docker
DotCS运行环境，测试版不保证可靠性

运行环境:
    && mkdir Python-env \

    && cd DotCS-Linux \

    && sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget \

    && wget https://www.python.org/ftp/python/Version/Python-Version.tar.xz \

    && tar -xf Python-Version.tar.xz \

    && cd Python-Version && ./configure --enable-optimizations \

    && make -j 10 && sudo make altinstall \

    && wget https://bootstrap.pypa.io/get-pip.py && python get-pip.py \

    && pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple \

    && pip install datetime psutil requests pymysql qrcode websocket brotli pillow rich
