Thanks for checking out the KVM/Qemu inter-VM shared memory PCI device

#Getting the Device Running#

There are two ways to get the shared memory device running.   The first is with _only_ shared memory; the second is with shared memory and interrupts.  The second method requires an external shared memory server.

Example programs for both approaches and the shared memory server are in the *guest-code.git* repository.

#Without Interrupts#

This is the simpler method

your Qemu/KVM command-line should have the following:

-device ivshmem,shm=_some name_,size=_size_

#With Interrupts#

If you want to be able to send interrupts between VMs you need to use the shared-memory server from the repo
