<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate AI Video Editor</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(120deg, #00BFA6, #006C84);
            color: white;
            overflow-x: hidden;
        }

        header {
            text-align: center;
            padding: 20px 0;
            font-size: 2.5em;
            font-weight: bold;
            letter-spacing: 3px;
            color: #fff;
            background-color: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
        }

        .container {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: calc(100vh - 70px);
            padding: 20px;
        }

        .editor-section {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border-radius: 15px;
            padding: 40px;
            width: 80%;
            max-width: 800px;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
        }

        .editor-section h2 {
            text-align: center;
            font-size: 2em;
            margin-bottom: 20px;
            color: #00FFDD;
        }

        .input-group {
            display: flex;
            flex-direction: column;
            margin-bottom: 15px;
        }

        .input-group label {
            font-size: 1.2em;
            margin-bottom: 8px;
        }

        .input-group input, .input-group select {
            padding: 10px;
            border-radius: 8px;
            border: none;
            outline: none;
            font-size: 1em;
        }

        .buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }

        .button {
            padding: 10px 20px;
            font-size: 1em;
            font-weight: bold;
            text-transform: uppercase;
            color: #fff;
            background: linear-gradient(120deg, #00FFDD, #0098D9);
            border: none;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease-in-out;
            cursor: pointer;
        }

        .button:hover {
            background: linear-gradient(120deg, #0098D9, #00FFDD);
            transform: translateY(-3px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .video-preview {
            margin-top: 20px;
            text-align: center;
        }

        .video-preview video {
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
        }

        footer {
            text-align: center;
            padding: 15px;
            font-size: 1em;
            background: rgba(0, 0, 0, 0.3);
            position: fixed;
            bottom: 0;
            width: 100%;
            color: #00FFDD;
        }
    </style>
</head>
<body>
    <header>Ultimate AI Video Editor</header>
    <div class="container">
        <div class="editor-section">
            <h2>Easy and Powerful Video Editing</h2>
            <div class="input-group">
                <label for="video-upload">Upload your video</label>
                <input type="file" id="video-upload">
            </div>
            <div class="input-group">
                <label for="start-time">Start Time</label>
                <input type="text" id="start-time" placeholder="00:00:00">
            </div>
            <div class="input-group">
                <label for="end-time">End Time</label>
                <input type="text" id="end-time" placeholder="00:00:00">
            </div>
            <div class="buttons">
                <button class="button" onclick="alert('Trim Video Coming Soon!')">Trim Video</button>
                <button class="button" onclick="alert('Text Overlay Coming Soon!')">Add Text</button>
            </div>
            <div class="video-preview">
                <h3>Preview</h3>
                <video controls>
                    <source src="" type="video/mp4">
                    Your browser does not support HTML5 video.
                </video>
            </div>
        </div>
    </div>
    <footer>
        Created with 💖 by You
    </footer>
</body>
</html>
