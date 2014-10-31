docker-cuda-fah
===============

Folding @Home image with CUDA support.

### Usage:

On a host with a CUDA device and drivers.

        docker run \
          --device=/dev/nvidia0:/dev/nvidia0 \
          --device=/dev/nvidiactl:/dev/nvidiactl \
          --device=/dev/nvidia-uvm:/dev/nvidia-uvm \
          -it \
          --rm cuda-fah \
          <FAHClient command line options>

Or, as the base of another image.

        FROM ozzyjohnson/cuda-fah

### Next:

- EXPOSE ports for the control program.
- We can probably just drop a config file in the directory mounted to /data and run without options. Have to test.
- Complete testing, fah.stanford.edu is unreachable as I commit this.
