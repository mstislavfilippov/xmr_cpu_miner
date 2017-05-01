

# How to use this image

## Configuration file

Create `config.txt` configuration file and adapt to your need before running.
You can copy file from a container:

```console
$ docker run -d --name some-xmr-stak-cpu-config minecoins/xmr-stak-cpu
$ docker cp some-xmr-stak-cpu-config:/usr/local/etc/config.txt .
$ docker stop some-xmr-stak-cpu-config
$ docker rm some-xmr-stak-cpu-config
```

or copy example from [GitHub](https://github.com/fireice-uk/xmr-stak-cpu/blob/v1.1.0-1.1.0/config.txt).

## Running

Run in background:

```console
$ docker run -itd --name some-xmr-stak-cpu -v "$PWD"/config.txt:/usr/local/etc/config.txt minecoins/xmr-stak-cpu
```

Use `--privileged` option for large pages support. Large pages need a properly set up OS.

Fetch logs of a container:

```console
$ docker logs some-xmr-stak-cpu
```

Attach:

```console
$ docker attach some-xmr-stak-cpu
```

# Image Variants

The images come in two flavors, with and without donation fee.

## `xmr-stak-cpu:<version>`

This is the defacto image. By default the miner will donate 1% of the hashpower (1 minute in 100 minutes) to dev's pool.

## `xmr-stak-cpu:nodevfee`

This variant has no donation fee.

# Donations

Donations for work on dockerizing are accepted at:

- XMR: `49mw3qFRFttFACrFSdtbM9XQrsnkyWr4ET9Sm9M3zGMud6AvfgJeMVJjWi1KB5jQUhajTpyJBasYKYZ1Rcrh6yvFR9CEkKv`
