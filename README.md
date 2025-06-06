# insecure-cpp.github.io

## x86_64

Linus branch : https://github.com/torvalds/linux/blob/master/arch/x86/entry/syscalls/syscall_64.tbl

### Based on 

* https://blog.rchapman.org/posts/Linux_System_Call_Table_for_x86_64/
* https://chromium.googlesource.com/chromiumos/docs/+/master/constants/syscalls.md#x86_64-64_bit

### TODO

* 333	common	__io_pgetevents__	sys_io_pgetevents
* 334	common	__rseq__			sys_rseq
* 335	common	__uretprobe__		sys_uretprobe

### Note

> "There are two 32-bit ABIs that can be supported by 64-bit x86 kernels, in addition to the native x86-64 ABI. The 32-bit ABIs are:
>
> The i386 ABI that emulates the ABI implemented by 32-bit x86 kernels.
The x32 ABI that is a newer 32-bit ABI for x86-64 kernels.
The GCC -m32 flag will generate code for the i386 ABI. Use the -mx32 flag to generate code for the x32 ABI.
>
> The "syscall_64.tbl" file enumerates the system calls for the x86-64 and x32 ABIs:
>
> The "64" entries are for the x64-64 ABI.
The "x32" entries are for the x32 ABI.
The "common" entries are for both the x64-64 and x32 ABI.
The "syscall_32.tbl" enumerates the system calls for the i386 ABI. For each system call number, the table lists two entry points:
>
> The entry point for 32-bit x86 kernels.
The "compat" entry point for i386 ABI emulation on x86-64 kernels.
Some obsolete system calls that are no longer implemented by the kernel are listed without an entry point.
>
> While there is a lot of old, 32-bit binary-only software that uses the i386 ABI and runs on both 32-bit and 64-bit systems, the newer x32 ABI never became very popular. Applications using the x32 ABI won't run on systems with 32-bit kernels."
> 
> https://stackoverflow.com/a/59823360