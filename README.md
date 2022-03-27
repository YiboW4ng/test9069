CVE-2020-27955
Git-LFS Remote Code Execution Vulnerability
==============

[Git LFS](https://git-lfs.github.com/) is a Git extension developed by Github to implement Git‘s support for large files. Remote code execution issue found on Git-LFS versions <= 2.12 on Windows platforms.
![Git LFS](./gitlfs.png)

Git LFS vulnerability allows attackers to compromise targets’ Windows systems
It allows attackers to achieve remote code execution if the Windows-using victim is tricked into cloning the attacker’s malicious repository using a vulnerable Git version control tool.


### How does this work
Once victim clone malicious repository and runs vulnerable Git-LFS version on their system.These automatically executed codes may be Trojans.
![how-does-work](./phishing&tabnabbing/images/图片1.png)

### Who uses Tabnabbing
* Attackers
* Teachers
* Microsoft
* ...

### Why is Tabnabbing useful
People can take measures to avoid net fishing attempts and slightly modify their browsing habits. When contacting a letter or account number that requires you to "check your identity" (or the gist of any other letter used in phishing), it is wise to contact the company from which the letter is obviously sourced to check whether the email is legal. In addition, the address known to individuals is the real website of the company, which can be visited by entering in the website bar of the browser, rather than blindly believing the hyperlinks in any suspected fraud email. The anti phishing working group (apwg), an industry and law enforcement agency, suggests that traditional phishing fraud techniques may become obsolete in the future as people become more aware of the social engineering tricks used by net fishermen. They predict that website grafting and other use of rogue software will become common tools to steal information.

### What is the real-world impact
Almost all legal e-mails from companies to their customers contain at least one message that online fishermen don't have at hand. Some companies, such as PayPal, always address their customers by their customer user name in their e-mail, and so on. If the recipient of an e-mail is addressed in a common format (such as "Dear PayPal customer"), it is likely to be an attempt to fish online. Emails from banks and credit card companies often include part of the account number. However, recent research shows that the public usually does not distinguish between the first and last numbers of account numbers, which is a serious problem because the first few numbers are usually the same for all customers of a financial institution. People can be trained to raise their suspicions if the email does not contain any specific personal information. However, in early 2006, online fishing attempted to use personalized information, which made it unsafe to list personal information to ensure that the email was legal. In addition, another recent study concluded that listing personal information did not significantly affect the success rate of phishing attacks, indicating that most people did not pay attention to these details.

Demo/How to run this Demo
----
Demo is in ./phishing&tabnabbing/demo, which contains four html pages. Firstly enter the file through CMD and deploy these four html files to the local server by command 'http-server'. A local host address will be generated, type the address in browser and we can enter the local host.
![p1](./phishing&tabnabbing/images/p1.png)
We start with A.html, which is a personal account with some tags and a 'open new page' button. This button is designed by a hacker to triger the tabnabbing. Users will find that the tags work as usual to open some pages they are familiar with. But if they click the button, a new page(B.html) occurs and it warns users something is wrong and they need to sign in again. When users come back to the original pege they will see a log in page(C.html). Actually now the address has been changed and this is a fake log in page. If users are careless and don't notice that stange address change they will trust this fake page and enter their log in information. Hacker can set some functions to this page, once users click 'sign in' buttom, their username and password will be passed to a new page(D.html) and hackers can access these information on the back-end of D.html. In this case users' account information leak out and users don't even know that. Hacker can do something bad with these information like stealing money or sell their account.
![p2](./phishing&tabnabbing/images/p2.png)
![p3](./phishing&tabnabbing/images/p3.png)
![p4](./phishing&tabnabbing/images/p4.png)
![p5](./phishing&tabnabbing/images/p5.png)


Citations
---------
* https://en.wikipedia.org/wiki/Phishing
* https://en.wikipedia.org/wiki/Tabnabbing
* https://xz.aliyun.com/t/7080
