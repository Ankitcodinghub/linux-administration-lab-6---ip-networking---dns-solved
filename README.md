# linux-administration-lab-6---ip-networking---dns-solved
**TO GET THIS SOLUTION VISIT:** [Linux Administration Lab 6 – IP Networking – DNS Solved](https://www.ankitcodinghub.com/product/linux-administration-lab-6-ip-networking-dns-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;119277&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Linux Administration Lab 6 - IP Networking - DNS Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Michael Scott and Dwight Schrute recently filmed an advertisement to air on the local NBC television station, WBRE. The ad includes the URL of the website for the local Scranton branch of Dunder-Mifflin.

Michael is worried that the current system will be unable to handle the extra traffic and demands that a backup web server be set up – in case the existing server catches fire from the increased load. While maybe a bit of an overreaction, he is wise, at least, to consider what might happen to the web server when the ad goes live.

Despite your best efforts to convince Michael that overloaded computers can’t catch fire, he insists that you set up a standby web server before the advertisement airs. You agree to Michael’s request on one condition – that you’ll also implement a couple of long overdue changes to centralize the administration of the network – namely the DHCP (Dynamic Host Configuration Protocol) and DNS (Domain Name System) services.

What’s needed to setup DNS?

We’ll need the daemon that serves DNS, known alternatively as BIND or named:

We’ll then need to populate the named configuration file to serve the addresses in the configuration table below:

Dunder Mifflin Network Topology &amp; Configuration

D-M currently has the following CentOS Linux machines:

1. router supports dhcp, ip_forwarding, and network/port address translation (nat/pat).

2. carriage (the http server) hosts the D-M website(s).

3. platen (the ftp server) updates prices and accepts batch orders.

4. chase (the dns server) maps between domain names and IP addresses.

5. roller (the file server) stores company files centrally.

6. saddle (the backup http server) makes Michael Scott happy.

Record

Name IP Address or Name TTL

Type

router.dundermifflin.com. 100.64.0.N A 1 hour

carriage.dundermifflin.com. 100.64.N.2 A 1 hour

platen.dundermifflin.com. 100.64.N.3 A 1 hour

chase.dundermifflin.com. 100.64.N.4 A 1 hour

roller.dundermifflin.com. 10.21.32.2 A 1 hour

saddle.dundermifflin.com. 100.64.N.5 A 1 hour

machinea.dundermifflin.com.router.dundermifflin.com. CNAME 7 days

machineb.dundermifflin.com.carriage.dundermifflin.com.CNAME 7 days machinec.dundermifflin.com.platen.dundermifflin.com. CNAME 7 days machined.dundermifflin.com.chase.dundermifflin.com. CNAME 7 days machinee.dundermifflin.com.roller.dundermifflin.com. CNAME 7 days machinef.dundermifflin.com. saddle.dundermifflin.com. CNAME 7 days

dundermifflin.com. 5

carriage.dundermifflin.com CNAME minutes

www.dundermifflin.com. 5

carriage.dundermifflin.com CNAME minutes

www2.dundermifflin.com. 5

saddle.dundermifflin.com. CNAME minutes

ftp.dundermifflin.com. 5

platen.dundermifflin.com. CNAME minutes

files.dundermifflin.com. roller.dundermifflin.com. CNAME 7 days

Submission Requirements

1. Please submit your notes as a .txt or .pdf file.

2. The dns server must be reachable and resolve dns requests for names external to D-M. It must also act as an authoritative server for the dundermifflin.com. domain

3. All names in the table above must be valid, point to the proper location, with the appropriate record type and time to live.

4. The hostnames on your machines must change to those outlined in the table above. The old names, machine a,b,c,d, e, and f, should still be valid on your DNS server.

5. The dhcp server running on router should push both the resolving dns server (100.64.N.4) and search path (dundermifflin.com) to all clients.

Hints &amp; Troubleshooting

The existing public key in /root/.ssh/authorized_keys labeled saclass-admins@donotremove must remain on all production machines, otherwise I won’t be able to login and grade your work.

If machine E cannot resolve dns queries with named running on machine D, ensure that allowquery { any; }; is set in the global bind options directive, right under listen-on {};.

Use the named-checkconf and named-checkzone programs to identify syntax errors in configuration files.

If bind appends a domain name to your hostname twice; e.g., chase.dundermifflin.com.dundermifflin.com., you likely forgot a dot somewhere in a zone file.

If you get a srvfail error message or no results for dundermifflin.com at all then double check your filesystem permissions on the zone file in /var/named/. The user named must be able to read all zone files.

Extra Challenges

Configure machine C to act as a slave/secondary dns server for the dundermifflin.com zone and accept zone transfers from the master/primary dns server on machine D.
