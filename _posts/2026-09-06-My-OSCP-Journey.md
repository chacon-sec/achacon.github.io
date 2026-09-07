<center>
    <h1>
        <strong>Intro</strong>
    </h1>
</center>
Around 2 years ago when I first got started in cybersecurity I did not consider offensive security to be a path that I would go down. A lot of that stemmed from imposter syndrome and a fear that I could never be technical enough to go down this path, but after passing Certified Red Team Operator by Zero Point Security back in June of 2024, I fell in love with offensive security and made it a goal for myself to dedicate the rest of the time in college to studying offensive security. So my main goal post CCDC season was to get my OSCP. In total, it took me around 10 months of really applying myself to get my OSCP so, here is my journey.
<!-- more -->

<center>
    <img src="/assets/img/oscp-journey/oscp-badge.png">
</center>

<center>
    <h1>
        <strong>My Background</strong>
    </h1>
</center>
When I started my OSCP journey I was pretty familiar with cybersecurity as a whole and would consider myself decently technical. I had competed in three cybersecurity competitions (CCDC, NCAE, and CyberForce) so I was familiar with the Linux CLI, had decent knowledge of Linux / web attacks, and hands on experience with Active Directory attacks. Post June 2024 after CRTO I ended up joining my schools CCDC team, working an internship during the summer, and working a part-time job as a full-time student so not much offensive security work got done from June 2024 - January 2025. Unfortunately (or depending on how you see it, fortunately) our CCDC season was cut short so I was able to focus on more offensive security related things.

<center>
    <h1>
        <strong>The Box Grind</strong>
    </h1>
</center>
My main study material came from doing Hack The Box / Proving Ground machines. A curated list of "OSCP Like" machines made by [**LainKusanagi**](https://medium.com/@luisgerardomoret_69654) and can be found [here](https://docs.google.com/spreadsheets/d/18weuz_Eeynr6sXFQ87Cd5F0slOj9Z6rt/edit?gid=487240997#gid=487240997). I would recommend going through at least all of the Hack The Box and Proving Ground machines before buying the OSCP Course.

<center>
    <img src="/assets/img/oscp-journey/box-grind.svg">
</center>

<center>
    <h2>
        <strong>Hack The Box</strong>
    </h2>
</center>

<center>
    <img src="/assets/img/oscp-journey/hackthebox.jpg" width="450">
</center>
From January 2025 - August 2025 I grinded out around ~60 boxes on the platform Hack The Box. I mainly utilized this platform to perfect my pentesting methodology and get comfortable with going through the motions. When doing boxes on HackTheBox I **heavily** relied on writeups to get me through these boxes. My rule was if I did not make any progress within an hour, I would go to a writeup for a nudge and I think this helped me learn and improve a lot faster. Also, even if I did complete a machine without using a writeup, I would still go back and read the writeup and take notes because the writeup author might have used a technique, or tool that I may have missed that could make my life easier.
<details>
    <summary><strong>Why use writeups when you can <del>try harder</del>?</strong></summary>
    <p>When starting out with pentesting, in my opinion, there is only so much you know and so much more you do not know. Spending 6 hours bashing your head against a wall only to find out you made 0 progress on a box because you used the wrong wordlist is not a productive use of your time. When starting out, do not feel bad about using writeups, but also do not depend on them. During your exam you won't have a writeup so really reinforce your methodology, and as you complete more boxes use writeups less.</p>
</details>

<center>
    <h2>
        <strong>Proving Grounds</strong>
    </h2>
</center>

<center>
    <img src="/assets/img/oscp-journey/proving-grounds.png">
</center>
Once I had completed all the Hack The Box machines I moved onto Proving Grounds, which is essentially Offsec's version of HTB Labs and contain the real "OSCP like" machines. From August 2025 - September 2025 I completed around 40 boxes and found these machines **significantly** easier than their HTB counterparts and more accurately reflected what I saw on my exam. I hardly used writeups when completing these machines and found myself rooting them in 2-4 hours depending on the difficulty of the machine. I would really recommend not skipping out on Proving Grounds as doing these machines pre-OSCP really helped me get used to Offsec styled boxes. If you can root the machines on this platform without using writeups in a timely manner, I'd say you're probably ready to buy the course.

<center>
    <h1>
        <strong>Going All In</strong>
    </h1>
</center>
Once I completed my list of machines and felt comfortable with rooting boxes on proving grounds I decided to buy the course. When I got access I briefly skimmed over the course material, skipping the knowledge checks, and wrote down anything that I did not already have in my notes. This took me a couple of hours and then I moved onto the challenge labs.
The challenge labs that I did mimicked the exam environment that you will be provided during the OSCP exam. I ended up doing OSCP A, OSCP B, OSCP C, and Secura in a weekend. This made me feel comfortable with the exam format, timing, and most importantly pivoting. Really practice your pivoting tooling and methodology here so you do not run into any hiccups during your exam.
<details>
    <summary><strong>Why not do ALL of the challenge labs?</strong></summary>
    <p>From my research, the challenge labs that I decided to do would most accurately reflect what I would see on the exam. Also I was pretty burnt out and tired up to this point, having just come back from an internship, and grinded out in total including the challenge labs, about another 70 boxes in just 45 days. All I wanted to do was take my exam. I also felt it would be a waste of time for me to do more lab practice, especially since I needed to prep for CPTC.</p>
</details>

<center>
    <h1>
        <strong>The Exam</strong>
    </h1>
</center>

<center>
    <img src="/assets/img/oscp-journey/cat-drown-milk.webp">
</center>
Once I had completed all of my prep material I scheduled my exam for a couple of days later at 10am on a Wednesday. The morning of my exam was like any other day. Woke up at 8am, ate breakfast, did my morning routine, and then logged into the Offsec exam portal by 9:45am.

<center>
    <img src="/assets/img/oscp-journey/exam-timeline.svg">
</center>

<center>
    <h2>
        <strong>Hiccups</strong>
    </h2>
</center>
My first exam hiccup was that the resolution on my webcam was not good enough to verify my ID so I needed to take a picture of my ID, send it to myself, and then upload it to the exam portal. That was no biggie and I resolved it very quick. The next hiccup was with my PC monitors. I spent about an hour trying to get the proctoring software to detect my second monitor. Eventually I told myself that if I failed my exam because I did not have two monitors, then I was not gonna pass in the first place. At this point I unplugged my second monitor, put it on the floor, and was ready to start the exam.

<center>
    <h2>
        <strong>Active Directory Set</strong>
    </h2>
</center>
With the new OSCP+ changes, Active Directory is now an assumed breach scenario. I felt most comfortable with Active Directory so I decided to start out with Active Directory. Within two hours I had full pwned the whole Active Directory set, taken my screenshots for my report and was ready to move onto the standalone machines.

<center>
    <h2>
        <strong>Standalones</strong>
    </h2>
</center>
The stand alone machines took me a significantly longer time to get access and pwn. For a good 6 hours I made 0 progress on getting initial access onto any of the machines and found myself getting tunnel visioned on the same rabbit holes that did not work. I had only really eaten breakfast at this point and decided to take a break to eat food and nap. I ended up resuming my exam after about a 90 minute break and this is when I started making progress.

<center>
    <h2>
        <strong>The Final Push</strong>
    </h2>
</center>
After re-going through my enumeration steps, I realized that I had skipped a crucial part of my enumeration process on all machines I had worked on. Once I realized and enumerated more I had found a way to gain initial access on one machine and started looking for privilege escalation vectors. I did this for about an hour and after going through some rabbit holes, I decided to go and check out the other machines.
I decided to repeat the crucial enumeration step I had missed and managed to gain access to another standalone. The privilege escalation on this machine was easy to identify and I escalated privileges very quickly, netting me enough points to pass the exam 12 hours into my exam.

<center>
    <h2>
        <strong>Wrapping It All Up</strong>
    </h2>
</center>
Once I had gained enough points to pass, I took a little break but kept my exam running and decided that I would finish my report while I still had access to the environment. This was very advantageous for me as I was missing some crucial screenshots for my report. I ended up finishing my report a couple of hours later and re-read it more times than I can remember. At this point it was 4am in the morning and I didn't feel like continuing the exam so I ended my exam and went to sleep. When I woke up I re-read my report a couple of more times and submitted my report. 7 days later, I was OSCP certified!

<center>
    <img src="/assets/img/oscp-journey/offsec-email.png">
</center>

<center>
    <h1>
        <strong>My Expectations and Opinions</strong>
    </h1>
</center>
Overall I think with OSCP it's important to manage expectations and the amount you can accomplish given a set amount of time and life circumstances. My plan originally was to get my OSCP before summer of 2025 but because of school, work, and just life in general it ended up taking me a couple of more months. One thing that I value a lot is a good work-life balance. During my OSCP prep I definitely had to make some sacrifices in my personal life when it came to my hobbies, but it was manageable and I didn't let cyber consume every aspect of my life. My advice to anyone else in a similar situation such as me, and something that I struggled with all throughout college, is to stop comparing your pace to people who have the privilege to study 8+ hours a day for a certification exam. That comparison will demoralize you fast. Set realistic goals that are attainable for your situation. Dedicating 1-2 hours a day where you can focus on studying for an exam adds up over months, and those opportunities where you do get that free time, take advantage of it.
Ultimately I do think that OSCP is worth it if you're trying to resume-maxx / interview-maxx. Post certification, the difference in interview opportunities has been night and day for me. Recruiters and hiring managers take notice of it, and having it on your resume gets your foot in the door in ways that other certifications do not.

<center>
    <h1>
        <strong>Resources</strong>
    </h1>
</center>
* **[Certified Red Team Operator — Zero Point Security](https://courses.zeropointsecurity.co.uk/courses/red-team-ops)** - The course that started it all for me. Great intro to Cobalt Strike, C2, and red team tradecraft in a Windows domain lab.
* **[Hack The Box](https://app.hackthebox.com)** - Where I built my pentesting methodology across ~60 machines. Progress beats perfection here.
* **[OffSec Proving Grounds](https://www.offsec.com/labs/)** - The most exam-accurate practice machines out there. Do not skip these.
* **[LainKusanagi's OSCP-like machine list](https://docs.google.com/spreadsheets/d/18weuz_Eeynr6sXFQ87Cd5F0slOj9Z6rt/edit?gid=487240997#gid=487240997)** - The curated list I worked through. ([his Medium here](https://medium.com/@luisgerardomoret_69654))
* **[IppSec](https://www.youtube.com/@IppSec)** - Watch HTB walkthroughs, take notes, and steal his methodology.
* **[PEN-200 / OSCP+ Course](https://www.offsec.com/courses/pen-200/)** - The course itself, plus the official exam guide.
