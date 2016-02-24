#!/bin/bash

set -e

IMAGE_A=$1
IMAGE_B=$2

container_a=$(docker create "$IMAGE_A" /dontexist)
container_b=$(docker create "$IMAGE_B" /dontexist)
if [ "$IGNORE_FILESIZE" = "1" ]; then
    AWK='{printf "%-10s %-100s\n",$1,$6}'
else
    AWK='{printf "%-10s %-10s %-100s\n",$1,$3,$6}'
fi

diff <(docker export "$container_a" | docker run -i --rm ubuntu tar tvf - | awk "$AWK") <(docker export "$container_b" | docker run -i --rm ubuntu tar tvf - | awk "$AWK")

docker rm -fv "$container_a" "$container_b"
