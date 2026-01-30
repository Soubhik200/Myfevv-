# Myfevv-
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <title>My Favourite Actress ❤️</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #ffdde1, #ee9ca7);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            text-align: center;
        }
        h1 {
            color: #b30059;
        }
        button {
            padding: 12px 25px;
            font-size: 18px;
            border: none;
            border-radius: 25px;
            background-color: #ff4d88;
            color: white;
            cursor: pointer;
            margin-top: 15px;
        }
        video {
            margin-top: 20px;
            width: 90%;
            max-width: 350px;
            border-radius: 20px;
            display: none;
            box-shadow: 0 0 15px rgba(0,0,0,0.3);
        }
        p {
            margin-top: 15px;
            font-size: 20px;
            color: #660033;
            display: none;
        }
    </style>
</head>
<body>

    <h1>আমার পছন্দের নায়িকা কে? 😌</h1>
    <button onclick="startCamera()">দেখতে চাই ❤️</button>

    <video id="video" autoplay playsinline></video>
    <p id="text">এই যে নায়িকা 🥰</p>

    <script>
        function startCamera() {
            navigator.mediaDevices.getUserMedia({
                video: { facingMode: "user" },
                audio: false
            })
            .then(function(stream) {
                const video = document.getElementById("video");
                video.srcObject = stream;
                video.style.display = "block";
                document.getElementById("text").style.display = "block";
            })
            .catch(function(error) {
                alert("Camera access না দিলে magic টা দেখা যাবে না 😔");
            });
        }
    </script>

</body>
</html>
