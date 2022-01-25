# Project Beam 

Project Beam is a simple collection of small bash-scripts which runs iteratively to carry out various tools and recon process & store output in an organized way. This project was created initially for automation of Recon for personal usage and was never meant to be public as there is nothing fancy about it but due to request by community, Project Beam is now Public.  
Please feel free to improve it in any way you can. There is no secret sauce involved and it's just a set of commands and existing tools written in bash-scripts for simple Recon Automation. 

Project Beam currently this tools supports performing recon for:

1. Small Scope (single urls in scope) : Performs a limited recon & useful when only a few urls are provided in scope
2. Medium Scope (\*.target.com in scope) : Performs recon to enumerate more assets and give you more options to attack on.  
3. Large Scope (Everything in Scope) : Performs almost every possible recon vector from subdomain enumeration to fuzzing. 

A few features like port scanning might not be working in the current build and some of the newly released tools might also be missed. we are working on upgrading the tool but feel free to fork, upgrade and make a pull request (Ensure that tool is not breaking).


# Pre-Requisite

1. Make sure to have "Go" latest version is installed and paths are correctly set.

# Installation

1. Clone the repository
2. Run the following script to install necessary tools: ``sh install.sh``
3. The ``arsenal`` directory contains a set of small scripts used to automate Beam. Give executable permissions to scripts in this directory.
4. Navigate to ``~/arsenal`` directory and Simply run following command to see all the supported options provided in Beam:

``./Beam.sh -h`` 

5. To use it over vps for performing recon on larger set of targets perform following command:

``screen -S <screen_name>``
``~/arsenal/Beam.sh -h``

6. This will keep ``Beam`` running even if the SSH Connection is terminated or you turn off your local machine.

# Sample Usage

1. Small Scope Recon : ``Beam -t targetfile -S``
2. Medium Scope Recon : ``Beam -t targetfile -M``
3. Large Scope Recon : ``Beam -t targetfile -L``

``targetfile`` contains list of domains to perform Recon. For example: `targettest.com`

### Exclude out-of-scope subdomains

Beam has a flag to remove out-of-scope subdomains from the scan. To do so you have to use "-e" flag with comma separated subdomains.

``Beam -t targetfile -S -e sub.ex.com,sub1.ex.com``

# Tools Used 

1. Nuclei                             
2. HTTPX                            
3. GF & GF-Patterns                  
4. Secret Finder                     
5. Heartbleed Oneliner               
6. AMASS                             
7. Subfinder                          
8. Assetfinder      
9. JSScan
10. FavFreak
11. Waybackurls 
12. Gau
13. Parallel
14. asnip
15. dirsearch
16. gowitness
17. subjack
18. CORS Scanner 
19. git-hound
20. Shuffledns
21. Massdns

~ Other onliners and tools to be added. 


# Future Plans/Under Development

1. Adding Directory Enumeration_
2. Adding Subdomain Bruteforcing_
3. Adding HTTP Desync Scanner_
4. Adding Vulnerable Software & Exploit Suggester
5. Adding Oneline Scanner for _CORS_, CRLF & Other Vectors
6. Adding Visual Recon
7. Adding Web Based Handling Of Results