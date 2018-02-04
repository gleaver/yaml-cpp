#!/usr/bin/env bash

set -e

root=$(pwd)
input="${root}/INPUT"
output="${root}/OUTPUT"
build="${root}/BUILD"

component=
config=

fail() {
  echo  >&2 && exit 1
}

build() {
  mkdir -p "${build}"  
  cd "${build}"
  
  cmake -DCMAKE_INSTALL_PREFIX=${output} ..
  cd ${build}
  make && make install

  cd "${root}"
}

build

