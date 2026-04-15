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
