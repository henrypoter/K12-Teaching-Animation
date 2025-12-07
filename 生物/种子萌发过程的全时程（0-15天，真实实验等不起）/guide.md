# 需求：种子萌发过程的全时程（0-15天，真实实验等不起）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **核心需求**：用户需要一个能够清晰、直观、生动地展示种子从休眠到萌发，再到幼苗早期生长（0-15天）全过程的教学工具。真实实验周期长、观察不连续，此动画旨在解决这一教学痛点。
2.  **用户画像**：主要为中小学科学课/生物课教师和学生，也可能包括对植物生长感兴趣的普通学习者。他们需要：
    *   **替代实验**：在无法进行长期实物观察时，获得完整的动态过程。
    *   **突破时空限制**：随时暂停、回放、观察关键细节（如胚根突破种皮）。
    *   **理解抽象过程**：将课本中静态的图文描述转化为动态的、可交互的连续过程。
    *   **激发兴趣**：通过美观、拟真的动画吸引学习者的注意力。
3.  **深层需求**：学习者不仅想“看到”过程，更希望理解萌发所需的**条件**（水、空气、适宜温度）以及内部**生理变化**（吸水膨胀、酶活化、物质转运）与外部形态变化的关联。

#### 教学设计思路
*   **核心概念**：
    *   **外部过程**：吸水膨胀 → 种皮破裂 → 胚根伸长（向下生长）→ 胚轴伸长 → 子叶出土（或留土）→ 真叶展开。
    *   **内部条件**：水分、氧气、适宜温度。
    *   **内部生理**：种子吸水、呼吸作用增强、贮藏物质分解转运。
*   **认知规律**：
    1.  **整体到局部**：先呈现种子在土壤中完整的时间线变化，再允许用户聚焦于单颗种子，甚至剖视其内部。
    2.  **具体到抽象**：从直观的形态动画入手，然后通过交互提示或图层切换，揭示其背后的生理和条件需求。
    3.  **控制学习节奏**：用户可通过时间轴自由控制进程，满足不同学习速度的需求。
*   **交互设计**：
    *   **主驱动**：一个清晰的时间轴（0-15天），可拖拽、可点击关键时间点。
    *   **视图切换**：提供“宏观土壤剖面视图”和“单颗种子特写视图”（可带剖视效果）的切换。
    *   **条件控制实验**：设置“水”、“空气”、“温度”三个开关，用户可关闭某一条件（如“无水”），观察动画如何变化（种子不萌发），以此强调萌发条件。
    *   **信息提示**：鼠标悬停在种子各部分（种皮、胚根、胚轴、子叶）或时间节点时，显示名称和关键变化描述。
*   **视觉呈现**：
    *   **风格**：采用**柔和、写实与示意图相结合**的风格。土壤、种子外形力求写实生动，内部物质转运、细胞活动等则用简洁的示意图和箭头表示。
    *   **动态效果**：种子吸水时的轻微膨胀感、根尖生长点的细胞分裂动画（示意性）、物质（如淀粉粒分解为糖分）的流动箭头。
    *   **层次清晰**：背景、土壤、种子、提示信息要有明确的视觉层次，避免杂乱。

#### 配色方案选择
*   **主色调**：
    *   **土壤**：使用不同明度的棕褐色系（如 #8B4513, #D2B48C），营造真实、温暖的土壤环境。
    *   **种子与幼苗**：
        *   干种子：浅褐色（#A0522D）。
        *   吸水后种子/胚根/胚轴：充满生机的浅黄色至嫩绿色渐变（#F5DEB3 -> #90EE90）。
        *   子叶与真叶：鲜绿色（#32CD32）。
*   **辅助色/功能色**：
    *   **水**：半透明的浅蓝色（#87CEEB， 透明度约0.6）。
    *   **空气（氧气）**：用微小的、上升的浅灰色半透明气泡（#D3D3D3）示意。
    *   **高亮与提示**：使用温和的橙色（#FFA500）或亮蓝色（#1E90FF）用于交互按钮、悬停高亮和重要箭头标注。
    *   **界面背景**：浅米色或浅灰色（#F5F5F5 或 #FAFAFA），确保内容突出且不刺眼。
*   **原则**：整体色调自然、柔和，符合生命主题，同时通过功能色确保交互元素清晰可辨。

#### 交互功能列表
1.  **核心时间轴控制**：
    *   拖拽滑块或点击刻度，快速跳转到特定天数。
    *   播放/暂停/重置按钮。
    *   关键阶段自动标记（如“吸水膨胀”、“胚根突破”、“子叶展开”）。
2.  **视图切换按钮**：
    *   “土壤剖面视图”：显示多颗种子在土壤中的萌发情况，体现差异性。
    *   “种子特写视图”：聚焦单颗种子，可切换“外观模式”和“剖视模式”，观察内部变化。
3.  **萌发条件实验面板**：
    *   三个带图标的开关：“水滴”（水）、“风扇”（空气/氧气）、“温度计”（适宜温度）。
    *   默认全部开启。关闭任一开关，动画将展示在该条件下种子状态停滞（如不吸水、不破裂）。
    *   旁边配有简短的文字解释。
4.  **悬停提示系统**：
    *   悬停种子各部分：显示结构名称和当前阶段的功能（如“胚根：向下生长，吸收水分和无机盐”）。
    *   悬停时间点：显示该天的典型形态特征描述。
    *   悬停条件开关：显示该条件的详细作用。
5.  **图层显示控制**（可选高级功能）：
    *   复选框：“显示水分吸收”、“显示物质转运”、“显示呼吸作用”。勾选后，动画上会叠加相应的示意性动画（蓝色水渍蔓延、箭头流动、气泡产生）。
6.  **数据与测量**（可选增强功能）：
    *   在特写视图下，随时间显示胚根/胚轴的长度变化简图或数值，将生长过程量化。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>种子萌发全时程交互教学动画 (0-15天)</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid #8B4513;
        }

        h1 {
            color: #2e7d32;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #666;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }

        .animation-section {
            flex: 3;
            min-width: 300px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
        }

        .control-section {
            flex: 2;
            min-width: 280px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .section-title {
            color: #8B4513;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 1px solid #eee;
            font-size: 1.3em;
        }

        /* 画布容器 */
        #animationCanvas {
            background-color: #fafafa;
            border-radius: 8px;
            border: 1px solid #ddd;
            width: 100%;
            height: 400px;
            cursor: pointer;
            margin-bottom: 15px;
        }

        /* 视图切换按钮 */
        .view-toggle {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }

        .view-btn {
            flex: 1;
            padding: 10px;
            background-color: #e8f5e9;
            border: 2px solid #a5d6a7;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            color: #2e7d32;
            transition: all 0.3s;
        }

        .view-btn:hover {
            background-color: #c8e6c9;
        }

        .view-btn.active {
            background-color: #4caf50;
            color: white;
            border-color: #388e3c;
        }

        /* 时间轴 */
        .timeline-container {
            margin-top: 10px;
        }

        .timeline-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        #currentDay {
            font-weight: bold;
            color: #8B4513;
        }

        #timelineSlider {
            width: 100%;
            height: 30px;
            -webkit-appearance: none;
            appearance: none;
            background: linear-gradient(to right, #D2B48C, #8B4513);
            border-radius: 15px;
            outline: none;
        }

        #timelineSlider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            background: #1E90FF;
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.3);
        }

        .timeline-marks {
            display: flex;
            justify-content: space-between;
            margin-top: 5px;
            font-size: 0.85em;
            color: #666;
        }

        .timeline-mark {
            text-align: center;
            width: 40px;
        }

        .timeline-mark.highlight {
            color: #FF8C00;
            font-weight: bold;
        }

        /* 播放控制 */
        .playback-controls {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .playback-btn {
            flex: 1;
            padding: 10px;
            background-color: #e3f2fd;
            border: 2px solid #90caf9;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            color: #1565c0;
            transition: all 0.3s;
        }

        .playback-btn:hover {
            background-color: #bbdefb;
        }

        #playPauseBtn {
            flex: 2;
        }

        /* 条件控制 */
        .condition-controls {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .condition-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 12px;
            background-color: #f9f9f9;
            border-radius: 8px;
            border-left: 5px solid;
            transition: all 0.3s;
        }

        .condition-item.water {
            border-left-color: #87CEEB;
        }

        .condition-item.air {
            border-left-color: #D3D3D3;
        }

        .condition-item.temp {
            border-left-color: #FFA500;
        }

        .condition-icon {
            font-size: 1.8em;
            width: 40px;
            text-align: center;
        }

        .condition-info {
            flex: 1;
        }

        .condition-name {
            font-weight: 600;
            margin-bottom: 3px;
        }

        .condition-desc {
            font-size: 0.9em;
            color: #666;
        }

        /* 开关样式 */
        .switch {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 30px;
        }

        .switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: .4s;
            border-radius: 34px;
        }

        .slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }

        input:checked + .slider {
            background-color: #4caf50;
        }

        input:checked + .slider:before {
            transform: translateX(30px);
        }

        /* 信息面板 */
        .info-panel {
            background-color: #f0f7ff;
            border-radius: 8px;
            padding: 15px;
            border: 1px solid #bbdefb;
            min-height: 120px;
        }

        .info-title {
            color: #1E90FF;
            margin-bottom: 10px;
            font-weight: 600;
        }

        #infoText {
            font-size: 0.95em;
            line-height: 1.5;
        }

        .hint {
            font-size: 0.9em;
            color: #888;
            margin-top: 15px;
            text-align: center;
            font-style: italic;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 15px;
            border-top: 1px solid #ddd;
            color: #777;
            font-size: 0.9em;
        }

        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>种子萌发过程全时程交互教学动画</h1>
        <p class="subtitle">模拟0-15天的完整萌发过程，探索种子萌发的条件与内部变化</p>
    </header>

    <div class="container">
        <div class="main-content">
            <section class="animation-section">
                <h2 class="section-title">种子萌发过程</h2>
                
                <div class="view-toggle">
                    <button id="soilViewBtn" class="view-btn active">土壤剖面视图</button>
                    <button id="seedViewBtn" class="view-btn">种子特写视图</button>
                </div>
                
                <canvas id="animationCanvas" width="800" height="400"></canvas>
                
                <div class="timeline-container">
                    <div class="timeline-header">
                        <span>萌发时间线</span>
                        <span id="currentDay">第 0 天</span>
                    </div>
                    <input type="range" id="timelineSlider" min="0" max="15" value="0" step="0.1">
                    
                    <div class="timeline-marks">
                        <div class="timeline-mark">0天</div>
                        <div class="timeline-mark highlight">1天</div>
                        <div class="timeline-mark">3天</div>
                        <div class="timeline-mark highlight">5天</div>
                        <div class="timeline-mark">10天</div>
                        <div class="timeline-mark highlight">15天</div>
                    </div>
                </div>
                
                <div class="playback-controls">
                    <button id="playPauseBtn" class="playback-btn">▶ 播放</button>
                    <button id="resetBtn" class="playback-btn">↺ 重置</button>
                    <button id="speedBtn" class="playback-btn">速度: 1x</button>
                </div>
                
                <p class="hint">提示：将鼠标悬停在种子各部分上查看详细信息；拖动时间轴或使用播放控制观察不同阶段的变化。</p>
            </section>
            
            <section class="control-section">
                <h2 class="section-title">萌发条件控制</h2>
                
                <div class="condition-controls">
                    <div class="condition-item water">
                        <div class="condition-icon">💧</div>
                        <div class="condition-info">
                            <div class="condition-name">水分</div>
                            <div class="condition-desc">种子吸水膨胀，软化种皮，启动酶活性</div>
                        </div>
                        <label class="switch">
                            <input type="checkbox" id="waterToggle" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                    
                    <div class="condition-item air">
                        <div class="condition-icon">💨</div>
                        <div class="condition-info">
                            <div class="condition-name">空气（氧气）</div>
                            <div class="condition-desc">提供呼吸作用所需的氧气，释放能量</div>
                        </div>
                        <label class="switch">
                            <input type="checkbox" id="airToggle" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                    
                    <div class="condition-item temp">
                        <div class="condition-icon">🌡️</div>
                        <div class="condition-info">
                            <div class="condition-name">适宜温度</div>
                            <div class="condition-desc">维持酶的最佳活性，促进代谢过程</div>
                        </div>
                        <label class="switch">
                            <input type="checkbox" id="tempToggle" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                </div>
                
                <h2 class="section-title">信息提示</h2>
                <div class="info-panel">
                    <div class="info-title" id="infoTitle">欢迎探索种子萌发过程！</div>
                    <div id="infoText">请将鼠标悬停在动画中的种子、根、芽等部位，或调整时间轴和萌发条件，查看相应的解释信息。</div>
                </div>
                
                <div class="hint">实验：尝试关闭某个萌发条件（如水），观察种子萌发过程如何受到影响。</div>
            </section>
        </div>
    </div>
    
    <footer>
        <p>种子萌发教学动画 | 设计：熊猫老师 | 本动画模拟菜豆种子的萌发过程（子叶出土型）</p>
    </footer>

    <script>
        // 获取DOM元素
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        const timelineSlider = document.getElementById('timelineSlider');
        const currentDayEl = document.getElementById('currentDay');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const resetBtn = document.getElementById('resetBtn');
        const speedBtn = document.getElementById('speedBtn');
        const soilViewBtn = document.getElementById('soilViewBtn');
        const seedViewBtn = document.getElementById('seedViewBtn');
        const waterToggle = document.getElementById('waterToggle');
        const airToggle = document.getElementById('airToggle');
        const tempToggle = document.getElementById('tempToggle');
        const infoTitle = document.getElementById('infoTitle');
        const infoText = document.getElementById('infoText');

        // 动画状态变量
        let currentDay = 0;
        let isPlaying = false;
        let animationSpeed = 1; // 1x, 2x, 0.5x
        let currentView = 'soil'; // 'soil' 或 'seed'
        let hoveredPart = null;
        let lastTimestamp = 0;
        
        // 萌发条件
        const conditions = {
            water: true,
            air: true,
            temp: true
        };
        
        // 种子数据
        const seeds = [
            { x: 150, y: 250, size: 1, stage: 0, rootLength: 0, shootLength: 0 },
            { x: 400, y: 230, size: 1, stage: 0, rootLength: 0, shootLength: 0 },
            { x: 650, y: 260, size: 1, stage: 0, rootLength: 0, shootLength: 0 }
        ];
        
        // 颜色定义
        const colors = {
            soilDark: '#8B4513',
            soilLight: '#D2B48C',
            seedDry: '#A0522D',
            seedHydrated: '#F5DEB3',
            root: '#90EE90',
            shoot: '#32CD32',
            leaf: '#228B22',
            water: 'rgba(135, 206, 235, 0.6)',
            airBubble: 'rgba(211, 211, 211, 0.7)',
            highlight: '#FF8C00',
            infoHighlight: '#1E90FF'
        };
        
        // 信息提示数据
        const partInfo = {
            seed: {
                title: "种子",
                text: "种子是植物的繁殖器官，包含胚和营养物质。萌发需要水分、氧气和适宜温度。"
            },
            seedCoat: {
                title: "种皮",
                text: "保护种子内部结构。吸水后软化、破裂，允许胚根伸出。"
            },
            embryo: {
                title: "胚",
                text: "未来植物的雏形，包括胚根、胚轴和胚芽（子叶）。"
            },
            radicle: {
                title: "胚根",
                text: "首先突破种皮，向下生长形成主根，吸收水分和无机盐。"
            },
            hypocotyl: {
                title: "胚轴",
                text: "连接胚根和子叶的部分，伸长将子叶推出土壤（子叶出土型）。"
            },
            cotyledon: {
                title: "子叶",
                text: "储存或转运营养物质，为幼苗早期生长提供能量。"
            },
            trueLeaf: {
                title: "真叶",
                text: "在子叶之后展开，能进行光合作用，为植物制造有机物。"
            },
            rootHair: {
                title: "根毛",
                text: "增加根的表面积，大大提高水分和养分的吸收效率。"
            }
        };
        
        // 时间线关键事件
        const timelineEvents = [
            { day: 0, title: "干燥种子", text: "种子处于休眠状态，代谢活动极低。" },
            { day: 1, title: "吸水膨胀", text: "种子吸收水分，体积增大，种皮软化。" },
            { day: 2, title: "启动代谢", text: "酶活性恢复，呼吸作用增强，贮藏物质开始分解。" },
            { day: 3, title: "胚根突破", text: "胚根首先突破种皮，开始向下生长。" },
            { day: 5, title: "胚轴伸长", text: "胚轴开始伸长，将子叶向上推动。" },
            { day: 7, title: "子叶出土", text: "子叶露出土面，展开变绿，开始光合作用。" },
            { day: 10, title: "真叶展开", text: "第一对真叶展开，幼苗进入自养生长阶段。" },
            { day: 15, title: "幼苗建立", text: "根系扩展，真叶长大，幼苗独立进行光合作用。" }
        ];
        
        // 初始化
        function init() {
            updateCanvasSize();
            draw();
            
            // 事件监听
            timelineSlider.addEventListener('input', handleTimelineChange);
            playPauseBtn.addEventListener('click', togglePlayPause);
            resetBtn.addEventListener('click', resetAnimation);
            speedBtn.addEventListener('click', toggleSpeed);
            soilViewBtn.addEventListener('click', () => switchView('soil'));
            seedViewBtn.addEventListener('click', () => switchView('seed'));
            
            waterToggle.addEventListener('change', () => {
                conditions.water = waterToggle.checked;
                updateInfoFromConditions();
            });
            
            airToggle.addEventListener('change', () => {
                conditions.air = airToggle.checked;
                updateInfoFromConditions();
            });
            
            tempToggle.addEventListener('change', () => {
                conditions.temp = tempToggle.checked;
                updateInfoFromConditions();
            });
            
            canvas.addEventListener('mousemove', handleCanvasHover);
            canvas.addEventListener('mouseleave', () => {
                hoveredPart = null;
                draw();
            });
            
            // 窗口大小调整
            window.addEventListener('resize', updateCanvasSize);
            
            // 启动动画循环
            requestAnimationFrame(animate);
        }
        
        // 更新画布尺寸
        function updateCanvasSize() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = 400;
            draw();
        }
        
        // 处理时间轴变化
        function handleTimelineChange() {
            currentDay = parseFloat(timelineSlider.value);
            currentDayEl.textContent = `第 ${currentDay.toFixed(1)} 天`;
            updateInfoFromTimeline();
            draw();
        }
        
        // 切换播放/暂停
        function togglePlayPause() {
            isPlaying = !isPlaying;
            playPauseBtn.textContent = isPlaying ? '⏸ 暂停' : '▶ 播放';
            lastTimestamp = performance.now();
        }
        
        // 重置动画
        function resetAnimation() {
            currentDay = 0;
            timelineSlider.value = 0;
            currentDayEl.textContent = '第 0 天';
            isPlaying = false;
            playPauseBtn.textContent = '▶ 播放';
            updateInfoFromTimeline();
            draw();
        }
        
        // 切换播放速度
        function toggleSpeed() {
            if (animationSpeed === 1) {
                animationSpeed = 2;
                speedBtn.textContent = '速度: 2x';
            } else if (animationSpeed === 2) {
                animationSpeed = 0.5;
                speedBtn.textContent = '速度: 0.5x';
            } else {
                animationSpeed = 1;
                speedBtn.textContent = '速度: 1x';
            }
        }
        
        // 切换视图
        function switchView(view) {
            currentView = view;
            soilViewBtn.classList.toggle('active', view === 'soil');
            seedViewBtn.classList.toggle('active', view === 'seed');
            
            if (view === 'soil') {
                infoTitle.textContent = "土壤剖面视图";
                infoText.textContent = "观察多颗种子在土壤中的萌发情况。每颗种子的萌发速度可能略有差异，这是自然现象。";
            } else {
                infoTitle.textContent = "种子特写视图";
                infoText.textContent = "聚焦观察单颗种子的详细萌发过程。将鼠标悬停在种子各部分查看详细信息。";
            }
            
            draw();
        }
        
        // 处理画布悬停
        function handleCanvasHover(event) {
            const rect = canvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            const y = event.clientY - rect.top;
            
            hoveredPart = null;
            
            if (currentView === 'soil') {
                // 检查是否悬停在种子上
                for (let i = 0; i < seeds.length; i++) {
                    const seed = seeds[i];
                    const seedSize = getSeedSize(seed);
                    const seedX = seed.x * (canvas.width / 800);
                    const seedY = seed.y;
                    
                    if (Math.abs(x - seedX) < seedSize * 15 && Math.abs(y - seedY) < seedSize * 15) {
                        hoveredPart = 'seed';
                        updateInfoFromPart('seed');
                        break;
                    }
                }
            } else {
                // 种子特写视图的悬停检测
                const centerX = canvas.width / 2;
                const centerY = canvas.height / 2;
                
                // 根据当前天数确定显示哪些部分
                if (currentDay >= 1) {
                    // 检查是否悬停在胚根上
                    const rootLength = Math.min(currentDay * 8, 80);
                    if (x > centerX - 10 && x < centerX + 10 && y > centerY && y < centerY + rootLength) {
                        hoveredPart = 'radicle';
                        updateInfoFromPart('radicle');
                    }
                }
                
                if (currentDay >= 3 && !hoveredPart) {
                    // 检查是否悬停在胚轴/子叶上
                    const shootLength = Math.max(0, (currentDay - 3) * 6);
                    if (x > centerX - 20 && x < centerX + 20 && y > centerY - shootLength && y < centerY) {
                        if (currentDay >= 7) {
                            hoveredPart = 'cotyledon';
                            updateInfoFromPart('cotyledon');
                        } else {
                            hoveredPart = 'hypocotyl';
                            updateInfoFromPart('hypocotyl');
                        }
                    }
                }
                
                if (!hoveredPart && x > centerX - 25 && x < centerX + 25 && y > centerY - 30 && y < centerY + 30) {
                    hoveredPart = 'seed';
                    updateInfoFromPart('seed');
                }
            }
            
            draw();
        }
        
        // 根据时间线更新信息
        function updateInfoFromTimeline() {
            let event = timelineEvents[0];
            for (let i = timelineEvents.length - 1; i >= 0; i--) {
                if (currentDay >= timelineEvents[i].day) {
                    event = timelineEvents[i];
                    break;
                }
            }
            
            infoTitle.textContent = `第 ${currentDay.toFixed(1)} 天: ${event.title}`;
            infoText.textContent = event.text;
            
            // 添加条件影响信息
            if (!conditions.water || !conditions.air || !conditions.temp) {
                infoText.textContent += " 由于萌发条件不满足，萌发过程受阻。";
            }
        }
        
        // 根据部位更新信息
        function updateInfoFromPart(part) {
            if (partInfo[part]) {
                infoTitle.textContent = partInfo[part].title;
                infoText.textContent = partInfo[part].text;
            }
        }
        
        // 根据条件更新信息
        function updateInfoFromConditions() {
            const missingConditions = [];
            if (!conditions.water) missingConditions.push("水分");
            if (!conditions.air) missingConditions.push("空气(氧气)");
            if (!conditions.temp) missingConditions.push("适宜温度");
            
            if (missingConditions.length > 0) {
                infoTitle.textContent = "萌发条件实验";
                infoText.textContent = `当前缺少: ${missingConditions.join("、")}。种子萌发过程将受到影响。`;
            } else {
                updateInfoFromTimeline();
            }
        }
        
        // 获取种子大小（基于当前天数和条件）
        function getSeedSize(seed) {
            let size = seed.size;
            
            // 如果有水，种子会吸水膨胀
            if (conditions.water && currentDay > 0) {
                size = 1 + Math.min(currentDay / 5, 0.5); // 最大膨胀50%
            }
            
            return size;
        }
        
        // 绘制土壤剖面视图
        function drawSoilView() {
            const width = canvas.width;
            const height = canvas.height;
            
            // 清除画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制土壤背景
            ctx.fillStyle = colors.soilLight;
            ctx.fillRect(0, height * 0.6, width, height * 0.4);
            
            // 绘制土壤纹理
            ctx.fillStyle = colors.soilDark;
            for (let i = 0; i < 50; i++) {
                const x = Math.random() * width;
                const y = height * 0.6 + Math.random() * height * 0.4;
                const size = Math.random() * 3 + 1;
                ctx.fillRect(x, y, size, size);
            }
            
            // 绘制土壤表层
            ctx.fillStyle = colors.soilDark;
            ctx.fillRect(0, height * 0.6, width, 10);
            
            // 绘制每颗种子
            seeds.forEach((seed, index) => {
                const seedSize = getSeedSize(seed);
                const seedX = seed.x * (width / 800);
                const seedY = seed.y;
                
                // 计算萌发进度（每颗种子略有差异）
                let seedProgress = Math.max(0, currentDay - index * 0.3);
                if (!conditions.water || !conditions.air || !conditions.temp) {
                    seedProgress = Math.min(seedProgress, 1); // 条件不足时限制生长
                }
                
                // 绘制种子
                ctx.fillStyle = conditions.water && seedProgress > 0 ? colors.seedHydrated : colors.seedDry;
                ctx.beginPath();
                ctx.ellipse(seedX, seedY, 15 * seedSize, 10 * seedSize, 0, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制种皮裂纹（第1天后）
                if (seedProgress > 1 && conditions.water) {
                    ctx.strokeStyle = colors.soilDark;
                    ctx.lineWidth = 1;
                    ctx.beginPath();
                    ctx.moveTo(seedX - 8 * seedSize, seedY - 3);
                    ctx.lineTo(seedX + 5 * seedSize, seedY + 4);
                    ctx.stroke();
                }
                
                // 绘制胚根（第2天后）
                if (seedProgress > 2 && conditions.water && conditions.air && conditions.temp) {
                    const rootLength = Math.min((seedProgress - 2) * 25, 60);
                    ctx.fillStyle = colors.root;
                    ctx.beginPath();
                    ctx.moveTo(seedX, seedY + 10 * seedSize);
                    ctx.lineTo(seedX - 5, seedY + 10 * seedSize + rootLength);
                    ctx.lineTo(seedX + 5, seedY + 10 * seedSize + rootLength);
                    ctx.closePath();
                    ctx.fill();
                    
                    // 根尖
                    ctx.fillStyle = colors.highlight;
                    ctx.beginPath();
                    ctx.arc(seedX, seedY + 10 * seedSize + rootLength, 3, 0, Math.PI * 2);
                    ctx.fill();
                }
                
                // 绘制胚轴和子叶（第4天后）
                if (seedProgress > 4 && conditions.water && conditions.air && conditions.temp) {
                    const shootLength = Math.min((seedProgress - 4) * 15, 40);
                    ctx.fillStyle = colors.shoot;
                    ctx.fillRect(seedX - 3, seedY - shootLength, 6, shootLength);
                    
                    // 子叶（第6天后）
                    if (seedProgress > 6) {
                        ctx.fillStyle = colors.leaf;
                        // 左子叶
                        ctx.beginPath();
                        ctx.ellipse(seedX - 10, seedY - shootLength, 8, 5, 0, 0, Math.PI * 2);
                        ctx.fill();
                        // 右子叶
                        ctx.beginPath();
                        ctx.ellipse(seedX + 10, seedY - shootLength, 8, 5, 0, 0, Math.PI * 2);
                        ctx.fill();
                    }
                }
                
                // 绘制悬停高亮
                if (hoveredPart === 'seed') {
                    ctx.strokeStyle = colors.infoHighlight;
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.ellipse(seedX, seedY, 18 * seedSize, 13 * seedSize, 0, 0, Math.PI * 2);
                    ctx.stroke();
                }
            });
            
            // 绘制条件效果
            if (conditions.water && currentDay > 0) {
                // 绘制水渗透效果
                ctx.fillStyle = colors.water;
                for (let i = 0; i < 3; i++) {
                    const x = 100 + i * 300;
                    const radius = Math.min(currentDay * 3, 50);
                    ctx.beginPath();
                    ctx.arc(x * (width / 800), height * 0.7, radius, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            if (conditions.air && currentDay > 0) {
                // 绘制气泡（表示氧气）
                ctx.fillStyle = colors.airBubble;
                for (let i = 0; i < 10; i++) {
                    const x = 50 + Math.random() * (width - 100);
                    const y = height * 0.65 + Math.random() * height * 0.35;
                    const size = Math.random() * 4 + 2;
                    const offset = (currentDay * 5 + i * 10) % 100;
                    ctx.beginPath();
                    ctx.arc(x, y - offset, size, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制标题
            ctx.fillStyle = colors.soilDark;
            ctx.font = "16px Arial";
            ctx.fillText("土壤剖面视图 - 观察多颗种子的萌发", 20, 30);
            
            // 绘制图例
            drawLegend();
        }
        
        // 绘制种子特写视图
        function drawSeedView() {
            const width = canvas.width;
            const height = canvas.height;
            const centerX = width / 2;
            const centerY = height / 2;
            
            // 清除画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = '#f0f8ff';
            ctx.fillRect(0, 0, width, height);
            
            // 根据条件调整当前进度
            let effectiveDay = currentDay;
            if (!conditions.water || !conditions.air || !conditions.temp) {
                effectiveDay = Math.min(effectiveDay, 1); // 条件不足时停止在早期阶段
            }
            
            // 绘制种子
            const seedSize = 1 + Math.min(effectiveDay / 5, 0.5);
            ctx.fillStyle = conditions.water && effectiveDay > 0 ? colors.seedHydrated : colors.seedDry;
            ctx.beginPath();
            ctx.ellipse(centerX, centerY, 30 * seedSize, 20 * seedSize, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制种皮裂纹（第1天后）
            if (effectiveDay > 1 && conditions.water) {
                ctx.strokeStyle = colors.soilDark;
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(centerX - 15 * seedSize, centerY - 8);
                ctx.lineTo(centerX + 10 * seedSize, centerY + 10);
                ctx.stroke();
            }
            
            // 绘制胚（始终存在，但颜色变化）
            ctx.fillStyle = effectiveDay > 0 ? colors.root : '#888';
            ctx.beginPath();
            ctx.ellipse(centerX, centerY, 15 * seedSize, 10 * seedSize, 0, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制胚根（第2天后）
            if (effectiveDay > 2 && conditions.water && conditions.air && conditions.temp) {
                const rootLength = Math.min((effectiveDay - 2) * 10, 80);
                ctx.fillStyle = colors.root;
                ctx.beginPath();
                ctx.moveTo(centerX, centerY + 20 * seedSize);
                ctx.lineTo(centerX - 8, centerY + 20 * seedSize + rootLength);
                ctx.lineTo(centerX + 8, centerY + 20 * seedSize + rootLength);
                ctx.closePath();
                ctx.fill();
                
                // 根尖和根毛
                ctx.fillStyle = colors.highlight;
                ctx.beginPath();
                ctx.arc(centerX, centerY + 20 * seedSize + rootLength, 5, 0, Math.PI * 2);
                ctx.fill();
                
                // 根毛
                if (effectiveDay > 4) {
                    ctx.strokeStyle = colors.root;
                    ctx.lineWidth = 1;
                    for (let i = 0; i < 8; i++) {
                        const yPos = centerY + 20 * seedSize + 20 + i * 8;
                        ctx.beginPath();
                        ctx.moveTo(centerX - 8, yPos);
                        ctx.lineTo(centerX - 15, yPos);
                        ctx.stroke();
                        ctx.beginPath();
                        ctx.moveTo(centerX + 8, yPos);
                        ctx.lineTo(centerX + 15, yPos);
                        ctx.stroke();
                    }
                }
            }
            
            // 绘制胚轴和子叶（第4天后）
            if (effectiveDay > 4 && conditions.water && conditions.air && conditions.temp) {
                const shootLength = Math.min((effectiveDay - 4) * 8, 50);
                ctx.fillStyle = colors.shoot;
                ctx.fillRect(centerX - 5, centerY - shootLength, 10, shootLength);
                
                // 子叶（第6天后）
                if (effectiveDay > 6) {
                    ctx.fillStyle = colors.leaf;
                    // 左子
<!--检测到代码截断，自动续写中...-->
叶
                    ctx.beginPath();
                    ctx.ellipse(centerX - 15, centerY - shootLength, 12, 8, -0.3, 0, Math.PI * 2);
                    ctx.fill();
                    // 右子叶
                    ctx.beginPath();
                    ctx.ellipse(centerX + 15, centerY - shootLength, 12, 8, 0.3, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 真叶（第10天后）
                    if (effectiveDay > 10) {
                        ctx.fillStyle = colors.leaf;
                        // 左真叶
                        ctx.beginPath();
                        ctx.moveTo(centerX - 5, centerY - shootLength - 5);
                        ctx.lineTo(centerX - 20, centerY - shootLength - 25);
                        ctx.lineTo(centerX - 5, centerY - shootLength - 20);
                        ctx.closePath();
                        ctx.fill();
                        // 右真叶
                        ctx.beginPath();
                        ctx.moveTo(centerX + 5, centerY - shootLength - 5);
                        ctx.lineTo(centerX + 20, centerY - shootLength - 25);
                        ctx.lineTo(centerX + 5, centerY - shootLength - 20);
                        ctx.closePath();
                        ctx.fill();
                    }
                }
            }
            
            // 绘制内部物质转运示意（第1-5天）
            if (effectiveDay > 1 && effectiveDay < 6 && conditions.water && conditions.air && conditions.temp) {
                ctx.strokeStyle = colors.highlight;
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 3]);
                
                // 从子叶到胚根的箭头
                ctx.beginPath();
                ctx.moveTo(centerX - 10, centerY - 5);
                ctx.lineTo(centerX - 5, centerY + 10);
                ctx.lineTo(centerX, centerY + 25);
                ctx.stroke();
                
                // 箭头头
                ctx.fillStyle = colors.highlight;
                ctx.beginPath();
                ctx.moveTo(centerX, centerY + 25);
                ctx.lineTo(centerX - 3, centerY + 20);
                ctx.lineTo(centerX + 3, centerY + 20);
                ctx.closePath();
                ctx.fill();
                
                ctx.setLineDash([]);
            }
            
            // 绘制呼吸作用气泡（第1天后，有空气时）
            if (effectiveDay > 1 && conditions.air) {
                ctx.fillStyle = colors.airBubble;
                for (let i = 0; i < 5; i++) {
                    const x = centerX - 20 + i * 10;
                    const y = centerY + 10 - (effectiveDay * 2 + i * 5) % 30;
                    const size = Math.random() * 3 + 2;
                    ctx.beginPath();
                    ctx.arc(x, y, size, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制悬停高亮
            if (hoveredPart) {
                ctx.strokeStyle = colors.infoHighlight;
                ctx.lineWidth = 3;
                
                if (hoveredPart === 'seed') {
                    ctx.beginPath();
                    ctx.ellipse(centerX, centerY, 35 * seedSize, 25 * seedSize, 0, 0, Math.PI * 2);
                    ctx.stroke();
                } else if (hoveredPart === 'radicle') {
                    const rootLength = Math.min((effectiveDay - 2) * 10, 80);
                    ctx.beginPath();
                    ctx.moveTo(centerX - 10, centerY + 20 * seedSize);
                    ctx.lineTo(centerX - 15, centerY + 20 * seedSize + rootLength);
                    ctx.lineTo(centerX + 15, centerY + 20 * seedSize + rootLength);
                    ctx.lineTo(centerX + 10, centerY + 20 * seedSize);
                    ctx.closePath();
                    ctx.stroke();
                } else if (hoveredPart === 'hypocotyl' || hoveredPart === 'cotyledon') {
                    const shootLength = Math.min((effectiveDay - 4) * 8, 50);
                    ctx.beginPath();
                    ctx.rect(centerX - 8, centerY - shootLength - 5, 16, shootLength + 10);
                    ctx.stroke();
                }
            }
            
            // 绘制标题
            ctx.fillStyle = colors.soilDark;
            ctx.font = "16px Arial";
            ctx.fillText("种子特写视图 - 观察内部结构与变化", 20, 30);
            
            // 绘制标注
            ctx.fillStyle = "#333";
            ctx.font = "12px Arial";
            
            if (effectiveDay > 0) {
                ctx.fillText("种皮", centerX + 40 * seedSize, centerY);
            }
            
            if (effectiveDay > 2) {
                ctx.fillText("胚根", centerX, centerY + 20 * seedSize + 40);
            }
            
            if (effectiveDay > 4) {
                ctx.fillText("胚轴", centerX + 25, centerY - 20);
            }
            
            if (effectiveDay > 6) {
                ctx.fillText("子叶", centerX - 40, centerY - 40);
            }
            
            // 绘制图例
            drawLegend();
        }
        
        // 绘制图例
        function drawLegend() {
            const width = canvas.width;
            
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.fillRect(width - 160, 50, 150, 120);
            
            ctx.strokeStyle = '#333';
            ctx.lineWidth = 1;
            ctx.strokeRect(width - 160, 50, 150, 120);
            
            ctx.fillStyle = '#333';
            ctx.font = "bold 14px Arial";
            ctx.fillText("图例", width - 150, 70);
            
            ctx.font = "12px Arial";
            
            // 水分
            ctx.fillStyle = colors.water;
            ctx.fillRect(width - 150, 85, 12, 12);
            ctx.fillStyle = '#333';
            ctx.fillText("水分", width - 130, 95);
            
            // 空气
            ctx.fillStyle = colors.airBubble;
            ctx.beginPath();
            ctx.arc(width - 150, 110, 6, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#333';
            ctx.fillText("空气(氧气)", width - 130, 115);
            
            // 物质转运
            ctx.strokeStyle = colors.highlight;
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 3]);
            ctx.beginPath();
            ctx.moveTo(width - 155, 125);
            ctx.lineTo(width - 140, 125);
            ctx.stroke();
            ctx.setLineDash([]);
            ctx.fillStyle = '#333';
            ctx.fillText("物质转运", width - 130, 135);
            
            // 生长点
            ctx.fillStyle = colors.highlight;
            ctx.beginPath();
            ctx.arc(width - 150, 150, 4, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = '#333';
            ctx.fillText("生长点", width - 130, 155);
        }
        
        // 绘制函数
        function draw() {
            if (currentView === 'soil') {
                drawSoilView();
            } else {
                drawSeedView();
            }
        }
        
        // 动画循环
        function animate(timestamp) {
            if (isPlaying) {
                if (lastTimestamp === 0) lastTimestamp = timestamp;
                const deltaTime = timestamp - lastTimestamp;
                
                // 根据速度更新天数
                currentDay += deltaTime * 0.001 * animationSpeed;
                
                // 限制天数范围
                if (currentDay > 15) {
                    currentDay = 15;
                    isPlaying = false;
                    playPauseBtn.textContent = '▶ 播放';
                }
                
                // 更新UI
                timelineSlider.value = currentDay;
                currentDayEl.textContent = `第 ${currentDay.toFixed(1)} 天`;
                updateInfoFromTimeline();
                
                // 重绘
                draw();
                
                lastTimestamp = timestamp;
            } else {
                lastTimestamp = 0;
            }
            
            requestAnimationFrame(animate);
        }
        
        // 启动应用
        window.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 《种子萌发全时程交互教学动画》使用指南

欢迎使用“种子萌发全时程交互教学动画”！本工具旨在通过动态、交互的方式，帮助您直观理解种子从休眠到幼苗建立的完整过程（0-15天）。无论您是教师、学生还是植物爱好者，都能通过自主探索，突破真实实验周期长、观察不连续的局限，深入掌握种子萌发的核心知识。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas技术构建的交互式教学工具，集成了**动态模拟**、**条件控制实验**和**分层信息提示**三大核心功能。它模拟了菜豆种子（子叶出土型）在适宜条件下的萌发全过程，并允许您通过调整关键变量，观察其对萌发进程的影响。

### 二、 主要功能与操作

#### 1. **核心观察区（左侧画布）**
*   **动态模拟**：动画自动或手动展示种子从第0天到第15天的连续变化，包括吸水膨胀、胚根突破、胚轴伸长、子叶出土、真叶展开等关键阶段。
*   **视图切换**：
    *   **土壤剖面视图**：模拟多颗种子在土壤环境中的萌发，观察自然条件下的个体差异。
    *   **种子特写视图**：聚焦单颗种子，可清晰观察其内部结构（如胚、子叶）的变化以及物质转运的示意过程。
*   **交互探索**：将鼠标悬停在画布中的种子、胚根、子叶等部位，会实时高亮该部分并显示其名称和功能说明。

#### 2. **时间线控制**
*   **滑块拖拽**：直接拖动时间轴滑块，可以快速跳转到萌发过程中的任何一天（如第3.5天），实现过程的精细观察。
*   **播放控制**：
    *   **播放/暂停**：以恒定速度播放或暂停动画。
    *   **速度调节**：点击“速度”按钮可在“1倍速”、“2倍速”、“0.5倍速”间循环切换，适应不同的观察节奏。
    *   **重置**：一键将动画恢复到第0天的初始状态。

#### 3. **萌发条件实验面板（右侧控制区）**
这是本动画的核心探究功能。您可以像科学家一样设计对照实验：
*   **三个可控条件**：“水分”、“空气（氧气）”、“适宜温度”。
*   **操作**：点击每个条件旁的开关按钮，可以**开启或关闭**该条件。
*   **观察**：当关闭任一条件（如关闭“水分”）后，左侧动画将直观展示萌发过程如何受阻（种子仅略微膨胀但不破裂、不生长），从而深刻理解每个条件的必要性。

#### 4. **智能信息提示面板**
位于控制区下方，它会根据您的操作动态显示相关信息：
*   默认显示当前时间点的阶段描述。
*   当鼠标悬停于种子某部分时，显示该结构的详细说明。
*   当您操作条件开关时，解释条件改变带来的影响。

### 三、 设计特色

1.  **科学性与艺术性结合**：外部形态变化力求写实（如土壤、种子颜色），内部生理过程（物质转运、呼吸作用）则采用清晰的示意图和箭头表示，化抽象为具体。
2.  **分层可视化设计**：提供“宏观”（土壤剖面）与“微观”（种子特写）两种视角，符合从整体到局部的认知规律。
3.  **探究式学习导向**：“条件控制”模块不是被动的知识呈现，而是主动的实验工具，鼓励用户提出假设、验证猜想。
4.  **友好的用户体验**：界面布局清晰，配色柔和自然，交互反馈即时，关键元素均有高亮和文字提示，降低使用门槛。

### 四、 教学要点与建议

#### 适用于课堂教学：
*   **新课导入**：播放完整动画，引发学生对种子萌发这一生命现象的兴趣与疑问。
*   **核心概念讲解**：结合“种子特写视图”，分步讲解胚根、胚轴、子叶的结构与功能。
*   **探究实验**：将学生分组，分别操作关闭水、空气、温度条件，观察并记录现象，最后全班分享，共同归纳出种子萌发的三大必要条件。
*   **复习与巩固**：让学生操作时间轴，复述或书写从第0天到第15天的变化顺序，巩固知识脉络。

#### 适用于自主学习：
*   **自主探索**：鼓励学生先自由操作所有功能，提出问题。
*   **目标挑战**：布置任务，如“请展示出第5天时种子是什么样子？”或“设计一个实验，证明温度对萌发的影响”。
*   **联系实际**：观察动画后，尝试在家种植豆芽，将虚拟观察与真实体验相结合。

### 五、 使用建议

1.  **推荐使用流程**：
    *   第一步：在“土壤剖面视图”下，点击**播放**，完整观看一遍0-15天的过程，建立整体印象。
    *   第二步：切换到“**种子特写视图**”，将时间轴拖到**第1-3天**，悬停观察种子吸水、种皮破裂、胚根突出的细节。
    *   第三步：进行“**条件控制实验**”，分别关闭水、空气、温度，对比观察萌发如何停止，理解各条件的作用。
    *   第四步：将时间轴拖到**第7天和第10天**，观察子叶和真叶的差异，理解幼苗从异养到自养的转变。

2.  **技术提示**：
    *   本动画为单HTML文件，可在大多数现代浏览器（Chrome, Edge, Firefox, Safari）中直接打开运行。
    *   为获得最佳体验，建议在电脑或平板电脑上使用。

3.  **教学延伸**：
    *   **讨论**：动画中的种子萌发速度是理想的，现实中会受到哪些更多因素影响？（光照、土壤深度、种子活力等）。
    *   **对比**：引导学生思考：花生、玉米、豌豆的种子萌发过程与本动画中的菜豆有何异同？（子叶留土与出土）。

---

希望这份指南能帮助您充分利用这个交互式工具，让种子萌发这一神奇的生命旅程生动地展现在您和学生面前。祝您探索愉快，教学相长！

**设计者：熊猫老师**  
*让抽象的概念生根发芽，让探究的乐趣触手可及。*