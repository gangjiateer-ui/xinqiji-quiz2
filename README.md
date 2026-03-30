# xinqiji-quiz2
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>辛弃疾《菩萨蛮·书江西造口壁》测验</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #f1f2f6;
            font-family: 'Segoe UI', 'Roboto', 'Noto Sans', system-ui, -apple-system, 'Microsoft YaHei', sans-serif;
            padding: 20px;
            color: #1e2a3e;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 32px;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            padding: 20px 24px 32px;
        }

        h1 {
            font-size: 1.8rem;
            text-align: center;
            margin-bottom: 0.25rem;
            color: #1e466e;
        }

        .sub {
            text-align: center;
            color: #5a6e85;
            font-size: 0.9rem;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 18px;
            margin-bottom: 24px;
        }

        .question-card {
            background: #f9fafc;
            border-radius: 24px;
            padding: 18px 20px;
            margin-bottom: 24px;
            border: 1px solid #e9edf2;
        }

        .question-title {
            font-weight: 700;
            font-size: 1.2rem;
            margin-bottom: 14px;
            display: flex;
            align-items: baseline;
            gap: 8px;
            flex-wrap: wrap;
        }

        .q-type {
            background: #d4e2f0;
            font-size: 0.7rem;
            font-weight: 600;
            padding: 2px 10px;
            border-radius: 40px;
            color: #1e466e;
        }

        .q-text {
            font-weight: 500;
            line-height: 1.4;
        }

        .options {
            margin: 16px 0 8px 0;
            padding-left: 8px;
        }

        .option {
            display: flex;
            align-items: flex-start;
            gap: 12px;
            margin-bottom: 12px;
            cursor: pointer;
            font-size: 0.95rem;
            padding: 6px 0;
        }

        .option input {
            margin-top: 2px;
            transform: scale(1.05);
            flex-shrink: 0;
        }

        .option label {
            line-height: 1.4;
            color: #1e2a3e;
            cursor: pointer;
            flex: 1;
        }

        .multi-hint {
            font-size: 0.75rem;
            color: #6c7a91;
            margin-top: 6px;
            margin-left: 26px;
        }

        .feedback {
            margin-top: 12px;
            padding: 12px 14px;
            border-radius: 16px;
            font-size: 0.85rem;
            background: #f0f3f8;
            display: none;
            border-left: 4px solid #cbd5e1;
        }

        .feedback.correct {
            background: #e0f2e9;
            border-left-color: #2b9b5e;
            color: #1f6e43;
            display: block;
        }

        .feedback.wrong {
            background: #fee9e6;
            border-left-color: #e25c5c;
            color: #b13e3e;
            display: block;
        }

        .answer-key {
            font-size: 0.85rem;
            margin-top: 8px;
            color: #4b5e7a;
        }

        .action-buttons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 16px;
            margin: 30px 0 20px;
        }

        button {
            background: #1e466e;
            color: white;
            border: none;
            font-size: 1rem;
            font-weight: 600;
            padding: 12px 24px;
            border-radius: 48px;
            cursor: pointer;
            transition: 0.2s;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            min-width: 140px;
        }

        button:hover {
            background: #0f2f4f;
            transform: scale(0.98);
        }

        .reset-btn {
            background: #5c6f87;
        }

        .reset-btn:hover {
            background: #3e4f66;
        }

        .score-area {
            text-align: center;
            font-size: 1.3rem;
            font-weight: 700;
            background: #eef3fc;
            border-radius: 60px;
            padding: 12px 16px;
            margin-top: 8px;
            margin-bottom: 12px;
        }

        .footer-note {
            text-align: center;
            font-size: 0.75rem;
            color: #8a9bb0;
            margin-top: 20px;
            border-top: 1px solid #e2e8f0;
            padding-top: 18px;
        }

        @media (max-width: 560px) {
            .container {
                padding: 16px;
            }
            .question-card {
                padding: 14px;
            }
            .q-text {
                font-size: 0.95rem;
            }
            button {
                padding: 10px 18px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <h1>📜 辛弃疾 · 菩萨蛮</h1>
    <div class="sub">《书江西造口壁》· 素养测评</div>

    <form id="quizForm">
        <!-- 题目1 单选 -->
        <div class="question-card" data-qid="1">
            <div class="question-title">
                <span class="q-type">单选题</span>
                <span class="q-text">1. 辛弃疾《菩萨蛮·书江西造口壁》中“郁孤台下清江水”的“郁孤台”位于今（    ）</span>
            </div>
            <div class="options">
                <div class="option"><input type="radio" name="q1" value="A" id="q1_a"><label for="q1_a">A. 江西南昌</label></div>
                <div class="option"><input type="radio" name="q1" value="B" id="q1_b"><label for="q1_b">B. 江西赣州</label></div>
                <div class="option"><input type="radio" name="q1" value="C" id="q1_c"><label for="q1_c">C. 福建福州</label></div>
                <div class="option"><input type="radio" name="q1" value="D" id="q1_d"><label for="q1_d">D. 湖南长沙</label></div>
            </div>
            <div class="feedback" id="fb1"></div>
        </div>

        <!-- 题目2 单选 -->
        <div class="question-card" data-qid="2">
            <div class="question-title">
                <span class="q-type">单选题</span>
                <span class="q-text">2. 下列对“江晚正愁余，山深闻鹧鸪”一句赏析正确的是（    ）</span>
            </div>
            <div class="options">
                <div class="option"><input type="radio" name="q2" value="A" id="q2_a"><label for="q2_a">A. 以乐景写哀情，反衬词人归乡之喜</label></div>
                <div class="option"><input type="radio" name="q2" value="B" id="q2_b"><label for="q2_b">B. 鹧鸪鸟象征高洁志向，暗含自我勉励</label></div>
                <div class="option"><input type="radio" name="q2" value="C" id="q2_c"><label for="q2_c">C. 借暮色苍茫与鹧鸪哀鸣，渲染家国沦丧的沉痛</label></div>
                <div class="option"><input type="radio" name="q2" value="D" id="q2_d"><label for="q2_d">D. 通过视觉与听觉转换，表现词人隐逸之思</label></div>
            </div>
            <div class="feedback" id="fb2"></div>
        </div>

        <!-- 题目3 单选 -->
        <div class="question-card" data-qid="3">
            <div class="question-title">
                <span class="q-type">单选题</span>
                <span class="q-text">3. 词中“西北望长安，可怜无数山”化用了（    ）的典故？</span>
            </div>
            <div class="options">
                <div class="option"><input type="radio" name="q3" value="A" id="q3_a"><label for="q3_a">A. 屈原《离骚》</label></div>
                <div class="option"><input type="radio" name="q3" value="B" id="q3_b"><label for="q3_b">B. 司马迁《史记》</label></div>
                <div class="option"><input type="radio" name="q3" value="C" id="q3_c"><label for="q3_c">C. 李煜《虞美人》</label></div>
                <div class="option"><input type="radio" name="q3" value="D" id="q3_d"><label for="q3_d">D. 杜甫《小寒食舟中作》</label></div>
            </div>
            <div class="feedback" id="fb3"></div>
        </div>

        <!-- 题目4 多选 -->
        <div class="question-card" data-qid="4">
            <div class="question-title">
                <span class="q-type">多选题</span>
                <span class="q-text">4. 下列对《菩萨蛮·书江西造口壁》的理解，正确的有（    ）</span>
            </div>
            <div class="options">
                <div class="option"><input type="checkbox" name="q4" value="A" id="q4_a"><label for="q4_a">A. “行人泪”暗指北宋南渡逃难民众的苦难</label></div>
                <div class="option"><input type="checkbox" name="q4" value="B" id="q4_b"><label for="q4_b">B. “长安”实指北宋都城汴京</label></div>
                <div class="option"><input type="checkbox" name="q4" value="C" id="q4_c"><label for="q4_c">C. “青山遮不住”象征抗金力量不可阻挡</label></div>
                <div class="option"><input type="checkbox" name="q4" value="D" id="q4_d"><label for="q4_d">D. “东流去”暗含历史潮流不可逆转的感慨</label></div>
                <div class="option"><input type="checkbox" name="q4" value="E" id="q4_e"><label for="q4_e">E. 全词以雄浑豪放为主调，兼有婉约之致</label></div>
            </div>
            <div class="multi-hint">✔️ 多选题，可选多个答案</div>
            <div class="feedback" id="fb4"></div>
        </div>

        <!-- 题目5 多选 -->
        <div class="question-card" data-qid="5">
            <div class="question-title">
                <span class="q-type">多选题</span>
                <span class="q-text">5. 下列对词中艺术手法的分析，正确的有（    ）</span>
            </div>
            <div class="options">
                <div class="option"><input type="checkbox" name="q5" value="A" id="q5_a"><label for="q5_a">A. “郁孤台下清江水”以地名起笔，奠定沉痛基调</label></div>
                <div class="option"><input type="checkbox" name="q5" value="B" id="q5_b"><label for="q5_b">B. “可怜无数山”用拟人手法，强化空间阻隔感</label></div>
                <div class="option"><input type="checkbox" name="q5" value="C" id="q5_c"><label for="q5_c">C. “江晚正愁余”化用《楚辞》句法，增添苍凉意蕴</label></div>
                <div class="option"><input type="checkbox" name="q5" value="D" id="q5_d"><label for="q5_d">D. 全词以“水”为线索贯穿，形成连绵不绝的意境</label></div>
                <div class="option"><input type="checkbox" name="q5" value="E" id="q5_e"><label for="q5_e">E. 末尾鹧鸪啼声以动衬静，突显词人孤独</label></div>
            </div>
            <div class="multi-hint">✔️ 多选题，可选多个答案</div>
            <div class="feedback" id="fb5"></div>
        </div>

        <!-- 题目6 多选 -->
        <div class="question-card" data-qid="6">
            <div class="question-title">
                <span class="q-type">多选题</span>
                <span class="q-text">6. 关于本词的思想情感，下列说法正确的有（    ）</span>
            </div>
            <div class="options">
                <div class="option"><input type="checkbox" name="q6" value="A" id="q6_a"><label for="q6_a">A. 追怀北宋灭亡的国耻</label></div>
                <div class="option"><input type="checkbox" name="q6" value="B" id="q6_b"><label for="q6_b">B. 批判南宋朝廷苟安东南</label></div>
                <div class="option"><input type="checkbox" name="q6" value="C" id="q6_c"><label for="q6_c">C. 抒发对中原故土的思念</label></div>
                <div class="option"><input type="checkbox" name="q6" value="D" id="q6_d"><label for="q6_d">D. 表达对个人仕途坎坷的愤懑</label></div>
                <div class="option"><input type="checkbox" name="q6" value="E" id="q6_e"><label for="q6_e">E. 暗含抗金复国的坚定信念</label></div>
            </div>
            <div class="multi-hint">✔️ 多选题，可选多个答案</div>
            <div class="feedback" id="fb6"></div>
        </div>
    </form>

    <div class="action-buttons">
        <button id="submitBtn">✅ 提交答案</button>
        <button id="resetBtn" class="reset-btn">🔄 重置所有</button>
    </div>
    <div id="scoreDisplay" class="score-area" style="display: none;">✨ 得分：-- / 6 ✨</div>
    <div class="footer-note">
        📖 多选题必须完全正确才得分（选多、选少或选错均不得分）。提交后显示详细解析。
    </div>
</div>

<script>
    // 标准答案库
    const answerMap = {
        1: { type: 'single', correct: 'B' },
        2: { type: 'single', correct: 'C' },
        3: { type: 'single', correct: 'D' },
        4: { type: 'multiple', correct: ['A','B','D'] },
        5: { type: 'multiple', correct: ['A','C','D'] },
        6: { type: 'multiple', correct: ['A','B','C','E'] }
    };

    // 详细解析
    const explanationMap = {
        1: '郁孤台位于今江西赣州，是赣州名胜。词人登台北望，暗含家国之痛。',
        2: '暮色苍茫，鹧鸪哀啼（“行不得也哥哥”），渲染了山河破碎、归乡无望的沉痛。',
        3: '化用杜甫“愁看直北是长安”，以长安借指汴京，表达被群山阻隔、望而不见的悲愤。',
        4: 'A、B、D正确。C项“青山”象征投降派阻挠；E项本词风格沉郁顿挫而非豪放为主。',
        5: 'A、C、D正确。B项“可怜无数山”并非拟人，而是抒情；E项“以动衬静”在此不准确。',
        6: 'A、B、C、E正确。本词贯穿家国情怀，未直接表达个人仕途坎坷（D项为干扰）。'
    };

    // 获取用户某题的答案
    function getUserAnswer(qid) {
        const info = answerMap[qid];
        if (!info) return null;
        if (info.type === 'single') {
            const selected = document.querySelector(`input[name="q${qid}"]:checked`);
            return selected ? selected.value : null;
        } else {
            const checkboxes = document.querySelectorAll(`input[name="q${qid}"]:checked`);
            if (checkboxes.length === 0) return [];
            return Array.from(checkboxes).map(cb => cb.value).sort();
        }
    }

    // 比较单选
    function isSingleCorrect(userVal, correctVal) {
        return userVal === correctVal;
    }

    // 比较多选（必须完全一致）
    function isMultiCorrect(userArr, correctArr) {
        if (!Array.isArray(userArr) || !Array.isArray(correctArr)) return false;
        if (userArr.length !== correctArr.length) return false;
        return userArr.every((val, idx) => val === correctArr[idx]);
    }

    // 显示单题反馈
    function showFeedback(qid, isCorrect, userAnswer, correctAnswer) {
        const fbDiv = document.getElementById(`fb${qid}`);
        if (!fbDiv) return;

        let userDisplay = '';
        if (answerMap[qid].type === 'single') {
            userDisplay = userAnswer || '未作答';
        } else {
            userDisplay = (userAnswer && userAnswer.length) ? userAnswer.join(', ') : '未作答';
        }
        let correctDisplay = Array.isArray(correctAnswer) ? correctAnswer.join(', ') : correctAnswer;

        let extraMsg = '';
        if (!isCorrect && answerMap[qid].type === 'multiple' && userAnswer && userAnswer.length) {
            extraMsg = '<br>⚠️ 答案不完全正确（可能多选、少选或选错），多选题需完全匹配才得分。';
        } else if (!isCorrect && answerMap[qid].type === 'multiple' && (!userAnswer || userAnswer.length === 0)) {
            extraMsg = '<br>⚠️ 未作答，不得分。';
        }

        const explanation = explanationMap[qid] || '';

        fbDiv.innerHTML = `
            <strong>${isCorrect ? '✓ 回答正确' : '✗ 回答错误'}</strong><br>
            📌 你的答案：${userDisplay}<br>
            ✅ 正确答案：${correctDisplay}<br>
            📖 解析：${explanation}${extraMsg}
        `;
        fbDiv.className = `feedback ${isCorrect ? 'correct' : 'wrong'}`;
    }

    // 计算总分并刷新所有反馈
    function evaluateAndDisplay() {
        let totalScore = 0;

        for (let qid = 1; qid <= 6; qid++) {
            const info = answerMap[qid];
            const userAnswer = getUserAnswer(qid);
            let isCorrect = false;

            if (info.type === 'single') {
                if (userAnswer && isSingleCorrect(userAnswer, info.correct)) {
                    isCorrect = true;
                    totalScore++;
                }
                showFeedback(qid, isCorrect, userAnswer, info.correct);
            } else {
                if (userAnswer && userAnswer.length && isMultiCorrect(userAnswer, info.correct)) {
                    isCorrect = true;
                    totalScore++;
                }
                showFeedback(qid, isCorrect, userAnswer, info.correct);
            }
        }

        const scoreDiv = document.getElementById('scoreDisplay');
        scoreDiv.style.display = 'block';
        scoreDiv.innerHTML = `🏆 得分：${totalScore} / 6 🏆<br><span style="font-size:0.85rem;">${totalScore === 6 ? '🎉 完美掌握！家国情怀深得词心 🎉' : '📚 再品稼轩词，体会沉郁中的赤诚'}</span>`;
        scoreDiv.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
    }

    // 重置所有
    function resetAll() {
        // 清空所有单选和多选
        document.querySelectorAll('input[type="radio"], input[type="checkbox"]').forEach(input => input.checked = false);
        // 清空反馈区域
        for (let i = 1; i <= 6; i++) {
            const fb = document.getElementById(`fb${i}`);
            if (fb) {
                fb.innerHTML = '';
                fb.className = 'feedback';
            }
        }
        const scoreDiv = document.getElementById('scoreDisplay');
        scoreDiv.style.display = 'none';
        scoreDiv.innerHTML = '✨ 得分：-- / 6 ✨';
        // 轻提示
        const msg = document.createElement('div');
        msg.textContent = '🖌️ 已清空所有答案，可重新作答';
        msg.style.textAlign = 'center';
        msg.style.fontSize = '0.8rem';
        msg.style.color = '#2c6e9e';
        msg.style.marginTop = '10px';
        document.querySelector('.container').appendChild(msg);
        setTimeout(() => msg.remove(), 1800);
    }

    // 绑定按钮
    document.getElementById('submitBtn').addEventListener('click', (e) => {
        e.preventDefault();
        evaluateAndDisplay();
    });
    document.getElementById('resetBtn').addEventListener('click', (e) => {
        e.preventDefault();
        resetAll();
    });
</script>
</body>
</html>
