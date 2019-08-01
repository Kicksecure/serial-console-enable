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

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
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
