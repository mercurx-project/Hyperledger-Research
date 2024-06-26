## Usage

### Output a genesis block

Write a genesis block to `genesis_block.pb` for channel `application-channel-1`
for profile `SampleSingleMSPRaftV1_1`.

```
configtxgen -outputBlock genesis_block.pb -profile SampleSingleMSPRaftV1_1 -channelID application-channel-1
```

### Output a channel creation tx (deprecated)
**Note:** The channel creation transaction was used in order to create a new application channel using a system channel. Because the system channel is no longer supported since release v3.0, it is now deprecated.

Write a channel creation transaction to `create_chan_tx.pb` for profile
`SampleSingleMSPChannelV1_1`.

```
configtxgen -outputCreateChannelTx create_chan_tx.pb -profile SampleSingleMSPChannelV1_1 -channelID application-channel-1
```

### Inspect a genesis block

Print the contents of a genesis block named `genesis_block.pb` to the screen as
JSON.

```
configtxgen -inspectBlock genesis_block.pb
```

### Inspect a channel creation tx (deprecated)
**Note:** The channel creation transaction was used in order to create a new application channel using a system channel. Because the system channel is no longer supported since release v3.0, it is now deprecated.

Print the contents of a channel creation tx named `create_chan_tx.pb` to the
screen as JSON.

```
configtxgen -inspectChannelCreateTx create_chan_tx.pb
```

### Print an organization definition

Construct an organization definition based on the parameters such as MSPDir
from `configtx.yaml` and print it as JSON to the screen. (This output is useful
for channel reconfiguration workflows, such as adding a member).

```
configtxgen -printOrg Org1
```


## Configuration

The `configtxgen` tool's output is largely controlled by the content of
`configtx.yaml`.  This file is searched for at `FABRIC_CFG_PATH` and must be
present for `configtxgen` to operate.

Refer to the sample `configtx.yaml` shipped with Fabric for all possible
configuration options.  You may find this file in the `config` directory of
the release artifacts tar, or you may find it under the `sampleconfig` folder
if you are building from source.


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
