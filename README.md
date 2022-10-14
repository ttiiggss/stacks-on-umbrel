# Stacks Blockchain with Docker

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Pull Requests Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

Run your own Stacks Blockchain node easily with just few commands.

---

## **Quick Start for Umbrel:**

```bash
$ git clone --depth 1 https://github.com/ceramicwhite/stacks-on-umbrel.git
$ cd stacks-on-umbrel
$ cp sample.env .env
$ export BTC_RPC_PASS="<umbrel btc rpc password>"  # Visit Bitcoin App on Umbrel and click "+ Connect" for RPC Password 
$ sed -i "
    /^password/s/.*/password = \"${BTC_RPC_PASS}\"/; \
" ./conf/mainnet/Config.toml.sample
$ ./manage.sh -n mainnet -a start
```

---

## **Requirements:**

- [Docker](https://docs.docker.com/get-docker/) >= `17.09`
- [docker-compose](https://github.com/docker/compose/releases/) >= `1.27.4`
- [git](https://git-scm.com/downloads)
- [jq binary](https://stedolan.github.io/jq/download/)
- [sed](https://www.gnu.org/software/sed/)
- Machine with (at a minimum):
  - 4GB memory
  - 1 Vcpu
  - 50GB storage
