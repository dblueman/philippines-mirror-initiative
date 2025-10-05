Follow secure setup guide for Ubuntu 24.04 LTS:
https://gist.github.com/dblueman/e8556d11a7b16a5026df78b79661a7a9

Install HTTP mirroring packages:
```bash
apt install --no-install-recommends nvme-cli f2fs-tools nginx ubumirror rpi-imager stress-ng linux-tools-raspi ubumirror
```

Validate RaspberryPi is stable under maximum processor load:
```base
stress-ng --verify --thermalstat 10m --timeout 4h --msyncmany 0
```

Validate RasperrbyPi is stable under maximum HTTP load from external client:
```bash
wrk -t16 -c64 -d20s -s wrk-urls.lua http://192.168.1.2/ --latency
```
example output:
```
Running 30s test @ http://192.168.1.153/ubuntu/ls-lR.gz
  16 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     0.00us    0.00us   0.00us    -nan%
    Req/Sec     0.00      0.00     0.00      -nan%
  0 requests in 30.10s, 3.26GB read
Requests/sec:      0.00
Transfer/sec:    111.00MB
```
