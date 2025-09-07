1 set ip:
https://blackarch.ru/?p=483

sudo ip address add 85.159.230.8/24 dev ens18
sudo ip link set dev ens18 mtu 1500
sudo ip link set dev ens18 up
sudo ip route add default via 85.159.230.1 dev ens18 proto dhcp src 85.159.230.8 metric 100

output "ip route show":
default via 85.159.230.1 dev ens18 proto dhcp src 85.159.230.8 metric 100
85.159.230.0/24 dev ens18 proto kernel scope link src 85.159.230.8

in /etc/resolv.conf write 
nameserver 8.8.8.8


2 refresh keys:
pacman-key --refresh-keys
pacman -S archlinux-keyring


menuentry "Windows XP" {
 chainloader (hd0,1)+1
}

(hd0,1) - 1 is partition num with windows in drive
