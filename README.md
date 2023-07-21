# URL-template
This is a basic HTML/CSS template for a browser-like user interface
CODE:-
<!DOCTYPE html>
<html>
<head>
    <title>Best Browser Design</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        #address-bar {
            background-color: #f0f0f0;
            padding: 10px;
        }

        #address-bar input[type="text"] {
            width: 80%;
            padding: 5px;
            font-size: 16px;
            border: 1px solid #ccc;
        }

        #address-bar button {
            padding: 5px 10px;
            font-size: 16px;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            cursor: pointer;
        }

        #web-view {
            height: 80vh;
            border: 1px solid #ccc;
            overflow: auto;
            padding: 10px;
        }
    </style>
</head>
<body>
    <div id="address-bar">
        <input type="text" placeholder="Enter URL">
        <button onclick="loadPage()">Go</button>
    </div>
    <div id="web-view">
        <!-- Web page content will be loaded here -->
    </div>

    <script>
        function loadPage() {
            var url = document.querySelector('input[type="text"]').value;
            if (!url.startsWith("http://") && !url.startsWith("https://")) {
                url = "http://" + url;
            }
            window.location.href = url;
        }
    </script>
</body>
</html>
