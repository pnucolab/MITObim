MITObim for rootless docker & docker compose
============================================

You can find the original version of MITObim [here](https://github.com/chrishah/MITObim).

Usage
-----

1. Open `docker-compose.yml` and edit the path to the data directory.

2. Build and run image.

```
$ docker compose up -d
```

3. Get into `bash` to run MITObim pipeline.

```
$ docker compose exec mitobim bash
```

4. Remove image.
```
$ docker compose down
```
