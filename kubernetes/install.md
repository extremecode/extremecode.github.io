# kubernetes installation on Centos

##  If working in a proxy enviroment 
Copy to /etc/enviroment of all the nodes
```markdown
export http_proxy="http://web-proxy.in.softwaregrp.net:8080"
export https_proxy="http://web-proxy.in.softwaregrp.net:8080"
export HTTP_PROXY="http://web-proxy.in.softwaregrp.net:8080"
export HTTPS_PROXY="http://web-proxy.in.softwaregrp.net:8080"
export no_proxy="127.0.0.1,localhost,ip_address_1,ip_address_2"  -- optional if all the nodes in the same network
export NO_PROXY="127.0.0.1,localhost,ip_address_1,ip_address_2"  -- optional if all the nodes in the same network
```
## if all the nodes are not in the same network
copy /etc/hosts on all the nodes
```markdown
ip_address_1
ip_address_2
..
ip_address_n
``2
