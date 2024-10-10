<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>金额提取器</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;
            line-height: 1.4;
            color: #333;
            background-color: #f0f4f8;
        }
        .container {
            max-width: 100%;
            padding: 20px;
            margin: 0 auto;
        }
        h1 {
            font-size: 1.8em;
            color: #2c3e50;
            margin-bottom: 20px;
            text-align: center;
        }
        .instructions {
            background-color: #e8f4fd;
            border-left: 4px solid #3498db;
            padding: 10px;
            margin-bottom: 20px;
            font-size: 0.9em;
            border-radius: 0 5px 5px 0;
        }
        .input-group {
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #2c3e50;
        }
        input[type="text"], textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #bdc3c7;
            border-radius: 5px;
            font-size: 16px;
        }
        textarea {
            height: 100px;
            resize: vertical;
        }
        button {
            display: block;
            width: 100%;
            padding: 12px;
            background-color: #3498db;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #2980b9;
        }
        .output-container {
            margin-top: 20px;
        }
        .output-box {
            background-color: #fff;
            border: 1px solid #bdc3c7;
            border-radius: 5px;
            padding: 5px;
            margin-bottom: 5px;
        }
        .output-box h2 {
            font-size: 1.2em;
            margin-bottom: 5px;
            color: #2c3e50;
        }
        .item {
            display: flex;
            justify-content: space-between;
            padding: 5px 0;
            border-bottom: 1px solid #ecf0f1;
        }
        .item:last-child {
            border-bottom: none;
        }
        .total {
            font-size: 1.1em;
            font-weight: bold;
            margin-top: 10px;
            color: #e74c3c;
        }
        #output3 {
            background-color: #e8f8f5;
            border: 1px solid #2ecc71;
            border-radius: 5px;
            padding: 15px;
            text-align: center;
            font-size: 1.1em;
            color: red;
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
    <div class="input-group">
        <label for="textInputSP">收入分割符号：</label>
        <input type="text" id="textInputSP" placeholder="默认使用换行">
    </div>
    <div class="input-group">
        <label for="textInput">收入金额：</label>
        <textarea id="textInput" placeholder="在此输入需要计算的收入金额..."></textarea>
    </div>
    <div class="input-group">
        <label for="textInputSP2">支出分割符号：</label>
        <input type="text" id="textInputSP2" placeholder="默认使用换行">
    </div>
    <div class="input-group">
        <label for="textInput2">支出金额：</label>
        <textarea id="textInput2" placeholder="在此输入需要计算的支出金额..."></textarea>
    </div>
    <button onclick="processText()">提取金额</button>
    <div class="output-container">
        <div id="output" class="output-box">
            <h2>收入</h2>
        </div>
        <div id="output2" class="output-box">
            <h2>支出</h2>
        </div>
    </div>
    <div id="output3"></div>
</div>

<script>
    function processText() {
        const income = calculateAmount('', '收入');
        const expense = calculateAmount('2', '支出');
        const balance = income - expense;

        document.getElementById("output3").innerHTML = `
            <div>收入总额：${income.toFixed(2)}元</div>
            <div>支出总额：${expense.toFixed(2)}元</div>
            <div><strong>结余：${balance.toFixed(2)}元</strong></div>
        `;
    }

    function calculateAmount(id, type) {
        const text = document.getElementById(`textInput${id}`).value;
        const separator = document.getElementById(`textInputSP${id}`).value || '\n';
        const lines = text.split(separator).filter(line => line.trim() !== '');

        const amounts = lines.map(line => {
            const cleanedLine = cleanLine(line);
            const amount = extractAmount(cleanedLine);
            return { line: cleanedLine, amount };
        }).filter(item => !isNaN(item.amount) && item.amount > 0);

        //amounts.sort((a, b) => b.amount - a.amount);

        const totalAmount = amounts.reduce((sum, item) => sum + item.amount, 0);

        const outputHtml = amounts.map((item, index) =>
            `<div class="item"><span>${index + 1}. ${item.line}</span><span>${item.amount.toFixed(2)}元</span></div>`
        ).join('') + `<div class="total">${type}总金额：${totalAmount.toFixed(2)}元</div>`;

        document.getElementById(`output${id}`).innerHTML = `<h2>${type}</h2>${outputHtml}`;

        return totalAmount;
    }

    function cleanLine(line) {
        // 移除多余的空格
        line = line.trim().replace(/\s+/g, ' ');
        // 如果有多个"元"字，只保留最后一个
        const yuanCount = (line.match(/元/g) || []).length;
        if (yuanCount > 1) {
            const lastYuanIndex = line.lastIndexOf('元');
            line = line.slice(0, lastYuanIndex).replace(/元/g, '') + line.slice(lastYuanIndex);
        }
        // 如果没有"元"字，在最后一个数字后添加
        if (!line.includes('元')) {
            const match = line.match(/(\d+(?:\.\d+)?)/g);
            if (match) {
                const lastNumber = match[match.length - 1];
                line = line.replace(lastNumber, `${lastNumber}元`);
            }
        }
        return line;
    }

    function extractAmount(line) {
        const match = line.match(/(\d+(?:\.\d+)?)元/);
        return match ? parseFloat(match[1]) : NaN;
    }
</script>
</body>
</html>
