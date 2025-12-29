// assets/js/main.js

console.log("Free Voice website loaded");

// Smooth scroll for anchor links (if any)
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});

// Example: Premium / Download Buttons
const downloadBtn = document.querySelector('.btn');
const premiumBtn = document.querySelector('.btn-premium');

if(downloadBtn) {
    downloadBtn.addEventListener('click', () => {
        alert("Redirecting to download page...");
        window.location.href = "download.html";
    });
}

if(premiumBtn) {
    premiumBtn.addEventListener('click', () => {
        alert("Redirecting to premium subscription...");
        window.location.href = "premium.html";
    });
}

// Future Stripe Integration Placeholder
function goToStripe(url) {
    // Example: url = Stripe Checkout link
    window.open(url, "_blank");
}

// Future Firebase Google Sign-In Placeholder
function googleSignIn() {
    // Implement Firebase Auth Google sign-in here
    console.log("Google Sign-In function triggered");
}
