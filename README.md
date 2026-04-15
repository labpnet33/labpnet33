<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vijay Katariya | Network Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: #0f172a;
    color: #e2e8f0;
}

.container {
    text-align: center;
    padding: 50px 20px;
}

h1 {
    font-size: 3rem;
    color: #38bdf8;
    animation: fadeIn 2s ease-in-out;
}

h2 {
    font-weight: 300;
    margin-bottom: 30px;
    animation: fadeIn 3s ease-in-out;
}

.card {
    background: #1e293b;
    margin: 20px auto;
    padding: 20px;
    border-radius: 15px;
    max-width: 800px;
    box-shadow: 0 0 20px rgba(0,0,0,0.5);
    animation: slideUp 1.5s ease-in-out;
}

.badge {
    display: inline-block;
    padding: 8px 15px;
    margin: 5px;
    border-radius: 20px;
    background: #38bdf8;
    color: black;
    font-size: 0.9rem;
}

.typing {
    color: #22c55e;
    font-size: 1.2rem;
    height: 30px;
}

@keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
}

@keyframes slideUp {
    from {transform: translateY(50px); opacity: 0;}
    to {transform: translateY(0); opacity: 1;}
}

.footer {
    margin-top: 40px;
    font-size: 0.9rem;
    color: #94a3b8;
}

</style>
</head>
<body>

<div class="container">
    <h1>Hi 👋, I'm Vijay Katariya</h1>
    <h2>Network Engineer | Security Explorer 😈</h2>

    <div class="typing" id="typing"></div>

    <div class="card">
        <h3>👨‍💻 About Me</h3>
        <p>I create problems → solve them → call it experience 😄</p>
        <p>Breaking configs just to prove I can fix them 💥</p>
        <p>Debugging networks, packets & sometimes my own mistakes 🛠️</p>
    </div>

    <div class="card">
        <h3>🚀 Working On</h3>
        <p>🔧 VulnScan (because manual testing is boring 😅)</p>
        <p>🌱 Learning Server Architecture & Security</p>
    </div>

    <div class="card">
        <h3>🌐 Experience</h3>
        <div class="badge">FortiGate 🔥</div>
        <div class="badge">Cisco Meraki ☁️</div>
        <div class="badge">Troubleshooting 🛠️</div>
    </div>

    <div class="card">
        <h3>🐛 Reality Check</h3>
        <p>90% issues = small changes</p>
        <p>10% issues = also my changes 💀</p>
    </div>

    <div class="card">
        <h3>📫 Contact</h3>
        <p>Email: labpnet33@gmail.com</p>
        <p>GitHub: github.com/labpnet33</p>
    </div>

    <div class="footer">
        🚀 Create → Break → Fix → Repeat
    </div>
</div>

<script>
const texts = [
    "Network Engineer",
    "Security Learner",
    "Building VulnScan",
    "Breaking & Fixing Things"
];

let i = 0;
let j = 0;
let currentText = '';
let isDeleting = false;

function type() {
    if (i < texts.length) {
        if (!isDeleting && j <= texts[i].length) {
            currentText = texts[i].substring(0, j++);
        } else if (isDeleting && j >= 0) {
            currentText = texts[i].substring(0, j--);
        }

        document.getElementById("typing").innerHTML = currentText;

        if (j == texts[i].length) isDeleting = true;
        if (j == 0 && isDeleting) {
            isDeleting = false;
            i++;
            if (i == texts.length) i = 0;
        }
    }
    setTimeout(type, isDeleting ? 50 : 100);
}

type();
</script>

</body>
</html>
