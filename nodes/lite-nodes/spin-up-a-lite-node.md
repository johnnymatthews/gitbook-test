---
description: >-
  Lite-nodes are a simplified node option that allow developers to perform
  lightweight tasks on a local node. This page covers how to spin-up a lite node
  on your local machine.
---

# Spin up a lite-node

In this guide, we’re going to use the [Lotus](https://docs.filecoin.io/nodes/lite-nodes/spin-up-a-lite-node/) Filecoin implementation. We’ll show how to install a lite-node on MacOS and Ubuntu. For other Linux distributions, check out the [Lotus documentation](https://lotus.filecoin.io/lotus/install/linux/#building-from-source). To run a lite-node on Windows, install [WLS with Ubuntu](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#1-overview) on your system and follow the _Ubuntu_ instructions below.

### Prerequisites

Lite-nodes have relatively lightweight hardware requirements – it’s possible to run a lite-node on a Raspberry Pi 4. Your machine should meet the following hardware requirements:

1. At least 2 GiB of RAM
2. A dual-core CPU.

To build the lite-node, you’ll need some specific software. Run the following command to install the software prerequisites:

{% tabs %}
{% tab title="MacOS" %}
1. Ensure you have [XCode](https://developer.apple.com/xcode/) and [Homebrew](https://brew.sh/) installed.
2. Install the following dependencies:

```sh
brew install go bzr jq pkg-config hwloc coreutils
```

3. Install Rust and source the `~/.cargo/env` config file:

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
```
{% endtab %}

{% tab title="Ubuntu" %}
1. Install the following dependencies:

```
sudo apt update -y
sudo apt install mesa-opencl-icd ocl-icd-opencl-dev gcc git bzr jq pkg-config curl clang build-essential hwloc libhwloc-dev wget -y
```

2. Install Go and add `/usr/local/go/bin` to your `$PATH` variable:

```
wget -c https://golang.org/dl/go1.18.8.linux-amd64.tar.gz -O - | sudo tar -xz -C /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc && source ~/.bashrc
```

3. Install Rust and source the `~/.cargo/env` config file:

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source "$HOME/.cargo/env"
```

4. Done! You can move on to the [Pre-build](https://docs.filecoin.io/nodes/lite-nodes/spin-up-a-lite-node/#pre-build) section.
{% endtab %}
{% endtabs %}

### Pre-build

Before we can build the Lotus binaries, there’s some setup we need to do. MacOS users should select their CPU architecture from the tabs:

{% tabs %}
{% tab title="MacOS Intel" %}
1. Clone the repository, and move into the `lotus` directory:

```
```

2. asd

```
```

3. Done! You can move on to the [Build](https://docs.filecoin.io/nodes/lite-nodes/spin-up-a-lite-node/#build-the-binary) section.
{% endtab %}

{% tab title="MacOS ARM" %}
1. Clone the repository, and move into the `lotus` directory:

```
```

2. asd

```
```

3. Done! You can move on to the [Build](https://docs.filecoin.io/nodes/lite-nodes/spin-up-a-lite-node/#build-the-binary) section.
{% endtab %}

{% tab title="Ubuntu" %}
1. Clone the repository, and move into the `lotus` directory:

```
git clone https://github.com/filecoin-project/lotus.git
cd lotus/
```

2. Switch to the branch representing the network you want to use:

```
# Checkout to mainnet
git checkout releases

# Checkout to the Calibration testnet
# git checkout ntwk/calibration
```

3. If your processor was released later than an AMD Zen or Intel Ice Lake CPU, enable the use of SHA extensions by adding these two environment variables. If in doubt, ignore this command and move on to [the next section](https://docs.filecoin.io/nodes/lite-nodes/spin-up-a-lite-node/#build-the-binary).

```
export RUSTFLAGS="-C target-cpu=native -g"
export FFI_BUILD_FROM_SOURCE=1
```

4. Done! You can move on to the Build section.
{% endtab %}
{% endtabs %}

### Build the binary

The last thing we need to do to get our node setup is to build the package. The command you need to run depends on which network you want to connect to:

{% tabs %}
{% tab title="Mainnet" %}

{% endtab %}

{% tab title="Calibration" %}

{% endtab %}
{% endtabs %}
