FROM lukasheinrich/slc6_cern_server_x86_64_2015-02-10
RUN yum groupinstall -y "Development Tools"; yum clean all
RUN yum install -y git make gcc-c++ gcc binutils libX11-devel libXpm-devel libXft-devel libXext-devel gcc-gfortran openssl-devel pcre-devel mesa-libGL-devel glew-devel ftgl-devel mysql-devel fftw-devel cfitsio-devel graphviz-devel avahi-compat-libdns_sd-devel libldap-dev python-devel libxml2-devel gsl-static procmail openssl098e.x86_64 compat-libf2c-34.x86_64 libtool-ltdl libtool-ltdl-devel mktemp; yum clean all
RUN curl -sSL https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64 > /usr/local/bin/jq && chmod +x /usr/local/bin/jq
RUN mkdir /code ~/.ssh
WORKDIR /code
ENV ATLAS_LOCAL_ROOT_BASE="/cvmfs/atlas.cern.ch/repo/ATLASLocalRootBase"
ADD resources/bashrc /root/.bashrc
ADD resources/krb5.conf /etc/krb5.conf
ADD resources/custom_ssh_config /etc/ssh/ssh_config
