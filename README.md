# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

## PROGRAM:
Find out the ip address of the attackers system

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/f53b0ba8-f1d7-4ef8-996e-f483d621920b)

## invoke msfconsole:

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/a1185fb2-2e51-4946-b0af-89bb59d0f9f8)
Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.


## OUTPUT:

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/faccad26-5e12-41b2-9e73-2ee30b700df3)

Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

## OUTPUT:

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/9af59f80-3f5d-44b5-9d17-849e543ea7a2)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/6cb480c3-9aff-4437-aa80-201a1a828521)

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/3789786f-7b1e-48c1-822d-6136a90b5eca)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/e3454c47-211d-46ff-bb79-44dbe16bf7f1)

The info command provides information regarding a module or platform.

## OUTPUT:

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/41800261-758b-4f96-a075-d4b52b09cbbd)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/373e5067-5493-433d-a7d3-31807ab2ee6c)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/3674e541-9567-46dc-b5cf-65951469fbf3)

Use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/cc1b70e5-42e1-43b6-b2af-af33f1d1d97b)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/7a4ec53c-038e-41a4-8d38-f166dd8eb8fd)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.

![image](https://github.com/NAVEENKUMAR4325/Metasploit-for-reconnaissance/assets/119479566/873017db-58af-4e5b-b0ec-054cadbe24a5)


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
