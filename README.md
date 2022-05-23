This is a set of binaries for secure boot and ovmf development.

The files here are used by the test harness for [stubby](https://github.com/puzzleos/stubby)
stubby, but are probably convienent as a collection for use elsewhere.

What is here:
 * info.yaml: Just some loosely typed information on where these files came from.
 * collect: an executable that was run in Ubuntu to collect these files.
 * boot-vm: a script to execute qemu
 * ovmf-insecure-code.fd, ovmf-insecure-vars: a OVMF code and vars file set for boot without secureboot (insecure).
 * ovmf-secure-code.fd, ovmf-secure-vars.fd: a OVMF code and vars file set for boot with secureboot.
 * signing.cert, signing.key, signing.password: a signing certificate, key and password.  An EFI signed with this set will be trusted in a guest booted with ovmf-secure-vars.fd.
 * shim.efi: an unsigned shim executable capable of loading another (signed) efi program.
