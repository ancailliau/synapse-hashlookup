# Rapid PowerUp Synapse-HashLookup

Synapse-HashLookup is a Rapid PowerUp for Synapse, enabling users to query hash
values against a known database of files. This integration includes the NSRL
RDS database and many other sources, enhancing your ability to perform hash
lookups seamlessly within your Synapse environment.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Hooks and Alerts](#hooks-and-alerts)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

1. **Synapse:** You must have a functioning installation of Synapse. If you
haven't already, refer to the Synapse documentation for installation
instructions.

## Installation from source

1. **Clone the Repository:** Clone this repository to your Synapse environment
using Git or download it as a ZIP archive and extract it.

2. **Deploy the Power-Up:** Copy the synapse-hashlookup directory to your
Synapse Power-Ups directory. The location may vary depending on your Synapse
installation.

```
python -m synapse.tools.genpkg ./synapse-hashlookup.yaml \
  --push tcp://USER:PASSWORD@localhost/cortex
```

## Usage

Once Synapse-HashLookup is installed and configured, you can use it to query
HashLookup directly from your Synapse environment. Here are some essential
commands and usage instructions:

- **Querying for MD5 hash**: Retrieve detailed information about a
  specific MD5 hash using the HashLookup Power-Up.

  ```
  > hash:md5=8ED4B4ED952526D89899E723F3488DE4 | cyl.hashlookup.enrich --yield
  ```

- **Querying for SHA1 hash**: Retrieve detailed information about a
  specific SHA1 hash using the HashLookup Power-Up.

  ```
  > hash:sha1=FFFFFDAC1B1B4C513896C805C2C698D9688BE69F | cyl.hashlookup.enrich --yield
  ```

- **Querying for SHA256 hash**: Retrieve detailed information about a
  specific SHA256 hash using the HashLookup Power-Up.

  ```
  > hash:sha256=301c9ec7a9aadee4d745e8fd4fa659dafbbcc6b75b9ff491d14cbbdd840814e9 | cyl.hashlookup.enrich --yield
  ```
  
These are just a few examples of what you can achieve with Synapse-HashLookup.
Refer to the documentation for more advanced queries and options.

## Contributing

We welcome contributions from the community to improve and expand the
capabilities of Synapse-HashLookup. If you have ideas, bug reports, or feature
requests, please feel free to open an issue or submit a pull request in this
repository.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use,
modify, and distribute it in accordance with the terms of the license.

---

Thank you for using Synapse-HashLookup! We hope this Power-Up enhances your
cybersecurity efforts and threat intelligence workflows. 