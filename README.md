# GitHub Actions are Awesome!

```
version: "3"
services:
  ganache:
    container_name: ganache
    env_file:
      - .env
    image: trufflesuite/ganache-cli:latest
    ports:
      - "8545:8545"
    volumes:
      - ./ganache_data:/ganache_data
    # entrypoint:
    #   - node
    #   - ./build/cli.node.js
    #   - --deterministic
    #   - --db=/ganache_data
    #   - --mnemonic
    #   - "$MNEMONIC"
    #   - --networkId
    #   - "5777"
    #   - --hostname
    #   - "0.0.0.0"
    #   - --debug
  ipfs:
    container_name: ipfs
    env_file:
      - .env
    image: ipfs/go-ipfs:latest
    ports:
      - "8080:8080"
      - "5001:5001"
```
