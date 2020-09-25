# Selecting SL7 as the base OS 
FROM scientificlinux/sl:7 
MAINTAINER Marco Mambelli "marcom@fnal.gov"

# Install the quired RPMS
# and clean yum
RUN yum install -y wget sed git;\
    yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm;\
    yum install -y yum-priorities;\
    yum install -y https://repo.opensciencegrid.org/osg/3.5/osg-3.5-el7-release-latest.rpm;\
    yum install -y osg-ca-certs

# yum dep program needs to be added
ADD gwms-sl7/yumalldeps.sh /usr/bin/yumalldeps.sh

# Specific dependencies for GlideinWMS will be added 

# Default entry point 
CMD ["/bin/bash"] 


# build info
RUN echo "Source: fermilab/gwms-sl7" > /image-source-info.txt
RUN echo "Timestamp:" `date --utc` | tee /image-build-info.txt
