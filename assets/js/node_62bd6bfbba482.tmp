// Import the functions you need from the SDKs you need
import { initializeApp } from "https://www.gstatic.com/firebasejs/9.8.4/firebase-app.js";
import { getAnalytics } from "https://www.gstatic.com/firebasejs/9.8.4/firebase-analytics.js";
import { getDatabase, ref, set } from "https://www.gstatic.com/firebasejs/9.8.4/firebase-database.js";

// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
// For Firebase JS SDK v7.20.0 and later, measurementId is optional
const firebaseConfig = {
    apiKey: "AIzaSyAUSW8nqlPu6D7sm15Yz03ZsInVhDylglc",
    authDomain: "personal-c0961.firebaseapp.com",
    projectId: "personal-c0961",
    storageBucket: "personal-c0961.appspot.com",
    messagingSenderId: "912397286131",
    appId: "1:912397286131:web:2dd93b7439ca6a9f0e9586",
    measurementId: "G-CF9CDWZCLB"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
const analytics = getAnalytics(app);
const database = getDatabase(app);



document.getElementById("contact").addEventListener("submit", submitForm);

function submitForm(e) {
    e.preventDefault();

    var name = document.getElementById("name").value;
    var email = document.getElementById("email").value;
    var subject = document.getElementById("subject").value;
    var latter = document.getElementById("latter").value;

    function writeUserData(name, email, subject, latter) {
        set(ref(database, 'contact/' + userId), {
            name: name,
            email: email,
            subject: subject,
            latter: latter
        })
        then(() => {
                alert('user created!');
            })
            .catch((error) => {
                const errorCode = error.code;
                const errorMessage = error.message;

                alert(errorMessage);
            });

    }
}