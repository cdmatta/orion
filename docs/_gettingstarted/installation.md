---
layout: default
title: Installation
nav_order: 1
---
<link rel="stylesheet" href="../../assets/css/custom.css">

# Installation

## orion

### Install the pre-compiled binary

**manually**: Download the pre-compiled binaries from the [releases page](https://github.com/wesovilabs/orion/releases) and copy to the desired location

Latest version: beta-v2

- [osx](https://github.com/wesovilabs/orion/releases/download/beta-v2/orion.darwin) 
- [linux](https://github.com/wesovilabs/orion/releases/download/beta-v2/orion.linux) 
- [windows](https://github.com/wesovilabs/orion/releases/download/beta-v2/orion.exe) 

**Tip**

Once you download the binary I recommend you to do the below: 

```bash
mkdir ~/.orion
mv orion.darwin ~/.orion/orion   
```                                       
Add an entry to your `~/.bash_profile`

```bash
export PATH="~/.orion:$PATH"
```

To verify you installed orion correctly, you just need to execute

```bash
orion help
```

## Running with Docker

You can also use it within a Docker container. To do that, you'll need to execute something more-or-less like the following:

```bash
docker run --rm  \
  -v $(PWD):/vars/feaatures \
  wesovilabs/orion:beta-v2 run --input  /vars/feaatures/feature.hcl
```

## Compiling from source

```bash
git clone git@github.com:wesovilabs/orion.git
cd orion
make setup
make build
```
