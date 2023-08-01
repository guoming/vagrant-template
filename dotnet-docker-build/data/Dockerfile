FROM docker-bkrepo.ztn.cn:443/paas/bkdevops/centos7.2:v1
RUN rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm &&  \
yum install -y dotnet-sdk-3.1 aspnetcore-runtime-3.1 && \
mkdir /usr/share/dotnet/bin && \
cp /usr/share/dotnet/dotnet /usr/share/dotnet/bin/ && \
dotnet tool install --global dotnet-sonarscanner --add-source 'https://api.nuget.org/v3/index.json' --ignore-failed-sources --version 5.13.0 && \
yum install dotnet-runtime-2.2 -y && \
yum install dotnet-sdk-2.2 -y && \
yum install dotnet-runtime-3.1 -y && \
yum install dotnet-sdk-3.1 -y && \
yum install dotnet-runtime-6.0 -y && \
yum install dotnet-sdk-6.0 -y

ENV DOTNET_HOME /usr/share/dotnet
ENV PATH ${PATH}:${DOTNET_HOME}/bin

RUN yum install autoconf automake libtool -y && \
yum install freetype-devel fontconfig libXft-devel -y && \
yum install libjpeg-turbo-devel libpng-devel giflib-devel libtiff-devel libexif-devel -y && \
yum install glib2-devel cairo-devel -y 

RUN yum install -y git  && \
git clone https://github.com/mono/libgdiplus 

RUN yum install -y make && \
cd libgdiplus  && \
./autogen.sh    && \
make && \
make install && \
ln -s /usr/local/lib/libgdiplus.so /usr/lib64/libgdiplus.so

