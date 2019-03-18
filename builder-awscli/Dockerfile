FROM gcr.io/jenkinsxio/builder-go:0.1.289

RUN curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip" && \
  unzip awscli-bundle.zip && \
	./awscli-bundle/install -b /bin/aws
