<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>金额提取器</title>
    <style>
        body {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            margin: 0;
            padding: 20px;
            min-height: 100vh;
            background: linear-gradient(135deg, #3494E6, #EC6EAD);
            color: #333;
            display: flex;
            justify-content: center;
            align-items: flex-start;
        }
        .container {
            width: 90%;
            max-width: 600px;
            background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }
        h1 {
            margin-top: 0;
            margin-bottom: 20px;
            text-align: center;
            font-weight: 300;
            font-size: 2em;
            color: #3494E6;
        }
        .instructions {
            background-color: #f0f4f8;
            border-left: 4px solid #3494E6;
            padding: 5px;
            margin-bottom: 5px;
            border-radius: 0 5px 5px 0;
            font-size: 0.9em;
            line-height: 1;
        }
        #textInput {
            width: 100%;
            padding: 15px;
            margin-bottom: 20px;
            background-color: #f0f4f8;
            border: 1px solid #d0d9e1;
            border-radius: 10px;
            color: #333;
            font-size: 1em;
            resize: vertical;
            min-height: 100px;
            box-sizing: border-box;
        }
        #textInput::placeholder {
            color: #94a3b8;
        }
        button {
            display: block;
            width: 100%;
            padding: 15px;
            background-color: #3494E6;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.1em;
            transition: background-color 0.3s ease, transform 0.1s ease;
        }
        button:hover {
            background-color: #2980b9;
        }
        button:active {
            transform: scale(0.98);
        }
        #output {
            margin-top: 20px;
            font-size: 1em;
            background-color: #f0f4f8;
            border-radius: 10px;
            padding: 15px;
            border: 1px solid #d0d9e1;
        }
        .total {
            font-size: 1.2em;
            font-weight: bold;
            margin-top: 10px;
            color: #3494E6;
            border-top: 2px solid #3494E6;
            padding-top: 10px;
        }
        .item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-size: 0.9em;
            border-bottom: 1px solid #d0d9e1;
            padding-bottom: 5px;
        }
        .item:last-child {
            border-bottom: none;
        }

        #textInputSP {
            width: 20%;
            padding: 5px;
            margin-bottom: 5px;
            background-color: #f0f4f8;
            border: 1px solid #d0d9e1;
            border-radius: 5px;
            color: #333;
            font-size: 1em;
            resize: vertical;
            min-height: 5px;
            box-sizing: border-box;
        }
        #textInputSP::placeholder {
            color: #94a3b8;
        }
    </style>
</head>
<body>
<div class="container">
    <h1>金额提取器</h1>
    <div class="instructions">
        <p><strong>使用说明：</strong></p>
        <p>1. 每行输入一个包含金额的文本，如果是逗号分割数字，在分割符号写入","或者"，"</p>
        <p>2. 如果文本中有多个"元"字，只保留最后一个</p>
        <p>3. 如果文本中没有"元"字，会自动在最后一个数字后添加</p>
        <p>4. 点击"提取金额"按钮获取明细和总金额</p>
    </div>
    <input id="textInputSP" placeholder="分割符号" value=""></input>
    <textarea id="textInput" placeholder="在此输入需要计算的文本..."></textarea>
    <button onclick="processText()">提取金额</button>
    <div id="output"></div>
</div>

<script>
    function formatLine(line) {
        if (line.trim() === '') return '';

        let yuanCount = (line.match(/元/g) || []).length;
        if (yuanCount > 1) {
            let lastIndex = line.lastIndexOf('元');
            line = line.slice(0, lastIndex).replace(/元/g, '') + line.slice(lastIndex);
        }

        if (!line.includes('元')) {
            let match = line.match(/\d+(?!.*\d)/);
            if (match) {
                let index = match.index + match[0].length;
                line = line.slice(0, index) + '元' + line.slice(index);
            }
        }

        return line;
    }

    function processText() {
        const text = document.getElementById("textInput").value;
        let sp = document.getElementById("textInputSP").value;
        if(sp==''){
            sp = "\n";
        }
        const lines = text.split(sp).map(formatLine);
        const pattern = /(\d+)元/;
        let totalAmount = 0;
        let itemizedHtml = '';

        let leng = 1
        lines.forEach(line => {
            const matcher = line.match(pattern);
            if (matcher) {
                const amount = parseFloat(matcher[1]);
                totalAmount += amount;
                itemizedHtml += `<div class="item"><span>${leng++}.${line}</span><span>${amount} 元</span></div>`;
            }
        });

        const totalHtml = `<div class="total">总金额：${totalAmount} 元</div>`;
        document.getElementById("output").innerHTML = itemizedHtml + totalHtml;
    }
</script>
</body>
</html>
