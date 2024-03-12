# devops-interview-questions and guidance
Repository with DevOps interview questions.

## Intervew guidance

* Even if we pressed by time, HRs etc. - we shouldn't low our expectation from the candidate. Because bad engineer in the team will actually make things worse for us and we will have even less time to work on IT infrastructure.
* For DevOps engineers ask more questions about DevOps/NetOps/SysOps with a bit of DBRE and SecOps questions.
* For DBRE concentrate more on DBRE questions with a bit of a DevOps/NetOps/SysOps/SecOps questions.
* For DevSecOps, ask about deep TCP/IP knowledge, as most threats are over the network.
  * SecOps and NetOps questions followed by DevOps/NetOps/SysOps questions

### Red flags

* Candidate constantly mention - "we" instead of talking about what he/she did, even after several questions about his/her experience
* Candidate doesn’t tell - I don’t know to questions that he/she doesn’t know answer for, but try to answer you with as many as possible technology words in non-sensible manner.

# Questions
## Simple intro questions for candidate (can be given to HR for initial screening)

* which network protocol is used to synchronise clocks?
  * **NTP**
* how to check for Linux syscalls of a running process?
  * **strace**
* on Unix systems, the file descriptor number 2 is?
  * **stderr**
* where is the upstream DNS server address stored on Linux?
  * check `/etc/resolv.conf` or `resolvectl --status`
* on Unix systems, which syscall is used to create a new process from an already running process?
  * **fork**
* what process states do you know?
  * **Spawn**
  * **Waiting**
  * **Runnable**
  * **Running**
  * **Stopped**
  * **Zombie**
  * **Removed from process table**
* what signal child process send to parent process on exit?
  * **SIGCHILD**
* *on Linux, what's the ID number of the init process?
  * **1**
* /var/log/syslog contains messages that starts with `I/O error occurred`, what could it mean?
  * hardware issues with hard drive
* O(N) O(logN) O(N*N) - which one is faster?
  * **O(logN)**
* which protocol ping uses?
  * **ICMP**
* What is NAT?
  * Network Address Translation
* How to see network packets?
  * `tcpdump`
* How many bits is in IPv6 address? 
  * **128 bits**
* data structure with O(N) complexity to access value by key?
  * **Dictionary/Hash**

## Programming

* What is your favorite scripting/programming language(s)? Why ?
* General CS, algorithms Q&A: 5 minutes
    * Data structures - discuss possible implementations and applications:
        * Binary tree
        * Hash map
        * Heap
    * Complexity classes - discuss and give examples:
        * Linear
        * Polynomial
        * NP Complete / NP Hard
    * Sorting algorithms - discuss:
        * What is the fastest sorting algorithm?
        * What is the complexity of quick sort?
    * Distributed systems:
        * What’s Paxos?
        * What's Raft?
        * What’s consistent hashing?
    * Hands-on coding:
        * Inverse a string in place

## DevOps

* What DevOps is? Why do we need it?
    * Example of answers:
        * Why do we need it?
            * Increase deployment frequency
            * Lower failure rate of new releases
            * Shortened lead time between fixes
            * Faster mean time to recovery in the event of new release crashing
        * What DevOps is?
            * CALMS
            * C – Culture (promotes collaborative and open culture between Dev and Ops)
            * A – Automation (automate wherever applicable)
            * L- Learning (continuous learning & experimentation)
            * M – Measure (Measure with shared metrics across the Dev and ops for better management)
            * S – Sharing (Shared delivery process across Dev and Ops to build , deploy, maintain and monitor product with mentality of One Team – One Goal)
* What is the purpose of a post-mortem meeting?
* What is meant by Continuous Integration?
* What are the success factors for Continuous Integration?
  * Examples of answers:
      * Maintain a code repository
      * Automate the build
      * Make the build self-testing
      * Everyone commits to the baseline every day
      * Every commit (to baseline) should be built
      * Keep the build fast
      * Test in a clone of the production environment
      * Make it easy to get the latest deliverables
      * Everyone can see the results of the latest build
      * Automate deployment
* What is Continious Delivery? Continious Deployment?
* What is the difference between Continuous Integration, Continious Delivery and Continious Deployment?
* What’s the difference between git and github ? What about git and SVN ?
* What is `git rebase`?
* In Git how do you revert a commit that has already been pushed and made public?
* What is puppet/chef/ansible used for? What are the advantages over shell scripts ?
* What do you understand by “Infrastructure as code”? How does it fit into the DevOps methodology? What purpose does it achieve?
* How do you give your developers access to the production logs ?
* Tell me about the worst-run/best-run outage you’ve been a part of. What made it bad/well-run?
* How do you monitor your application ? How do you make sure it is working ? How do you get alerts when it stops working ?
* What would be the availability and performance metrics for a key value store ? What about for MySQL replication ?
* What is caching ? Where should a large scale application cache, and what data should be cached ?

## SysOps

* What is your favorite editor?
* What is RAID? What is RAID0, RAID1, RAID5, RAID10?
* Describe the general file system hierarchy of a Linux system.
* Describe what each of the following command line utilities do:
    * tee
    * awk
    * tr
    * cut
    * curl
    * tail
    * sed
* Command line demo:
  * Search for "my konfu is the best" in all `*.py` files
  * Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files
  * Find all files which have been accessed within the last 30 days
* What is the difference between virtual memory and swap ?
* What is the difference between hardlinks and symlinks?
* What is an inode and what fields are stored in an inode?
* What are zombie processes ?
* Can you have several HTTPS virtual hosts sharing the same IP?
* What is the difference between processes and threads?
* What is the difference between exec and fork?
* How nginx can handle a lot of connections? What does it use inside?
    * Example of answer: Eventloop.
* What is "nohup" used for?
* What is an atomic operation?
* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?
* How do you catch a SIGHUP ? What about SIGSEGV ? What about SIGKILL ?
* What is the Linux Kernel OOM and how does it work ?
* What's a chroot jail?
* Describe the Linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.
* What's LD_PRELOAD and when is it used?
* You ran a binary and nothing happened. How would you debug this?
* When can a socket receive E_AGAIN ?
* What is a dynamically/statically linked file?
* A careless sysadmin executes the following command: chmod 444 /bin/chmod - what do you do to fix this?
* I've lost my root password, what can I do?
* You have accidentally deleted a running script, how could you restore it ?
* What load balancers have you used ?
* AWS:
    * What is the difference between an AMI and an instance?
    * What’s EBS? What’s an EBS snapshot ? What is the real cost of having an EBS snapshot?
    * What’s a VPC?
    * What’s the difference between a region and an availability zone?
    * What’s an ELB? ALB? NLB?
    * What’s S3? What are the features supported on S3?

## NetOps/Networking

* What is time synchronization? Why do we need it?
  * **NTP**
  * TLS certificates
  * ID generation in distributed systems
* How does ping work ? What about traceroute ?
* I type http://www.yahoo.com in my browser’s URL bar and I press enter. What happens ? (discuss at every OSI layer - Physical, data link, network, transport, session, presentation, application)
    * DNS & anycast, IP, UDP, routing, BGP, TCP, HTTP, transparent proxy
    * What is BGP?
    * What’s a PTR in DNS? Why should we care?
* What if I change from http://www.yahoo.com to https://www.yahoo.com  ?
    * Public/private certificates, CAs, proxying, MiTM, etc.
* What happens when I press the send button in my email client ?
* How do we prevent bots crawling ? How would you deal with a syn flood ?
* How many hosts in a /24  network? What about a /22 ?
* What is the difference between DNAT and SNAT ? When do you use either ?
* What is a virtual IP address? What is a cluster?
* What is IPv6 ? Why should we care?

## DBRE

* What's ACID ? How is it implemented ?
* What is row level locking ? Table level locking ?
* How do you check which jobs are running?
* Imagine you have a filesystem that supports snapshots - how do you take hot backups using volume managers (LVM/EBS)?
* What is the need for master/slave replication in MySQL ? What about master/master replication ? How does replication work in MySQL ?
* How would you handle DB migrations? How would you automate DB migration process?
* What pros/cons could you tell about MySQL/PostgreSQL?
* Which primary key is better - synthetic or natural one? Why?

## SecOps/Security

* What is the difference between authentication and authorization?
* What is SSO? How does it work?
* What about SCIM bridge? Why do we need to have SCIM bridge if we already have SSO?
* On a newly installed linux machine, what would you change in /etc/ssh/sshd_config?
* When would you use the TARPIT iptables target?
* You notice that the 20 year old web application stores the user's passwords hashed with MD5. How would you migrate to a new hash?
* You know that a 3rd party website allows googlebot. How would you scrape this website?
* How to prevent being scraped when someone sets their X-Forwarded-For header to a googlebot IP address?
* What's the most important defense against security incidents?
* An employee's password was leaked. Someone gained admin access on the website with this password. How to deal with this situation? What steps would you take to discover how was the password compromised? How to prevent it in the future?
* Come up with a good question about iptables ESTABLISHED and RELATED conntrack matches.
* You would like to discover the password of someone else who is on the same WiFi network. How would you do that? How could the user defend against this? How could the WiFi owner defend against this?
* What is OWASP?
* What is PCI DSS?
* What was the biggest or most interesting security issue you faced, and how did you resolve it?

## System design

* DevOps: How would you deploy software to 5000 systems?
* DevOps: How would you implement CI (continuous delivery) - end to end, including source control, branches, tools, etc. ?
* SysOps: Design a storage system for a database. Design a storage system for 30 TB of images (to be served over http(s)).
* NetOps: Let's design a fictitious aviation tracking system. We want our fleet of airplanes to report their locations and other vital parameters once every 5 minutes. Let's say we had a choice to use TCP or UDP which one would you pick and why?
* Programming: You run a website that stores it’s web sessions in memcache; you get a request to log off a user ID. How do you do it ?
* DBRE: A developer asks if he should create an InnoDB or MyISAM database, what would you recommend?
* SecOps: You are creating a new web application and you have to store the user's passwords in a database. How would you store the passwords?

## General

* What are some of the most common DevOps personality characteristics ?

## References

* https://www.springboard.com/blog/25-cybersecurity-job-interview-questions-and-answers/
* https://youtu.be/g35UumfZ-H4
