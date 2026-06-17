<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>manassesbinga</title>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600;700&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:      #0d1117;
      --surface: #161b22;
      --border:  #21262d;
      --blue:    #58A6FF;
      --cyan:    #0ea5e9;
      --purple:  #8257E5;
      --text:    #c9d1d9;
      --muted:   #6e7681;
      --green:   #3fb950;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Fira Code', monospace;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      padding: 48px 20px;
    }

    .card {
      width: 100%;
      max-width: 760px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 32px;
    }

    /* ── ASCII ── */
    .ascii {
      font-size: clamp(5px, 1.3vw, 10.5px);
      line-height: 1.2;
      white-space: pre;
      color: var(--blue);
      text-shadow: 0 0 10px rgba(88,166,255,.5), 0 0 28px rgba(88,166,255,.18);
      user-select: none;
      animation: flicker 7s infinite;
    }
    @keyframes flicker {
      0%,100%{opacity:1} 97%{opacity:1} 98%{opacity:.82} 99%{opacity:1}
    }
    @media (prefers-reduced-motion: reduce){ .ascii{ animation:none } }

    /* ── Typing ── */
    .typing img { display:block; height:28px; }

    /* ── Badge row ── */
    .badge-row { display:flex; flex-wrap:wrap; gap:8px; justify-content:center; align-items:center; }
    .badge-row img, .badge-row a img { display:block; height:20px; }

    /* ── Divider ── */
    .divider { width:100%; height:1px; background:var(--border); }

    /* ── Section label ── */
    .section-label {
      width:100%;
      font-size:13px;
      font-weight:600;
      color:var(--cyan);
    }
    .section-label code {
      background:var(--surface);
      border:1px solid var(--border);
      padding:3px 10px;
      border-radius:4px;
      font-family:inherit;
    }

    /* ── Terminal block ── */
    .terminal {
      width:100%;
      background:var(--surface);
      border:1px solid var(--border);
      border-radius:8px;
      overflow:hidden;
    }
    .terminal-bar {
      background:#1c2128;
      padding:8px 14px;
      display:flex;
      gap:7px;
      align-items:center;
      border-bottom:1px solid var(--border);
    }
    .dot { width:12px; height:12px; border-radius:50%; }
    .dot.r{background:#ff5f56;} .dot.y{background:#ffbd2e;} .dot.g{background:#27c93f;}
    .terminal-body {
      padding:18px 20px;
      font-size:12.5px;
      line-height:1.75;
      white-space:pre-wrap;
      color:var(--text);
    }
    .terminal-body .prompt { color:var(--green); }
    .terminal-body .key    { color:var(--blue); }
    .terminal-body .val    { color:var(--cyan); }
    .terminal-body .str    { color:#a5d6ff; }
    .terminal-body .arr    { color:var(--muted); }
    .terminal-body .brace  { color:var(--muted); }

    /* ── Tech groups ── */
    .tech-groups {
      width:100%;
      display:flex;
      flex-direction:column;
      gap:16px;
    }
    .tech-group {}
    .tech-group-label {
      font-size:10px;
      font-weight:600;
      color:var(--muted);
      letter-spacing:.1em;
      text-transform:uppercase;
      margin-bottom:8px;
    }

    /* ── Stats ── */
    .stats-row {
      display:flex;
      flex-wrap:wrap;
      gap:12px;
      justify-content:center;
    }
    .stats-row img { border-radius:6px; height:165px; }

    /* ── Streak ── */
    .streak img { border-radius:6px; max-width:100%; }

    /* ── Matrix ── */
    .matrix { text-align:center; }
    .matrix img { max-width:100%; border-radius:4px; }
    .matrix-sub {
      margin-top:10px;
      font-size:11px;
      color:var(--muted);
      line-height:1.7;
    }
    .matrix-sub code {
      font-family:inherit;
      background:none;
    }

    /* ── Certs ── */
    .certs-grid {
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      justify-content:center;
    }
    .certs-grid a img { display:block; height:20px; }

    /* ── Footer social ── */
    .social-row {
      display:flex;
      flex-wrap:wrap;
      gap:10px;
      justify-content:center;
    }
    .social-row a img { display:block; height:22px; }

    .section-wrap {
      width:100%;
      display:flex;
      flex-direction:column;
      align-items:center;
      gap:14px;
    }
  </style>
</head>
<body>
<div class="card">

  <!-- ASCII -->
  <pre class="ascii">███╗   ███╗ █████╗ ███╗   ██╗ █████╗ ███████╗███████╗███████╗
████╗ ████║██╔══██╗████╗  ██║██╔══██╗██╔════╝██╔════╝██╔════╝
██╔████╔██║███████║██╔██╗ ██║███████║███████╗███████╗█████╗  
██║╚██╔╝██║██╔══██║██║╚██╗██║██╔══██║╚════██║╚════██║██╔══╝  
██║ ╚═╝ ██║██║  ██║██║ ╚████║██║  ██║███████║███████║███████╗
╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝╚══════╝╚══════╝╚══════╝</pre>

  <!-- Typing -->
  <div class="typing">
    <a href="https://git.io/typing-svg">
      <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=58A6FF&width=500&lines=manassesbinga;software+engineer;building+in+public" alt="typing" />
    </a>
  </div>

  <!-- Visitor badge -->
  <div class="badge-row">
    <img src="https://vbr.nathanchung.dev/badge?page_id=manassesbinga.manassesbinga&color=0ea5e9&style=flat-square&logo=github" alt="visitors" />
  </div>

  <div class="divider"></div>

  <!-- whoami -->
  <div class="section-wrap">
    <div class="section-label"><code>&gt; whoami</code></div>
    <div class="terminal" style="width:100%">
      <div class="terminal-bar">
        <span class="dot r"></span><span class="dot y"></span><span class="dot g"></span>
      </div>
      <div class="terminal-body"><span class="prompt">$</span> cat profile.json
<span class="brace">{</span>
  <span class="key">"name"</span>  : <span class="str">"Manasses Binga"</span>,
  <span class="key">"role"</span>  : <span class="str">"Full-Stack Developer (Pleno)"</span>,
  <span class="key">"xp"</span>    : <span class="str">"7 years // 7 anos"</span>,
  <span class="key">"stack"</span> : <span class="arr">["Next.js", "React Native", "Python", "Node.js", "C# .NET"]</span>,
  <span class="key">"infra"</span> : <span class="arr">["Kubernetes", "Git", "SQL"]</span>,
  <span class="key">"ethic"</span> : <span class="str">"Hacker Ethic — build to understand, share to grow"</span>,
  <span class="key">"status"</span>: <span class="str">"building in public 🚀"</span>
<span class="brace">}</span></div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- tech --list -->
  <div class="section-wrap">
    <div class="section-label"><code>&gt; tech --list</code></div>
    <div class="tech-groups" style="width:100%">

      <div class="tech-group">
        <div class="tech-group-label">Frontend</div>
        <div class="badge-row" style="justify-content:flex-start;">
          <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js"/>
          <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"/>
          <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native"/>
          <img src="https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
          <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white" alt="TailwindCSS"/>
        </div>
      </div>

      <div class="tech-group">
        <div class="tech-group-label">Backend</div>
        <div class="badge-row" style="justify-content:flex-start;">
          <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
          <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
          <img src="https://img.shields.io/badge/C%23-239120?style=flat-square&logo=c-sharp&logoColor=white" alt="C#"/>
          <img src="https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt=".NET"/>
        </div>
      </div>

      <div class="tech-group">
        <div class="tech-group-label">Infra &amp; Data</div>
        <div class="badge-row" style="justify-content:flex-start;">
          <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes"/>
          <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker"/>
          <img src="https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
          <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git"/>
        </div>
      </div>

    </div>
  </div>

  <div class="divider"></div>

  <!-- git log --stats -->
  <div class="section-wrap">
    <div class="section-label"><code>&gt; git log --stats</code></div>
    <div class="stats-row">
      <img src="https://github-readme-stats.vercel.app/api?username=manassesbinga&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58A6FF&icon_color=0ea5e9&text_color=c9d1d9&count_private=true" alt="stats" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=manassesbinga&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58A6FF&text_color=c9d1d9&langs_count=6" alt="langs" />
    </div>
    <div class="streak">
      <a href="https://git.io/streak-stats">
        <img src="https://streak-stats.demolab.com?user=manassesbinga&theme=github-dark-blue&hide_border=true&background=0D1117&ring=58A6FF&fire=0ea5e9&currStreakLabel=58A6FF" alt="streak" />
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ping -->
  <div class="section-wrap">
    <div class="section-label"><code>&gt; ping manassesbinga</code></div>
    <div class="social-row">
      <a href="https://linkedin.com/in/manassesbinga">
        <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/>
      </a>
      <a href="https://linkedin.com/in/manassescahunda">
        <img src="https://img.shields.io/badge/linkedin-%230A66C2.svg?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn alt"/>
      </a>
      <a href="https://github.com/manassesbinga">
        <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"/>
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Matrix + tagline -->
  <div class="matrix">
    <img src="https://github.com/manassesbinga/profile/blob/main/matrix.svg" alt="matrix" />
    <div class="matrix-sub">
      <code>// 7 anos no terminal. ainda aprendendo. sempre construindo.</code><br/>
      <code>// 7 years in the terminal. still learning. always building.</code>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Certificações -->
  <div class="section-wrap">
    <div class="section-label"><code>🎓 Certificações &amp; Formação</code></div>
    <div class="certs-grid">

      <a href="https://app.rocketseat.com.br/certificates/a03cd2c8-3eb3-4ba4-bb0c-c9cea2f843b9">
        <img src="https://img.shields.io/badge/Rocketseat-Node.js_%26_React-8257E5?style=flat-square&logo=rocketseat&logoColor=white" alt="Rocketseat Node.js & React"/>
      </a>
      <a href="https://app.rocketseat.com.br/certificates/4b0cfc8a-daa5-48a0-b51a-fde5e0d4f1de">
        <img src="https://img.shields.io/badge/Rocketseat-React_Native-8257E5?style=flat-square&logo=rocketseat&logoColor=white" alt="Rocketseat React Native"/>
      </a>
      <a href="https://app.rocketseat.com.br/certificates/0eb92c4e-d5e7-4db8-a140-9f2f12df683c">
        <img src="https://img.shields.io/badge/Rocketseat-TypeScript-8257E5?style=flat-square&logo=rocketseat&logoColor=white" alt="Rocketseat TypeScript"/>
      </a>
      <a href="https://www.dio.me/certificate/ZWDFYXNE/share">
        <img src="https://img.shields.io/badge/DIO-Bootcamp-30A3DC?style=flat-square&logo=dio&logoColor=white" alt="DIO Bootcamp"/>
      </a>
      <a href="https://github.com/manassesbinga/manassesbinga/blob/main/formacao%20(5).pdf">
        <img src="https://img.shields.io/badge/Cyber_Security-Hacker_Ético-red?style=flat-square&logo=hackaday&logoColor=white" alt="Cyber Security"/>
      </a>
      <a href="https://github.com/manassesbinga/manassesbinga/blob/main/formacao%20(4).pdf">
        <img src="https://img.shields.io/badge/AWS-Solutions_Architect_Professional-FF9900?style=flat-square&logo=amazonaws&logoColor=white" alt="AWS"/>
      </a>
      <a href="https://github.com/manassesbinga/manassesbinga/blob/main/formacao%20(1).pdf">
        <img src="https://img.shields.io/badge/DIO-Bootcamp_Developer-30A3DC?style=flat-square&logo=dio&logoColor=white" alt="DIO Developer"/>
      </a>
      <a href="https://github.com/manassesbinga/manassesbinga/blob/main/formacao%20(2).pdf">
        <img src="https://img.shields.io/badge/DIO-Introdução_à_Computação-30A3DC?style=flat-square&logo=dio&logoColor=white" alt="DIO Intro"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/EGSWGL8P?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-Learn_Achievement-5E5E5E?style=flat-square&logo=microsoft&logoColor=white" alt="Microsoft Learn"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/CRFEYSP9?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-Azure_Fundamentals-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure Fundamentals"/>
      </a>
      <a href="https://www.dio.me/certificate/AJBIWOH2/share">
        <img src="https://img.shields.io/badge/DIO-Formação_Tech-30A3DC?style=flat-square&logo=dio&logoColor=white" alt="DIO Tech"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/JH9XH6KT?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-Cloud_Skills-0078D4?style=flat-square&logo=microsoft&logoColor=white" alt="Microsoft Cloud"/>
      </a>
      <a href="https://learn.microsoft.com/pt-pt/users/manassesbinga-2529/achievements/jh9xsllt">
        <img src="https://img.shields.io/badge/Microsoft-Learn_Profile-0078D4?style=flat-square&logo=microsoft&logoColor=white" alt="Microsoft Profile"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/3ZRE2XGH?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/JH9X864T?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-AI_Fundamentals-0078D4?style=flat-square&logo=microsoft&logoColor=white" alt="AI Fundamentals"/>
      </a>
      <a href="https://cs50.harvard.edu/certificates/17d0f2e9-8222-40d9-8668-53991b9bbf3c">
        <img src="https://img.shields.io/badge/Harvard-CS50x-A41034?style=flat-square&logo=harvard&logoColor=white" alt="Harvard CS50"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/9AXJW62U?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-GitHub_Fundamentals-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub Fundamentals"/>
      </a>
      <a href="https://learn.microsoft.com/api/achievements/share/pt-pt/ManassesBinga-2529/ABP8KL37?sharingId=A7BDBEDE26009B61">
        <img src="https://img.shields.io/badge/Microsoft-Azure_Developer-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure Developer"/>
      </a>

    </div>
  </div>

</div>
</body>
</html>
