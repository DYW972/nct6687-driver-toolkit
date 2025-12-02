# NCT6687-d Toolkit

## 📌 Project Overview

NCT6687-d Toolkit:
Secure Driver Signing for Hardware Monitoring on Ubuntu Noble (24.04)

The NCT6687-d Toolkit provides a structured approach to signing and loading
the Novuton NCT6687 hardware monitoring kernel module on Ubuntu Noble (24.04)
systems with Secure Boot enabled.
This project was developed to address the lack of native support
for temperature and fan speed monitoring on
the MSI MAG TOMAHAWK Z790 motherboard, which integrates the NCT6687 chip.

### 🔍 Background

While attempting to monitor system temperatures and fan speeds on Ubuntu Noble,
standard tools like lm-sensors, hwinfo, senors...
failed to provide complete or accurate data for the NCT6687 chip.

An open-source repository offered an updated kernel module for this hardware,
but loading it was blocked due to **Secure Boot enforcement**.

To maintain system security without disabling Secure Boot,
this toolkit automates the process of manually signing
the kernel module and loading it securely.

### ✨ Key Features

* **Secure Boot Compatibility**: Enables kernel module loading without disabling
Secure Boot, ensuring system integrity.
* **Automated Signing Workflow**: Simplifies the process of generating and
enrolling a Machine Owner Key (MOK) for module signing.
* **Ubuntu Noble Support**: Specifically tested and designed for Ubuntu 24.04
with kernel 6.8+.
* **Hardware-Specific**: Targets the NCT6687 chip, commonly found on MSI Z790 motherboards.

### ⚠️ Security Notice

>**Important Security Considerations**
>
> * Manually signing kernel modules introduces potential risks,
including system instability or exposure to unsigned/malicious code.
> * This toolkit is intended for **advanced Linux** users familiar with Secure Boot,
kernel module management, and cryptographic signing.
> * Always verify the source of the kernel module and the signing process.
Follow Ubuntu’s and **[ANSSI’s guidelines](https://www.ssi.gouv.fr/)** for
secure system configuration.
> * Enrolling a custom MOK requires physical access to the machine
(to set a BIOS/UEFI password and enroll the key).
Ensure this process is performed in a trusted environment.

### 🎯 Target Audience

This toolkit is designed for **experienced Linux users** who:

* Require hardware monitoring for NCT6687-equipped systems on Ubuntu Noble.
* Prefer to maintain Secure Boot for security reasons.
* Are comfortable with command-line operations, kernel module management,
and cryptographic signing.

## 🔄 Repository Information

### GitHub Mirror

This repository is a read-only public mirror of the original project,
which is actively developed on GitLab.

**👉 Main development happens here**:

<https://gitlab.com/crafted-by-yoh/system-security/platform-security/nct6687-driver-toolkit>

### Purpose of this mirror

* Increase project visibility.
* Simplify contributions from GitHub users.
* Offer a familiar platform for community discussions and pull requests.

## 🔄 Repository Workflow

This GitHub repository is synchronized automatically from GitLab using push mirroring.
**All direct modifications made on GitHub are overwritten during synchronization**.

If you'd like to contribute:

* Open an **Issue** or **Pull Request** on GitHub.
* PRs submitted on GitHub are reviewed and then merged upstream on the Gitlab
repository.
* Changes are later mirrored back to GitHub automatically.

## 🤝 Contributing

1. **Fork** this GitHub repository.
2. Create a new branch for your changes.
3. Submit a **Pull Request**
4. Your contribution will be reviewed.
5. Once approved, it will be merged in Gitlab.
6. Gitlab will automatically push the changes back to GitHub

## 📢 Important Note

* **This repository cannot accept direct pushes**
* All source code, releases, CI/CD and internal management
are handled exclusively on Gitlab 🦊

## 🙏 Acknowledgments

We would like to thank:

* The open-source community for their invaluable feedback and contributions.
* The developers of the
[original NCT6687 kernel module](https://github.com/Fred78290/nct6687d).
* Ubuntu and ANSSI for their security guidelines and best practices.

## 📝 License

This project is **[GNU General Public Licensed](https://gitlab.com/crafted-by-yoh/system-security/platform-security/nct6687-driver-toolkit/-/blob/ad78481502950d761954e3cb4d2b1da6b9d65000/LICENSE)**

## 📬 Contact

For questions or collaboration inquiries:
📧 <yohandunon@protonmail.com>

## Ressources

* [SecureBoot](https://wiki.ubuntu.com/UEFI/SecureBoot)
* <https://www.kernel.org/doc/Documentation/hwmon/nct6683.rst>
