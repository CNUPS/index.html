<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>나만의 자산 포트폴리오</title>
    <style>
        body { font-family: 'Malgun Gothic', sans-serif; background-color: #f4f7f6; color: #333; margin: 0; padding: 20px; }
        .container { max-width: 800px; margin: 0 auto; background: white; padding: 20px; border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1); }
        h1, h2 { color: #2c3e50; }
        .section { margin-bottom: 30px; padding: 20px; background: #eef2f5; border-radius: 8px; }
        label { display: block; margin-top: 10px; font-weight: bold; }
        input { width: 100%; padding: 8px; margin-top: 5px; box-sizing: border-box; border: 1px solid #ccc; border-radius: 4px; }
        button { margin-top: 15px; padding: 10px 15px; background-color: #3498db; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 16px; width: 100%; }
        button:hover { background-color: #2980b9; }
        .result-box { background-color: #dff0d8; padding: 15px; border-radius: 8px; margin-top: 20px; border: 1px solid #d6e9c6; }
        .result-item { font-size: 18px; margin-bottom: 10px; }
        .highlight { font-weight: bold; color: #d35400; }
        table { width: 100%; border-collapse: collapse; margin-top: 10px; }
        th, td { border: 1px solid #ccc; padding: 8px; text-align: center; }
        th { background-color: #bdc3c7; }
    </style>
</head>
<body>

<div class="container">
    <h1>💰 나만의 자산 포트폴리오</h1>

    <div class="section">
        <h2>1. 월별 투자 원금 입력</h2>
        <label for="month">월 (예: 1월)</label>
        <input type="text" id="month" placeholder="몇 월인가요?">
        
        <label for="salary">월급 (원)</label>
        <input type="number" id="salary" value="0">
        
        <label for="savingsInput">적금 넣은 금액 (원)</label>
        <input type="number" id="savingsInput" value="0">
        
        <label for="stockInput">주식/투자 넣은 금액 (원)</label>
        <input type="number" id="stockInput" value="0">
        
        <button onclick="addMonthlyData()">이번 달 데이터 저장하기</button>
    </div>

    <div class="section">
        <h2>📅 올해 누적 기록</h2>
        <table>
            <thead>
                <tr>
                    <th>월</th>
                    <th>월급</th>
                    <th>적금 원금</th>
                    <th>투자 원금</th>
                </tr>
            </thead>
            <tbody id="historyTable">
                </tbody>
        </table>
        <p>현재까지 총 투자 원금: <span id="totalPrincipal" class="highlight">0</span> 원</p>
        <button onclick="clearData()" style="background-color: #e74c3c;">기록 전체 초기화 (새해 시작)</button>
    </div>

    <div class="section">
        <h2>2. 연말 자산 평가 및 목표</h2>
        <label for="currentSavings">현재 예적금 총 잔액 (원)</label>
        <input type="number" id="currentSavings" value="0">
        
        <label for="currentStock">현재 주식 총 평가금액 (원)</label>
        <input type="number" id="currentStock" value="0">

        <label for="targetAsset">올해 희망 목표 자산 (원)</label>
        <input type="number" id="targetAsset" value="0">
        
        <button onclick="calculatePortfolio()" style="background-color: #27ae60;">자산 결과 분석하기</button>
    </div>

    <div id="resultSection" class="result-box" style="display: none;">
        <h2>📊 자산 분석 결과</h2>
        <div class="result-item">올해 총 투자 원금: <span id="resTotalInvest" class="highlight">0</span> 원</div>
        <div class="result-item">현재 총 자산: <span id="resTotalAsset" class="highlight">0</span> 원</div>
        <div class="result-item">순이익 (이자+수익): <span id="resNetProfit" class="highlight">0</span> 원</div>
        <div class="result-item">자산 증가율: <span id="resGrowthRate" class="highlight">0</span> %</div>
        <div class="result-item">투자 수익률 (원금 대비): <span id="resROI" class="highlight">0</span> %</div>
        <hr>
        <div class="result-item">올해 목표 자산: <span id="resTarget" class="highlight">0</span> 원</div>
        <div class="result-item">목표까지 부족한 금액: <span id="resShortfall" class="highlight">0</span> 원</div>
        <div class="result-item">목표 달성을 위해 필요했던 추가 수익률: <span id="resRequiredROI" class="highlight">0</span> %</div>
    </div>
</div>

<script>
    // 페이지가 로드될 때 저장된 데이터를 불러옵니다.
    window.onload = function() {
        renderHistory();
    };

    // 1. 월별 데이터 추가 및 로컬 스토리지 저장
    function addMonthlyData() {
        const month = document.getElementById('month').value;
        const salary = Number(document.getElementById('salary').value);
        const savings = Number(document.getElementById('savingsInput').value);
        const stock = Number(document.getElementById('stockInput').value);

        if (!month) {
            alert('월을 입력해주세요!');
            return;
        }

        // 기존 데이터 가져오기
        let records = JSON.parse(localStorage.getItem('assetRecords')) || [];
        records.push({ month, salary, savings, stock });
        
        // 다시 저장하기
        localStorage.setItem('assetRecords', JSON.stringify(records));
        alert(month + ' 데이터가 저장되었습니다!');
        
        // 입력창 초기화
        document.getElementById('month').value = '';
        document.getElementById('salary').value = '0';
        document.getElementById('savingsInput').value = '0';
        document.getElementById('stockInput').value = '0';

        renderHistory();
    }

    // 2. 화면에 누적 기록 보여주기 및 총 원금 계산
    function renderHistory() {
        let records = JSON.parse(localStorage.getItem('assetRecords')) || [];
        const tbody = document.getElementById('historyTable');
        tbody.innerHTML = '';
        
        let totalPrincipal = 0;

        records.forEach(record => {
            let row = `<tr>
                <td>${record.month}</td>
                <td>${record.salary.toLocaleString()}</td>
                <td>${record.savings.toLocaleString()}</td>
                <td>${record.stock.toLocaleString()}</td>
            </tr>`;
            tbody.innerHTML += row;
            totalPrincipal += (record.savings + record.stock);
        });

        document.getElementById('totalPrincipal').innerText = totalPrincipal.toLocaleString();
    }

    // 3. 기록 초기화 (데이터 삭제)
    function clearData() {
        if(confirm('정말 모든 기록을 지우시겠습니까?')) {
            localStorage.removeItem('assetRecords');
            renderHistory();
            document.getElementById('resultSection').style.display = 'none';
        }
    }

    // 4. 자산 평가 계산 및 결과 보여주기
    function calculatePortfolio() {
        let records = JSON.parse(localStorage.getItem('assetRecords')) || [];
        
        // 총 투자 원금 계산 (적금원금 + 주식원금)
        let totalInvested = records.reduce((sum, record) => sum + record.savings + record.stock, 0);
        
        // 사용자 입력값 가져오기
        const currentSavings = Number(document.getElementById('currentSavings').value);
        const currentStock = Number(document.getElementById('currentStock').value);
        const targetAsset = Number(document.getElementById('targetAsset').value);

        // 계산 로직
        const totalAsset = currentSavings + currentStock; // 현재 총 자산
        const netProfit = totalAsset - totalInvested; // 순이익
        
        // 자산 증가율 = ((현재 자산 - 원금) / 원금) * 100
        let growthRate = 0;
        let roi = 0;
        
        if (totalInvested > 0) {
            growthRate = ((totalAsset - totalInvested) / totalInvested) * 100;
            roi = (netProfit / totalInvested) * 100; // 수익률 (순이익 / 원금)
        }

        const shortfall = targetAsset - totalAsset; // 부족한 금액
        
        // 목표를 달성하기 위해 필요했던 총 수익률
        let requiredROI = 0;
        if (totalInvested > 0 && targetAsset > totalInvested) {
            requiredROI = ((targetAsset - totalInvested) / totalInvested) * 100;
        }

        // 화면에 결과 적용하기
        document.getElementById('resTotalInvest').innerText = totalInvested.toLocaleString();
        document.getElementById('resTotalAsset').innerText = totalAsset.toLocaleString();
        document.getElementById('resNetProfit').innerText = netProfit.toLocaleString();
        document.getElementById('resGrowthRate').innerText = growthRate.toFixed(2);
        document.getElementById('resROI').innerText = roi.toFixed(2);
        
        document.getElementById('resTarget').innerText = targetAsset.toLocaleString();
        
        if (shortfall > 0) {
            document.getElementById('resShortfall').innerText = shortfall.toLocaleString();
        } else {
            document.getElementById('resShortfall').innerText = "0 (목표 달성 완료! 🎉)";
        }
        
        document.getElementById('resRequiredROI').innerText = requiredROI.toFixed(2);

        // 결과 박스 보여주기
        document.getElementById('resultSection').style.display = 'block';
    }
</script>
</body>
</html>
