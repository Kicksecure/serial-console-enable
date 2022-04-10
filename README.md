# Enables serial console #

Ships a /etc/default/grub.d/30_serial_console.cfg configuration file, that
enables serial console.

Enables /lib/systemd/system/getty.target.wants/serial-getty@ttyS0.service by
creating a symlink from:
/lib/systemd/system/serial-getty@.service
to:
/lib/systemd/system/getty.target.wants/serial-getty@ttyS0.service

Useful for serial console login such as into Whonix KVM VMs from the host
operating system.

Forum discussion:
https://forums.whonix.org/t/how-do-i-enter-the-whonix-shell-from-cli/7271

Safe to remove if you do not require serial console login such as:
virsh console vm-name

## How to install `serial-console-enable` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/derivative.asc
```

Users can [check Whonix Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key..

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `serial-console-enable`.

```
sudo apt-get install serial-console-enable
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `serial-console-enable`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Professional Support](https://www.kicksecure.com/wiki/Professional_Support)

## Donate ##

`serial-console-enable` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
