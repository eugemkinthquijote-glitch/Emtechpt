<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CyberGuard | Cybersecurity & Online Safety</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
    font-family:Arial,Helvetica,sans-serif;
    background:#07111f;
    color:#eef8ff;
    line-height:1.6;
}
a{color:inherit}
nav{
    position:sticky;top:0;z-index:1000;
    display:flex;justify-content:space-between;align-items:center;
    padding:16px 7%;
    background:rgba(5,15,28,.94);
    border-bottom:1px solid #1d405c;
    backdrop-filter:blur(10px);
}
.logo{font-size:22px;font-weight:800;color:#38e8ff}
nav ul{display:flex;gap:22px;list-style:none}
nav a{text-decoration:none;color:#d9e9f4;font-size:14px}
nav a:hover{color:#38e8ff}
.hero{
    min-height:88vh;display:flex;align-items:center;justify-content:center;
    text-align:center;padding:70px 7%;
    background:
      radial-gradient(circle at 50% 20%,#124d6b 0,#0b253b 28%,transparent 58%),
      linear-gradient(145deg,#06101d,#07111f 55%,#0a1d2d);
}
.hero-inner{max-width:900px}
.shield{
    width:110px;height:110px;margin:0 auto 22px;
    display:flex;align-items:center;justify-content:center;
    border:2px solid #38e8ff;border-radius:28px;
    background:#0b2437;box-shadow:0 0 40px rgba(56,232,255,.18);
    font-size:56px;
}
.eyebrow{letter-spacing:3px;color:#72c9db;font-size:13px;font-weight:bold}
.hero h1{font-size:clamp(40px,7vw,72px);line-height:1.05;margin:14px 0}
.hero h1 span{color:#38e8ff}
.hero p{max-width:720px;margin:0 auto 28px;color:#b8cad8;font-size:18px}
.btn{
    display:inline-block;text-decoration:none;
    padding:13px 24px;border-radius:9px;
    background:#38e8ff;color:#04101a;font-weight:bold;
    margin:5px;transition:.25s;
}
.btn:hover{transform:translateY(-3px);background:#fff}
.btn.alt{background:transparent;color:#38e8ff;border:1px solid #38e8ff}
section{padding:82px 7%}
.section-head{text-align:center;max-width:760px;margin:0 auto 42px}
.section-head h2{font-size:36px;color:#38e8ff;margin-bottom:8px}
.section-head p{color:#9fb4c5}
.panel{
    max-width:980px;margin:auto;
    background:#0b1d2e;border:1px solid #1c405b;
    border-radius:20px;padding:30px;
    box-shadow:0 15px 45px rgba(0,0,0,.16);
}
.panel p{color:#c5d4df}
.fact-grid,.card-grid,.tip-grid,.team-grid{
    display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:18px;
}
.fact{
    padding:24px;border-radius:16px;background:#0c2235;border:1px solid #1b435e;
}
.fact strong{display:block;font-size:29px;color:#38e8ff;margin-bottom:5px}
.fact span{color:#a9bdcb;font-size:14px}
.card{
    padding:25px;border-radius:18px;background:#0b1d2e;
    border:1px solid #1c405b;transition:.25s;
}
.card:hover{transform:translateY(-6px);border-color:#38e8ff;box-shadow:0 15px 35px rgba(56,232,255,.08)}
.icon{font-size:35px;margin-bottom:10px}
.card h3{margin-bottom:8px}
.card p{color:#9fb4c5;font-size:14px}
.badge{
    display:inline-block;margin-top:13px;padding:4px 9px;border-radius:99px;
    font-size:11px;background:#12354b;color:#75dcec
}
.tip{
    padding:22px;border-left:4px solid #38e8ff;
    background:#0b1d2e;border-radius:12px;border-top:1px solid #173a55;
    border-right:1px solid #173a55;border-bottom:1px solid #173a55;
}
.tip h3{color:#38e8ff;font-size:17px;margin-bottom:6px}
.tip p{color:#b0c2d0;font-size:14px}
.steps{counter-reset:step;display:grid;gap:14px;max-width:900px;margin:auto}
.step{
    counter-increment:step;display:flex;gap:18px;align-items:flex-start;
    padding:20px;background:#0b1d2e;border:1px solid #1b405b;border-radius:14px
}
.step:before{
    content:counter(step);min-width:38px;height:38px;border-radius:50%;
    display:flex;align-items:center;justify-content:center;
    background:#38e8ff;color:#06111d;font-weight:bold
}
.step h3{margin-bottom:4px}.step p{color:#aebfcd;font-size:14px}
.warning{
    max-width:980px;margin:auto;padding:30px;border-radius:20px;
    background:linear-gradient(135deg,#173a4d,#0b1b2b);
    border:1px solid #2c667d;text-align:center
}
.warning h2{color:#38e8ff;margin-bottom:8px}
.warning p{color:#c3d2dd}
details{
    background:#0b1d2e;border:1px solid #1b405b;border-radius:12px;
    padding:17px 20px;margin-bottom:10px
}
summary{cursor:pointer;font-weight:bold;color:#e9f8ff}
details p{color:#aebfcd;margin-top:10px;font-size:14px}
.source{
    display:flex;gap:18px;align-items:flex-start;
    background:#0b1d2e;border:1px solid #1b405b;
    padding:22px;border-radius:15px;margin-bottom:14px
}
.source-num{
    min-width:38px;height:38px;border-radius:50%;
    background:#123a50;color:#38e8ff;
    display:flex;align-items:center;justify-content:center;font-weight:bold
}
.source h3{margin-bottom:4px}
.source p{color:#aebfcd;font-size:14px}
.source a{display:inline-block;margin-top:8px;color:#38e8ff;text-decoration:none;font-size:13px}
.source a:hover{text-decoration:underline}
.apa{
    margin-top:25px;padding:22px;background:#081726;
    border:1px dashed #28506b;border-radius:14px
}
.apa h3{color:#38e8ff;margin-bottom:10px}
.apa p{color:#aebfcd;font-size:13px;margin:7px 0}
.quiz{max-width:800px;margin:auto}
.question{
    background:#0b1d2e;border:1px solid #1b405b;border-radius:15px;
    padding:22px;margin-bottom:14px
}
.question h3{font-size:16px;margin-bottom:12px}
.option{
    display:block;padding:9px 12px;margin:6px 0;border-radius:8px;
    background:#10283c;color:#c4d4df;cursor:pointer
}
.option:hover{background:#14354d}
.result{
    display:none;text-align:center;margin-top:18px;
    padding:20px;border-radius:12px;background:#0e3042;color:#cfeaf3
}
.team-grid{max-width:1050px;margin:auto}
.member{
    background:#0b1d2e;border:1px solid #1b405b;border-radius:16px;
    padding:22px;text-align:center;transition:.25s
}
.member:hover{border-color:#38e8ff;transform:translateY(-4px)}
.avatar{font-size:30px;margin-bottom:8px}
.member h3{font-size:15px}.member p{font-size:12px;color:#38e8ff;margin-top:5px}
footer{
    padding:38px 7%;text-align:center;background:#040b13;
    border-top:1px solid #17334a;color:#8298a9
}
footer strong{color:#38e8ff}
@media(max-width:700px){
    nav{flex-direction:column;gap:12px}
    nav ul{gap:10px;flex-wrap:wrap;justify-content:center}
    section{padding:65px 5%}
    .hero{min-height:82vh}
    .hero p{font-size:16px}
    .panel{padding:22px}
}
</style>
</head>

<body>

<nav>
    <div class="logo">🛡️ CYBERSHIELD</div>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#threats">Threats</a></li>
        <li><a href="#safety">Safety</a></li>
        <li><a href="#resources">RRL</a></li>
        <li><a href="#team">Team</a></li>
    </ul>
</nav>

<section class="hero" id="home">
    <div class="hero-inner">
        <div class="shield">🛡️</div>
        <div class="eyebrow">GRADE 12 • STEM 3</div>
        <h1>Protect Your <span>Digital Life.</span></h1>
        <p>
            A student-friendly guide to cybersecurity, online safety,
            privacy, digital footprints, common cyber threats, and
            responsible internet use.
        </p>
        <a class="btn" href="#about">Explore the Guide ↓</a>
        <a class="btn alt" href="#quiz">Take the Safety Check</a>
    </div>
</section>

<section id="about">
    <div class="section-head">
        <h2>What Is Cybersecurity?</h2>
        <p>Understanding why digital protection matters.</p>
    </div>
    <div class="panel">
        <p>
            Cybersecurity is the practice of protecting computers, mobile
            devices, networks, accounts, and information from unauthorized
            access, damage, misuse, or other digital threats.
        </p>
        <br>
        <p>
            Online safety is closely connected to cybersecurity. It includes
            making responsible choices online, protecting personal information,
            recognizing suspicious activity, and treating other people
            respectfully in digital spaces.
        </p>
        <br>
        <p>
            For students, cybersecurity is not only a technical issue.
            Everyday actions such as choosing passwords, clicking links,
            posting information, downloading files, and using social media
            can affect digital privacy and security.
        </p>
    </div>
</section>

<section>
    <div class="section-head">
        <h2>Why Does Online Safety Matter?</h2>
        <p>Young people spend a significant part of their lives in digital spaces.</p>
    </div>
    <div class="fact-grid">
        <div class="fact"><strong>Privacy</strong><span>Personal information can create risks when it is shared carelessly.</span></div>
        <div class="fact"><strong>Security</strong><span>Accounts and devices can be targeted by scams, malware, and unauthorized access.</span></div>
        <div class="fact"><strong>Reputation</strong><span>Posts, comments, photos, and other online activity can contribute to a digital footprint.</span></div>
        <div class="fact"><strong>Well-being</strong><span>Cyberbullying and other harmful online experiences can negatively affect young people.</span></div>
    </div>
</section>

<section id="threats">
    <div class="section-head">
        <h2>⚠️ Common Cyber Threats</h2>
        <p>Know what you are dealing with before you react.</p>
    </div>
    <div class="card-grid">
        <div class="card"><div class="icon">🎣</div><h3>Phishing</h3><p>Fraudulent messages or websites that imitate trusted people or organizations to trick users into revealing information or clicking harmful links.</p><span class="badge">Think before clicking</span></div>
        <div class="card"><div class="icon">🦠</div><h3>Malware</h3><p>Malicious software that may disrupt a device, damage files, or gain unauthorized access to information.</p><span class="badge">Avoid unknown downloads</span></div>
        <div class="card"><div class="icon">🎭</div><h3>Online Scams</h3><p>Deceptive messages, offers, or websites designed to manipulate people into giving money, information, or account access.</p><span class="badge">Verify first</span></div>
        <div class="card"><div class="icon">🔑</div><h3>Password Attacks</h3><p>Attempts to gain access to accounts by stealing, guessing, reusing, or obtaining passwords.</p><span class="badge">Use unique passwords</span></div>
        <div class="card"><div class="icon">💬</div><h3>Cyberbullying</h3><p>Repeated harmful behavior using digital platforms to harass, embarrass, threaten, or hurt another person.</p><span class="badge">Report & seek help</span></div>
        <div class="card"><div class="icon">🪪</div><h3>Identity Theft</h3><p>Using another person's personal information without permission, potentially affecting accounts, privacy, or reputation.</p><span class="badge">Protect personal data</span></div>
        <div class="card"><div class="icon">📢</div><h3>Misinformation</h3><p>False or inaccurate information can spread quickly online. Check the source and compare important claims before sharing.</p><span class="badge">Check the source</span></div>
        <div class="card"><div class="icon">📱</div><h3>Unsafe Apps & Links</h3><p>Unknown apps, downloads, QR codes, and links may lead to scams, unwanted software, or information collection.</p><span class="badge">Use trusted sources</span></div>
    </div>
</section>

<section id="safety">
    <div class="section-head">
        <h2>🔐 How to Stay Safe Online</h2>
        <p>Simple habits can make your digital life much safer.</p>
    </div>
    <div class="tip-grid">
        <div class="tip"><h3>01 — Use Strong, Unique Passwords</h3><p>Use long, difficult-to-guess passwords and avoid reusing the same password across important accounts.</p></div>
        <div class="tip"><h3>02 — Turn On MFA</h3><p>Multifactor authentication adds another verification step beyond your password.</p></div>
        <div class="tip"><h3>03 — Recognize Phishing</h3><p>Be cautious with unexpected messages, urgent requests, suspicious links, and offers that seem too good to be true.</p></div>
        <div class="tip"><h3>04 — Protect Personal Information</h3><p>Think carefully before sharing your full name, address, phone number, passwords, school details, or other sensitive information.</p></div>
        <div class="tip"><h3>05 — Keep Devices Updated</h3><p>Install trusted software and security updates when they become available.</p></div>
        <div class="tip"><h3>06 — Check Before Sharing</h3><p>Look at the source, date, evidence, and other reliable references before spreading information.</p></div>
        <div class="tip"><h3>07 — Review Privacy Settings</h3><p>Check who can see your posts, contact you, or access information connected to your accounts.</p></div>
        <div class="tip"><h3>08 — Be Respectful Online</h3><p>Think about how your words and actions may affect other people. Report harmful behavior instead of joining it.</p></div>
    </div>
</section>

<section>
    <div class="section-head">
        <h2>🧭 Your Digital Footprint</h2>
        <p>What happens online can become part of your long-term digital record.</p>
    </div>
    <div class="panel">
        <p>
            A digital footprint is the record of information and activity
            connected to a person's online presence. Posts, comments,
            photos, accounts, and interactions can contribute to that record.
        </p>
        <br>
        <p>
            Before posting, ask yourself: <b>Would I be comfortable if this
            were seen by my family, teacher, future school, or future employer?</b>
            Privacy settings can help, but they do not guarantee that
            information will never be copied or shared.
        </p>
    </div>
</section>

<section>
    <div class="section-head">
        <h2>🚨 If Something Goes Wrong</h2>
        <p>Do not panic. Take sensible steps and ask a trusted adult for help when needed.</p>
    </div>
    <div class="steps">
        <div class="step"><div><h3>Stop interacting</h3><p>Do not continue clicking suspicious links, replying to suspicious messages, or sending additional information.</p></div></div>
        <div class="step"><div><h3>Secure your account</h3><p>If an account may be compromised, change the password from a trusted device and enable multifactor authentication if available.</p></div></div>
        <div class="step"><div><h3>Save evidence</h3><p>Keep relevant messages, usernames, dates, or screenshots if you need to report the incident.</p></div></div>
        <div class="step"><div><h3>Report and ask for help</h3><p>Use the platform's reporting tools and tell a trusted parent, teacher, guardian, or appropriate authority when necessary.</p></div></div>
    </div>
</section>

<section>
    <div class="warning">
        <h2>🧠 The Golden Rule</h2>
        <p>
            <b>STOP → THINK → VERIFY → ACT.</b><br>
            If a message, account, link, or offer makes you feel pressured,
            slow down and verify it using a trusted source.
        </p>
    </div>
</section>

<section id="quiz">
    <div class="section-head">
        <h2>🧪 Quick Safety Check</h2>
        <p>Test what you learned. This is an educational activity only.</p>
    </div>

    <div class="quiz">
        <div class="question">
            <h3>1. You receive an unexpected message asking you to click a link and verify your password. What should you do?</h3>
            <label class="option"><input type="radio" name="q1" value="0"> Click immediately.</label>
            <label class="option"><input type="radio" name="q1" value="1"> Stop and verify the message through a trusted source.</label>
            <label class="option"><input type="radio" name="q1" value="0"> Send your password first.</label>
        </div>

        <div class="question">
            <h3>2. Which is the safer password practice?</h3>
            <label class="option"><input type="radio" name="q2" value="0"> Use the same password everywhere.</label>
            <label class="option"><input type="radio" name="q2" value="1"> Use long, unique passwords for important accounts.</label>
            <label class="option"><input type="radio" name="q2" value="0"> Share your password with friends.</label>
        </div>

        <div class="question">
            <h3>3. What is a digital footprint?</h3>
            <label class="option"><input type="radio" name="q3" value="1"> The record of information and activity connected to your online presence.</label>
            <label class="option"><input type="radio" name="q3" value="0"> A type of computer virus.</label>
            <label class="option"><input type="radio" name="q3" value="0"> A password recovery method.</label>
        </div>

        <button class="btn" onclick="checkQuiz()">Check My Answers</button>
        <div class="result" id="result"></div>
    </div>
</section>

<section id="resources">
    <div class="section-head">
        <h2>📚 RRL & Supporting Resources</h2>
        <p>Our website is supported by credible organizations and Philippine-focused resources.</p>
    </div>

    <div class="panel">

        <div class="source">
            <div class="source-num">1</div>
            <div>
                <h3>UNICEF — Safety in Digital Education</h3>
                <p>
                    UNICEF explains that digital learning creates opportunities for children
                    while also introducing risks that need to be managed, including
                    cyberbullying, privacy, data protection, and other online safety concerns.
                </p>
                <a href="https://www.unicef.org/digitaleducation/safety" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="source">
            <div class="source-num">2</div>
            <div>
                <h3>UNICEF Philippines — Philippines Kids Online</h3>
                <p>
                    This Philippine study examines children's online experiences,
                    opportunities, risks, and barriers and was designed to help inform
                    efforts toward a safer online environment for Filipino children.
                </p>
                <a href="https://www.unicef.org/philippines/reports/philippines-kids-online" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="source">
            <div class="source-num">3</div>
            <div>
                <h3>National Privacy Commission — Kabataang Digital</h3>
                <p>
                    The NPC's Kabataang Digital campaign promotes safe online environments
                    for Filipino youth and teaches data protection, digital citizenship,
                    privacy rights, and safe choices online.
                </p>
                <a href="https://privacy.gov.ph/kd/" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="source">
            <div class="source-num">4</div>
            <div>
                <h3>National Privacy Commission — Kabataang Digital 2023</h3>
                <p>
                    The campaign provided students with knowledge about digital privacy,
                    online safety, age-appropriate use of online platforms, and the
                    implications of the digital environment for children's privacy rights.
                </p>
                <a href="https://privacy.gov.ph/kabataang-digital-2023-npc-raises-youth-awareness-on-data-privacy-and-online-safety/" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="source">
            <div class="source-num">5</div>
            <div>
                <h3>CISA — Secure Our World</h3>
                <p>
                    CISA recommends recognizing and reporting phishing, using strong and
                    unique passwords, and turning on multifactor authentication as important
                    steps for staying safer online.
                </p>
                <a href="https://www.cisa.gov/sites/default/files/2024-09/Secure-Our-World-4-Easy-Ways-Stay-Safe-Online-Tip-Sheet.pdf" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="source">
            <div class="source-num">6</div>
            <div>
                <h3>UNICEF — Online Privacy Checklist</h3>
                <p>
                    UNICEF highlights that online activity can create lasting digital records
                    and recommends protecting personal information, reviewing device and
                    privacy settings, and developing digital literacy.
                </p>
                <a href="https://www.unicef.org/parenting/child-care/online-privacy" target="_blank">Read the source →</a>
            </div>
        </div>

        <div class="apa">
            <h3>APA-Style Reference List</h3>
            <p>Cybersecurity and Infrastructure Security Agency. (2024). <i>Secure our world: 4 easy ways to stay safe online.</i></p>
            <p>National Privacy Commission. (n.d.). <i>Kabataang Digital.</i></p>
            <p>National Privacy Commission. (2023). <i>Kabataang Digital 2023: NPC raises youth awareness on data privacy and online safety.</i></p>
            <p>UNICEF. (n.d.). <i>Safety: Digital education.</i></p>
            <p>UNICEF Philippines. (2021). <i>Philippines Kids Online: The online experiences of children in the Philippines: Opportunities, risks and barriers.</i></p>
            <p>UNICEF Parenting. (n.d.). <i>Online privacy checklist for parents.</i></p>
        </div>

    </div>
</section>

<section id="team">
    <div class="section-head">
        <h2>👥 STEM 3 Group 2 — Project Team</h2>
        <p>CyberShield — Cybersecurity &amp; Online Safety</p>
    </div>

    <div class="team-grid">
        <div class="member"><div class="avatar">💻</div><h3>REN'Z BRIAN D CHAVEZ</h3><p>Team Leader / Content Developer</p></div>
        <div class="member"><div class="avatar">🔎</div><h3>SHAHER BEN ABDULLAH K LIMBA</h3><p>Researcher / Designer</p></div>
        <div class="member"><div class="avatar">✍️</div><h3>EUGEM KINTH Q. QUIJOTE</h3><p>Content Writer / Researcher</p></div>
        <div class="member"><div class="avatar">📝</div><h3>JOHN MIER A. PACQUIAO</h3><p>Content Writer / Editor</p></div>
        <div class="member"><div class="avatar">🎨</div><h3>HART KADEN P. MESIAS</h3><p>Designer / Layout Specialist</p></div>
        <div class="member"><div class="avatar">✅</div><h3>NOELLE KRISTEN B. TIRADO</h3><p>Researcher / Fact Checker</p></div>
        <div class="member"><div class="avatar">🔍</div><h3>MATT MENRYK M. GIRASOL</h3><p>Editor / Quality Assurance</p></div>
        <div class="member"><div class="avatar">📋</div><h3>JOHN KEVIN S. ABADIANO</h3><p>Designer / Content Organizer</p></div>
    </div>

    <div class="panel" style="margin-top:28px;">
        <h3 style="color:#38e8ff;font-size:24px;margin-bottom:18px;">📌 Project Details</h3>
        <p><b style="color:#fff;">Project Title:</b> CyberShield — Cybersecurity &amp; Online Safety</p>
        <p><b style="color:#fff;">Group Number:</b> Group 2</p>
        <p><b style="color:#fff;">Purpose:</b> Educational awareness on digital safety practices, threats, and protection measures.</p>
        <p><b style="color:#fff;">Message:</b> “We are committed to promoting a safer, more responsible digital environment for everyone.”</p>
    </div>
</section>

<footer>
    <strong>🛡️ CYBERSHIELD</strong>
    <p>Cybersecurity &amp; Online Safety • STEM 3 Group 2</p>
    <p>© 2026 Group 2 — Cybersecurity &amp; Online Safety Project</p>
    <p>All rights reserved | Educational Purpose Only.</p>
</footer>

<script>
function checkQuiz(){
    let score=0;
    const answers=["q1","q2","q3"];

    answers.forEach(function(q){
        const selected=document.querySelector('input[name="'+q+'"]:checked');
        if(selected && selected.value==="1") score++;
    });

    const result=document.getElementById("result");
    result.style.display="block";

    if(score===3){
        result.innerHTML="🎉 Excellent! You got 3/3. You know the basics of online safety!";
    }else if(score===2){
        result.innerHTML="👍 Good job! You got 2/3. Review the safety tips and try again.";
    }else if(score===1){
        result.innerHTML="📖 You got 1/3. Take another look at the guide and try again.";
    }else{
        result.innerHTML="🔎 You got 0/3. No worries—read the guide and try the Safety Check again.";
    }
}
</script>

</body>
</html>
