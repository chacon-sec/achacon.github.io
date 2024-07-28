
------
------
<center>
    <h1>
        <strong>Intro</strong>
    </h1>
</center>
Cyberforce is a cybersecurity competition hosted by the Department of Energy designed to simulate a real world attack on American critical infrastructure. This year the competition hosted over 100 teams with over 95 teams competing. Overall it went really well, considering five out of the six people on the team were first time competitors, me included(I won’t spoil our placement). My cybersecurity skills before this competition consisted of me doing Bandit on OverTheWire and some TryHackMe rooms but the preparation and competing in this competition has taught me a lot.
<!-- more -->

<center>
    <h1>
        <strong>Competition Overview</strong>
    </h1>
</center>
CyberForce isn’t your traditional cybersecurity competition like CCDC, CPTC, or even NCAE. There is preparatory work that has to be submitted prior to the competition day that will affect your teams overall score. To simplify what points would count for what let me break down the different ways we were scored during the competition
* **Red Team 2500** - There were 2 components to red team scoring. The first part consisted of traditional external pentesting where they attacked the boxes we secured. The other part was something called “Assumed Breach” where the Red Team is already given access to out boxes and attack us with predetermined attack chains. Defenders have to find out what they did and report it to their Red Teamer.
* **Blue Team 2000** - This component was essentially just service uptime and any additional energy you sold back to the power grid during the competition. Red Team really doesn’t mess with your services so it is pretty easy to get the full 2000.
* **Green Team 1500** - Green Team consists of a team of volunteers that runs checks on a website that you have to fix and configure to certain specifications. This again is pretty easy to get MOST of the points, as long as you configure the website to the right specifications, it is easy to get these points.
* **Orange Team 2000** - There were 2 components to the Orange Team score. The first part was a C-Suite panel brief, which basically is a 5 minute video discussing the business risk associated with a breach of a large number of smart meters. The video was to be submitted 2 weeks before the competition, before we got our infrastructure. The second part was security documentation which consisted of us writing about the vulnerabilities we found, an essay of the hardening of our machines, and a network diagram. This was to be submitted 1 week before the competition.
* **Anomaly Scoring 2000** - 8 hour long CTF.

<center>
    <img src="https://i.gyazo.com/00a7bb3a0c22b6042cde8fb8d129a720.png">
</center>

<center>
    <h1>
        <strong>Preparation</strong>
    </h1>
</center>
Preparation for the competition was pretty open ended. It mostly consisted of us setting up an environment that would be close to what we would see in the competition and then essentially purple teaming and testing our SIEM so that we would be ready for incident response during the competition. 
We ended up choosing Wazuh to be our SIEM of choice because it is very lightweight and seemed to get the job done(decently). Wazuh isn’t very good right out of the box so it took some time learning how to configure it but eventually one of my team members figured out how to configure it well enough for the competition. 
All of us also competed in NCL to get some experience in CTF challenges.

<center>
    <h1>
        <strong>Infrastructure</strong>
    </h1>
</center>
We were assigned 6 boxes with various services running on those boxes
<center>
    <img src="https://i.gyazo.com/f724df4a98c1054ca95dd3e9865a6389.png">
</center>
* **Web Server (CentOS 7)** -  Hosted a vulnerable web server. Ran SMTP
* **CNC (Windows Server 2016)** - edr.energy.local domain controller. Hosted the HMI to interact with the simulated houses on the PLC box.
* **PLC (Ubuntu 18.04)** - ICS that communicated with the DER that would send information to the HMI. Didn’t run any scored services.
* **Task Box (Windows Server 2022)** - Ran the company website, FTP, SMB, and RDP.
* **AD/DNS (Windows Server 2019)** - energy.local domain controller. Ran VNC and SSH.
* **Public DB (OpenSUSE 15)** - Ran NFS and SNMP. Not an actual database, more of a file sharing server.

<center>
    <h1>
        <strong>27 Days</strong>
    </h1>
</center>
From the day at which we were assigned the C-Suite Panel video to when we were actually going to compete was 27 Days. The first week from October 15th to October 22nd was the time we had to do our C-Suite Panel video. It really wasn’t hard. It took 2 people (me and a team member) 3 days to get it done. 2 days to prepare and 1 day to film. The preparation was mostly us trying to figure out what a distributed energy resource was and what a smart meter was. The rest was easy, just talked about mitigation techniques the company can implement now and some long term mitigation techniques. The filming part took about 2 hours because zoom is funny but it came out pretty good as we got about 900/1000 points. 

From October 23rd to October 30th was the time we had to do our security documentation. We utilized NESSUS and WinPeas/LinPeas to do most of our vulnerability assessment. We also did some manual enumeration to find some things that those scanners did not pick up. We spent most of the week just finding vulnerabilities and ways to harden our machines, the real report writing took place on October 29th and October 30th. I think we started writing the documentation around 6PM on the 29th and finished it on the 30th at 4AM. Top 5 college moments for me was when we moved one picture on sharepoint and it somehow deleted what was in our tables at 3AM and we had to remake the whole thing on Google Docs. I couldn’t help but just laugh for like 5 minutes. We ended up getting like 905/1000 points so it was definitely worth staying up till 4AM fixing our documentation.

From October 31st to November 3rd was the time we had to do more hardening and make a game plan for competition day. We ended up setting up some firewalls and found some more vulnerabilities on our machines. The game plan for the competition day was to assign 4 people to watch the 3 boxes that weren’t assumed breach and just do anomalies and then the 2 other people to do assumed break and anomalies but that went right out the window an hour into the competition.

<center>
    <h1>
        <strong>Competition Day</strong>
    </h1>
</center>
The day started off with me doing my normal morning routine then heading off to breakfast. The nerves were definitely getting to me and the cold ball room did not help with that. The competition started at 10AM and would last till 6PM.

I was assigned to watch the Public DB and AD/DNS box as those were the two boxes that I spent the most time hardening and doing vulnerability assessment. We quickly realized that they weren’t even attacking those boxes and after an hour and losing 2 red team blocks due to connectivity issues, I was assigned to do the assumed breach. The start of my assumed breaches looked something like this.

<center>
    <img src="https://i.gyazo.com/493d1da81ec8ff6904bb28dfa8cc5e20.png">
</center>

After this I started to get the hang of it. My eyes were glued to Wazuh, Windows Event Logs, and /var/log/auth.log. My messages to the red teamer started to look a lot better, which boosted my confidence and overall made me perform better.

<center>
    <img src="https://i.gyazo.com/ac444e80c341de2de7bb3faf49895aa3.png">
</center>

<center>
    <img src="https://i.gyazo.com/24daa6e9459019e4348f7deca61cf04f.png">
</center>

There was also a whack-a-mole component to this competition where the red team would attack our secured machines and see what vulnerabilities were still there. We did pretty good in that as well getting most of the points for both whack-a-mole events.

<center>
    <img src="https://i.gyazo.com/97380c55c1cbee175762e3920803034d.png">
</center>

Our incident response was pretty good and by the end of the competition I think we had around 1300 red team points and the top team had somewhere around 1500. I only really got to work on like 3 anomalies during the whole comp because I was so bogged down with incident response but, doing incident response was really fun and satisfying.

One area where my team definitely lacked during the competition was anomalies. The difficulty of anomalies in this competition were way above the levels of anyone on my team. One of my teammates is pretty cracked and placed well in NCL, but not even he could solve a lot of the challenges. Guess this just means we need to grind ctf time and read a lot more writeups!

Our Green Team and Blue Team scoring were very good as well. Most teams got full points for Blue Team because they didn't attack any boxes that were hosting the services that were scored. Setting up the Green Team website was a pain for one of my members, but once he got it running we got most of the points for the website the rest of the competition which really boosted us up. 

<center>
    <h1>
        <strong>Results</strong>
    </h1>
</center>

At the end of the day I was really proud of all of my teammates for their hard work and dedication to this competition. We ended up in 16th place out of 104 teams, which was a lot better than anyone expected(only 1 team member had competed in a RvB style cyber competition before this). If I could go back and do anything different for this competition, I would have more people assigned to incident response and learn how to do incident response better. It was decent enough to land us a good placement, but those extra points definitely could have moved us up a place or two. Oh I also need to grind ctf time and hack the box.

<center>
    <img src="https://media.licdn.com/dms/image/D5622AQFWE24EWC3IoQ/feedshare-shrink_800/0/1699428640616?e=1712188800&v=beta&t=RiDPsVbWGcQLSVRt-vtxTsR-XRwZDZDamVdrJ4LAlXM">
</center>

<center>
    <h1>
        <strong>My Thoughts</strong>
    </h1>
</center>

Honestly, I could not have asked for a better competition to compete in to jump start my cyber journey. There was not really an expectation for us to do to well during the competition because a lot of us were new to cyber, so there was a lot of weight lifted off my shoulders when it came to how we would place(we ended up doing good anyways though). The competition structure is also very enjoyable and well structured. From the vulnerability assessment to the actual day of, I definitely feel like I learned a lot. 

At the end of the day the competition was really fun and I am really excited to see what the future holds for me in this field. I hope to return to this competition and hope to compete in a lot more cyber competitions(NCAE soon?) as they are really fun. 

Oh and a little note, this was written on in Febuary of 2024 so its really short because I honestly forgot a lot and lost a lot of documentation. XC