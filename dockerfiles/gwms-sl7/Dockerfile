# Selecting SL7 as the base OS 
FROM scientificlinux/sl:7 
MAINTAINER Marco Mambelli "marcom@fnal.gov"

# Install the quired RPMS
# and clean yum
RUN yum install -y wget sed git;\
    yum clean all

# Default entry point 
CMD ["/bin/bash"] 


# build info
RUN echo "Source: fermilab/gwms-sl7" > /image-source-info.txt
RUN echo "Timestamp:" `date --utc` | tee /image-build-info.txt
