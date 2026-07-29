export GH_USERNAME=' $karakan-rt'
export GH_TOKEN= ''
GH_IMAGE_NAME='KUTANGA'
export GH_VER='1.0.0'
export TAG_NAME="ghcr.io/karakan-rt/hello-twoj-stary:1.0.0"

echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-twoj-stary:latest  $TAG_NAME

docker push  $TAG_NAME