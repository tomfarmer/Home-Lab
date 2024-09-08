# AdGuard Setup

1) To First setup an AdGuard sever you need to make an Ubuntu Server VM. Make sure you statically assign the DNS server.
	A) I like to make my DNS server either the `x.x.x.2` or the `x.x.x.53` 
	B) Give the ubuntu server 
			CPU: 2
			RAM: 4 GB
			Hard Drive: 25 GB (Thin Provisioned)
			
2) Once the Ubuntu server is setup download AdGuard from the link below:
	[Link to AdGuard Download](https://github.com/AdguardTeam/AdGuardHome#getting-started)
	
	Once at the Github page you can download ad setup AdGuard with just one command, example below:
```bash
curl -s -S -L https://raw.githubusercontent.com/AdguardTeam/AdGuardHome/master/scripts/install.sh | sh -s -- -v
```

3) In your browser enter the ip address you assigned to the ubuntu server with port 3000 after the ip address. Example:
		`x.x.x.2:3000`
		
4) Next I would pick a recent youtube video and follow it for the most up to date setup for AdGuard
