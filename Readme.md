<h3>qemu-arm-static for Fedora22, x86_64.</h3>
Setup:
<ul>
<li>
<ol><li>Copy file qemu-arm-static.conf to the /lib/binfmt.d
If qemu-arm.conf exists in /lib/binfmt.d, rename it to qemu-arm.conf.unu.</li>
<li>Or change qemu-arm to qemu-arm-static at the end of line in the /lib/binfmt.d/qemu-arm.conf.</li>
</ol>
</li>
<li>run 'systemctl restart systemd-binfmt.service'</li>
<p>For Raspberry, chroot, it may be neccessary to comment out content of
/etc/ld.so.preload for preventing qemu: "uncaught target signal 4 (Illegal instruction) - core dumped".</p>
