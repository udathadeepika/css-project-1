# css-project-1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Contact Form</title>
</head>
<body>
    <div class="container">
        <form class="contact-form">
            <h2>Contact Us</h2>
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="subject">Subject:</label>
                <input type="text" id="subject" name="subject" required>
            </div>
            <div class="form-group">
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="4" required></textarea>
            </div>
            <button type="submit">Submit</button>
        </form>
    </div>
</body>
<script>
    document.addEventListener("DOMContentLoaded", function () {
        document.querySelector(".container").classList.add("active");
    });
</script>

</html>
 68 changes: 68 additions & 0 deletions68  
styles.css
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,68 @@
body {
    margin: 0;
    padding: 0;
    font-family: 'Arial', sans-serif;
}

.container {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(to right, #348F50, #56B4D3);
    overflow: hidden; /* Prevents content overflow during animation */
}

.contact-form {
    background: rgba(255, 255, 255, 0.8);
    backdrop-filter: blur(10px);
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);

    /* Animation */
    transform: translateY(100%);
    transition: transform 0.5s ease-in-out;
}

.container.active .contact-form {
    transform: translateY(0);
}

.contact-form h2 {
    text-align: center;
    color: #333;
}

.form-group {
    margin-bottom: 20px;
}

label {
    display: block;
    margin-bottom: 8px;
    color: #555;
}

input,
textarea {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}

button {
    background: #56B4D3;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
}

button:hover {
    background: #348F50;
}
