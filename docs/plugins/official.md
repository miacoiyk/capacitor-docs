<！DOCTYPE超文本标记语言（html）>
<超文本标记语言>
<头>
    <梅塔字符集="utf-8">
    <标题>拼多多利润计算器</标题>
    <风格>
身体{ font-family: 天线, sans-serif; 衬垫:20小卖部; }
        .container { max-width:600小卖部; 边缘:0 汽车; }
        .input-group { margin-bottom:15小卖部; }
标签{ 显示:块; margin-bottom:5小卖部; }
输入{ 宽度:100%; 衬垫:8小卖部; margin-bottom:5小卖部; }
        #result { font-weight:大胆的; margin-top:20小卖部; 颜色:#3498db; }
按钮{ 衬垫:10小卖部 20小卖部; 背景:#2ecc71; 颜色:#fff; 边界:没有一个; 光标:指针; }
    </风格>
</头>
<身体>
    <级班级="container">
        <h2>拼多多利润计算器</h2>
        <级班级="input-group">
            <标签>采购成本（元）</标签>
            <输入类型="number" 步="0.01" 身份证="cost" 所需>
        </级>
        <级班级="input-group">
            <标签>产品原价（元）</标签>
            <输入类型="number" 步="0.01" 身份证="originalPrice" 所需>
        </级>
        <级班级="input-group">
            <标签>退货率（%）</标签>
            <输入类型="number" 步="0.1" 身份证="returnRate" 所需>
        </级>
        <级班级="input-group">
            <标签>平台优惠（元）</标签>
            <输入类型="number" 步="0.01" 身份证="discount" 价值="0" 所需>
        </div>
        <div class="input-group">
            <label>运费成本（元）</label>
            <input type="number" step="0.01" id="shipping" value="0" required>
        </div>
        <button onclick="calculateProfit()">计算利润</button>
        <div id="result"></级>
    </div>

    <script>
    函数calculateProfit（）{
    const cost = parseFloat(document.getElementById('cost').value);
    const originalPrice = parseFloat(document.getElementById('originalPrice').value);
    const returnRate = parseFloat(document.getElementById('returnRate').value)/100;
    const discount = parseFloat(document.getElementById('discount').value);
    const shipping = parseFloat(document.getElementById('shipping').value);
            
    const netPrice = originalPrice - discount - shipping;
    const actualIncome = netPrice * (1 - returnRate);
    持续利润=实际收入-成本；
            
    const resultDiv = document.getElementById('result');
    如果（利润>0）{
    resultDiv. innerHTML=you盈利：${profit.toFixed（2）}；
    resultDiv.style.color = '#2ecc71';
    }else如果（利润====0）{
    resultDiv.innerHTML='刚好保本'；
    resultDiv.style.color = '#f1c40f';
    } else {
    resultDiv.innerHTML=亏损：${Math.abs（profit）. toFixed(2)}；
    resultDiv.style.color = '#e74c3c';
            }
        }
    </script>
</身体>
</超文本标记语言>
