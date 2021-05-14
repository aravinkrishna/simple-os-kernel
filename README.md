# simple-os-kernel

A simple os kernel example 

Pre-requirements:
    1. Docker
    2. Qemu
    3. A text edittor (VS code)

Run the following commands in order after the above are installed:
    1. docker build buildenv -t myos-buildenv
    2. Powershell: docker run --rm -it -v "${pwd}:/root/env" myos-buildenv
       CMD: docker run --rm -it -v "%cd%":/root/env myos-buildenv
       MacOS: docker run --rm -it -v "$PWD":/root/env myos-buildenv
       Linux: docker run --rm -it -v "$pwd":/root/env myos-buildenv
    3. make build-x86_64
    After step 3 is run successfully type "exit" and exit the env.
    4. qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso -L "C:\Program Files\qemu"
    You might / might not require  `-L "C:\Program Files\qemu"` in the step 4 depending on your version of qemu
