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

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `serial-console-enable`.

```
sudo apt-get install serial-console-enable
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `serial-console-enable` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`serial-console-enable` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
