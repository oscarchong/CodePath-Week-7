# Week 7 Project - Wordpress Pentesting

Time spent: 8 hours

> Objective: To discover and demonstrate similar proofs-of-concept for at least an additional three and (up to five) exploits affecting an older version of WP.

## Exploit 1:
(Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)

#### Summary: 
- Wordpress tested version: 4.2
- Vulnerbility Type: XSS
- Fixed in version: 4.2.1

#### Steps to recreate:
- Go to any page where you can comment
- Comment any link with <svg onload=alert(1)> at the end
- Post comment
  
![](exploit-1.gif | width=100)


