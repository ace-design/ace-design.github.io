FROM python:3-alpine
# Build the image: docker build -t petitroll/bibble .
# Run the image: docker run -v "$PWD":/data -i petitroll/bibble
# Aliasing: alias bibble='docker run -v "$PWD":/data -i petitroll/bibble'
WORKDIR /usr/src/app
COPY . .
RUN pip install -e .

WORKDIR /data
ENTRYPOINT ["bibble"]
