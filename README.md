<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate AI Video Editor</title>
    <style>
        /* General Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: flex-start;
            min-height: 100vh;
            overflow-x: hidden;
        }

        header {
            background-color: #121212;
            width: 100%;
            padding: 15px 20px;
            text-align: center;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            animation: slideInDown 1s ease-out;
        }

        header h1 {
            font-size: 2.5rem;
            color: #00c6ff;
            text-shadow: 0 4px 6px rgba(0, 0, 0, 0.4);
        }

        @keyframes slideInDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .container {
            width: 90%;
            max-width: 1200px;
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            margin-top: 20px;
            animation: fadeIn 1.5s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            text-align: center;
        }

        .tool-section {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
            margin-top: 20px;
        }

        .tool-card {
            background: linear-gradient(135deg, #ff7eb3, #ff758c);
            color: #fff;
            border-radius: 15px;
            padding: 20px;
            width: 300px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s, box-shadow 0.3s;
            text-align: center;
            animation: zoomIn 0.8s ease-in;
        }

        @keyframes zoomIn {
            from {
                transform: scale(0.5);
                opacity: 0;
            }
            to {
                transform: scale(1);
                opacity: 1;
            }
        }

        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.4);
        }

        .tool-card h3 {
            margin-bottom: 15px;
            color: #fff;
            font-size: 1.5rem;
        }

        .tool-card p {
            font-size: 1rem;
            margin-bottom: 20px;
        }

        .tool-card button {
            padding: 10px 20px;
            background-color: #121212;
            border: none;
            color: #fff;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            transition: background-color 0.3s, transform 0.2s;
        }

        .tool-card button:hover {
            background-color: #00c6ff;
            transform: scale(1.1);
        }

        footer {
            margin-top: 30px;
            font-size: 0.9rem;
            color: #ddd;
            text-align: center;
            animation: fadeInUp 1.5s ease-in;
        }

        @keyframes fadeInUp {
            from {
                transform: translateY(50%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .floating-button {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: linear-gradient(135deg, #1e3c72, #2a5298);
            color: #fff;
            padding: 15px 20px;
            border-radius: 50%;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.4);
            font-size: 1.5rem;
            cursor: pointer;
            transition: transform 0.3s, background 0.3s;
        }

        .floating-button:hover {
            transform: rotate(360deg);
            background: #00c6ff;
        }
    </style>
</head>
<body>
    <header>
        <h1>Ultimate AI Video Editor</h1>
    </header>

    <div class="container">
        <h2>Powerful Tools for Video Editing</h2>
        <div class="tool-section">
            <div class="tool-card">
                <h3>Trim Video</h3>
                <p>Select a video and set start and end times to trim.</p>
                <button>Trim Now</button>
            </div>

            <div class="tool-card">
                <h3>Text Overlay</h3>
                <p>Add custom text to your video effortlessly.</p>
                <button>Overlay Text</button>
            </div>

            <div class="tool-card">
                <h3>Remove Background</h3>
                <p>Erase video backgrounds with AI precision.</p>
                <button>Remove Background</button>
            </div>

            <div class="tool-card">
                <h3>Merge Videos</h3>
                <p>Combine multiple videos into one seamless clip.</p>
                <button>Merge Files</button>
            </div>

            <div class="tool-card">
                <h3>AI Face Tracking</h3>
                <p>Automatically track and enhance faces in videos.</p>
                <button>Track Faces</button>
            </div>
        </div>
    </div>

    <footer>
        &copy; 2025 Ultimate AI Video Editor. All rights reserved.
    </footer>

    <div class="floating-button">+</div>
</body>
</html>
