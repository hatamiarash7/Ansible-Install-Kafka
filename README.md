# Install Kafka Cluster ( Ansible )

You can use this role to install a [Kafka](https://kafka.apache.org/) cluster on Kubernetes.

## Prerequisites

By default we have some PVCs here to manage data, so you should define `/mnt/kafka` & `/mnt/zoo` directories on suitable nodes.

> You can ignore this and make it ephemeral.

## How-to

First you need instal the role:

-   Clone this role:

    ```bash
    git clone git@github.com:hatamiarash7/Ansible-Install-Kafka.git install_kafka
    ```

-   Or you can install using galaxy:

    ```bash
    ansible-galaxy install hatamiarash7.install_kafka
    ```

Then, Include role in Playbook:

```yml
- hosts: all
    roles:
        - hatamiarash7.install_kafka
```

## Dependencies

You need **Docker** & **Kubernetes**. Take a look at these roles too:

-   [install_docker](https://github.com/hatamiarash7/Ansible-Install-Docker)
-   [install_kubernetes](https://github.com/hatamiarash7/Ansible-Install-Kubernetes/)

## Usage

We have two service for Kafka and two for ZK.

-   A headless service to create DNS records
-   A Normal service for clients

You can use `bootstrap` service to handle connections between your apps and Kafka cluster.

---

## Support 💛

[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz)](https://en.cryptobadges.io/donate/bc1qmmh6vt366yzjt3grjxjjqynrrxs3frun8gnxrz) [![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)](https://en.cryptobadges.io/donate/0x0831bD72Ea8904B38Be9D6185Da2f930d6078094)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing 🤝

Don't be shy and reach out to us if you want to contribute 😉

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them. 👍
