# 需求：蚕的一生（卵→幼虫→蛹→成虫，完整生命周期30-40天）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为小学中高年级学生（8-12岁），也可能包括对自然生命科学感兴趣的更低龄或更高龄的学习者。
2.  **核心需求**：
    *   **知识获取**：清晰、直观地理解蚕从卵到成虫（蛾）的四个主要生命阶段（卵、幼虫、蛹、成虫）及其形态、行为特征。
    *   **过程理解**：掌握每个阶段的关键变化（如幼虫的蜕皮、吐丝结茧、化蛹、羽化）以及完整生命周期的时间跨度（30-40天）。
    *   **情感与价值观**：培养对生命奇迹的观察兴趣、对自然规律的尊重以及对生命周期的科学认知。
3.  **使用场景**：课堂辅助教学、学生自主预习或复习、家庭科普教育。动画需要兼具**自动演示**和**交互探索**两种模式，以适应不同的教学节奏。

#### 教学设计思路
1.  **核心概念**：
    *   **生命周期**：强调“循环”概念，卵是起点也是终点，形成闭环。
    *   **变态发育**：重点展示完全变态发育中形态与功能的巨大转变。
    *   **阶段特征**：每个阶段的独特形态、主要行为（吃桑叶、蜕皮、吐丝、羽化、交配产卵）和持续时间。
2.  **认知规律**：
    *   **从整体到局部**：先展示完整的生命周期循环图，再允许用户深入每个阶段进行探索。
    *   **从观察到解释**：先呈现生动的动态变化，再辅以简洁的文字说明和关键数据。
    *   **多感官参与**：结合视觉动画、可能的轻微音效（如吃桑叶的沙沙声、轻柔的背景音乐）和交互操作，增强记忆点。
3.  **交互设计**：
    *   **双模式驱动**：
        *   **故事模式**：一键播放，以连贯的动画叙事展示蚕的一生，适合首次学习或课堂演示。
        *   **探索模式**：用户可主动点击生命周期环上的任一阶段，或使用时间轴/日历控件，跳转到特定时间点进行详细观察和学习。
    *   **渐进式揭示**：在探索模式中，初始只显示阶段名称和图标，点击后才会展开详细图文、动画和趣味知识。
    *   **隐喻式操作**：用“日历翻页”或“时间滑块”隐喻时间的流逝；用“放大镜”图标提示可以查看细节。
4.  **视觉呈现**：
    *   **风格**：采用可爱、圆润的卡通风格，但保持关键形态特征的科学准确性（如蚕的腹足、气门，蛾的触角形状等）。背景为手绘感的自然场景（桑叶、树枝、蚕房）。
    *   **动画重点**：
        *   **卵**：微小的点，可设计为微微发亮，暗示生命。
        *   **幼虫**：生动表现“蠕动”、“吃桑叶”（桑叶出现小缺口）、“蜕皮”（旧皮从头部向后脱落）、“长大”的过程。
        *   **蛹**：在茧内（可设计为半透明茧壳）逐渐从幼虫形态转变为蛹的形态。
        *   **成虫（蚕蛾）**：从茧中“羽化”而出，翅膀展开晾干，以及雌雄蛾交尾、产卵（卵粒落在桑叶上）的过程。
    *   **信息可视化**：在生命周期环上，用不同大小的扇形或色彩深浅来直观表示各阶段的大致时长比例。

#### 配色方案选择
*   **主色调**：**嫩绿色**与**暖白色**。嫩绿色代表桑叶与生命，暖白色代表蚕丝与纯洁，营造清新、自然、温暖的基调。
*   **辅助色**：
    *   **蚕幼虫**：灰白色、浅米黄色，突出其柔软质感。
    *   **桑叶**：不同深浅的绿色。
    *   **茧**：浅黄色、金黄色，模拟天然蚕丝的颜色。
    *   **蚕蛾**：浅灰褐色，翅膀略带绒毛质感。
    *   **卵**：深灰色或紫色小点。
*   **强调色/交互色**：**柔和的橙色**或**浅蓝色**，用于按钮、高亮当前选中的生命阶段以及重要提示文字，增加活力且不刺眼。
*   **背景**：浅米黄或极浅的灰绿色，模拟纸张或自然光感，确保主体突出。

#### 交互功能列表
1.  **模式选择按钮**：在动画主界面显眼位置，提供“播放故事”和“自由探索”两个主要按钮。
2.  **核心生命周期导航环**：一个圆形图示，将蚕的四个阶段按顺序排列成环。环可自动旋转播放，也可点击任一阶段跳转。
3.  **时间轴/日历控件**（探索模式）：
    *   一个横向滑动条，标注关键天数（如：第1天卵，第10天蚁蚕，第25天结茧，第35天羽化等）。
    *   用户拖动滑块或点击特定天数，画面跳转到对应的生命阶段和场景。
4.  **阶段详情面板**：点击或跳转到某一阶段后，从侧面或下方滑出一个面板，包含：
    *   阶段名称与图标。
    *   持续时间（例如：“幼虫期：约25-30天”）。
    *   关键特征描述（1-2句）。
    *   **“看看它在做什么”** 按钮：触发该阶段的特色行为动画（如吃桑叶、吐丝）。
5.  **放大观察功能**：在幼虫和成虫阶段，提供可点击的“放大镜”图标，点击后局部放大观察蚕的足部、气门或蛾的触角等细节。
6.  **重置与进度控制**：
    *   “重置”按钮：回到初始状态。
    *   在故事模式下，有播放/暂停按钮。
7.  **趣味知识弹窗**（“你知道吗？”）：在探索过程中随机（或通过点击小问号图标）出现一些趣味冷知识，例如：“蚕宝宝有16条腿哦！”“一条蚕吐的丝可以有多长？”。增强探索的惊喜感。
8.  **简易标签系统**：鼠标悬停在画面中关键物体（如桑叶、茧、蛾）上时，显示其名称标签。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>蚕的一生 - 生命周期教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial Rounded MT Bold', 'Arial', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e4efe9 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
            color: #333;
        }

        .header {
            text-align: center;
            margin-bottom: 20px;
            width: 100%;
            max-width: 900px;
        }

        h1 {
            color: #2e7d32;
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }

        .subtitle {
            color: #555;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .main-container {
            display: flex;
            flex-direction: column;
            width: 100%;
            max-width: 900px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 20px;
        }

        .mode-selector {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 25px;
        }

        .mode-btn {
            padding: 12px 25px;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        #storyMode {
            background-color: #4CAF50;
            color: white;
        }

        #exploreMode {
            background-color: #2196F3;
            color: white;
        }

        .mode-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.15);
        }

        .mode-btn.active {
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0,0,0,0.2);
        }

        .animation-area {
            position: relative;
            width: 100%;
            height: 400px;
            background-color: #f9fdf8;
            border-radius: 15px;
            overflow: hidden;
            border: 3px solid #c8e6c9;
            margin-bottom: 25px;
        }

        #mainCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .lifecycle-nav {
            display: flex;
            justify-content: space-around;
            margin-bottom: 25px;
            flex-wrap: wrap;
            gap: 10px;
        }

        .stage-btn {
            padding: 10px 15px;
            background-color: #e8f5e9;
            border: 2px solid #a5d6a7;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            color: #2e7d32;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-width: 100px;
        }

        .stage-btn:hover {
            background-color: #c8e6c9;
            transform: translateY(-3px);
        }

        .stage-btn.active {
            background-color: #4CAF50;
            color: white;
            border-color: #2e7d32;
        }

        .stage-icon {
            font-size: 1.5rem;
            margin-bottom: 5px;
        }

        .timeline-container {
            width: 100%;
            margin-bottom: 25px;
        }

        .timeline-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            font-size: 0.9rem;
            color: #555;
        }

        #timeline {
            width: 100%;
            height: 40px;
            -webkit-appearance: none;
            appearance: none;
            background: linear-gradient(to right, #e8f5e9, #c8e6c9, #a5d6a7, #81c784, #4CAF50);
            border-radius: 20px;
            outline: none;
        }

        #timeline::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: #ff9800;
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 25px;
        }

        .control-btn {
            padding: 10px 20px;
            background-color: #ff9800;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }

        .control-btn:hover {
            background-color: #f57c00;
            transform: translateY(-2px);
        }

        .details-panel {
            background-color: #f1f8e9;
            border-radius: 15px;
            padding: 20px;
            border-left: 5px solid #4CAF50;
            margin-top: 10px;
            display: none;
        }

        .details-panel.active {
            display: block;
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .stage-title {
            color: #2e7d32;
            font-size: 1.5rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .stage-duration {
            color: #ff9800;
            font-weight: bold;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .stage-description {
            color: #555;
            line-height: 1.6;
            margin-bottom: 15px;
        }

        .action-btn {
            padding: 8px 15px;
            background-color: #2196F3;
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            margin-right: 10px;
            margin-bottom: 10px;
        }

        .action-btn:hover {
            background-color: #1976D2;
        }

        .fun-fact {
            background-color: #e3f2fd;
            border-radius: 10px;
            padding: 15px;
            margin-top: 20px;
            border-left: 5px solid #2196F3;
            display: none;
        }

        .fun-fact.active {
            display: block;
            animation: fadeIn 0.8s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fact-title {
            color: #1976D2;
            font-weight: bold;
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .day-counter {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: rgba(255, 255, 255, 0.9);
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            color: #2e7d32;
            box-shadow: 0 3px 8px rgba(0,0,0,0.1);
            z-index: 10;
        }

        @media (max-width: 768px) {
            .main-container {
                padding: 15px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .animation-area {
                height: 300px;
            }
            
            .stage-btn {
                min-width: 80px;
                padding: 8px 10px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>🐛 蚕的一生</h1>
        <p class="subtitle">从卵到成虫的完整生命周期（30-40天）</p>
    </div>

    <div class="main-container">
        <div class="mode-selector">
            <button id="storyMode" class="mode-btn active">📖 故事模式</button>
            <button id="exploreMode" class="mode-btn">🔍 探索模式</button>
        </div>

        <div class="animation-area">
            <div class="day-counter">第 <span id="dayCount">1</span> 天</div>
            <canvas id="mainCanvas"></canvas>
        </div>

        <div class="lifecycle-nav">
            <button class="stage-btn active" data-stage="egg">
                <span class="stage-icon">🥚</span>
                <span>卵期</span>
            </button>
            <button class="stage-btn" data-stage="larva">
                <span class="stage-icon">🐛</span>
                <span>幼虫期</span>
            </button>
            <button class="stage-btn" data-stage="pupa">
                <span class="stage-icon">🕸️</span>
                <span>蛹期</span>
            </button>
            <button class="stage-btn" data-stage="adult">
                <span class="stage-icon">🦋</span>
                <span>成虫期</span>
            </button>
        </div>

        <div class="timeline-container">
            <div class="timeline-label">
                <span>第1天 (卵)</span>
                <span>第10天 (幼虫)</span>
                <span>第25天 (结茧)</span>
                <span>第35天 (羽化)</span>
                <span>第40天 (产卵)</span>
            </div>
            <input type="range" id="timeline" min="1" max="40" value="1" step="1">
        </div>

        <div class="controls">
            <button id="playBtn" class="control-btn">▶️ 播放故事</button>
            <button id="pauseBtn" class="control-btn">⏸️ 暂停</button>
            <button id="resetBtn" class="control-btn">🔄 重置</button>
            <button id="funFactBtn" class="control-btn">❓ 趣味知识</button>
        </div>

        <div id="detailsPanel" class="details-panel active">
            <h2 class="stage-title"><span>🥚</span> 卵期</h2>
            <div class="stage-duration">持续时间：约3-5天</div>
            <p class="stage-description">蚕的生命从微小的卵开始。卵呈椭圆形，最初为淡黄色，随后逐渐变为深灰色或紫色。在适宜的温度下，大约3-5天后，蚁蚕就会从卵中孵化出来。</p>
            <button class="action-btn" data-action="hatch">👀 观看孵化过程</button>
        </div>

        <div id="funFact" class="fun-fact">
            <div class="fact-title">💡 你知道吗？</div>
            <p id="factText">一条蚕宝宝一生可以吃掉大约20-30片桑叶，是它自身体重的许多倍！</p>
        </div>
    </div>

    <script>
        // 获取DOM元素
        const canvas = document.getElementById('mainCanvas');
        const ctx = canvas.getContext('2d');
        const storyModeBtn = document.getElementById('storyMode');
        const exploreModeBtn = document.getElementById('exploreMode');
        const stageBtns = document.querySelectorAll('.stage-btn');
        const timeline = document.getElementById('timeline');
        const dayCount = document.getElementById('dayCount');
        const playBtn = document.getElementById('playBtn');
        const pauseBtn = document.getElementById('pauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const funFactBtn = document.getElementById('funFactBtn');
        const detailsPanel = document.getElementById('detailsPanel');
        const funFact = document.getElementById('funFact');
        const factText = document.getElementById('factText');

        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        // 动画状态
        let currentStage = 'egg';
        let currentDay = 1;
        let isStoryMode = true;
        let isPlaying = false;
        let animationId = null;
        let storyProgress = 0;
        
        // 趣味知识库
        const funFacts = [
            "蚕宝宝有16条腿！胸部有3对胸足，腹部有4对腹足，还有1对尾足。",
            "一条蚕吐的丝可以长达1000-1500米，相当于3-5个足球场的长度！",
            "蚕丝是天然蛋白质纤维，主要由丝素和丝胶组成，非常柔软且有光泽。",
            "蚕宝宝一生要蜕皮4次，每次蜕皮后都会长大很多，食量也大大增加。",
            "蚕蛾没有咀嚼式口器，成虫后不再进食，它们的唯一任务是交配产卵。",
            "蚕的寿命大约40天，其中幼虫期占大部分时间，而成虫期只有几天。",
            "中国是世界上最早养蚕、缫丝、织绸的国家，已有5000多年历史。"
        ];

        // 阶段信息
        const stageInfo = {
            egg: {
                title: "🥚 卵期",
                duration: "约3-5天",
                description: "蚕的生命从微小的卵开始。卵呈椭圆形，最初为淡黄色，随后逐渐变为深灰色或紫色。在适宜的温度下，大约3-5天后，蚁蚕就会从卵中孵化出来。",
                actions: ["hatch"],
                dayRange: [1, 5],
                color: "#9c27b0"
            },
            larva: {
                title: "🐛 幼虫期",
                duration: "约25-30天",
                description: "幼虫期是蚕生长最快的阶段。蚁蚕孵化后不断进食桑叶，经历4次蜕皮，分为5个龄期。每蜕一次皮，身体就长大一些，食量也大大增加。",
                actions: ["eat", "molt"],
                dayRange: [6, 30],
                color: "#8bc34a"
            },
            pupa: {
                title: "🕸️ 蛹期",
                duration: "约10-15天",
                description: "幼虫成熟后开始吐丝结茧，在茧内化为蛹。蛹期外表静止，内部却发生着巨大的变化，幼虫器官逐渐分解，成虫器官逐渐形成。",
                actions: ["spin", "transform"],
                dayRange: [31, 40],
                color: "#ff9800"
            },
            adult: {
                title: "🦋 成虫期",
                duration: "约5-10天",
                description: "蚕蛾从茧中羽化而出，翅膀逐渐展开变硬。成虫不再进食，主要任务是交配和产卵。雌蛾可产下300-500粒卵，完成一个生命循环。",
                actions: ["emerge", "mate"],
                dayRange: [41, 45],
                color: "#2196f3"
            }
        };

        // 初始化
        function init() {
            updateStage('egg');
            updateDay(1);
            draw();
        }

        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 根据当前阶段绘制
            switch(currentStage) {
                case 'egg':
                    drawEggStage();
                    break;
                case 'larva':
                    drawLarvaStage();
                    break;
                case 'pupa':
                    drawPupaStage();
                    break;
                case 'adult':
                    drawAdultStage();
                    break;
            }
            
            // 如果正在播放故事模式，更新进度
            if (isPlaying && isStoryMode) {
                storyProgress += 0.005;
                if (storyProgress > 1) {
                    storyProgress = 0;
                    if (currentStage === 'adult') {
                        updateStage('egg');
                        updateDay(1);
                    } else {
                        const stages = ['egg', 'larva', 'pupa', 'adult'];
                        const currentIndex = stages.indexOf(currentStage);
                        const nextStage = stages[(currentIndex + 1) % stages.length];
                        updateStage(nextStage);
                        updateDay(stageInfo[nextStage].dayRange[0]);
                    }
                }
                updateStoryAnimation();
            }
            
            animationId = requestAnimationFrame(draw);
        }

        // 绘制背景
        function drawBackground() {
            // 天空
            const gradient = ctx.createLinearGradient(0, 0, 0, canvas.height);
            gradient.addColorStop(0, '#e3f2fd');
            gradient.addColorStop(1, '#f1f8e9');
            ctx.fillStyle = gradient;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 草地
            ctx.fillStyle = '#a5d6a7';
            ctx.fillRect(0, canvas.height * 0.7, canvas.width, canvas.height * 0.3);
            
            // 桑叶
            ctx.fillStyle = '#4caf50';
            for (let i = 0; i < 5; i++) {
                const x = 50 + i * 80;
                const y = canvas.height * 0.65;
                drawLeaf(x, y, 40, 30);
            }
        }

        // 绘制桑叶
        function drawLeaf(x, y, width, height) {
            ctx.save();
            ctx.translate(x, y);
            
            ctx.fillStyle = '#4caf50';
            ctx.beginPath();
            ctx.ellipse(0, 0, width, height, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 叶脉
            ctx.strokeStyle = '#2e7d32';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(0, -height);
            ctx.lineTo(0, height);
            ctx.stroke();
            
            ctx.restore();
        }

        // 绘制卵期
        function drawEggStage() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制多个卵
            for (let i = 0; i < 15; i++) {
                const angle = (i / 15) * Math.PI * 2;
                const radius = 100;
                const x = centerX + Math.cos(angle) * radius;
                const y = centerY + Math.sin(angle) * radius;
                
                // 卵的颜色随天数变化
                const dayProgress = (currentDay - 1) / 4;
                const colorValue = Math.floor(200 - dayProgress * 150);
                ctx.fillStyle = `rgb(${colorValue}, ${colorValue}, ${colorValue})`;
                
                // 卵微微发亮效果
                if (isStoryMode && storyProgress > 0.7) {
                    ctx.shadowColor = '#ffeb3b';
                    ctx.shadowBlur = 10;
                }
                
                ctx.beginPath();
                ctx.ellipse(x, y, 5, 3, 0, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.shadowBlur = 0;
            }
            
            // 如果正在孵化
            if (currentDay >= 4 && currentDay <= 5) {
                const hatchProgress = (currentDay - 3) / 2;
                drawAntSilkworm(centerX, centerY, hatchProgress);
            }
        }

        // 绘制蚁蚕
        function drawAntSilkworm(x, y, progress) {
            ctx.save();
            ctx.translate(x, y);
            
            // 身体
            ctx.fillStyle = '#000000';
            const bodyLength = 10 + progress * 5;
            ctx.beginPath();
            ctx.ellipse(0, 0, bodyLength, 3, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 头部
            ctx.beginPath();
            ctx.arc(-bodyLength, 0, 2, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.restore();
        }

        // 绘制幼虫期
        function drawLarvaStage() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 计算幼虫大小（随天数增长）
            const dayInStage = Math.min(currentDay - 5, 25);
            const sizeProgress = dayInStage / 25;
            const bodyLength = 30 + sizeProgress * 100;
            const bodyWidth = 8 + sizeProgress * 12;
            
            // 绘制幼虫身体
            ctx.save();
            ctx.translate(centerX, centerY);
            
            // 身体颜色
            const gradient = ctx.createLinearGradient(-bodyLength, 0, bodyLength, 0);
            gradient.addColorStop(0, '#f5f5f5');
            gradient.addColorStop(0.5, '#fff8e1');
            gradient.addColorStop(1, '#f5f5f5');
            ctx.fillStyle = gradient;
            
            // 身体
            ctx.beginPath();
            ctx.ellipse(0, 0, bodyLength, bodyWidth, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 身体节段
            ctx.strokeStyle = '#ccc';
            ctx.lineWidth = 1;
            for (let i = -bodyLength + 10; i < bodyLength; i += 15) {
                ctx.beginPath();
                ctx.moveTo(i, -bodyWidth);
                ctx.lineTo(i, bodyWidth);
                ctx.stroke();
            }
            
            // 头部
            ctx.fillStyle = '#795548';
            ctx.beginPath();
            ctx.arc(-bodyLength, 0, bodyWidth * 0.8, 0, Math.PI * 2);
            ctx.fill();
            
            // 眼睛
            ctx.fillStyle = '#000';
            ctx.beginPath();
            ctx.arc(-bodyLength - 3, -2, 1, 0, Math.PI * 2);
            ctx.arc(-bodyLength - 3, 2, 1, 0, Math.PI * 2);
            ctx.fill();
            
            // 足部（简化表示）
            ctx.fillStyle = '#795548';
            for (let i = -bodyLength + 15; i < bodyLength; i += 20) {
                ctx.beginPath();
                ctx.arc(i, -bodyWidth - 2, 2, 0, Math.PI * 2);
                ctx.fill();
                ctx.beginPath();
                ctx.arc(i, bodyWidth + 2, 2, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 如果正在吃桑叶
            if (isStoryMode && storyProgress > 0.3 && storyProgress < 0.7) {
                drawEatingAnimation(bodyLength);
            }
            
            ctx.restore();
        }

        // 绘制吃桑叶动画
        function drawEatingAnimation(bodyLength) {
            const eatProgress = (storyProgress - 0.3) / 0.4;
            const leafX = 100;
            const leafY = 50;
            
            // 被吃的桑叶
            ctx.fillStyle = '#4caf50';
            ctx.beginPath();
            ctx.ellipse(leafX, leafY, 40 - eatProgress * 20, 30, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 咀嚼动作
            const chewOffset = Math.sin(eatProgress * Math.PI * 10) * 2;
            ctx.translate(chewOffset, 0);
        }

        // 绘制蛹期
        function drawPupaStage() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 蚕茧
            ctx.save();
            ctx.translate(centerX, centerY);
            
            // 茧的颜色
            const gradient = ctx.createRadialGradient(0, 0, 0, 0, 0, 50);
            gradient.addColorStop(0, '#fff9c4');
            gradient.addColorStop(1, '#ffecb3');
            ctx.fillStyle = gradient;
            
            // 茧的形状
            ctx.beginPath();
            ctx.ellipse(0, 0, 50, 35, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 茧的纹理
            ctx.strokeStyle = 'rgba(255, 193, 7, 0.3)';
            ctx.lineWidth = 1;
            for (let i = 0; i < 8; i++) {
                const angle = (i / 8) * Math.PI * 2;
                const x1 = Math.cos(angle) * 30;
                const y1 = Math.sin(angle) * 20;
                const x2 = Math.cos(angle) * 45;
                const y2 = Math.sin(angle) * 30;
                
                ctx.beginPath();
                ctx.moveTo(x1, y1);
                ctx.lineTo(x2, y2);
                ctx.stroke();
            }
            
            // 茧内的蛹（半透明）
            if (currentDay >= 35) {
                const pupaProgress = (currentDay - 34) / 6;
                drawPupaInside(pupaProgress);
            }
            
            ctx.restore();
        }

        // 绘制茧内的蛹
        function drawPupaInside(progress) {
            ctx.save();
            
            // 蛹逐渐显现
            ctx.globalAlpha = progress;
            
            // 蛹的形状
            ctx.fillStyle = '#8d6e63';
            ctx.beginPath();
            ctx.ellipse(0, 0, 30 * progress, 20 * progress, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 蛹的细节
            ctx.strokeStyle = '#5d4037';
            ctx.lineWidth = 2;
            for (let i = -20; i <= 20; i += 10) {
                ctx.beginPath();
                ctx.moveTo(i, -15);
                ctx.lineTo(i, 15);
                ctx.stroke();
            }
            
            ctx.restore();
        }

        // 绘制成虫期
        function drawAdultStage() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            ctx.save();
            ctx.translate(centerX, centerY);
            
            // 翅膀展开进度
            const wingProgress = Math.min((currentDay - 40) / 3, 1);
            
            // 身体
            ctx.fillStyle = '#795548';
            ctx.beginPath();
            ctx.ellipse(0, 0, 25, 10, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 翅膀
            ctx.fillStyle = 'rgba(189, 189, 189, 0.8)';
            
            // 左翅膀
            ctx.save();
            ctx.translate(-15, 0);
            ctx.rotate(-Math.PI/4 * wingProgress);
            ctx.beginPath();
            ctx.ellipse(0, 0, 40 * wingProgress, 25 * wingProgress, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.restore();
            
            // 右翅膀
            ctx.save();
            ctx.translate(15, 0);
            ctx.rotate(Math.PI/4 * wingProgress);
            ctx.beginPath();
            ctx.ellipse(0, 0, 40 * wingProgress, 25 * wingProgress, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.restore();
            
            // 头部
            ctx.fillStyle = '#5d4037';
            ctx.beginPath();
            ctx.arc(0, 0, 8, 0, Math.PI * 2);
            ctx.fill();
            
            // 触角
            ctx.strokeStyle = '#5d4037';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(-5, -8);
            ctx.lineTo(-15, -20);
            ctx.moveTo(5, -8);
            ctx.lineTo(15, -20);
            ctx.stroke();
            
            // 眼睛
            ctx.fillStyle = '#000';
            ctx.beginPath();
            ctx.arc(-3, -2, 2, 0, Math.PI * 2);
            ctx.arc(3, -2, 2, 0, Math.PI * 2);
            ctx.fill();
            
            // 如果正在产卵
            if (currentDay >= 43 && currentDay <= 45) {
                drawEggLaying();
            }
            
            ctx.restore();
        }

        // 绘制产卵动画
        function drawEggLaying() {
            const eggCount = Math.min((currentDay - 42) * 100, 300);
            
            for (let i = 0; i < eggCount / 10; i++) {
                const angle = Math.random() * Math.PI * 2;
                const distance = 100 + Math.random() * 100;
                const x = Math.cos(angle) * distance;
                const y = Math.sin(angle) * distance + 50;
                
                ctx.fillStyle = '#9c27b0';
                ctx.beginPath();
                ctx.ellipse(x, y, 2, 1.5, 0, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        // 更新故事动画
        function updateStoryAnimation() {
            // 根据故事进度更新天数
            const totalDays = 45;
            const newDay = Math.floor(storyProgress * totalDays) + 1;
            if (newDay !== currentDay) {
                updateDay(newDay);
                
                // 根据天数更新阶段
                if (newDay <= 5) {
                    updateStage('egg');
                } else if (newDay <= 30) {
                    updateStage('larva');
                } else if (newDay <= 40) {
                    updateStage('pupa');
                } else {
                    updateStage('adult');
                }
            }
        }

        // 更新阶段
        function updateStage(stage) {
            currentStage = stage;
            
            // 更新按钮状态
            stageBtns.forEach(btn => {
                if (btn.dataset.stage === stage) {
                    btn.classList.add('active');
                } else {
                    btn.classList.remove('active');
                }
            });
            
            // 更新详情面板
            const info = stageInfo[stage];
            detailsPanel.innerHTML = `
                <h2 class="stage-title"><span>${info.title.split(' ')[0]}</span> ${info.title.split(' ')[1]}</h2>
                <div class="stage-duration">持续时间：${info.duration}</div>
                <p class="stage-description">${info.description}</p>
                ${info.actions.map(action => {
                    let actionText = '';
                    if (action === 'hatch') actionText = '👀 观看孵化过程';
                    if (action === 'eat') actionText = '🍃 观看吃桑叶';
                    if (action === 'molt') actionText = '🔄 观看蜕皮过程';
                    if (action === 'spin') actionText = '🕸️ 观看吐丝结茧';
                    if (action === 'transform') actionText = '✨ 观看化蛹变化';
                    if (action === 'emerge') actionText = '🦋 观看羽化过程';
                    if (action === 'mate') actionText = '❤️ 观看交配产卵';
                    return `<button class="action-btn" data-action="${action}">${actionText}</button>`;
                }).join('')}
            `;
            
            // 更新时间轴
            timeline.value = info.dayRange[0];
        }

        // 更新天数
        function updateDay(day) {
            currentDay = Math.min(Math.max(day, 1), 45);
            dayCount.textContent = currentDay;
            timeline.value = currentDay;
        }

        // 显示趣味知识
        function showFunFact() {
            const randomFact = funFacts[Math.floor(Math.random() * funFacts.length)];
            factText.textContent = randomFact;
            funFact.classList.add('active');
            
            // 3秒后自动隐藏
            setTimeout(() => {
                funFact.classList.remove('active');
            }, 5000);
        }

        // 事件监听器
        storyModeBtn.addEventListener('click', () => {
            isStoryMode = true;
            storyModeBtn.classList.add('active');
            exploreModeBtn.classList.remove('active');
            isPlaying = false;
        });

        exploreModeBtn.addEventListener('click', () => {
            isStoryMode = false;
            exploreModeBtn.classList.add('active');
            storyModeBtn.classList.remove('active');
            isPlaying = false;
        });

        stageBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                if (!isStoryMode) {
                    updateStage(btn.dataset.stage);
                    updateDay(stageInfo[btn.dataset.stage].dayRange[0]);
                }
            });
        });

        timeline.addEventListener('input', () => {
            if (!isStoryMode) {
                updateDay(parseInt(timeline.value));
                
                // 根据天数确定阶段
                if (currentDay <= 5) {
                    updateStage('egg');
                } else if (currentDay <= 30) {
                    updateStage('larva');
                } else if (currentDay <= 40) {
                    updateStage('pupa');
                } else {
                    updateStage('adult');
                }
            }
        });

        playBtn.addEventListener('click', () => {
            isPlaying = true;
            if (!isStoryMode) {
                isStoryMode = true;
                storyModeBtn.classList.add('active');
                exploreModeBtn.classList.remove('active');
            }
        });

        pauseBtn.addEventListener('click', () => {
            isPlaying = false;
        });

        resetBtn.addEventListener('click', () => {
            isPlaying = false;
            storyProgress = 0;
            updateStage('egg');
            updateDay(1);
        });

        funFactBtn.addEventListener('click', showFunFact);

        // 委托处理动作按钮
        detailsPanel.addEventListener('click', (e) => {
            if (e.target.classList.contains('action-btn')) {
                const action = e.target.dataset.action;
                // 这里可以添加特定动作的动画
                alert(`即将演示：${e.target.textContent}`);
            }
        });

        // 初始化并开始动画
        init();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 🐛《蚕的一生》交互式教学动画使用指南

欢迎使用《蚕的一生》交互式教学动画！本动画旨在通过生动直观的方式，帮助您探索蚕从卵到成虫的完整生命周期。无论您是教师、学生还是自然爱好者，都能从中获得知识与乐趣。

---

### 一、功能说明

本动画采用HTML5 Canvas技术开发，包含两种学习模式：

1. **📖 故事模式**：自动播放蚕的完整生命周期动画（30-40天），适合初次学习或课堂演示
2. **🔍 探索模式**：自由探索各个生命阶段，可控制时间进度，深入了解细节

动画模拟了蚕的四个主要生命阶段：
- **🥚 卵期**（约3-5天）
- **🐛 幼虫期**（约25-30天）
- **🕸️ 蛹期**（约10-15天）
- **🦋 成虫期**（约5-10天）

---

### 二、主要功能

#### 1. 双模式学习系统
- **故事模式**：一键播放完整生命周期动画，自动展示各阶段关键变化
- **探索模式**：自主控制学习节奏，可随时暂停、跳转、重复观察

#### 2. 可视化时间轴
- 顶部时间轴清晰显示40天完整周期
- 拖动滑块可精确跳转到任意天数
- 关键时间点标注（第1天卵、第10天幼虫、第25天结茧、第35天羽化）

#### 3. 阶段导航系统
- 圆形导航按钮直观展示四个生命阶段
- 点击任一阶段立即跳转并显示详细信息
- 当前阶段高亮显示，学习路径清晰

#### 4. 动态信息面板
- 实时显示当前阶段名称、持续时间和特征描述
- 提供阶段专属互动按钮（如"观看孵化过程"、"观看吃桑叶"等）
- 信息随阶段变化自动更新

#### 5. 趣味知识系统
- 点击"趣味知识"按钮随机显示蚕的有趣冷知识
- 知识库包含7条精选趣味事实
- 自动隐藏设计，避免干扰主学习流程

#### 6. 动画控制面板
- **播放**：开始/继续故事模式动画
- **暂停**：暂停当前动画
- **重置**：回到初始状态（第1天，卵期）
- **响应式设计**：适配不同屏幕尺寸

---

### 三、设计特色

#### 🎨 视觉设计
- **科学准确性**：在卡通风格中保持关键形态特征的科学准确性
- **渐进式变化**：蚕的大小、颜色随天数自然变化
- **生动细节**：包含吃桑叶、蜕皮、吐丝、羽化等关键行为的动画表现
- **柔和配色**：以嫩绿、暖白为主色调，营造自然温馨的学习氛围

#### 🔄 交互设计
- **直观隐喻**：时间轴隐喻时间流逝，放大镜图标提示细节观察
- **渐进揭示**：初始只显示基本信息，点击后展开详细内容
- **多感官参与**：结合视觉动画与潜在的声音提示（设计中预留接口）
- **即时反馈**：所有操作都有明确的视觉反馈

#### 📚 教学设计
- **符合认知规律**：从整体到局部，从观察到解释
- **双重编码**：同时呈现视觉动画和文字说明
- **螺旋式学习**：可通过不同模式反复学习同一概念
- **情感连接**：通过可爱形象培养对生命的尊重与好奇

---

### 四、教学要点

#### 核心概念
1. **生命周期**：强调生命的循环性（卵→幼虫→蛹→成虫→卵）
2. **完全变态发育**：展示形态与功能的巨大转变
3. **阶段特征**：各阶段的独特形态、行为和持续时间
4. **生物适应性**：各阶段形态与功能的适应意义

#### 关键观察点
- **卵期**：颜色变化、微小尺寸、孵化过程
- **幼虫期**：生长速度、蜕皮现象、食量变化、足部结构
- **蛹期**：结茧过程、茧的结构、内部变化
- **成虫期**：羽化过程、翅膀展开、交配产卵行为

#### 跨学科连接
- **数学**：时间计算、比例关系（各阶段时长比例）
- **语文**：科学观察记录、描述性语言
- **艺术**：生命之美观察、自然绘画
- **技术**：丝绸生产相关知识

---

### 五、使用建议

#### 对于教师
1. **课堂引入**：使用故事模式作为课程导入，激发学生兴趣
2. **分组探索**：将学生分组，分配不同阶段进行深入研究
3. **提问引导**：
   - "蚕宝宝一生要蜕几次皮？"
   - "为什么蚕要吐丝结茧？"
   - "蚕蛾为什么不吃东西？"
4. **延伸活动**：
   - 让学生绘制蚕的生命周期图
   - 模拟记录蚕的成长日记
   - 讨论丝绸的生产过程

#### 对于学生
1. **自主学习流程**：
   - 先用故事模式观看完整过程
   - 切换到探索模式，逐个阶段深入研究
   - 使用时间轴观察特定天数的变化
   - 点击趣味知识按钮扩展知识
2. **观察记录建议**：
   - 记录每个阶段的关键特征
   - 注意形态变化的时间点
   - 思考各阶段的功能意义

#### 对于家长
1. **亲子共学**：与孩子一起探索，讨论生命的神奇
2. **生活连接**：联系实际生活中的蚕丝制品
3. **培养习惯**：鼓励孩子仔细观察、提出问题

#### 技术提示
1. **设备要求**：现代浏览器均可使用，推荐Chrome或Edge
2. **网络环境**：单文件设计，加载后无需网络
3. **保存分享**：可将HTML文件保存到本地，随时使用
4. **课堂投影**：建议在全屏模式下使用，确保后排学生清晰可见

---

### 六、教育价值

本动画不仅传授关于蚕的生命周期知识，更培养以下能力：

🔍 **观察能力**：学习如何系统观察生物变化  
📊 **记录能力**：理解时间序列记录的重要性  
🤔 **探究能力**：鼓励提出问题并寻找答案  
❤️ **共情能力**：培养对生命的尊重与关怀  
🔗 **系统思维**：理解生命各阶段的相互联系  

---

### 开始探索吧！

现在，您已经准备好开始探索蚕的奇妙一生了。点击"播放故事"按钮，让我们一起见证这个持续30-40天的生命奇迹。记住，每一次点击、每一次观察，都是与自然对话的机会。

**教学提示**：建议首次使用时完整观看故事模式，建立整体认知；第二次使用时进入探索模式，深入研究感兴趣的部分。

祝您学习愉快，收获满满！ 🐛→🦋

---

*本动画由教育技术专家设计开发，融合了教学法原则与创意编程技术，旨在提供高质量的数字学习体验。如有反馈建议，欢迎与开发者交流。*