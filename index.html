<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>모바일 가계부 입력 폼</title>
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
            padding: 25px;
            text-align: center;
        }

        .header h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }

        .month-selector {
            background: rgba(255, 255, 255, 0.2);
            padding: 10px 15px;
            border-radius: 10px;
            display: flex;
            gap: 10px;
            align-items: center;
            justify-content: center;
        }

        .month-selector input {
            padding: 8px 12px;
            border: none;
            border-radius: 8px;
            font-size: 18px;
            width: 120px;
            text-align: center;
        }

        .content {
            padding: 0;
            max-height: 60vh;
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

        .footer {
            padding: 20px;
            background: #f8f9fa;
            display: flex;
            gap: 10px;
        }

        .copy-btn, .reset-btn {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 10px;
            font-size: 26px;
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

        .reset-btn {
            background: #ddd;
            color: #333;
        }

        .reset-btn:hover {
            background: #ccc;
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
            font-size: 32px;
            font-weight: 700;
            color: #667eea;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📱 모바일 가계부</h1>
            <div class="month-selector">
                <label for="yearMonth">년월:</label>
                <input type="month" id="yearMonth">
            </div>
        </div>

        <div class="content">
            <!-- 수입 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>💰 수입</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content show">
                    <div class="summary">
                        <div class="summary-item">
                            <label>총 수입</label>
                            <div class="value" id="incomeSummary">₩0</div>
                        </div>
                    </div>
                    <div id="incomeContainer"></div>
                    <button class="add-item-btn" onclick="addNewItem('income')">+ 수입 항목 추가</button>
                </div>
            </div>

            <!-- 생활비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('life')">+ 생활비 항목 추가</button>
                </div>
            </div>

            <!-- 활동비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('activity')">+ 활동비 항목 추가</button>
                </div>
            </div>

            <!-- 교육비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('education')">+ 교육비 항목 추가</button>
                </div>
            </div>

            <!-- 주거비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('housing')">+ 주거비 항목 추가</button>
                </div>
            </div>

            <!-- 저축 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('savings')">+ 저축 항목 추가</button>
                </div>
            </div>

            <!-- 비정기 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
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
                    <button class="add-item-btn" onclick="addNewItem('misc')">+ 비정기 항목 추가</button>
                </div>
            </div>
        </div>

        <div class="footer">
            <button class="copy-btn" onclick="copyToClipboard()">📋 복사하기</button>
            <button class="reset-btn" onclick="resetForm()">🔄 초기화</button>
        </div>
    </div>

    <script>
        const defaultData = {
            income: [
                { name: 'BM', day: '10일', amount: 3400000 },
                { name: 'MS', day: '30일', amount: 3613056 }
            ],
            life: [
                { name: '현대해상보험(4건)', day: '5일', amount: 229730 },
                { name: '준규 보험(한화)', day: '11일', amount: 66370 },
                { name: '오빠 치과보험 에이스(4건)', day: '', amount: 30730 },
                { name: 'LG 유플러스 TV, 인터넷', day: '10일', amount: 46200 },
                { name: '쿠쿠 정수기', day: '10일', amount: 25900 },
                { name: '준규 핸드폰(SK)', day: '11일', amount: 23400 },
                { name: '태규 핸드폰(LG)', day: '11일', amount: 23400 },
                { name: '도시가스', day: '14일', amount: 7880 },
                { name: '쿠팡 월결제', day: '', amount: 7890 },
                { name: '네이버 페이 월결제', day: '말일', amount: 4900 },
                { name: '관리비', day: '', amount: 250000 },
                { name: '식비, 생필품, 장보기 등', day: '', amount: 200000 }
            ],
            activity: [
                { name: '@병민', day: '', amount: 450000 },
                { name: '@민서', day: '', amount: 260000 },
                { name: '구글 드라이브', day: '19일', amount: 2400 },
                { name: '클로드 AI', day: '', amount: 0 },
                { name: '미리캔버스', day: '', amount: 0 },
                { name: '카카오', day: '5일', amount: 50000 },
                { name: '망고보드', day: '', amount: 0 },
                { name: '챗GPT', day: '', amount: 0 },
                { name: '캡컷', day: '', amount: 0 }
            ],
            education: [
                { name: '와이케이(영,수과) 3과목 준규', day: '말일', amount: 820000 },
                { name: '와이케이 교재비 준규', day: '말일', amount: 50000 },
                { name: '더올바스켓 농구(선수반) 준규', day: '25일', amount: 240000 },
                { name: '경기 비용 / 준규', day: '', amount: 50000 },
                { name: 'C&C 미술 / 태규 주 3회', day: '7일', amount: 450000 },
                { name: 'C&C 미술 재료비 시험비 / 태규', day: '요청시', amount: 25000 },
                { name: '화정초 운동 / 태규', day: '', amount: 0 },
                { name: '패드 수업 / 태규', day: '', amount: 0 },
                { name: '준규 용돈', day: '1일', amount: 50000 },
                { name: '태규 용돈', day: '1일', amount: 50000 }
            ],
            housing: [
                { name: '의정부 자가 주담대(원금+이자)', day: '', amount: 760000 },
                { name: '마통 이자', day: '', amount: 66370 },
                { name: '토스 신용대출 400만원 이자', day: '', amount: 30730 },
                { name: '오빠 용인 대출 3천 이자', day: '', amount: 0 },
                { name: '별빛부영 월세', day: '', amount: 1050000 },
                { name: '의정부 포뷰 월세', day: '', amount: 0 },
                { name: '현대보험대출이자(매월)', day: '5일', amount: 0 }
            ],
            savings: [
                { name: '규규 저축(오빠)', day: '5일', amount: 200000 },
                { name: '토스 자동 주식', day: '', amount: 200000 },
                { name: '연금저축펀드(미래에셋)', day: '말일', amount: 500000 },
                { name: '토스 적금', day: '', amount: 200000 },
                { name: '케이뱅크(경조사)', day: '1일', amount: 100000 }
            ],
            misc: [
                { name: '재산세', day: '', amount: 0 },
                { name: '자동차세', day: '', amount: 0 },
                { name: '조의금, 축의금 등', day: '1일', amount: 100000 },
                { name: '주민세, 기타 등등', day: '', amount: 0 }
            ]
        };

        const today = new Date();
        const year = today.getFullYear();
        const month = String(today.getMonth() + 1).padStart(2, '0');
        document.getElementById('yearMonth').value = `${year}-${month}`;

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

        function createItemHTML(type, item) {
            return `
                <div class="item-group">
                    <span class="input-label">항목명</span>
                    <input type="text" class="item-name" value="${item.name}" style="font-size: 24px;" onchange="calculateSummary()">
                    
                    <span class="input-label">결제일</span>
                    <input type="text" class="item-day" placeholder="예: 5일, 말일" value="${item.day}" style="font-size: 20px;" onchange="calculateSummary()">
                    
                    <span class="input-label">금액</span>
                    <input type="number" class="${type}-expense" placeholder="금액 입력" value="${item.amount}" style="font-size: 24px;" onchange="calculateSummary()">
                    
                    <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">🗑️ 제거</button>
                </div>
            `;
        }

        function initializeData() {
            Object.keys(defaultData).forEach(type => {
                const container = document.getElementById(`${type}Container`);
                container.innerHTML = defaultData[type].map((item) => 
                    createItemHTML(type, item)
                ).join('');
            });
            calculateSummary();
        }

        function calculateSummary() {
            const types = ['income', 'life', 'activity', 'education', 'housing', 'savings', 'misc'];
            
            types.forEach(type => {
                const inputs = document.querySelectorAll(`.${type}-expense`);
                const total = Array.from(inputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
                const summaryId = type === 'income' ? 'incomeSummary' : type + 'Summary';
                document.getElementById(summaryId).textContent = formatNumber(total);
            });
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
                    <input type="number" class="${type}-expense" placeholder="금액 입력" value="0" style="font-size: 24px;" onchange="calculateSummary()">
                    
                    <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">🗑️ 제거</button>
                </div>
            `;
            container.insertAdjacentHTML('beforeend', html);
        }

        function copyToClipboard() {
            const month = document.getElementById('yearMonth').value;
            let text = `📱 가계부 입력 - ${month}\n\n`;

            const types = [
                { id: 'income', label: '💰 수입' },
                { id: 'life', label: '🛒 생활비' },
                { id: 'activity', label: '👤 활동비' },
                { id: 'education', label: '📚 교육비' },
                { id: 'housing', label: '🏠 주거비' },
                { id: 'savings', label: '🏦 저축' },
                { id: 'misc', label: '📌 비정기' }
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

        function resetForm() {
            if (confirm('정말 초기화하시겠습니까?')) {
                location.reload();
            }
        }

        initializeData();
    </script>
</body>
</html>
