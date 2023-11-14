# apt-daily-clean

This is a simple Debian package providing a cron job in `/etc/cron.daily` that runs `apt-get clean`. I use this on Raspberry Pis and similar devices with limited disk space.

## Installation

### Debian via Apt repository

Install my Debian repository if you haven't already:

```shell
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://dist.cdzombak.net/deb.key | sudo gpg --dearmor -o /etc/apt/keyrings/dist-cdzombak-net.gpg
sudo chmod 0644 /etc/apt/keyrings/dist-cdzombak-net.gpg
echo -e "deb [signed-by=/etc/apt/keyrings/dist-cdzombak-net.gpg] https://dist.cdzombak.net/deb/oss any oss\n" | sudo tee -a /etc/apt/sources.list.d/dist-cdzombak-net.list > /dev/null
sudo apt update
```

Then install `apt-daily-clean`:

```shell
sudo apt install apt-daily-clean
```

### Manual installation from build artifacts

Pre-built `.deb` packages are downloadable from each [GitHub Release](https://github.com/cdzombak/apt-daily-clean/releases).

## License

Unlicense; see [LICENSE](https://github.com/cdzombak/apt-daily-clean/blob/main/UNLICENSE) in this repo.

## Author

[Chris Dzombak](https://www.dzombak.com) (GitHub [@cdzombak](https://github.com/cdzombak))
