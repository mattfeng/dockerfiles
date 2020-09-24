FROM alpine:3.12.0

RUN apk update && apk add curl python3 which bash

RUN curl https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-311.0.0-linux-x86_64.tar.gz > /tmp/gcloud-sdk.tar.gz

RUN mkdir -p /usr/local/gcloud && \
    tar -C /usr/local/gcloud -xvf /tmp/gcloud-sdk.tar.gz && \
    /usr/local/gcloud/google-cloud-sdk/install.sh

ENV PATH $PATH:/usr/local/gcloud/google-cloud-sdk/bin

ENTRYPOINT ["sleep"]
CMD ["999999"]
