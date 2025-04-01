<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Video Downloader</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
            background: linear-gradient(to right, #8e44ad, #2c3e50);
            color: white;
        }
        .container {
            max-width: 500px;
            margin: auto;
            background: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
        }
        input, button {
            margin: 10px;
            padding: 12px;
            font-size: 16px;
            border: none;
            border-radius: 5px;
            width: 90%;
        }
        input {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            outline: none;
        }
        input::placeholder {
            color: #ddd;
        }
        button {
            background-color: #ffcc00;
            color: #333;
            font-weight: bold;
            cursor: pointer;
        }
        button:hover {
            background-color: #ffaa00;
        }
        #message {
            margin-top: 15px;
            color: #ffcc00;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Instagram Video Downloader</h2>
        <input type="text" id="instaUrl" placeholder="Enter Instagram Video URL">
        <button onclick="downloadVideo()">Get Download Link</button>
        <p id="message"></p>
    </div>

    <script>
        function downloadVideo() {
            let url = document.getElementById('instaUrl').value;
            if (!url) {
                document.getElementById('message').innerText = "Please enter a valid Instagram URL.";
                return;
            }

            // For demonstration purposes, we assume you're using a service like InstaDownloader.
            // Replace with actual API or service URLs for video download.
            let downloadLink = `https://ssstik.io/instagram?url=${encodeURIComponent(url)}`;
            window.location.href = downloadLink;

            document.getElementById('message').innerText = "Redirecting to download...";
        }
    </script>
</body>
</html>
