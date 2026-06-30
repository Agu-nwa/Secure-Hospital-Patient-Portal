# Secure-Hospital-Patient-Portal

## ⚙️: Update Public Ec2 Packages

### Command
```bash
[ec2-user@ip-10-20-1-245 ~]$ sudo dnf update -y
Amazon Linux 2023 Kernel Livepatch repository                                                                                                                               424 kB/s |  55 kB     00:00    
Dependencies resolved.
Nothing to do.
Complete!
[ec2-user@ip-10-20-1-245 ~]$ 

## ⚙️: Install Web Server

### Command
```bash
[ec2-user@ip-10-20-1-245 ~]$ sudo dnf install -y httpd
Last metadata expiration check: 0:01:00 ago on Tue Jun 30 18:41:13 2026.
Dependencies resolved.
============================================================================================================================================================================================================
 Package                                              Architecture                            Version                                                    Repository                                    Size
============================================================================================================================================================================================================
Installing:
 httpd                                                x86_64                                  2.4.68-1.amzn2023.0.1                                      amazonlinux                                   46 k
Installing dependencies:
 apr                                                  x86_64                                  1.7.5-1.amzn2023.0.4                                       amazonlinux                                  129 k
 apr-util                                             x86_64                                  1.6.3-1.amzn2023.0.2                                       amazonlinux                                   97 k
 apr-util-lmdb                                        x86_64                                  1.6.3-1.amzn2023.0.2                                       amazonlinux                                   13 k
 generic-logos-httpd                                  noarch                                  18.0.0-12.amzn2023.0.3                                     amazonlinux                                   19 k
 httpd-core                                           x86_64                                  2.4.68-1.amzn2023.0.1                                      amazonlinux                                  1.4 M
 httpd-filesystem                                     noarch                                  2.4.68-1.amzn2023.0.1                                      amazonlinux                                   12 k
 httpd-tools                                          x86_64                                  2.4.68-1.amzn2023.0.1                                      amazonlinux                                   80 k
 libbrotli                                            x86_64                                  1.0.9-4.amzn2023.0.2                                       amazonlinux                                  315 k
 mailcap                                              noarch                                  2.1.49-3.amzn2023.0.3                                      amazonlinux                                   33 k
Installing weak dependencies:
 apr-util-openssl                                     x86_64                                  1.6.3-1.amzn2023.0.2                                       amazonlinux                                   15 k
 mod_http2                                            x86_64                                  2.0.42-1.amzn2023.0.1                                      amazonlinux                                  167 k
 mod_lua                                              x86_64                                  2.4.68-1.amzn2023.0.1                                      amazonlinux                                   59 k

Transaction Summary
============================================================================================================================================================================================================
Install  13 Packages

Total download size: 2.4 M
Installed size: 7.0 M
Downloading Packages:
(1/13): apr-1.7.5-1.amzn2023.0.4.x86_64.rpm                                                                                                                                 3.5 MB/s | 129 kB     00:00    
(2/13): apr-util-lmdb-1.6.3-1.amzn2023.0.2.x86_64.rpm                                                                                                                       342 kB/s |  13 kB     00:00    
(3/13): apr-util-1.6.3-1.amzn2023.0.2.x86_64.rpm                                                                                                                            2.2 MB/s |  97 kB     00:00    
(4/13): apr-util-openssl-1.6.3-1.amzn2023.0.2.x86_64.rpm                                                                                                                    612 kB/s |  15 kB     00:00    
(5/13): generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch.rpm                                                                                                               750 kB/s |  19 kB     00:00    
(6/13): httpd-2.4.68-1.amzn2023.0.1.x86_64.rpm                                                                                                                              1.7 MB/s |  46 kB     00:00    
(7/13): httpd-core-2.4.68-1.amzn2023.0.1.x86_64.rpm                                                                                                                          37 MB/s | 1.4 MB     00:00    
(8/13): httpd-filesystem-2.4.68-1.amzn2023.0.1.noarch.rpm                                                                                                                   319 kB/s |  12 kB     00:00    
(9/13): httpd-tools-2.4.68-1.amzn2023.0.1.x86_64.rpm                                                                                                                        2.2 MB/s |  80 kB     00:00    
(10/13): libbrotli-1.0.9-4.amzn2023.0.2.x86_64.rpm                                                                                                                          9.0 MB/s | 315 kB     00:00    
(11/13): mailcap-2.1.49-3.amzn2023.0.3.noarch.rpm                                                                                                                           1.0 MB/s |  33 kB     00:00    
(12/13): mod_http2-2.0.42-1.amzn2023.0.1.x86_64.rpm                                                                                                                         4.6 MB/s | 167 kB     00:00    
(13/13): mod_lua-2.4.68-1.amzn2023.0.1.x86_64.rpm                                                                                                                           2.5 MB/s |  59 kB     00:00    
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Total                                                                                                                                                                        12 MB/s | 2.4 MB     00:00     
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                                                                                    1/1 
  Installing       : apr-1.7.5-1.amzn2023.0.4.x86_64                                                                                                                                                   1/13 
  Installing       : apr-util-lmdb-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                         2/13 
  Installing       : apr-util-openssl-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                      3/13 
  Installing       : apr-util-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                              4/13 
  Installing       : mailcap-2.1.49-3.amzn2023.0.3.noarch                                                                                                                                              5/13 
  Installing       : httpd-tools-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                          6/13 
  Installing       : libbrotli-1.0.9-4.amzn2023.0.2.x86_64                                                                                                                                             7/13 
  Running scriptlet: httpd-filesystem-2.4.68-1.amzn2023.0.1.noarch                                                                                                                                     8/13 
  Installing       : httpd-filesystem-2.4.68-1.amzn2023.0.1.noarch                                                                                                                                     8/13 
  Installing       : httpd-core-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                           9/13 
  Installing       : mod_http2-2.0.42-1.amzn2023.0.1.x86_64                                                                                                                                           10/13 
  Installing       : mod_lua-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                             11/13 
  Installing       : generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch                                                                                                                                12/13 
  Installing       : httpd-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                               13/13 
  Running scriptlet: httpd-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                               13/13 
  Verifying        : apr-1.7.5-1.amzn2023.0.4.x86_64                                                                                                                                                   1/13 
  Verifying        : apr-util-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                              2/13 
  Verifying        : apr-util-lmdb-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                         3/13 
  Verifying        : apr-util-openssl-1.6.3-1.amzn2023.0.2.x86_64                                                                                                                                      4/13 
  Verifying        : generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch                                                                                                                                 5/13 
  Verifying        : httpd-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                                6/13 
  Verifying        : httpd-core-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                           7/13 
  Verifying        : httpd-filesystem-2.4.68-1.amzn2023.0.1.noarch                                                                                                                                     8/13 
  Verifying        : httpd-tools-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                          9/13 
  Verifying        : libbrotli-1.0.9-4.amzn2023.0.2.x86_64                                                                                                                                            10/13 
  Verifying        : mailcap-2.1.49-3.amzn2023.0.3.noarch                                                                                                                                             11/13 
  Verifying        : mod_http2-2.0.42-1.amzn2023.0.1.x86_64                                                                                                                                           12/13 
  Verifying        : mod_lua-2.4.68-1.amzn2023.0.1.x86_64                                                                                                                                             13/13 

Installed:
  apr-1.7.5-1.amzn2023.0.4.x86_64                         apr-util-1.6.3-1.amzn2023.0.2.x86_64        apr-util-lmdb-1.6.3-1.amzn2023.0.2.x86_64       apr-util-openssl-1.6.3-1.amzn2023.0.2.x86_64       
  generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch       httpd-2.4.68-1.amzn2023.0.1.x86_64          httpd-core-2.4.68-1.amzn2023.0.1.x86_64         httpd-filesystem-2.4.68-1.amzn2023.0.1.noarch      
  httpd-tools-2.4.68-1.amzn2023.0.1.x86_64                libbrotli-1.0.9-4.amzn2023.0.2.x86_64       mailcap-2.1.49-3.amzn2023.0.3.noarch            mod_http2-2.0.42-1.amzn2023.0.1.x86_64             
  mod_lua-2.4.68-1.amzn2023.0.1.x86_64                   

Complete!
[ec2-user@ip-10-20-1-245 ~]$ 

## ⚙️: Make Apache start automatically after reboot

### Command
```bash
sudo systemctl enable httpd
Created symlink /etc/systemd/system/multi-user.target.wants/httpd.service → /usr/lib/systemd/system/httpd.service.
[ec2-user@ip-10-20-1-245 ~]$ 

## ⚙️: Start Apache 

### Command
```bash
[ec2-user@ip-10-20-1-245 ~]$ sudo systemctl start httpd
[ec2-user@ip-10-20-1-245 ~]$

## ⚙️: Create the public web page

### Command
```bash
[ec2-user@ip-10-20-1-245 ~]$ echo "<h1>Hospital Patient Portal</h1><p>Public patient landing page running in hospital VPC.</p>" | sudo tee /var/www/html/index.html
<h1>Hospital Patient Portal</h1><p>Public patient landing page running in hospital VPC.</p>
[ec2-user@ip-10-20-1-245 ~]$ 

