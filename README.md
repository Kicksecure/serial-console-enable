# Enables verbose output during boot #

Ships a /etc/default/grub.d/30_output_verbose.cfg configuration file, that
removes "quiet" from the GRUB_CMDLINE_LINUX_DEFAULT variable.

For better usability, so it doesn't look like boot hangs on slow systems and
to ease debugging in case of issues.
## How to install `serial-console-enable` using apt-get ##

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org buster main" | sudo tee /etc/apt/sources.list.d/whonix.list
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

## Payments ##

`serial-console-enable` requires [payments](https://www.whonix.org/wiki/Payments) to stay alive!
