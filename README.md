# asya5644.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate AI Video Editor</title>
    <script src="https://cdn.jsdelivr.net/npm/@ffmpeg/ffmpeg@0.10.0"></script>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/body-pix"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        canvas { display: block; margin: 20px auto; border: 1px solid #ccc; }
    </style>
</head>
<body>
    <h1>Ultimate AI Video Editor</h1>
    <input type="file" id="videoUpload" accept="video/*">
    <video id="videoPlayer" controls></video>
    <br>
    <label>Start Time: <input type="number" id="startTime" min="0"></label>
    <label>End Time: <input type="number" id="endTime" min="0"></label>
    <button onclick="trimVideo()">Trim Video</button>
    <br>
    <label>Text Overlay: <input type="text" id="overlayText"></label>
    <button onclick="addTextOverlay()">Add Text</button>
    <br>
    <input type="file" id="mergeVideoUpload" accept="video/*">
    <button onclick="mergeVideos()">Merge Videos</button>
    <br>
    <label>Filter: 
        <select id="filterSelect" onchange="applyFilter()">
            <option value="none">None</option>
            <option value="grayscale">Grayscale</option>
            <option value="sepia">Sepia</option>
            <option value="invert">Invert</option>
        </select>
    </label>
    <br>
    <button onclick="removeBackground()">Remove Background</button>
    <br>
    <button onclick="addFaceTracking()">Add Face Tracking</button>
    <br>
    <button onclick="exportVideo()">Export Video</button>
    <canvas id="videoCanvas"></canvas>
    <script>
        const { createFFmpeg, fetchFile } = FFmpeg;
        const ffmpeg = createFFmpeg({ log: true });
        let video = document.getElementById("videoPlayer");
        let canvas = document.getElementById("videoCanvas");
        let ctx = canvas.getContext("2d");

        document.getElementById("videoUpload").addEventListener("change", function(event) {
            let file = event.target.files[0];
            if (file) {
                let url = URL.createObjectURL(file);
                video.src = url;
            }
        });

        function trimVideo() {
            let start = parseFloat(document.getElementById("startTime").value);
            let end = parseFloat(document.getElementById("endTime").value);
            if (!isNaN(start) && !isNaN(end) && start < end) {
                video.currentTime = start;
                setTimeout(() => video.pause(), (end - start) * 1000);
            }
        }

        function addTextOverlay() {
            let overlayText = document.getElementById("overlayText").value;
            canvas.width = video.videoWidth;
            canvas.height = video.videoHeight;
            ctx.drawImage(video, 0, 0, canvas.width, canvas.height);
            ctx.font = "30px Arial";
            ctx.fillStyle = "white";
            ctx.fillText(overlayText, 50, 50);
        }

        function mergeVideos() {
            alert("Video merging feature with FFmpeg.js is under development.");
        }

        function applyFilter() {
            let filter = document.getElementById("filterSelect").value;
            video.style.filter = filter;
        }

        async function removeBackground() {
            const net = await bodyPix.load();
            const segmentation = await net.segmentPerson(video);
            const mask = bodyPix.toMask(segmentation);
            ctx.putImageData(mask, 0, 0);
        }

        function addFaceTracking() {
            alert("Face tracking feature is under development.");
        }

        async function exportVideo() {
            if (!ffmpeg.isLoaded()) await ffmpeg.load();
            const inputFile = document.getElementById("videoUpload").files[0];
            if (!inputFile) {
                alert("Please upload a video first.");
                return;
            }
            
            ffmpeg.FS('writeFile', 'input.mp4', await fetchFile(inputFile));
            await ffmpeg.run('-i', 'input.mp4', 'output.mp4');
            
            const data = ffmpeg.FS('readFile', 'output.mp4');
            const url = URL.createObjectURL(new Blob([data.buffer], { type: 'video/mp4' }));
            const a = document.createElement('a');
            a.href = url;
            a.download = 'edited_video.mp4';
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
        }
    </script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Awesome GitHub Page</title>
    <style>
        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background: linear-gradient(120deg, #84fab0, #8fd3f4);
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            text-align: center;
        }

        h1 {
            font-size: 3rem;
            color: #222;
            margin-bottom: 1rem;
        }

        p {
            font-size: 1.2rem;
            color: #555;
            margin-bottom: 2rem;
        }

        .button {
            padding: 0.8rem 2rem;
            background-color: #ff6f61;
            color: #fff;
            border: none;
            border-radius: 5px;
            text-decoration: none;
            font-size: 1rem;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
        }

        .button:hover {
            background-color: #ff3d2e;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            transform: translateY(-3px);
        }

        footer {
            margin-top: auto;
            font-size: 0.9rem;
            color: #777;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Amazing Website!</h1>
    <p>This is my first GitHub Page. I’m just getting started, but it’s already looking cool!</p>
    <a href="#" class="button">Click Me!</a>
    <footer>
        &copy; 2025 Created by Me. All rights reserved.
    </footer>
</body>
</html>
