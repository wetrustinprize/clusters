<div align="center">
    <img src="logo.png">
</div>

This is a simple `dockerfile` and `docker-compose` for a [QSMP][2]-like server for me and my friends.

It runs Forge + Bukkit using [Magma][3].

## Steps to deploy:

1. Execute a `docker compose up` with the **required** env variables.
2. The first execution will cause an **error**, asking you to accept the EULA.
   1. Access the `psmp-server` bind folder and edit the `eula.txt` file. _(change the false to true)_
3. Restart the container and it should be working.
   1. If the server crashes with an Java error, try restarting again. Otherwise, open an issue here.

## Environment Variables

| Variable  | Description                             | Default  |
| --------- | --------------------------------------- | -------- |
| MC_RAM    | Amount of RAM to allocate to the server | 1G       |
| PSMP_BIND | The host path to bind the files to      | Required |

## Credits

Most of the code was taken from [Siverten's Magma Dockerfile][1].

[1]: https://hub.docker.com/r/siverten/magma
[2]: https://twitter.com/qsmpen?lang=en
[3]: https://magmafoundation.org