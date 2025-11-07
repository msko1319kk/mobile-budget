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
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .item-group:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .item-group label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
            color: #333;
            font-size: 28px;
        }

        .item-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 28px;
            margin-bottom: 5px;
        }

        .item-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 5px rgba(102, 126, 234, 0.3);
        }

        .item-note {
            font-size: 16px;
            color: #999;
            margin-top: 3px;
        }

        .add-item-btn {
            background: #667eea;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
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
            padding: 5px 10px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 8px;
            width: 100%;
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
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
        }

        .summary-item {
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

        @media (max-width: 600px) {
            .container {
                border-radius: 0;
                max-width: 100%;
            }

            body {
                padding: 0;
            }

            .header {
                padding: 20px;
            }

            .header h1 {
                font-size: 20px;
            }
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
                    <div class="item-group">
                        <label>BM (기업)</label>
                        <input type="number" class="income" placeholder="금액 입력" data-name="BM" value="3400000">
                    </div>
                    <div class="item-group">
                        <label>MS (우리 1002-494)</label>
                        <input type="number" class="income" placeholder="금액 입력" data-name="MS" value="3613056">
                    </div>
                    <button class="add-item-btn" onclick="addIncomeItem()">+ 수입 항목 추가</button>
                    <div id="incomeItems"></div>
                </div>
            </div>

            <!-- 생활비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>🛒 생활비 (보험, 공과금, 인터넷 등)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="lifeSummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>현대해상보험(4건)</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="현대해상보험(4건)" value="229730">
                        <div class="item-note">결제일: 5일</div>
                    </div>
                    <div class="item-group">
                        <label>준규 보험(한화)</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="준규 보험(한화)" value="66370">
                        <div class="item-note">결제일: 11일</div>
                    </div>
                    <div class="item-group">
                        <label>오빠 치과보험 에이스(4건)</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="오빠 치과보험 에이스(4건)" value="30730">
                    </div>
                    <div class="item-group">
                        <label>LG 유플러스 TV, 인터넷</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="LG 유플러스 TV, 인터넷" value="46200">
                        <div class="item-note">결제일: 10일</div>
                    </div>
                    <div class="item-group">
                        <label>쿠쿠 정수기</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="쿠쿠 정수기" value="25900">
                        <div class="item-note">결제일: 10일</div>
                    </div>
                    <div class="item-group">
                        <label>준규 핸드폰(SK)</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="준규 핸드폰(SK)" value="23400">
                        <div class="item-note">결제일: 11일</div>
                    </div>
                    <div class="item-group">
                        <label>태규 핸드폰(LG)</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="태규 핸드폰(LG)" value="23400">
                        <div class="item-note">결제일: 11일</div>
                    </div>
                    <div class="item-group">
                        <label>도시가스</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="도시가스" value="7880">
                        <div class="item-note">결제일: 14일 (짝수달만)</div>
                    </div>
                    <div class="item-group">
                        <label>쿠팡 월결제</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="쿠팡 월결제" value="7890">
                    </div>
                    <div class="item-group">
                        <label>네이버 페이 월결제</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="네이버 페이 월결제" value="4900">
                    </div>
                    <div class="item-group">
                        <label>관리비</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="관리비" value="250000">
                    </div>
                    <div class="item-group">
                        <label>식비, 생필품, 장보기 등</label>
                        <input type="number" class="life-expense" placeholder="금액 입력" data-name="식비, 생필품, 장보기 등" value="200000">
                    </div>
                    <button class="add-item-btn" onclick="addLifeExpense()">+ 생활비 항목 추가</button>
                    <div id="lifeItems"></div>
                </div>
            </div>

            <!-- 활동비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>👤 활동비 (BM, MS 개인 활동비)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="activitySummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>@병민</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="@병민" value="450000">
                        <div class="item-note">식비: 250,000 / 차&주류비+용돈: 140,000 / 핸드폰비: 60,000</div>
                    </div>
                    <div class="item-group">
                        <label>@민서</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="@민서" value="260000">
                        <div class="item-note">출퇴근차비: 100,000 / 커피&삭사+용돈: 100,000 / 핸드폰비: 60,000</div>
                    </div>
                    <div class="item-group">
                        <label>구글 드라이브</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="구글 드라이브" value="2400">
                        <div class="item-note">결제일: 19일</div>
                    </div>
                    <div class="item-group">
                        <label>클로드 AI</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="클로드 AI" value="0">
                    </div>
                    <div class="item-group">
                        <label>미리캔버스</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="미리캔버스" value="0">
                    </div>
                    <div class="item-group">
                        <label>카카오 매달 5일</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="카카오" value="50000">
                    </div>
                    <div class="item-group">
                        <label>망고보드</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="망고보드" value="0">
                    </div>
                    <div class="item-group">
                        <label>챗GPT</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="챗GPT" value="0">
                    </div>
                    <div class="item-group">
                        <label>캡컷</label>
                        <input type="number" class="activity-expense" placeholder="금액 입력" data-name="캡컷" value="0">
                    </div>
                    <button class="add-item-btn" onclick="addActivityExpense()">+ 활동비 항목 추가</button>
                    <div id="activityItems"></div>
                </div>
            </div>

            <!-- 교육비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>📚 교육비 (학원, 운동, 미술 등)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="educationSummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>와이케이(영,수과) 3과목 준규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="와이케이(영,수과) 3과목 준규" value="820000">
                        <div class="item-note">결제일: 말일</div>
                    </div>
                    <div class="item-group">
                        <label>와이케이 교재비 준규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="와이케이 교재비 준규" value="50000">
                    </div>
                    <div class="item-group">
                        <label>더올바스켓 농구(선수반) 준규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="더올바스켓 농구(선수반) 준규" value="240000">
                        <div class="item-note">결제일: 25일</div>
                    </div>
                    <div class="item-group">
                        <label>경기 비용 / 준규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="경기 비용 / 준규" value="50000">
                    </div>
                    <div class="item-group">
                        <label>C&C 미술 / 태규 주 3회</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="C&C 미술 / 태규 주 3회" value="450000">
                        <div class="item-note">결제일: 7일</div>
                    </div>
                    <div class="item-group">
                        <label>C&C 미술 재료비 시험비 / 태규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="C&C 미술 재료비 시험비 / 태규" value="25000">
                    </div>
                    <div class="item-group">
                        <label>화정초 운동 / 태규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="화정초 운동 / 태규" value="0">
                    </div>
                    <div class="item-group">
                        <label>패드 수업 / 태규</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="패드 수업 / 태규" value="0">
                    </div>
                    <div class="item-group">
                        <label>준규 용돈</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="준규 용돈" value="50000">
                        <div class="item-note">결제일: 1일</div>
                    </div>
                    <div class="item-group">
                        <label>태규 용돈</label>
                        <input type="number" class="education-expense" placeholder="금액 입력" data-name="태규 용돈" value="50000">
                        <div class="item-note">결제일: 1일</div>
                    </div>
                    <button class="add-item-btn" onclick="addEducationExpense()">+ 교육비 항목 추가</button>
                    <div id="educationItems"></div>
                </div>
            </div>

            <!-- 주거비 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>🏠 주거비 (대출, 월세 등)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="housingSummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>의정부 자가 주담대(원금+이자)</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="의정부 자가 주담대(원금+이자)" value="760000">
                    </div>
                    <div class="item-group">
                        <label>마통 이자</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="마통 이자" value="66370">
                    </div>
                    <div class="item-group">
                        <label>토스 신용대출 400만원 이자</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="토스 신용대출 400만원 이자" value="30730">
                    </div>
                    <div class="item-group">
                        <label>오빠 용인 대출 3천 이자</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="오빠 용인 대출 3천 이자" value="0">
                        <div class="item-note">기한: 26년 7월 24일까지</div>
                    </div>
                    <div class="item-group">
                        <label>별빛부영 월세</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="별빛부영 월세" value="1050000">
                    </div>
                    <div class="item-group">
                        <label>의정부 포뷰 월세</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="의정부 포뷰 월세" value="0">
                        <div class="item-note">음수 입력 가능 (-1050000)</div>
                    </div>
                    <div class="item-group">
                        <label>현대보험대출이자(매월)</label>
                        <input type="number" class="housing-expense" placeholder="금액 입력" data-name="현대보험대출이자(매월)" value="0">
                        <div class="item-note">결제일: 5일</div>
                    </div>
                    <button class="add-item-btn" onclick="addHousingExpense()">+ 주거비 항목 추가</button>
                    <div id="housingItems"></div>
                </div>
            </div>

            <!-- 저축 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>🏦 저축 (적금, 펀드, 주식 등)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="savingsSummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>규규 저축(오빠)</label>
                        <input type="number" class="savings-expense" placeholder="금액 입력" data-name="규규 저축(오빠)" value="200000">
                        <div class="item-note">결제일: 5일</div>
                    </div>
                    <div class="item-group">
                        <label>토스 자동 주식</label>
                        <input type="number" class="savings-expense" placeholder="금액 입력" data-name="토스 자동 주식" value="200000">
                    </div>
                    <div class="item-group">
                        <label>연금저축펀드(미래에셋)</label>
                        <input type="number" class="savings-expense" placeholder="금액 입력" data-name="연금저축펀드(미래에셋)" value="500000">
                        <div class="item-note">결제일: 말일</div>
                    </div>
                    <div class="item-group">
                        <label>토스 적금</label>
                        <input type="number" class="savings-expense" placeholder="금액 입력" data-name="토스 적금" value="200000">
                    </div>
                    <div class="item-group">
                        <label>케이뱅크(경조사)</label>
                        <input type="number" class="savings-expense" placeholder="금액 입력" data-name="케이뱅크(경조사)" value="100000">
                        <div class="item-note">결제일: 1일</div>
                    </div>
                    <button class="add-item-btn" onclick="addSavingsExpense()">+ 저축 항목 추가</button>
                    <div id="savingsItems"></div>
                </div>
            </div>

            <!-- 비정기 섹션 -->
            <div class="section">
                <div class="section-header" onclick="toggleSection(this)">
                    <span>📌 비정기 (경조사, 세금 등)</span>
                    <span class="toggle">▼</span>
                </div>
                <div class="section-content">
                    <div class="summary">
                        <div class="summary-item">
                            <label>소계</label>
                            <div class="value" id="miscSummary">₩0</div>
                        </div>
                    </div>
                    <div class="item-group">
                        <label>재산세 (1년에 2번)</label>
                        <input type="number" class="misc-expense" placeholder="금액 입력" data-name="재산세" value="0">
                    </div>
                    <div class="item-group">
                        <label>자동차세 (1년에 2번)</label>
                        <input type="number" class="misc-expense" placeholder="금액 입력" data-name="자동차세" value="0">
                    </div>
                    <div class="item-group">
                        <label>조의금, 축의금 등</label>
                        <input type="number" class="misc-expense" placeholder="금액 입력" data-name="조의금, 축의금 등" value="100000">
                        <div class="item-note">결제일: 1일</div>
                    </div>
                    <div class="item-group">
                        <label>주민세, 기타 등등</label>
                        <input type="number" class="misc-expense" placeholder="금액 입력" data-name="주민세, 기타 등등" value="0">
                    </div>
                    <button class="add-item-btn" onclick="addMiscExpense()">+ 비정기 항목 추가</button>
                    <div id="miscItems"></div>
                </div>
            </div>
        </div>

        <div class="footer">
            <button class="copy-btn" onclick="copyToClipboard()">📋 복사하기</button>
            <button class="reset-btn" onclick="resetForm()">🔄 초기화</button>
        </div>
    </div>

    <script>
        // 현재 월을 기본값으로 설정
        const today = new Date();
        const year = today.getFullYear();
        const month = String(today.getMonth() + 1).padStart(2, '0');
        document.getElementById('yearMonth').value = `${year}-${month}`;

        // 섹션 토글
        function toggleSection(header) {
            header.classList.toggle('collapsed');
            const content = header.nextElementSibling;
            content.classList.toggle('show');
        }

        // 숫자 포맷팅
        function formatNumber(num) {
            return new Intl.NumberFormat('ko-KR', {
                style: 'currency',
                currency: 'KRW',
                minimumFractionDigits: 0,
                maximumFractionDigits: 0
            }).format(num);
        }

        // 합계 계산
        function calculateSummary() {
            const incomeInputs = document.querySelectorAll('.income');
            const lifeInputs = document.querySelectorAll('.life-expense');
            const activityInputs = document.querySelectorAll('.activity-expense');
            const educationInputs = document.querySelectorAll('.education-expense');
            const housingInputs = document.querySelectorAll('.housing-expense');
            const savingsInputs = document.querySelectorAll('.savings-expense');
            const miscInputs = document.querySelectorAll('.misc-expense');

            const income = Array.from(incomeInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const life = Array.from(lifeInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const activity = Array.from(activityInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const education = Array.from(educationInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const housing = Array.from(housingInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const savings = Array.from(savingsInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);
            const misc = Array.from(miscInputs).reduce((sum, input) => sum + (parseInt(input.value) || 0), 0);

            document.getElementById('incomeSummary').textContent = formatNumber(income);
            document.getElementById('lifeSummary').textContent = formatNumber(life);
            document.getElementById('activitySummary').textContent = formatNumber(activity);
            document.getElementById('educationSummary').textContent = formatNumber(education);
            document.getElementById('housingSummary').textContent = formatNumber(housing);
            document.getElementById('savingsSummary').textContent = formatNumber(savings);
            document.getElementById('miscSummary').textContent = formatNumber(misc);
        }

        // 동적 항목 추가
        function addIncomeItem() {
            const container = document.getElementById('incomeItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 수입 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="income" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addLifeExpense() {
            const container = document.getElementById('lifeItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 생활비 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="life-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addActivityExpense() {
            const container = document.getElementById('activityItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 활동비 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="activity-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addEducationExpense() {
            const container = document.getElementById('educationItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 교육비 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="education-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addHousingExpense() {
            const container = document.getElementById('housingItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 주거비 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="housing-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addSavingsExpense() {
            const container = document.getElementById('savingsItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 저축 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="savings-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        function addMiscExpense() {
            const container = document.getElementById('miscItems');
            const itemGroup = document.createElement('div');
            itemGroup.className = 'item-group';
            itemGroup.innerHTML = `
                <label>새 비정기 항목</label>
                <input type="text" placeholder="항목명 입력">
                <input type="number" class="misc-expense" placeholder="금액 입력" value="0">
                <button class="remove-btn" onclick="this.parentElement.remove(); calculateSummary();">제거</button>
            `;
            container.appendChild(itemGroup);
        }

        // 복사
        function copyToClipboard() {
            const month = document.getElementById('yearMonth').value;
            let text = `📱 가계부 입력 - ${month}\n\n`;

            text += `💰 수입\n`;
            document.querySelectorAll('.income').forEach(input => {
                const name = input.dataset.name || '수입';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#incomeItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n🛒 생활비\n`;
            document.querySelectorAll('.life-expense').forEach(input => {
                const name = input.dataset.name || '생활비';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#lifeItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n👤 활동비\n`;
            document.querySelectorAll('.activity-expense').forEach(input => {
                const name = input.dataset.name || '활동비';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#activityItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n📚 교육비\n`;
            document.querySelectorAll('.education-expense').forEach(input => {
                const name = input.dataset.name || '교육비';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#educationItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n🏠 주거비\n`;
            document.querySelectorAll('.housing-expense').forEach(input => {
                const name = input.dataset.name || '주거비';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#housingItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n🏦 저축\n`;
            document.querySelectorAll('.savings-expense').forEach(input => {
                const name = input.dataset.name || '저축';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#savingsItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            text += `\n📌 비정기\n`;
            document.querySelectorAll('.misc-expense').forEach(input => {
                const name = input.dataset.name || '비정기';
                const value = parseInt(input.value) || 0;
                text += `${name}: ₩${value.toLocaleString()}\n`;
            });
            document.querySelectorAll('#miscItems input[type="text"]').forEach((input, index) => {
                if (input.value) {
                    const valueInput = input.nextElementSibling;
                    const value = parseInt(valueInput.value) || 0;
                    text += `${input.value}: ₩${value.toLocaleString()}\n`;
                }
            });

            navigator.clipboard.writeText(text).then(() => {
                alert('✅ 복사되었습니다!\n스프레드시트에 붙여넣기하세요.');
            });
        }

        // 초기화
        function resetForm() {
            if (confirm('정말 초기화하시겠습니까?')) {
                location.reload();
            }
        }

        // 이벤트 리스너
        document.addEventListener('input', calculateSummary);
        
        // 초기 계산
        calculateSummary();
    </script>
</body>
</html>
