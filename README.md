<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechEdu Blog</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, Helvetica, sans-serif;
        }
        body {
            background: #f6f8fa;
            color: #222;
        }
        header {
            background: #1e2a47;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 15px;
            background: #304266;
        }
        nav a {
            text-decoration: none;
            color: white;
            font-weight: bold;
        }
        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
            padding: 30px 0;
        }
        h2 { margin-bottom: 15px; }
        .blog-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
        }
        .card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 8px rgba(0,0,0,0.1);
        }
        .tags {
            margin-top: 10px;
        }
        .tag {
            background: #1e2a47;
            color: white;
            padding: 5px 10px;
            border-radius: 12px;
            font-size: 12px;
            margin-right: 5px;
        }
        /* Comment Section */
        .comments-box {
            margin-top: 40px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 6px rgba(0,0,0,0.1);
        }
        form {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        input, textarea {
            padding: 10px;
            border-radius: 6px;
            border: 1px solid #ccc;
        }
        button {
            padding: 10px;
            background: #1e2a47;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
        }
        button:hover { background: #162238; }
        footer {
            margin-top: 40px;
            text-align: center;
            padding: 15px;
            color: white;
            background: #1e2a47;
        }
        .comment-display {
            margin-top: 10px;
            padding: 10px;
            border-bottom: 1px solid #ddd;
        }
    </style>
</head>
<body>

<header>
    <h1>Tarun Blog</h1>
    <p>Your daily dose of Technology Learning</p>
</header>

<nav>
    <a href="#ai">Artificial Intelligence</a>
    <a href="#coding">Programming</a>
    <a href="#gadgets">Latest Gadgets</a>
</nav>

<div class="container" id="ai">
    <h2>Artificial Intelligence</h2>
    <div class="blog-list">
        <div class="card">
            <h3>How AI is changing the world</h3>
            <p>Artificial Intelligence is transforming industries and our daily lives...</p>
            <div class="tags">
                <span class="tag">AI</span><span class="tag">Future</span>
            </div>
        </div>
        <div class="card">
            <h3>Machine Learning Basics</h3>
            <p>A beginner-friendly guide on how machines learn from data...</p>
            <div class="tags">
                <span class="tag">ML</span><span class="tag">Data</span>
            </div>
        </div>
    </div>
</div>

<div class="container" id="coding">
    <h2>Programming</h2>
    <div class="blog-list">
        <div class="card">
            <h3>How to start learning Python</h3>
            <p>Python is a great beginner-friendly programming language...</p>
            <div class="tags">
                <span class="tag">Python</span><span class="tag">Coding</span>
            </div>
        </div>
        <div class="card">
            <h3>Why HTML & CSS matter</h3>
            <p>Everything you see on the web starts from HTML and CSS...</p>
            <div class="tags">
                <span class="tag">Web Dev</span><span class="tag">Frontend</span>
            </div>
        </div>
    </div>
</div>

<div class="container" id="gadgets">
    <h2>Latest Gadgets</h2>
    <div class="blog-list">
        <div class="card">
            <h3>Best budget smartphones 2025</h3>
            <p>Top affordable smartphones that offer flagship-level performance...</p>
            <div class="tags">
                <span class="tag">Smartphones</span><span class="tag">Tech</span>
            </div>
        </div>
    </div>
</div>

<div class="container comments-box">
    <h2>Leave a Comment</h2>
    <form onsubmit="postComment(event)">
        <input type="text" id="userName" placeholder="Your Name" required>
        <textarea id="userComment" placeholder="Your Comment..." required></textarea>
        <button type="submit">Post Comment</button>
    </form>
    <div id="commentSection"></div>
</div>

<footer>
    <p>© 2025 TechEdu Blog | All Rights Reserved</p>
</footer>

<script>
    function postComment(event) {
        event.preventDefault();
        let name = document.getElementById("userName").value;
        let comment = document.getElementById("userComment").value;

        let newComment = document.createElement("div");
        newComment.classList.add("comment-display");
        newComment.innerHTML = `<strong>${name}</strong><p>${comment}</p>`;

        document.getElementById("commentSection").appendChild(newComment);
        document.getElementById("userName").value = "";
        document.getElementById("userComment").value = "";
    }
</script>

</body>
</html>
