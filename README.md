# Week 7 Project - Wordpress Pentesting

Time spent: 6 hours

> Objective: To discover and demonstrate similar proofs-of-concept for at least an additional three and (up to five) exploits affecting an older version of WP.

## Exploit 1:
(Required) Authenticated Stored Cross-Site Scripting (XSS)

#### Summary: 
- Wordpress tested version: 4.2
- Vulnerbility Type: XSS
- Fixed in version: 4.2.1

#### Steps to recreate:
- Go to any page where you can comment
- Comment any link with < svg onload=alert(1) > at the end
- Post comment

![](exploit-1.gif)

#### Source: 
- [Link](https://github.com/WordPress/WordPress/commit/7ab65139c6838910426567849c7abed723932b87)


## Exploit 2:
(Required) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds

#### Summary:
- Wordpress tested version: 4.2
- Vulnerbility Type: XSS
- Fixed in version: 4.2.13

#### Steps to recreate:
- Log in as admin
- Create a post
- In the post body add the following code [embed src='https://youtube.com/embed/123\x3csvg onload=alert(1)\x3e'][/embed]
- Preview or view the post

![](exploit-2.gif)

#### Source:
- [Link](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)


## Exploit 3:
(Required) Authenticated Shortcode Tags Cross-Site Scripting

#### Summary:
- Wordpress tested version: 4.2
- Vulnerbility Type: XSS
- Fixed in version: 4.3

#### Steps to recreate:
- Go to a page
- Then paste the following code : TEST!!![caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">Click me</a>
- Click update and then preview

![](exploit-3.gif)

#### Source:
- [Link](https://wpvulndb.com/vulnerabilities/8186)






