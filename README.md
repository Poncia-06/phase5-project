# phase5-project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple Blog with Comments</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
      background-color: #f9f9f9;
    }
    .blog-post {
      background-color: white;
      padding: 20px;
      border-radius: 6px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin-bottom: 40px;
    }
    .comments {
      margin-top: 30px;
    }
    .comment {
      margin-bottom: 10px;
      padding: 10px;
      background-color: #efefef;
      border-radius: 4px;
    }
    form {
      margin-top: 20px;
    }
    textarea {
      width: 100%;
      height: 80px;
    }
    button {
      margin-top: 10px;
      padding: 10px 15px;
    }
  </style>
</head>
<body>

  <div class="blog-post">
    <h1>My First Blog Post</h1>
    <p>This is a simple blog post about learning HTML, CSS, and JavaScript. It's amazing how you can build something functional with just a few lines of code!</p>

    <div class="comments">
      <h3>Comments</h3>
      <div id="comment-list"></div>

      <form id="comment-form">
        <label for="comment-input">Add a comment:</label><br>
        <textarea id="comment-input" required></textarea><br>
        <button type="submit">Post Comment</button>
      </form>
    </div>
  </div>

  <script>
    const form = document.getElementById('comment-form');
    const commentInput = document.getElementById('comment-input');
    const commentList = document.getElementById('comment-list');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const commentText = commentInput.value.trim();
      if (commentText !== '') {
        const comment = document.createElement('div');
        comment.className = 'comment';
        comment.innerText = commentText;
        commentList.appendChild(comment);
        commentInput.value = '';
      }
    });
  </script>

</body>
</html>
