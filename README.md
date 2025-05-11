# NLP-many-to-many
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Project Checklist</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f7f7f7;
      padding: 40px;
      max-width: 600px;
      margin: auto;
    }
    h1 {
      color: #333;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      background: #fff;
      border-radius: 8px;
      padding: 12px 16px;
      margin-bottom: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      display: flex;
      align-items: center;
      cursor: pointer;
      transition: background 0.2s ease;
    }
    li:hover {
      background: #e8f0fe;
    }
    input[type="checkbox"] {
      margin-right: 12px;
      transform: scale(1.2);
    }
    .completed {
      text-decoration: line-through;
      color: green;
    }
  </style>
</head>
<body>

  <h1>✅ NLP Project Checklist</h1>
  <ul id="taskList">
    <li><input type="checkbox"> 1. Choose a dataset</li>
    <li><input type="checkbox"> 2. Download and check the shape of the dataset</li>
    <li><input type="checkbox"> 3. Clean the data if needed (regex)</li>
    <li><input type="checkbox"> 4. Decide the tokenization strategy</li>
    <li><input type="checkbox"> 5. Build the vocabulary</li>
    <li><input type="checkbox"> 6. Build a wrapper around the dataset</li>
    <li><input type="checkbox"> 7. Create a DataLoader → train[0] (input, label)</li>
    <li><input type="checkbox"> 8. Build network architecture</li>
    <li><input type="checkbox"> 9. Training loop</li>
    <li><input type="checkbox"> 10. Evaluate</li>
  </ul>

  <script>
    const tasks = document.querySelectorAll('#taskList li');
    tasks.forEach(task => {
      const checkbox = task.querySelector('input[type="checkbox"]');
      checkbox.addEventListener('change', () => {
        task.classList.toggle('completed', checkbox.checked);
      });
    });
  </script>

</body>
</html>
