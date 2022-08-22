- ### sudo iptables -A INPUT --jump ACCEPT --protocol all --source 127.0.0.1
 accept all incoming connections from 127.0.0.1 (localhost)
- ### sudo iptables -A INPUT --jump ACCEPT --protocol tcp --dport 2001
 accept incoming tcp connections on port 2001 (needed to ssh into the server)
- ### sudo iptables -A INPUT --jump ACCEPT --protocol icmp
 accept incoming [icmp](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) connections (e.g. to ping the validator)
- ### sudo iptables -A INPUT -i lo -j ACCEPT
- ### sudo iptables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT
- ### sudo iptables -P INPUT DROP
- ### sudo iptables -P FORWARD DROP
- ### sudo ip6tables -A INPUT -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT
- ### sudo ip6tables -P INPUT DROP
- ### sudo ip6tables -P FORWARD DROP
- ### sudo apt install -y iptables-persistent
- ### sudo iptables -nL -v
- ### sudo ip6tables -nL -v
