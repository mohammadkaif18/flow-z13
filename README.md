# flow-z13 &nbsp; [![bluebuild build badge](https://github.com/adelsjarlen/flow-z13/actions/workflows/build.yml/badge.svg)](https://github.com/adelsjarlen/flow-z13/actions/workflows/build.yml)

Welcome to the **flow-z13** repository! This project provides a framework for creating custom images based on the BlueBuild system. You can find detailed setup instructions in the [BlueBuild docs](https://blue-build.org/how-to/setup/). 

After you set up your repository, we recommend updating this README to reflect your custom image specifics.

## Table of Contents

1. [Overview](#overview)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Features](#features)
5. [Contributing](#contributing)
6. [License](#license)
7. [Releases](#releases)
8. [Contact](#contact)

## Overview

**flow-z13** aims to simplify the process of building and managing custom images. This project focuses on using the latest technologies to ensure a smooth experience. It supports atomic updates and provides a robust framework for creating immutable operating systems.

### Key Topics

- Atomic
- BlueBuild
- Custom Images
- Image-Based Systems
- Immutable Linux
- OCI Images

## Installation

To install and rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. **Rebase to the Unsigned Image**

   First, rebase to the unsigned image. This step ensures that you install the proper signing keys and policies:

   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/adelsjarlen/flow-z13:latest
   ```

2. **Reboot the System**

   After the rebase, reboot your system to complete the process:

   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image**

   Once your system has rebooted, you can rebase to the signed image:

   ```bash
   rpm-ostree rebase ostree-image-signed:docker://
   ```

> **Note:** This feature is experimental. Use it at your own discretion. You can read more about it in the [Fedora Project Wiki](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable).

## Usage

After installation, you can start using the custom image. The flow-z13 image provides a clean environment for various applications. You can manage packages, updates, and configurations seamlessly.

### Basic Commands

Here are some basic commands to help you get started:

- **Check Current Image:**

   ```bash
   rpm-ostree status
   ```

- **Update Packages:**

   ```bash
   rpm-ostree upgrade
   ```

- **Rollback to Previous Image:**

   ```bash
   rpm-ostree rollback
   ```

These commands help you maintain and manage your custom image effectively.

## Features

**flow-z13** comes with several features that enhance your experience:

- **Atomic Updates:** Ensure that your system remains consistent and reliable.
- **Immutable Infrastructure:** Reduce the risk of configuration drift.
- **Customizable Images:** Tailor the environment to meet your specific needs.
- **Robust Security:** Benefit from the latest security practices.

## Contributing

We welcome contributions from the community. If you want to contribute to **flow-z13**, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Create a pull request.

Your contributions help improve the project and benefit all users.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Releases

You can find the latest releases of **flow-z13** [here](https://github.com/mohammadkaif18/flow-z13/releases). Visit this link to download the necessary files and execute them as needed.

If you are looking for specific versions or want to check the changelog, please refer to the "Releases" section in the repository.

## Contact

For questions or suggestions, feel free to reach out. You can open an issue in the repository or contact the maintainers directly.

---

Thank you for using **flow-z13**! We hope you enjoy working with this project and find it useful for your needs.