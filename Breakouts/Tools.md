# Tools

## Webserver Scanners:

- wpscan
    
    
    ```bash
    wpscan --url http://wordpress.local --enumerate p
    ```
    
    wpscan can be a good WordPress brute force tool
    
    ```bash
    wpscan --url http://dc-2 -U ~/lab/DC/dc2/files/users.txt -P ~/lab/DC/dc2/files/dict.txt
    ```
    
- gobuster
    
     
    
    ```bash
    gobuster -e -u [http://192.168.0.155/](http://192.168.0.155/) -w /usr/share/wordlists/dirb/common.txt
    ```
    
- nikto
    
    
    ```bash
    nikto -h http://10.10.2.8
    ```
    
- dirb
    
    dirb [http://192.168.1.224/](http://192.168.1.224/) /usr/share/wordlists/dirb/common.txt
    

## Brute force attack

- hydra
    
    ## Website login brute force
    
    ### ssh
    
    ```bash
    hydra -l root -P /usr/share/wordlists/metasploit/unix_passwords.txt -t 6 ssh://192.168.1.123
    ```
    
    ### Post Request
    
    ```bash
     hydra -l admin -P /usr/share/wordlists/metasploit/password.lst http-post-form://10.20.30.6/wp-login.php:"log=^USER^&pwd=^PASS^&wp-submit=Log+In":"incorrect"
    ```
    

- cewl
    
    
    ```bash
    cewl -d 3 http://dc-2 > dict.txt
    ```