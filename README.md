# hw23
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Design to Code Example</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
</head>
<body>

<div class="content-wrapper">
    <div class="image-container">
        <img src="https://via.placeholder.com/450x240" alt="Sample View" class="main-image">
        <button id="infoBtn" class="spec-button">查看資訊</button>
    </div>

    <div id="infoPanel" class="info-panel hidden">
        <p><strong>修改日期:</strong> 2017/10/12</p>
        <p><strong>類型:</strong> JPG</p>
        <p><strong>大小:</strong> 466.97KB</p>
        <p><strong>路徑:</strong> /vdesigncenter.qnap.com/tw/DesignCenter/...</p>
    </div>
</div>

<script>
    const btn = document.getElementById('infoBtn');
    const panel = document.getElementById('infoPanel');

    btn.addEventListener('click', () => {
        panel.classList.toggle('hidden');
    });
</script>

</body>
</html>
/* style.css */
body {
    font-family: 'Roboto', sans-serif;
    background-color: #f6f6f6;
    display: flex;
    justify-content: center;
    padding-top: 50px;
}

.content-wrapper {
    width: 496px; /* Matches the width in the mockup */
}

.image-container {
    position: relative;
    background: #ffffff;
    padding: 20px;
    border: 1px solid #cecece;
}

.main-image {
    width: 100%;
    display: block;
}

/* Specific Button Implementation */
.spec-button {
    /* Dimensions & Shape */
    height: 22px;
    border-radius: 8px;
    padding: 0 10px;
    
    /* Colors & Border */
    background-color: #ffffff;
    border: 1px solid #2f2f2f;
    color: #2f2f2f;
    
    /* Text Specs */
    font-family: 'Roboto', sans-serif;
    font-size: 13px;
    cursor: pointer;
    
    /* Positioning (placed roughly as seen in mockup) */
    position: absolute;
    top: 35px;
    right: 35px;
    
    /* Smooth transition for hover */
    transition: background-color 0.2s;
}

.spec-button:hover {
    background-color: #f0f0f0;
}

/* Info Panel Styling */
.info-panel {
    background-color: #e8f3ff; /* Matching the 'list select color' */
    border-top: 1px solid #cfddff;
    padding: 10px 20px;
    font-size: 13px;
    color: #707070;
    line-height: 1.6;
}

.hidden {
    display: none;
}
