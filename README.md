# simple-os-kernel

<h3>A simple os kernel example </h3>

<h3>Pre-requirements:</h3>
    <ul>
        <ol>1. Docker</ol>
        <ol>2. Qemu</ol>
        <ol>3. A text edittor (VS code)</ol>
    </ul>

<p>Run the following commands in order after the above are installed:</p>
<ul>
    <ol>1. `docker build buildenv -t myos-buildenv`</ol>
    <ol>2. Powershell: `docker run --rm -it -v "${pwd}:/root/env" myos-buildenv` <br>
       CMD: `docker run --rm -it -v "%cd%":/root/env myos-buildenv` <br>
       MacOS: `docker run --rm -it -v "$PWD":/root/env myos-buildenv` <br>
       Linux: `docker run --rm -it -v "$pwd":/root/env myos-buildenv`</ol>
    <ol>3. `make build-x86_64`
    After step 3 is run successfully type `exit` and exit the env.</ol>
    <ol>4. `qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso -L "C:\Program Files\qemu"`
    You might / might not require  `-L "C:\Program Files\qemu"` in the step 4 depending on your version of qemu</ol>
</ul>

<p>Please note that this is purely for educational purpose</p>
