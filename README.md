## Penglai Enclave Linux Driver

This repo contains the linux driver for Penglai Enclave.

The Makefile is customized for Nuclei Linux SDK.

### Version Logs

* **2022-01-11**: Version of penglai-driver is the align with [Penglai-sPMP](https://github.com/penglai-enclave/penglai-enclave-sPMP)'s enclave driver.
The commit number is: d297f13.

### Building

You shall first build the kernel, e.g., using

	make bootimages

in the main repo of Nuclei Linux SDK.

Then, copy the linux-deps/module.lds into work/demosoc/linux/scripts/

In this dir,

	make

You shall see the penglai.ko genereated.

### Usage

Copy the penglai.ko into your rootfs (or disk images),
and install the module after the system is booted:

	insmod ./penglai.ko

Afterthat, you are ready to use penglai enclaves.
