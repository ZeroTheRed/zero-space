KVM (Kernel Virtual Machine) is a free and open-source virtualization module that enables the Linux kernel as a hypervisor 

KVM contains two modules
* A generic loadable kernel module `kvm.ko` that contains the core virtualization module
* A processor-specific module such as `kvm-intel.ko` and `kvm-amd.ko`