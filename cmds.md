VMware Workstation how to see 8.8.8.8 and see host from VM:
goto Edit -> Virtual Network Editor
Add Network -> VMnet8
Subnet IP must be different from the local subnet, for example 192.168.64.0
Subnet mask 255.255.255.0
check NAT, in default in NAT Settings gateway must be 192.168.64.2 for example
check "Connect a host virtual adapter to this network"
check "Use local DHCP service to distribute IP address to VMs"
click Apply, OK
goto  VM Settings -> Network Adapter
check "Custom"
select VMnet8 (NAT)
click OK
if use AmneziaVPN
goto Split tunelling -> Site-based
change list to "should not be accessed via VPN"
add 192.168.0.0/16


dotnet new sln --name "sln name"
dotnet new classlib -o <classlib name>
dotnet new console -o <console project name>
dotnet sln Obfuscator.sln add <path to proj>
dotnet add app/app.csproj reference lib/lib.csproj