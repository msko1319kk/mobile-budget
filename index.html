<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>규규네 가계부</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 10px;
        }

        .container {
            max-width: 500px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px;
            text-align: center;
        }

        .header h1 {
            font-size: 20px;
            margin-bottom: 5px;
        }

        .month-selector {
            background: rgba(255, 255, 255, 0.2);
            padding: 8px 12px;
            border-radius: 8px;
            display: flex;
            gap: 10px;
            align-items: center;
            justify-content: center;
            font-size: 20px;
        }

        .month-selector input {
            padding: 10px 12px;
            border: none;
            border-radius: 6px;
            font-size: 24px;
            width: 140px;
            text-align: center;
            font-weight: 600;
        }

        .month-selector button {
            padding: 10px 12px;
            background: rgba(255,255,255,0.3);
            color: white;
            border: none;
            border-radius: 6px;
            font-size: 20px;
            cursor: pointer;
            font-weight: 600;
        }

        .month-selector button:hover {
            background: rgba(255,255,255,0.5);
        }

        .month-display {
            color: white;
            font-size: 18px;
            font-weight: 600;
            min-width: 80px;
            text-align: center;
        }

        .total-summary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px;
            margin: 0;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .total-item {
            text-align: center;
        }

        .total-item label {
            display: block;
            font-size: 13px;
            margin-bottom: 5px;
            opacity: 0.9;
        }

        .total-item .value {
            font-size: 24px;
            font-weight: 700;
        }

        .content {
            padding: 0;
            max-height: 70vh;
            overflow-y: auto;
        }

        .section {
            border-bottom: 1px solid #eee;
        }

        .section:last-child {
            border-bottom: none;
        }

        .section-header {
            background: #f8f9fa;
            padding: 15px;
            font-weight: 600;
            color: #333;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 26px;
            border-bottom: 2px solid #667eea;
        }

        .section-header:hover {
            background: #f0f1f5;
        }

        .section-header .toggle {
            font-size: 20px;
            transition: transform 0.3s;
        }

        .section-header.collapsed .toggle {
            transform: rotate(-90deg);
        }

        .section-content {
            padding: 15px;
            display: none;
        }

        .section-content.show {
            display: block;
        }

        .item-group {
            margin-bottom: 20px;
            padding: 12px;
            background: #f9f9f9;
            border-radius: 8px;
            border-bottom: 1px solid #eee;
        }

        .item-group:last-child {
            border-bottom: none;
            margin-bottom: 0;
        }

        .item-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 24px;
            margin-bottom: 8px;
        }

        .item-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 5px rgba(102, 126, 234, 0.3);
        }

        .item-group input:disabled {
            background: #f0f0f0;
            color: #666;
        }

        .input-label {
            font-size: 16px;
            color: #666;
            margin-bottom: 3px;
            display: block;
            font-weight: 600;
        }

        .add-item-btn {
            background: #667eea;
            color: white;
            border: none;
            padding: 12px 15px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 20px;
            width: 100%;
            margin-top: 10px;
            font-weight: 600;
        }

        .add-item-btn:hover {
            background: #5568d3;
        }

        .add-item-btn:disabled {
            background: #ccc;
            cursor: not-allowed;
        }

        .remove-btn {
            background: #ff6b6b;
            color: white;
            border: none;
            padding: 8px 10px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 18px;
            margin-top: 8px;
            width: 100%;
            font-weight: 600;
        }

        .remove-btn:hover {
            background: #ff5252;
        }

        .remove-btn:disabled {
            background: #ccc;
            cursor: not-allowed;
        }

        .footer {
            padding: 20px;
            background: #f8f9fa;
            display: flex;
            gap: 10px;
        }

        .save-btn {
            flex: 2;
            padding: 15px;
            border: none;
            border-radius: 10px;
            font-size: 26px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            background: #28a745;
            color: white;
        }

        .save-btn:hover {
            background: #218838;
            transform: translateY(-2px);
        }

        .copy-btn, .share-btn {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 10px;
            font-size: 20px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }

        .copy-btn {
            background: #667eea;
            color: white;
        }

        .copy-btn:hover {
            background: #5568d3;
            transform: translateY(-2px);
        }

        .share-btn {
            background: #51cf66;
            color: white;
        }

        .share-btn:hover {
            background: #40c057;
            transform: translateY(-2px);
        }

        .reset-btn {
            flex: 0.6;
            padding: 12px;
            background: #ff6b6b;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
        }

        .reset-btn:hover {
            background: #ff5252;
        }

        .summary {
            background: #f8f9fa;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 15px;
            text-align: center;
        }

        .summary-item label {
            display: block;
            font-size: 16px;
            color: #666;
            margin-bottom: 5px;
        }

        .summary-item .value {
            font-size: 28px;
            font-weight: 700;
            color: #667eea;
        }

        .view-mode {
            background: #fff3cd;
            padding: 10px;
            text-align: center;
            font-weight: 600;
            color: #856404;
            margin: 10px;
            border-radius: 8px;
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📱 모바일 가계부</h1>
            <div class="month-selector">
                <label for="yearMonth">년월:</label>
                <input type="month" id="yearMonth" onchange="loadMonthData(); updateMonthDisplay()">
                <div class="month-display" id="monthDisplay"></div>
                <button onclick="copyPreviousMonth()" title="이전달 데이터 복사">↩️</button>
            </div>
        </div>

        <div id="viewModeNotice"></div>

        <!-- 전체 합계 -->
        <div class="total-summary">
            <div class="total-item">
                <label>총 수입</label>
                <div class="value" id="totalIncome">₩0</div>
            </div>
            <div class="total-item">
                <label>총 지출</label>
                <div class="value" id="totalExpense">₩0</div>
            </div>
        </div>

        <div class="content">
            <!-- 수입 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>💰 수입</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="incomeSummary">₩0</div>
                        </div>
                    </div>
                    <div id="incomeContainer"></div>
                    <button class="add-item-btn" id="addIncomeBtn" onclick="addNewItem('income')">+ 수입 항목 추가</button>
                </div>
            </div>

            <!-- 생활비 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>🛒 생활비</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="lifeSummary">₩0</div>
                        </div>
                    </div>
                    <div id="lifeContainer"></div>
                    <button class="add-item-btn" id="addLifeBtn" onclick="addNewItem('life')">+ 생활비 항목 추가</button>
                </div>
            </div>

            <!-- 활동비 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>👤 활동비</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="activitySummary">₩0</div>
                        </div>
                    </div>
                    <div id="activityContainer"></div>
                    <button class="add-item-btn" id="addActivityBtn" onclick="addNewItem('activity')">+ 활동비 항목 추가</button>
                </div>
            </div>

            <!-- 교육비 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>📚 교육비</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="educationSummary">₩0</div>
                        </div>
                    </div>
                    <div id="educationContainer"></div>
                    <button class="add-item-btn" id="addEducationBtn" onclick="addNewItem('education')">+ 교육비 항목 추가</button>
                </div>
            </div>

            <!-- 주거비 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>🏠 주거비</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="housingSummary">₩0</div>
                        </div>
                    </div>
                    <div id="housingContainer"></div>
                    <button class="add-item-btn" id="addHousingBtn" onclick="addNewItem('housing')">+ 주거비 항목 추가</button>
                </div>
            </div>

            <!-- 저축 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>🏦 저축</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="savingsSummary">₩0</div>
                        </div>
                    </div>
                    <div id="savingsContainer"></div>
                    <button class="add-item-btn" id="addSavingsBtn" onclick="addNewItem('savings')">+ 저축 항목 추가</button>
                </div>
            </div>

            <!-- 비정기 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>📌 비정기</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="miscSummary">₩0</div>
                        </div>
                    </div>
                    <div id="miscContainer"></div>
                    <button class="add-item-btn" id="addMiscBtn" onclick="addNewItem('misc')">+ 비정기 항목 추가</button>
                </div>
            </div>

            <!-- 기타 섹션 -->
            <div class="section">
                <div class="section-header collapsed" onclick="toggleSection(this)">
                    <span>⭐ 기타 <span style="font-size: 15px; color: #999; font-weight: normal;">(이 달의 추가 지출 내역)</span></span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="etcSummary">₩0</div>
                        </div>
                    </div>
                    <div id="etcContainer"></div>
                    <button class="add-item-btn" id="addEtcBtn" onclick="addNewItem('etc')">+ 기타 항목 추가</button>
                </div>
            </div>
        </div>

        <div class="footer">
            <button class="save-btn" id="saveBtn" onclick="saveData()">💾 저장</button>
            <button class="share-btn" id="shareBtn" onclick="generateShareLink()">🔗 공유</button>
            <button class="copy-btn" id="copyBtn" onclick="copyToClipboard()">📋</button>
            <button class="reset-btn" id="resetBtn" onclick="resetForm()">초기화</button>
        </div>
    </div>

    <script>
        const defaultData = {
            income: [
                { name: 'BM', day: '10일', amount: 0 },
                { name: 'MS', day: '30일', amount: 0 }
            ],
            life: [
                { name: '현대해상보험(4건)', day: '5일', amount: 0 },
                { name: '준규 보험(한화)', day: '11일', amount: 0 },
                { name: '오빠 치과보험 에이스(4건)', day: '', amount: 0 },
                { name: 'LG 유플러스 TV, 인터넷', day: '10일', amount: 0 },
                { name: '쿠쿠 정수기', day: '10일', amount: 0 },
                { name: '준규 핸드폰(SK)', day: '11일', amount: 0 },
                { name: '태규 핸드폰(LG)', day: '11일', amount: 0 },
                { name: '도시가스', day: '14일', amount: 0 },
                { name: '쿠팡 월결제', day: '', amount: 0 },
                { name: '네이버 페이 월결제', day: '말일', amount: 0 },
                { name: '관리비', day: '', amount: 0 },
                { name: '식비, 생필품, 장보기 등', day: '', amount: 0 }
            ],
            activity: [
                { name: '@병민', day: '', amount: 0 },
                { name: '@민서', day: '', amount: 0 },
                { name: '구글 드라이브', day: '19일', amount: 0 },
                { name: '클로드 AI', day: '', amount: 0 },
                { name: '미리캔버스', day: '', amount: 0 },
                { name: '카카오', day: '5일', amount: 0 },
                { name: '망고보드', day: '', amount: 0 },
                { name: '챗GPT', day: '', amount: 0 },
                { name: '캡컷', day: '', amount: 0 }
            ],
            education: [
                { name: '와이케이(영,수과) 3과목 준규', day: '말일', amount: 0 },
                { name: '와이케이 교재비 준규', day: '말일', amount: 0 },
                { name: '더올바스켓 농구(선수반) 준규', day: '25일', amount: 0 },
                { name: '경기 비용 / 준규', day: '', amount: 0 },
                { name: 'C&C 미술 / 태규 주 3회', day: '7일', amount: 0 },
                { name: 'C&C 미술 재료비 시험비 / 태규', day: '요청시', amount: 0 },
                { name: '화정초 운동 / 태규', day: '', amount: 0 },
                { name: '패드 수업 / 태규', day: '', amount: 0 },
                { name: '준규 용돈', day: '1일', amount: 0 },
                { name: '태규 용돈', day: '1일', amount: 0 }
            ],
            housing: [
                { name: '의정부 자가 주담대(원금+이자)', day: '', amount: 0 },
                { name: '마통 이자', day: '', amount: 0 },
                { name: '토스 신용대출 400만원 이자', day: '', amount: 0 },
                { name: '오빠 용인 대출 3천 이자', day: '', amount: 0 },
                { name: '별빛부영 월세', day: '', amount: 0 },
                { name: '의정부 포뷰 월세', day: '', amount: 0 },
                { name: '현대보험대출이자(매월)', day: '5일', amount: 0 }
            ],
            savings: [
                { name: '규규 저축(오빠)', day: '5일', amount: 0 },
                { name: '토스 자동 주식', day: '', amount: 0 },
                { name: '연금저축펀드(미래에셋)', day: '말일', amount: 0 },
                { name: '토스 적금', day: '', amount: 0 },
                { name: '케이뱅크(경조사)', day: '1일', amount: 0 }
            ],
            misc: [
                { name: '재산세', day: '', amount: 0 },
                { name: '자동차세', day: '', amount: 0 },
                { name: '조의금, 축의금 등', day: '1일', amount: 0 },
                { name: '주민세, 기타 등등', day: '', amount: 0 }
            ],
            etc: [
                { name: '기타항목1', day: '', amount: 0 }
            ]
        };

        let isViewMode = false;

        const today = new Date();
        const year = today.getFullYear();
        const month = String(today.getMonth() + 1).padStart(2, '0');
        document.getElementById('yearMonth').value = `${year}-${month}`;
        updateMonthDisplay();

        function toggleSection(header) {
            header.classList.toggle('collapsed');
            const content = header.nextElementSibling;
            content.classList.toggle('show');
        }

        function formatNumber(num) {
            return new Intl.NumberFormat('ko-KR', {
                style: 'currency',
                currency: 'KRW',
                minimumFractionDigits: 0,
                maximumFractionDigits: 0
            }).format(num);
        }

        function getMonthKey() {
            return document.getElementById('yearMonth').value;
        }

        function updateMonthDisplay() {
            const monthKey = getMonthKey();
            const [year, month] = monthKey.split('-');
            const monthNames = ['1월', '2월', '3월', '4월', '5월', '6월', '7월', '8월', '9월', '10월', '11월', '12월'];
            const displayText = `${year}년 ${monthNames[parseInt(month) - 1]}`;
            document.getElementById('monthDisplay').textContent = displayText;
        }

        function saveData() {
            if (isViewMode) return;
            
            const monthKey = getMonthKey();
            const data = {};

            Object.keys(defaultData).forEach(type => {
                data[type] = [];
                const container = document.getElementById(`${type}Container`);
                const items = container.querySelectorAll('.item-group');
                
                items.forEach(item => {
                    const nameInput = item.querySelector('.item-name');
                    const dayInput = item.querySelector('.item-day');
                    const amountInput = item.querySelector(`input[class*="${type}-expense"]`);
                    
                    data[type].push({
                        name: nameInput.value,
                        day: dayInput.value,
                        amount: parseInt(amountInput.value) || 0
                    });
                });
            });

            localStorage.setItem(`budget_${monthKey}`, JSON.stringify(data));
            calculateSummary();
            alert('✅ 저장되었습니다!');
        }

        function loadMonthData() {
            const monthKey = getMonthKey();
            const savedData = localStorage.getItem(`budget_${monthKey}`);
            const data = savedData ? JSON.parse(savedData) : defaultData;

            Object.keys(data).forEach(type => {
                const container = document.getElementById(`${type}Container`);
                container.innerHTML = data[type].map((item) => 
                    createItemHTML(type, item, isViewMode)
                ).join('');
            });

            calculateSummary();
        }

        function createItemHTML(type, item, disabled = false) {
            return `
                <div class="item-group">
                    <span class="input-label">항목명</span>
                    <input type="text" class="item-name" value="${item.name}" style="font-size: 24px;" ${disabled ? 'disabled' : 'onchange="saveData()"'}>
                    
                    <span class="input-label">결제일</span>
                    <input type="text" class="item-day" placeholder="예: 5일, 말일" value="${item.day}" style="font-size: 20px;" ${disabled ? 'disabled' : 'onchange="saveData()"'}>
                    
                    <span class="input-label">금액</span>
                    <input type="number" class="${type}-expense" placeholder="금액 입력" value="${item.amount}" style="font-size: 24px;" ${disabled ? 'disabled' : 'onchange="saveData()"'}>
                    
                    <button class="remove-btn" ${disabled ? 'disabled' : ''} onclick="this.parentElement.remove(); saveData();">🗑️ 제거</button>
                </div>
            `;
        }

        function calculateSummary() {
            const types = ['income', 'life', 'activity', 'education', 'housing', 'savings', 'misc', 'etc'];
            let totalIncome = 0;
            let totalExpense = 0;
            
            types.forEach(type => {
                const inputs = document.querySelectorAll(`.${type}-expense`);
                const total = Array.from(inputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
                const summaryId = type === 'income' ? 'incomeSummary' : type + 'Summary';
                document.getElementById(summaryId).textContent = formatNumber(total);

                if (type === 'income') {
                    totalIncome = total;
                } else {
                    totalExpense += total;
                }
            });

            document.getElementById('totalIncome').textContent = formatNumber(totalIncome);
            document.getElementById('totalExpense').textContent = formatNumber(totalExpense);
        }

        function addNewItem(type) {
            const container = document.getElementById(`${type}Container`);
            const html = `
                <div class="item-group">
                    <span class="input-label">항목명</span>
                    <input type="text" class="item-name" placeholder="항목명 입력" style="font-size: 24px;">
                    
                    <span class="input-label">결제일</span>
                    <input type="text" class="item-day" placeholder="예: 5일, 말일" style="font-size: 20px;">
                    
                    <span class="input-label">금액</span>
                    <input type="number" class="${type}-expense" placeholder="금액 입력" value="0" style="font-size: 24px;" onchange="saveData()">
                    
                    <button class="remove-btn" onclick="this.parentElement.remove(); saveData();">🗑️ 제거</button>
                </div>
            `;
            container.insertAdjacentHTML('beforeend', html);
        }

        function copyToClipboard() {
            const month = getMonthKey();
            let text = `📱 가계부 입력 - ${month}\n\n`;

            const types = [
                { id: 'income', label: '💰 수입' },
                { id: 'life', label: '🛒 생활비' },
                { id: 'activity', label: '👤 활동비' },
                { id: 'education', label: '📚 교육비' },
                { id: 'housing', label: '🏠 주거비' },
                { id: 'savings', label: '🏦 저축' },
                { id: 'misc', label: '📌 비정기' },
                { id: 'etc', label: '⭐ 기타' }
            ];

            types.forEach(type => {
                text += `\n${type.label}\n`;
                const container = document.getElementById(`${type.id}Container`);
                const items = container.querySelectorAll('.item-group');
                
                items.forEach(item => {
                    const nameInput = item.querySelector('.item-name');
                    const dayInput = item.querySelector('.item-day');
                    const amountInput = item.querySelector(`input[class*="${type.id}-expense"]`);
                    
                    const name = nameInput.value || '항목';
                    const day = dayInput && dayInput.value ? `(${dayInput.value})` : '';
                    const amount = parseInt(amountInput.value) || 0;
                    
                    if (amount > 0 || name !== '항목') {
                        text += `${name} ${day}: ₩${amount.toLocaleString()}\n`;
                    }
                });
            });

            navigator.clipboard.writeText(text).then(() => {
                alert('✅ 복사되었습니다!\n스프레드시트에 붙여넣기하세요.');
            });
        }

        function generateShareLink() {
            try {
                // 코드 입력받기
                const code = prompt('공유 코드를 입력하세요 (예: abc1319):');
                
                if (!code) {
                    alert('코드 입력이 취소되었습니다.');
                    return;
                }
                
                if (code.length < 3) {
                    alert('코드는 3자 이상이어야 합니다.');
                    return;
                }
                
                const monthKey = getMonthKey();
                const data = {};

                Object.keys(defaultData).forEach(type => {
                    data[type] = [];
                    const container = document.getElementById(`${type}Container`);
                    if (!container) return;
                    
                    const items = container.querySelectorAll('.item-group');
                    items.forEach(item => {
                        const nameInput = item.querySelector('.item-name');
                        const dayInput = item.querySelector('.item-day');
                        const amountInput = item.querySelector(`input[class*="${type}-expense"]`);
                        
                        if (nameInput && dayInput && amountInput) {
                            data[type].push({
                                name: nameInput.value || '',
                                day: dayInput.value || '',
                                amount: parseInt(amountInput.value) || 0
                            });
                        }
                    });
                });

                // 코드로 localStorage에 저장
                localStorage.setItem(`shared_${code}`, JSON.stringify({
                    data: data,
                    month: monthKey,
                    createdAt: new Date().toISOString()
                }));

                const baseUrl = window.location.href.split('?')[0];
                const shareLink = `${baseUrl}?code=${code}`;
                
                // 팝업 생성
                const popup = document.createElement('div');
                popup.style.cssText = `
                    position: fixed;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    background: white;
                    padding: 20px;
                    border-radius: 12px;
                    box-shadow: 0 4px 20px rgba(0,0,0,0.3);
                    z-index: 10000;
                    width: 90%;
                    max-width: 400px;
                `;
                
                popup.innerHTML = `
                    <h3 style="margin-bottom: 15px; text-align: center;">✅ 공유 준비 완료!</h3>
                    <p style="font-size: 13px; color: #666; margin-bottom: 10px;">아래 링크를 A에게 보내세요:</p>
                    <textarea style="width: 100%; height: 80px; padding: 10px; border: 1px solid #ddd; border-radius: 8px; font-size: 12px; font-family: monospace; resize: none;" readonly>${shareLink}</textarea>
                    <p style="font-size: 12px; color: #999; margin-top: 10px; text-align: center;">코드: <strong>${code}</strong></p>
                    <div style="margin-top: 15px; display: flex; gap: 10px;">
                        <button onclick="navigator.clipboard.writeText('${shareLink}').then(() => alert('복사되었습니다!')).catch(() => alert('복사 실패'))" style="flex: 1; padding: 10px; background: #667eea; color: white; border: none; border-radius: 8px; cursor: pointer; font-weight: 600;">📋 복사하기</button>
                        <button onclick="this.parentElement.parentElement.remove()" style="flex: 1; padding: 10px; background: #ddd; color: #333; border: none; border-radius: 8px; cursor: pointer; font-weight: 600;">닫기</button>
                    </div>
                `;
                
                document.body.appendChild(popup);
                
            } catch (error) {
                alert('❌ 에러 발생: ' + error.message);
                console.error(error);
            }
        }

        function loadSharedData() {
            const params = new URLSearchParams(window.location.search);
            const code = params.get('code');

            if (code) {
                try {
                    console.log('공유 코드 감지됨:', code);
                    const sharedData = localStorage.getItem(`shared_${code}`);
                    
                    if (!sharedData) {
                        alert('❌ 코드를 찾을 수 없습니다.');
                        loadMonthData();
                        return;
                    }
                    
                    const parsed = JSON.parse(sharedData);
                    const data = parsed.data;
                    const month = parsed.month;
                    
                    isViewMode = true;
                    
                    document.getElementById('viewModeNotice').innerHTML = '<div class="view-mode">👀 뷰어 모드 (수정 불가)</div>';
                    document.getElementById('copyBtn').disabled = false;
                    document.getElementById('shareBtn').disabled = true;
                    document.getElementById('resetBtn').disabled = true;
                    document.getElementById('yearMonth').disabled = true;
                    
                    Array.from(document.querySelectorAll('.add-item-btn')).forEach(btn => btn.disabled = true);
                    
                    if (month) {
                        document.getElementById('yearMonth').value = month;
                        updateMonthDisplay();
                    }

                    Object.keys(data).forEach(type => {
                        const container = document.getElementById(`${type}Container`);
                        if (container) {
                            container.innerHTML = data[type].map((item) => 
                                createItemHTML(type, item, true)
                            ).join('');
                        }
                    });

                    calculateSummary();
                    alert('✅ 공유된 데이터를 불러왔습니다!');
                } catch (e) {
                    console.error('데이터 로드 실패:', e);
                    alert('❌ 데이터 로드 실패: ' + e.message);
                    loadMonthData();
                }
            } else {
                loadMonthData();
            }
        }

        function resetForm() {
            if (confirm('이 달의 데이터를 초기화하시겠습니까?')) {
                const monthKey = getMonthKey();
                localStorage.removeItem(`budget_${monthKey}`);
                loadMonthData();
            }
        }

        function copyPreviousMonth() {
            const currentMonth = getMonthKey();
            const [year, month] = currentMonth.split('-');
            let prevMonth = parseInt(month) - 1;
            let prevYear = parseInt(year);

            if (prevMonth === 0) {
                prevMonth = 12;
                prevYear -= 1;
            }

            const prevMonthKey = `${prevYear}-${String(prevMonth).padStart(2, '0')}`;
            const prevData = localStorage.getItem(`budget_${prevMonthKey}`);

            if (!prevData) {
                alert(`${prevMonthKey} 데이터가 없습니다.`);
                return;
            }

            if (confirm(`${prevMonthKey} 데이터를 ${currentMonth}로 복사하시겠습니까?`)) {
                localStorage.setItem(`budget_${currentMonth}`, prevData);
                loadMonthData();
                alert('복사되었습니다!');
            }
        }

        loadSharedData();
    </script>
</body>
</html>
