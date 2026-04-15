<div class="container">
    <h1>Hi 👋, I'm Vijay Katariya</h1>
    <h2>Network Engineer | Security Explorer 😈</h2>
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
