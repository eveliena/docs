# Validator Backup

{% embed url="https://github.com/SecretFoundation/docs/blob/main/docs/backup/backup-a-validator.md" %}

{% embed url="https://github.com/SecretFoundation/docs/blob/main/docs/backup/backup-a-full-node.md" %}

## &#x20;<a href="#validator-backup" id="validator-backup"></a>

## Validator Backup <a href="#validator-backup" id="validator-backup"></a>

It is **CRUCIAL** to backup your validator's private key. It's the only way to restore your validator in an event of a disaster.

The validator private key is a Tendermint Key - a unique key used to sign consensus votes.

To backup everything you need to restore your validator, simply do the following

If you are using the software sign (which is the default signing method of tendermint), your Tendermint Key is located in `~/.secretd/config/priv_validator_key.json`.

1. Backup `~/.secretd/config/priv_validator_key.json`.
1. Backup `~/.secretd/data/priv_validator_state.json`.
1. Backup the self-delegator wallet. See the [wallet section](https://docs.scrt.network/backup/backup/wallets).

The easiest way is to backup the whole config folder.

Also see [Backup a Validator](../node-runners/validator-backup.md) and [Migrate a Validator](../node-runners/migrating-a-validator.md).

To see the associated public key:

```bash
secretd tendermint show-validator
```

To see the associated consensus address:

```bash
secretd tendermint show-address
```

Or you can use hardware to manage your Tendermint Key much more safely, such as [YubiHSM2](https://developers.yubico.com/YubiHSM2/).
