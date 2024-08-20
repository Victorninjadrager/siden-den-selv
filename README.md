<!DOCTYPE html>
<html lang="da">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interaktiv Webside</title>
    <link href="https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Permanent Marker', cursive;
            background-color: #f4f4f4;
            text-align: center;
            padding-top: 50px;
        }
        h1 {
            font-size: 48px;
            color: #333;
            animation: bounce 1s infinite;
        }
        p {
            font-size: 24px;
            color: #666;
        }
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
        }
        .question input[type="text"], .question input[type="submit"] {
            width: 100%;
            padding: 15px;
            margin-top: 10px;
            font-size: 18px;
            border-radius: 5px;
            border: 1px solid #ddd;
            box-sizing: border-box;
        }
        .question input[type="submit"] {
            background-color: #28a745;
            color: white;
            cursor: pointer;
        }
        .question input[type="submit"]:hover {
            background-color: #218838;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Velkommen til Den Særlige Side</h1>
    <p>Skriv "sikker" for at få adgang til en speciel hjemmeside.</p>
    
    <div class="question">
        <form id="secureForm">
            <input type="text" id="userInput" placeholder="Indtast 'sikker' for at fortsætte...">
            <input type="submit" value="Gå videre">
        </form>
    </div>

    <p id="feedback" style="display: none; color: red;">Forkert kode! Prøv igen.</p>
</div>

<script>
    document.getElementById("secureForm").addEventListener("submit", function(event){
        event.preventDefault(); // Forhindrer siden i at reloade
        
        var userInput = document.getElementById("userInput").value.toLowerCase();
        
        if(userInput === "sikker") {
            window.location.href = "https://www.pornhub.com"; // Omdirigerer til den ønskede URL
        } else {
            document.getElementById("feedback").style.display = "block"; // Viser en fejlbesked
        }
    });
</script>

</body>
</html>
