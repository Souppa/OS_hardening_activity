# OS_hardening_activity
OS Hardening against disgruntled baker

I am given a task that I am working as a cybersecurity analyst for yummyrecipesforme.com, a website that sells recipes and cookbooks. A disgruntled baker has decided to publish the website’s best-selling recipes for the public to access for free. 

The baker executed a brute force attack to gain access to the web host. They repeatedly entered several known default passwords for the administrative account until they correctly guessed the right one. After they obtained the login credentials, they were able to access the admin panel and change the website’s source code. They embedded a javascript function in the source code that prompted visitors to download and run a file upon visiting the website. After running the downloaded file, the customers are redirected to a fake version of the website where the seller’s recipes are now available for free.

Several hours after the attack, multiple customers emailed yummyrecipesforme’s helpdesk. They complained that the company’s website had prompted them to download a file to update their browsers. The customers claimed that, after running the file, the address of the website changed and their personal computers began running more slowly. 

In response to this incident, the website owner tries to log in to the admin panel but is unable to, so they reach out to the website hosting provider. Me and other cybersecurity analysts are tasked with investigating this security event.

To address the incident, I created a sandbox environment to observe the suspicious website behavior. I ran the network protocol analyzer tcpdump, then typed in the URL for the website, yummyrecipesforme.com. As soon as the website loads, I was prompted to download an executable file to update my browser. I accepted the download and allow the file to run. I then observed that my browser redirects me to a different URL, greatrecipesforme.com, which is designed to look like the original site. However, the recipes my company sells were posted for free on the new website.  

A senior analyst confirms that the website was compromised. The analyst checks the source code for the website. They notice that javascript code had been added to prompt website visitors to download an executable file. Analysis of the downloaded file found a script that redirects the visitors’ browsers from yummyrecipesforme.com to greatrecipesforme.com. 

The cybersecurity team reports that the web server was impacted by a brute force attack. The disgruntled baker was able to guess the password easily because the admin password was still set to the default password. Additionally, there were no controls in place to prevent a brute force attack. 

My job was to document the incident in detail, including identifying the network protocols used to establish the connection between the user and the website.  I also needed to recommend a security action to take to prevent brute force attacks in the future.

