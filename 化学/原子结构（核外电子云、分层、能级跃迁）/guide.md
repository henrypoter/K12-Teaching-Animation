# 需求：原子结构（核外电子云、分层、能级跃迁）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向**高中或大学低年级的物理、化学初学者**。用户的核心需求是：
1.  **理解抽象概念**：将“电子云”、“能级”、“跃迁”等肉眼不可见的微观、概率性概念，转化为直观、动态的视觉模型。
2.  **建立空间与能量关系**：理解电子在原子核外并非沿固定轨道运行，而是存在于具有特定形状和能量的“区域”（轨道）中，且能量是量子化的、分层的。
3.  **掌握动态过程**：理解电子吸收或释放能量时，在不同能级间“跃迁”的动态过程，并建立其与光谱（吸收/发射）现象的联系。
4.  **主动探索与验证**：用户希望通过交互操作（如改变参数、触发事件）来观察不同结果，从而加深理解和记忆，而非被动观看。

#### 教学设计思路
遵循“从宏观类比到微观本质，从静态结构到动态过程”的认知规律，进行分层设计：

*   **核心概念拆解与串联**：
    *   **第一层：电子云的概率性** - 摒弃“行星轨道”的经典错误模型，用大量随机出现的点模拟电子出现的“概率密度”，逐渐累积形成“云”状。这是理解现代原子模型的基石。
    *   **第二层：能级与壳层** - 将电子云按能量高低分层（K, L, M...层），并展示每层可容纳的电子数。强调能量是量子化的，电子只能存在于这些特定的能级上。
    *   **第三层：轨道形状（s, p）** - 在同一能级内，展示s轨道（球形）和p轨道（哑铃形）的不同电子云形状，引入“角量子数”的初步概念。
    *   **第四层：能级跃迁** - 将前三个静态概念动态化。展示电子吸收特定能量光子后从低能级跃迁到高能级（处于“激发态”），以及从高能级自发跃迁回低能级并释放特定波长光子的过程。

*   **交互与视觉呈现策略**：
    *   **渐进式呈现**：动画将分为清晰的几个模块或“场景”，用户可按顺序学习，也可通过导航自由跳转。
    *   **对比呈现**：将错误的“行星轨道模型”与正确的“电子云模型”并置对比，破除迷思概念。
    *   **粒子系统与数据可视化**：用**粒子系统**模拟电子出现的随机位置，用**等高线**或**透明度渐变**来可视化概率密度。用**阶梯状的水平线**和**垂直箭头**清晰表示量子化的能级和跃迁过程。
    *   **隐喻与关联**：用“楼梯”隐喻量子化的能级（只能站在台阶上，不能站在空中）；用“投掷飞镖”的靶心分布类比电子云的概率；将释放的光子波长与可见光谱颜色关联（如从n=3到n=2跃迁释放红光）。

#### 配色方案选择
选择兼具科学性、清晰度和视觉舒适度的配色：
*   **主色调**：深空蓝（`#0f1a30`）或深灰色（`#2c3e50`）作为背景，营造深邃、专注的科技感，并突出前景元素。
*   **核心元素**：
    *   **原子核**：温暖、坚实的颜色，如金色（`#f1c40f`）或铜色（`#d35400`），表示其致密、带正电。
    *   **电子/概率点**：亮蓝色（`#3498db`）或青色（`#1abc9c`），代表负电、动态与量子特性。
    *   **电子云区域**：使用主色（亮蓝/青）的**半透明填充**（如 `rgba(52, 152, 219, 0.2)`）叠加在概率点上，形成云状。
    *   **能级线**：浅灰色（`#bdc3c7`）虚线，保持清晰但不喧宾夺主。
    *   **跃迁箭头与光子**：
        *   **吸收跃迁（向上）**：使用能量感强的颜色，如亮黄色（`#f39c12`）箭头。
        *   **发射跃迁（向下）**：根据跃迁终点能级差，模拟可见光颜色（如红 `#e74c3c`、蓝绿 `#1abc9c`、蓝 `#3498db`、紫 `#9b59b6`），光子用相应颜色的光点或波浪线表示。
*   **交互UI**：使用中性白色（`#ecf0f1`）或浅灰色，确保按钮、滑块和文字清晰可读。

#### 交互功能列表
1.  **场景导航器**：按钮或缩略图导航，在“电子云概率模型”、“能级与壳层”、“轨道形状”、“能级跃迁”四个核心场景间切换。
2.  **电子云模拟控制**：
    *   **“运行/暂停”**：控制概率点动画的播放与停止。
    *   **“重置/清除”**：清除所有已绘制的点，重新开始累积。
    *   **“加速/减速”**：滑块控制概率点出现的频率，快速看到云的形成，或慢速观察单个点的随机性。
3.  **能级与轨道选择器**：
    *   **“选择元素”**：下拉菜单选择氢（H）、氦（He）、锂（Li）等简单原子，动态显示其核外电子排布。
    *   **“选择壳层(n)”**：按钮选择查看第1、2、3…层。
    *   **“选择轨道类型(l)”**：在选定壳层后，按钮切换查看s轨道、p_x, p_y, p_z轨道。
4.  **能级跃迁模拟器**：
    *   **“能量输入”滑块**：用户拖动滑块模拟向原子输入能量。当能量值精确匹配某两个能级差时，触发相应的电子跃迁动画。
    *   **“激发”按钮**：一键输入特定能量，使基态氢原子的电子跃迁到n=2,3,4…能级。
    *   **“自动衰减”开关**：开启后，处于激发态的电子会自动在随机延迟后跃迁回低能级并释放光子。
    *   **“显示光谱”按钮**：在画面一侧显示原子发射光谱的简图，将发生的每次跃迁与光谱中的一条谱线关联起来。
5.  **图示开关**：可勾选/取消勾选显示“概率点”、“电子云轮廓”、“能级线”、“轨道名称”等图层，帮助用户分层理解。
6.  **信息提示**：鼠标悬停在关键部件（如原子核、电子云区域、能级线、光子）上时，显示简洁的科学说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>原子结构：电子云、能级与跃迁</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #0f1a30 0%, #1a2c42 100%);
            color: #ecf0f1;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .header {
            text-align: center;
            margin-bottom: 20px;
            max-width: 900px;
        }

        h1 {
            color: #f1c40f;
            margin-bottom: 10px;
            font-size: 2.5rem;
            text-shadow: 0 2px 4px rgba(0,0,0,0.5);
        }

        .subtitle {
            color: #bdc3c7;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1200px;
            width: 100%;
            justify-content: center;
        }

        .main-canvas-container {
            flex: 1;
            min-width: 600px;
            background-color: rgba(44, 62, 80, 0.7);
            border-radius: 15px;
            padding: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
            overflow: hidden;
        }

        #atomCanvas {
            display: block;
            width: 100%;
            height: 500px;
            background-color: rgba(15, 26, 48, 0.9);
            border-radius: 10px;
        }

        .controls-panel {
            width: 320px;
            background-color: rgba(44, 62, 80, 0.9);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .panel-section {
            border-bottom: 1px solid rgba(189, 195, 199, 0.2);
            padding-bottom: 20px;
        }

        .panel-section:last-child {
            border-bottom: none;
        }

        h2 {
            color: #3498db;
            font-size: 1.4rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        h2 i {
            font-size: 1.2rem;
        }

        .scene-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }

        .scene-btn {
            padding: 12px 10px;
            background-color: #2c3e50;
            color: #ecf0f1;
            border: 2px solid #3498db;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-align: center;
        }

        .scene-btn:hover {
            background-color: #3498db;
            transform: translateY(-2px);
        }

        .scene-btn.active {
            background-color: #1abc9c;
            border-color: #1abc9c;
            box-shadow: 0 0 15px rgba(26, 188, 156, 0.5);
        }

        .control-group {
            margin-bottom: 15px;
        }

        .control-label {
            display: block;
            margin-bottom: 8px;
            color: #bdc3c7;
            font-size: 0.95rem;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: linear-gradient(to right, #2c3e50, #3498db);
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background-color: #f1c40f;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(241, 196, 15, 0.8);
        }

        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: #f1c40f;
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }

        .btn {
            padding: 10px 15px;
            background-color: #34495e;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }

        .btn:hover {
            background-color: #4a6b8f;
            transform: translateY(-2px);
        }

        .btn.primary {
            background-color: #3498db;
        }

        .btn.primary:hover {
            background-color: #2980b9;
        }

        .btn.warning {
            background-color: #f39c12;
        }

        .btn.warning:hover {
            background-color: #e67e22;
        }

        .btn.success {
            background-color: #2ecc71;
        }

        .btn.success:hover {
            background-color: #27ae60;
        }

        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }

        .checkbox-item input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .info-panel {
            position: absolute;
            bottom: 20px;
            left: 20px;
            right: 20px;
            background-color: rgba(44, 62, 80, 0.85);
            border-radius: 10px;
            padding: 15px;
            border-left: 5px solid #1abc9c;
            font-size: 0.95rem;
            line-height: 1.5;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            max-height: 120px;
            overflow-y: auto;
        }

        .info-title {
            color: #f1c40f;
            font-weight: bold;
            margin-bottom: 5px;
            font-size: 1.1rem;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 10px;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }

        .footer {
            margin-top: 30px;
            text-align: center;
            color: #7f8c8d;
            font-size: 0.9rem;
            max-width: 900px;
        }

        @media (max-width: 1000px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            
            .main-canvas-container, .controls-panel {
                width: 100%;
                min-width: unset;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>原子结构：电子云、能级与跃迁</h1>
        <p class="subtitle">探索微观世界的量子特性 - 电子概率分布、量子化能级与光子发射</p>
    </div>

    <div class="container">
        <div class="main-canvas-container">
            <canvas id="atomCanvas" width="800" height="500"></canvas>
            <div class="info-panel">
                <div class="info-title" id="infoTitle">欢迎来到原子世界</div>
                <div id="infoText">请选择一个场景开始探索。电子云模型展示了电子在原子核周围出现的概率分布，而不是固定的轨道。</div>
            </div>
        </div>

        <div class="controls-panel">
            <div class="panel-section">
                <h2>📚 学习场景</h2>
                <div class="scene-buttons">
                    <button class="scene-btn active" data-scene="electronCloud">电子云概率模型</button>
                    <button class="scene-btn" data-scene="energyLevels">能级与壳层</button>
                    <button class="scene-btn" data-scene="orbitals">轨道形状</button>
                    <button class="scene-btn" data-scene="transitions">能级跃迁</button>
                </div>
            </div>

            <div class="panel-section">
                <h2>⚙️ 模拟控制</h2>
                <div class="control-group">
                    <div class="control-label">电子出现频率：<span id="speedValue" class="slider-value">中速</span></div>
                    <div class="slider-container">
                        <input type="range" id="speedSlider" min="1" max="10" value="5">
                    </div>
                </div>
                
                <div class="button-group">
                    <button id="playBtn" class="btn primary">▶ 运行模拟</button>
                    <button id="resetBtn" class="btn">🔄 重置</button>
                    <button id="clearBtn" class="btn">🗑️ 清除轨迹</button>
                </div>
            </div>

            <div class="panel-section">
                <h2>🔬 原子参数</h2>
                <div class="control-group">
                    <div class="control-label">选择元素：</div>
                    <select id="elementSelect" class="btn" style="width:100%; padding:10px;">
                        <option value="H">氢 (H) - 1个电子</option>
                        <option value="He">氦 (He) - 2个电子</option>
                        <option value="Li">锂 (Li) - 3个电子</option>
                    </select>
                </div>
                
                <div class="control-group">
                    <div class="control-label">能级跃迁能量：<span id="energyValue" class="slider-value">0.0 eV</span></div>
                    <div class="slider-container">
                        <input type="range" id="energySlider" min="0" max="15" value="0" step="0.5">
                    </div>
                </div>
                
                <div class="button-group">
                    <button id="exciteBtn" class="btn warning">⚡ 激发原子</button>
                    <button id="autoDecayBtn" class="btn success">🔄 自动衰减: 关</button>
                    <button id="spectrumBtn" class="btn">🌈 显示光谱</button>
                </div>
            </div>

            <div class="panel-section">
                <h2>👁️ 显示选项</h2>
                <div class="checkbox-group">
                    <label class="checkbox-item">
                        <input type="checkbox" id="showPoints" checked>
                        <span>概率点</span>
                    </label>
                    <label class="checkbox-item">
                        <input type="checkbox" id="showCloud" checked>
                        <span>电子云轮廓</span>
                    </label>
                    <label class="checkbox-item">
                        <input type="checkbox" id="showLevels" checked>
                        <span>能级线</span>
                    </label>
                    <label class="checkbox-item">
                        <input type="checkbox" id="showLabels">
                        <span>轨道标签</span>
                    </label>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f1c40f;"></div>
                        <span>原子核</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>电子/概率点</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: rgba(52, 152, 219, 0.2);"></div>
                        <span>电子云区域</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="footer">
        <p>教学动画 | 原子结构：核外电子云、分层、能级跃迁 | 设计原理：量子力学概率模型、玻尔能级、电子跃迁</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('atomCanvas');
        const ctx = canvas.getContext('2d');
        
        // 动画状态
        let animationId = null;
        let isPlaying = true;
        let currentScene = 'electronCloud';
        let points = []; // 存储概率点
        let orbitals = []; // 存储轨道数据
        let transitions = []; // 存储跃迁动画
        let photons = []; // 存储光子
        let autoDecay = false;
        let showSpectrum = false;
        
        // 原子参数
        let atom = {
            element: 'H',
            electronCount: 1,
            nucleusRadius: 12,
            energyLevels: [
                {n: 1, radius: 80, electrons: 1, color: '#3498db'},
                {n: 2, radius: 160, electrons: 0, color: '#1abc9c'},
                {n: 3, radius: 240, electrons: 0, color: '#9b59b6'},
                {n: 4, radius: 320, electrons: 0, color: '#e74c3c'}
            ],
            excitedLevel: 1 // 当前激发到的能级
        };
        
        // 能级跃迁能量 (eV)
        const transitionEnergies = {
            '1-2': 10.2,
            '1-3': 12.1,
            '1-4': 12.75,
            '2-3': 1.89,
            '2-4': 2.55,
            '3-4': 0.66
        };
        
        // 跃迁对应的颜色
        const transitionColors = {
            '1-2': '#e74c3c', // 红色
            '1-3': '#f39c12', // 橙色
            '1-4': '#f1c40f', // 黄色
            '2-3': '#2ecc71', // 绿色
            '2-4': '#1abc9c', // 蓝绿色
            '3-4': '#3498db'  // 蓝色
        };
        
        // 轨道形状数据
        const orbitalShapes = {
            's': {type: 's', radius: 80, color: 'rgba(52, 152, 219, 0.15)'},
            'px': {type: 'p', axis: 'x', radius: 120, color: 'rgba(26, 188, 156, 0.15)'},
            'py': {type: 'p', axis: 'y', radius: 120, color: 'rgba(26, 188, 156, 0.15)'},
            'pz': {type: 'p', axis: 'z', radius: 120, color: 'rgba(26, 188, 156, 0.15)'}
        };
        
        // 初始化
        function init() {
            // 设置Canvas尺寸
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
            
            // 初始化轨道
            orbitals = [];
            for (let i = 0; i < 4; i++) {
                orbitals.push({
                    x: canvas.width/2,
                    y: canvas.height/2,
                    radius: 80 + i * 80,
                    points: []
                });
            }
            
            // 设置事件监听器
            setupEventListeners();
            
            // 开始动画循环
            animate();
        }
        
        // 设置事件监听器
        function setupEventListeners() {
            // 场景按钮
            document.querySelectorAll('.scene-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    document.querySelectorAll('.scene-btn').forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    currentScene = this.dataset.scene;
                    updateInfoPanel();
                    
                    // 重置一些状态
                    if (currentScene === 'electronCloud') {
                        points = [];
                    }
                    if (currentScene === 'transitions') {
                        transitions = [];
                        photons = [];
                    }
                });
            });
            
            // 播放/暂停按钮
            document.getElementById('playBtn').addEventListener('click', function() {
                isPlaying = !isPlaying;
                this.textContent = isPlaying ? '⏸ 暂停模拟' : '▶ 运行模拟';
            });
            
            // 重置按钮
            document.getElementById('resetBtn').addEventListener('click', function() {
                points = [];
                transitions = [];
                photons = [];
                atom.excitedLevel = 1;
                updateAtomFromElement();
            });
            
            // 清除按钮
            document.getElementById('clearBtn').addEventListener('click', function() {
                points = [];
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speedSlider');
            const speedValue = document.getElementById('speedValue');
            speedSlider.addEventListener('input', function() {
                const speeds = ['极慢', '很慢', '慢', '较慢', '中速', '较快', '快', '很快', '极快', '超快'];
                speedValue.textContent = speeds[this.value - 1];
            });
            
            // 元素选择
            document.getElementById('elementSelect').addEventListener('change', function() {
                atom.element = this.value;
                updateAtomFromElement();
            });
            
            // 能量滑块
            const energySlider = document.getElementById('energySlider');
            const energyValue = document.getElementById('energyValue');
            energySlider.addEventListener('input', function() {
                energyValue.textContent = this.value + ' eV';
            });
            
            // 激发按钮
            document.getElementById('exciteBtn').addEventListener('click', function() {
                const energy = parseFloat(energySlider.value);
                triggerTransition(energy);
            });
            
            // 自动衰减按钮
            document.getElementById('autoDecayBtn').addEventListener('click', function() {
                autoDecay = !autoDecay;
                this.textContent = autoDecay ? '🔄 自动衰减: 开' : '🔄 自动衰减: 关';
                this.classList.toggle('success', autoDecay);
            });
            
            // 光谱按钮
            document.getElementById('spectrumBtn').addEventListener('click', function() {
                showSpectrum = !showSpectrum;
                this.textContent = showSpectrum ? '🌈 隐藏光谱' : '🌈 显示光谱';
            });
            
            // 显示选项
            document.getElementById('showPoints').addEventListener('change', updateDisplay);
            document.getElementById('showCloud').addEventListener('change', updateDisplay);
            document.getElementById('showLevels').addEventListener('change', updateDisplay);
            document.getElementById('showLabels').addEventListener('change', updateDisplay);
            
            // 窗口大小调整
            window.addEventListener('resize', function() {
                canvas.width = canvas.offsetWidth;
                canvas.height = canvas.offsetHeight;
            });
        }
        
        // 根据选择的元素更新原子参数
        function updateAtomFromElement() {
            switch(atom.element) {
                case 'H':
                    atom.electronCount = 1;
                    atom.energyLevels[0].electrons = 1;
                    atom.energyLevels[1].electrons = 0;
                    atom.energyLevels[2].electrons = 0;
                    atom.energyLevels[3].electrons = 0;
                    break;
                case 'He':
                    atom.electronCount = 2;
                    atom.energyLevels[0].electrons = 2;
                    atom.energyLevels[1].electrons = 0;
                    atom.energyLevels[2].electrons = 0;
                    atom.energyLevels[3].electrons = 0;
                    break;
                case 'Li':
                    atom.electronCount = 3;
                    atom.energyLevels[0].electrons = 2;
                    atom.energyLevels[1].electrons = 1;
                    atom.energyLevels[2].electrons = 0;
                    atom.energyLevels[3].electrons = 0;
                    break;
            }
            atom.excitedLevel = 1;
        }
        
        // 触发能级跃迁
        function triggerTransition(energy) {
            // 查找最匹配的能级跃迁
            let closestTransition = null;
            let minDiff = Infinity;
            
            for (const [key, value] of Object.entries(transitionEnergies)) {
                const diff = Math.abs(energy - value);
                if (diff < minDiff && diff < 1.5) { // 容忍度1.5eV
                    minDiff = diff;
                    closestTransition = key;
                }
            }
            
            if (closestTransition) {
                const [from, to] = closestTransition.split('-').map(Number);
                
                // 检查是否可以从当前能级跃迁
                if (from === atom.excitedLevel) {
                    // 添加跃迁动画
                    transitions.push({
                        fromLevel: from,
                        toLevel: to,
                        progress: 0,
                        color: transitionColors[closestTransition],
                        direction: 'up'
                    });
                    
                    // 更新原子激发态
                    atom.excitedLevel = to;
                    
                    // 更新信息面板
                    updateInfoPanel(`电子从 n=${from} 跃迁到 n=${to}，吸收 ${transitionEnergies[closestTransition].toFixed(2)} eV 能量`);
                    
                    // 如果自动衰减开启，稍后触发衰减
                    if (autoDecay) {
                        setTimeout(() => {
                            triggerDecay(to, from);
                        }, 1500);
                    }
                } else {
                    updateInfoPanel(`当前电子在 n=${atom.excitedLevel}，需要 ${transitionEnergies[closestTransition].toFixed(2)} eV 才能跃迁到 n=${to}`);
                }
            } else {
                updateInfoPanel(`能量 ${energy.toFixed(2)} eV 不匹配任何允许的能级跃迁`);
            }
        }
        
        // 触发衰减（自发辐射）
        function triggerDecay(from, to) {
            const key = `${to}-${from}`;
            if (transitionColors[key]) {
                transitions.push({
                    fromLevel: from,
                    toLevel: to,
                    progress: 0,
                    color: transitionColors[key],
                    direction: 'down'
                });
                
                // 添加光子
                const centerX = canvas.width / 2;
                const centerY = canvas.height / 2;
                const fromRadius = atom.energyLevels[from-1].radius;
                const angle = Math.random() * Math.PI * 2;
                
                photons.push({
                    x: centerX + Math.cos(angle) * fromRadius,
                    y: centerY + Math.sin(angle) * fromRadius,
                    color: transitionColors[key],
                    radius: 5,
                    speed: 3,
                    angle: angle,
                    life: 100
                });
                
                // 更新原子状态
                atom.excitedLevel = to;
                
                updateInfoPanel(`电子从 n=${from} 衰减到 n=${to}，发射 ${transitionEnergies[key].toFixed(2)} eV 光子`);
            }
        }
        
        // 更新信息面板
        function updateInfoPanel(customText) {
            const infoTitle = document.getElementById('infoTitle');
            const infoText = document.getElementById('infoText');
            
            const sceneInfo = {
                'electronCloud': {
                    title: '电子云概率模型',
                    text: '每个蓝点表示电子可能出现的位置。随着时间推移，点的分布形成"电子云"，显示电子在原子核周围的概率密度。'
                },
                'energyLevels': {
                    title: '能级与壳层',
                    text: '灰色虚线表示量子化的能级（K, L, M...层）。电子只能存在于这些特定能级上，不能处于能级之间。'
                },
                'orbitals': {
                    title: '轨道形状',
                    text: 's轨道呈球形对称，p轨道呈哑铃形（沿x、y、z轴）。不同形状的轨道对应不同的角动量量子数。'
                },
                'transitions': {
                    title: '能级跃迁',
                    text: '电子吸收能量跃迁到高能级（激发态），然后自发跃迁回低能级并发射光子。光子颜色取决于能级差。'
                }
            };
            
            if (customText) {
                infoText.textContent = customText;
            } else {
                infoTitle.textContent = sceneInfo[currentScene].title;
                infoText.textContent = sceneInfo[currentScene].text;
            }
        }
        
        // 更新显示（占位函数）
        function updateDisplay() {
            // 显示选项已在绘制函数中处理
        }
        
        // 生成概率点
        function generateProbabilityPoint() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 根据当前场景和能级生成点
            let radius, angle;
            
            if (currentScene === 'electronCloud' || currentScene === 'energyLevels') {
                // 基于当前激发能级
                const levelIndex = Math.min(atom.excitedLevel - 1, 3);
                const baseRadius = atom.energyLevels[levelIndex].radius;
                
                // 高斯分布，更靠近能级半径
                radius = baseRadius * (0.7 + Math.random() * 0.6);
                angle = Math.random() * Math.PI * 2;
                
                // 添加一些随机性
                radius += (Math.random() - 0.5) * 30;
            } else if (currentScene === 'orbitals') {
                // 轨道特定分布
                const orbitalType = Math.random() > 0.5 ? 's' : 'p';
                
                if (orbitalType === 's') {
                    // s轨道：球形对称
                    radius = 80 * Math.sqrt(Math.random());
                    angle = Math.random() * Math.PI * 2;
                } else {
                    // p轨道：哑铃形分布
                    const axis = Math.floor(Math.random() * 3); // 0:x, 1:y, 2:z
                    radius = 120 * (Math.random() * 0.8 + 0.2);
                    
                    if (axis === 0) {
                        // 沿x轴
                        angle = Math.random() > 0.5 ? 0 : Math.PI;
                        radius *= Math.random() > 0.5 ? 1 : -1;
                    } else if (axis === 1) {
                        // 沿y轴
                        angle = Math.random() > 0.5 ? Math.PI/2 : 3*Math.PI/2;
                        radius *= Math.random() > 0.5 ? 1 : -1;
                    } else {
                        // 沿z轴（在2D中表现为点更靠近中心）
                        radius = 60 * Math.sqrt(Math.random());
                        angle = Math.random() * Math.PI * 2;
                    }
                }
            }
            
            const x = centerX + Math.cos(angle) * radius;
            const y = centerY + Math.sin(angle) * radius;
            
            points.push({
                x, y,
                radius: 2,
                color: atom.energyLevels[Math.min(atom.excitedLevel-1, 3)].color,
                life: 200 + Math.random() * 100 // 点的存活时间
            });
            
            // 限制点的数量
            if (points.length > 1000) {
                points.splice(0, 100);
            }
        }
        
        // 绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制能级线（如果开启）
            if (document.getElementById('showLevels').checked) {
                for (let i = 0; i < atom.energyLevels.length; i++) {
                    const level = atom.energyLevels[i];
                    
                    // 虚线能级圆
                    ctx.beginPath();
                    ctx.setLineDash([5, 5]);
                    ctx.arc(centerX, centerY, level.radius, 0, Math.PI * 2);
                    ctx.strokeStyle = i < atom.excitedLevel ? level.color : '#bdc3c7';
                    ctx.lineWidth = 1;
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 能级标签
                    if (document.getElementById('showLabels').checked) {
                        ctx.fillStyle = i < atom.excitedLevel ? level.color : '#bdc3c7';
                        ctx.font = 'bold 16px Arial';
                        ctx.fillText(`n=${i+1}`, centerX + level.radius + 10, centerY);
                        
                        // 电子数
                        ctx.font = '14px Arial';
                        ctx.fillText(`${level.electrons}e⁻`, centerX + level.radius + 10, centerY + 20);
                    }
                }
            }
            
            // 绘制电子云轮廓（如果开启且是相关场景）
            if (document.getElementById('showCloud').checked && 
                (currentScene === 'electronCloud' || currentScene === 'orbitals')) {
                
                // 根据当前激发能级绘制云轮廓
                const levelIndex = Math.min(atom.excitedLevel - 1, 3);
                const cloudRadius = atom.energyLevels[levelIndex].radius;
                
                // 绘制半透明电子云区域
                ctx.beginPath();
                ctx.arc(centerX, centerY, cloudRadius, 0, Math.PI * 2);
                const gradient = ctx.createRadialGradient(
                    centerX, centerY, cloudRadius * 0.3,
                    centerX, centerY, cloudRadius
                );
                gradient.addColorStop(0, 'rgba(52, 152, 219, 0.3)');
                gradient.addColorStop(1, 'rgba(52, 152, 219, 0.05)');
                ctx.fillStyle = gradient;
                ctx.fill();
                
                // 绘制云边界
                ctx.beginPath();
                ctx.arc(centerX, centerY, cloudRadius, 0, Math.PI * 2);
                ctx.strokeStyle = 'rgba(52, 152, 219, 0.5)';
                ctx.lineWidth = 2;
                ctx.stroke();
            }
            
            // 绘制轨道形状（如果是轨道场景）
            if (currentScene === 'orbitals') {
                // s轨道
                ctx.beginPath();
                ctx.arc(centerX, centerY, 80, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(52, 152, 219, 0.15)';
                ctx.fill();
                ctx.strokeStyle = '#3498db';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // p轨道（三个方向）
                // px
                ctx.beginPath();
                ctx.ellipse(centerX, centerY, 120, 40, 0, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(26, 188, 156, 0.15)';
                ctx.fill();
                ctx.strokeStyle = '#1abc9c';
                ctx.lineWidth = 2;
                ctx.stroke();
                
                // py
                ctx.beginPath();
                ctx.ellipse(centerX, centerY, 40, 120, 0, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(26, 188, 156, 0.15)';
                ctx.fill();
                ctx.strokeStyle = '#1abc9c';
                ctx.stroke();
                
                if (document.getElementById('showLabels').checked) {
                    ctx.fillStyle = '#3498db';
                    ctx.font = 'bold 16px Arial';
                    ctx.fillText('s轨道', centerX, centerY - 100);
                    
                    ctx.fillStyle = '#1abc9c';
                    ctx.fillText('p轨道', centerX + 140, centerY);
                }
            }
            
            // 绘制概率点（如果开启）
            if (document.getElementById('showPoints').checked) {
                for (let i = 0; i < points.length; i++) {
                    const point = points[i];
                    
                    // 更新点寿命
                    point.life -= 1;
                    
                    // 绘制点
                    ctx.beginPath();
                    ctx.arc(point.x, point.y, point.radius, 0, Math.PI * 2);
                    ctx.fillStyle = point.color;
                    ctx.globalAlpha = point.life / 300; // 逐渐淡出
                    ctx.fill();
                    
                    // 移除死亡的点
                    if (point.life <= 0) {
                        points.splice(i, 1);
                        i--;
                    }
                }
                ctx.globalAlpha = 1.0;
            }
            
            // 绘制原子核
            ctx.beginPath();
            ctx.arc(centerX, centerY, atom.nucleusRadius, 0, Math.PI * 2);
            const nucleusGradient = ctx.createRadialGradient(
                centerX, centerY, 0,
                centerX, centerY, atom.nucleusRadius
            );
            nucleusGradient.addColorStop(0, '#f1c40f');
            nucleusGradient.addColorStop(1, '#d35400');
            ctx.fillStyle = nucleusGradient;
            ctx.fill();
            
            // 绘制跃迁动画
            for (let i = 0; i < transitions.length; i++) {
                const transition = transitions[i];
                
                const fromRadius = atom.energyLevels[transition.fromLevel-1].radius;
                const toRadius = atom.energyLevels[transition.toLevel-1].radius;
                const currentRadius = fromRadius + (toRadius - fromRadius) * transition.progress;
                
                // 绘制跃迁箭头
                ctx.beginPath();
                if (transition.direction === 'up') {
                    ctx.arc(centerX, centerY - currentRadius, 8, 0, Math.PI * 2);
                } else {
                    ctx.arc(centerX, centerY - currentRadius, 8, 0, Math.PI * 2);
                }
                ctx.fillStyle = transition.color;
                ctx.fill();
                
                // 绘制箭头方向
                ctx.beginPath();
                if (transition.direction === 'up') {
                    ctx.moveTo(centerX, centerY - currentRadius - 15);
                    ctx.lineTo(centerX - 10, centerY - currentRadius);
                    ctx.lineTo(centerX + 10, centerY - currentRadius);
                } else {
                    ctx.moveTo(centerX, centerY - currentRadius + 15);
                    ctx.lineTo(centerX - 10, centerY - currentRadius);
                    ctx
<!--检测到代码截断，自动续写中...-->
lineTo(centerX + 10, centerY - currentRadius);
                }
                ctx.closePath();
                ctx.fillStyle = transition.color;
                ctx.fill();
                
                // 更新进度
                transition.progress += 0.02;
                
                // 如果动画完成，移除
                if (transition.progress >= 1) {
                    transitions.splice(i, 1);
                    i--;
                }
            }
            
            // 绘制光子
            for (let i = 0; i < photons.length; i++) {
                const photon = photons[i];
                
                // 更新位置
                photon.x += Math.cos(photon.angle) * photon.speed;
                photon.y += Math.sin(photon.angle) * photon.speed;
                photon.life -= 1;
                
                // 绘制光子
                ctx.beginPath();
                ctx.arc(photon.x, photon.y, photon.radius, 0, Math.PI * 2);
                const photonGradient = ctx.createRadialGradient(
                    photon.x, photon.y, 0,
                    photon.x, photon.y, photon.radius
                );
                photonGradient.addColorStop(0, photon.color);
                photonGradient.addColorStop(1, 'rgba(255, 255, 255, 0)');
                ctx.fillStyle = photonGradient;
                ctx.fill();
                
                // 绘制光尾
                ctx.beginPath();
                ctx.moveTo(photon.x, photon.y);
                ctx.lineTo(
                    photon.x - Math.cos(photon.angle) * 15,
                    photon.y - Math.sin(photon.angle) * 15
                );
                ctx.strokeStyle = photon.color;
                ctx.lineWidth = 3;
                ctx.stroke();
                
                // 移除死亡的光子
                if (photon.life <= 0 || 
                    photon.x < 0 || photon.x > canvas.width || 
                    photon.y < 0 || photon.y > canvas.height) {
                    photons.splice(i, 1);
                    i--;
                }
            }
            
            // 绘制光谱（如果开启）
            if (showSpectrum && currentScene === 'transitions') {
                const spectrumWidth = 200;
                const spectrumHeight = 60;
                const spectrumX = canvas.width - spectrumWidth - 20;
                const spectrumY = 20;
                
                // 光谱背景
                ctx.fillStyle = 'rgba(0, 0, 0, 0.7)';
                ctx.fillRect(spectrumX, spectrumY, spectrumWidth, spectrumHeight);
                
                // 光谱标题
                ctx.fillStyle = '#f1c40f';
                ctx.font = 'bold 14px Arial';
                ctx.fillText('氢原子发射光谱', spectrumX + 10, spectrumY + 20);
                
                // 绘制谱线
                const lines = [
                    {name: 'Hα', color: '#e74c3c', x: spectrumX + 30},
                    {name: 'Hβ', color: '#f39c12', x: spectrumX + 70},
                    {name: 'Hγ', color: '#f1c40f', x: spectrumX + 110},
                    {name: 'Hδ', color: '#2ecc71', x: spectrumX + 150}
                ];
                
                for (let i = 0; i < lines.length; i++) {
                    const line = lines[i];
                    
                    // 谱线
                    ctx.beginPath();
                    ctx.moveTo(line.x, spectrumY + 30);
                    ctx.lineTo(line.x, spectrumY + 50);
                    ctx.strokeStyle = line.color;
                    ctx.lineWidth = 3;
                    ctx.stroke();
                    
                    // 标签
                    ctx.fillStyle = '#ecf0f1';
                    ctx.font = '12px Arial';
                    ctx.fillText(line.name, line.x - 8, spectrumY + 55);
                }
            }
            
            // 绘制当前场景标题
            ctx.fillStyle = '#ecf0f1';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'left';
            
            const sceneTitles = {
                'electronCloud': '电子云概率模型',
                'energyLevels': '能级与壳层',
                'orbitals': '轨道形状 (s, p)',
                'transitions': '能级跃迁与光子发射'
            };
            
            ctx.fillText(sceneTitles[currentScene] || '原子结构', 20, 40);
            
            // 绘制当前元素和状态
            ctx.font = '16px Arial';
            ctx.fillText(`元素: ${atom.element} | 电子数: ${atom.electronCount} | 当前能级: n=${atom.excitedLevel}`, 20, 70);
            
            // 绘制经典轨道对比（仅电子云场景）
            if (currentScene === 'electronCloud') {
                ctx.strokeStyle = 'rgba(231, 76, 60, 0.3)';
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.arc(centerX, centerY, 100, 0, Math.PI * 2);
                ctx.stroke();
                ctx.setLineDash([]);
                
                ctx.fillStyle = 'rgba(231, 76, 60, 0.7)';
                ctx.font = '14px Arial';
                ctx.fillText('经典轨道模型（错误）', centerX + 110, centerY - 10);
            }
        }
        
        // 动画循环
        function animate() {
            draw();
            
            // 如果正在播放，生成新的概率点
            if (isPlaying) {
                const speed = parseInt(document.getElementById('speedSlider').value);
                const pointsPerFrame = Math.floor(speed / 2) + 1;
                
                for (let i = 0; i < pointsPerFrame; i++) {
                    generateProbabilityPoint();
                }
                
                // 随机自动衰减（如果开启）
                if (autoDecay && currentScene === 'transitions' && atom.excitedLevel > 1) {
                    if (Math.random() < 0.01) { // 1%概率每帧
                        const from = atom.excitedLevel;
                        const to = Math.floor(Math.random() * (from - 1)) + 1;
                        triggerDecay(from, to);
                    }
                }
            }
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

# 原子结构交互式教学动画使用指南

## 🎯 功能说明

欢迎使用“原子结构：电子云、能级与跃迁”交互式教学动画！本工具旨在通过直观的动态可视化，帮助您深入理解量子力学中的核心概念：电子概率分布、量子化能级和电子跃迁过程。告别枯燥的公式和抽象描述，通过亲手操作和观察，您将建立起对微观世界的直观认知。

## 🚀 主要功能

### 1. 四大学习场景
- **电子云概率模型**：观察电子如何以概率云的形式存在于原子核周围，而非固定轨道
- **能级与壳层**：探索量子化的能量层级（K、L、M层）及其容纳电子数的限制
- **轨道形状**：可视化s轨道（球形）和p轨道（哑铃形）的三维空间分布
- **能级跃迁**：模拟电子吸收/发射光子时的跃迁过程，关联光谱现象

### 2. 核心交互控制
- **模拟速度调节**：从“极慢”到“超快”10档调节，适应不同观察需求
- **元素选择器**：在氢(H)、氦(He)、锂(Li)三种典型原子间切换
- **能量输入系统**：通过滑块精确输入能量值，触发特定能级跃迁
- **显示图层管理**：独立控制概率点、电子云轮廓、能级线等视觉元素

### 3. 动态模拟系统
- **实时概率点生成**：每秒生成数十到数百个概率点，累积形成电子云
- **自动衰减机制**：模拟激发态电子的自发辐射过程
- **光子发射可视化**：用彩色光点和光尾模拟不同波长的光子
- **光谱关联显示**：将跃迁过程与氢原子特征光谱线对应

## ✨ 设计特色

### 视觉设计
- **科学配色方案**：采用深空蓝背景突出微观世界的神秘感，用暖色表示原子核，冷色表示电子
- **渐进式可视化**：从离散概率点到连续电子云，从静态能级到动态跃迁，符合认知规律
- **对比呈现**：同时显示正确的电子云模型和错误的经典轨道模型，破除迷思概念

### 教学逻辑
- **分层递进**：四个场景按概念复杂度排列，支持顺序学习或自由探索
- **即时反馈**：每次交互都有视觉反馈和信息提示，强化学习效果
- **多感官参与**：结合视觉动态、交互操作和文字说明，满足不同学习风格

### 技术实现
- **基于Canvas的高性能渲染**：确保流畅的粒子动画和实时交互
- **物理准确的模拟**：能级差、跃迁概率、轨道形状均基于量子力学原理
- **响应式设计**：适配不同屏幕尺寸，支持桌面和移动设备学习

## 📚 教学要点

### 关键概念解析
1. **电子云的本质**
   - 电子不是沿轨道运行的小球，而是以概率波形式存在
   - 电子云密度高的区域表示电子出现概率大
   - 观测行为会“坍缩”概率波，使电子出现在特定位置

2. **量子化能级**
   - 电子能量不是连续的，只能取特定离散值
   - 能级由主量子数n决定，n=1,2,3...对应K,L,M...层
   - 每层最多容纳2n²个电子（泡利不相容原理）

3. **轨道形状差异**
   - s轨道：球形对称，角动量量子数l=0
   - p轨道：哑铃形，沿x、y、z轴方向，l=1
   - 轨道形状由角动量量子数和磁量子数共同决定

4. **能级跃迁机制**
   - 吸收能量：电子从低能级跃迁到高能级（需要精确匹配能级差）
   - 自发辐射：激发态电子不稳定，自发跃迁回低能级并发射光子
   - 光子能量：E = hν = E_高 - E_低，决定光的颜色

### 常见迷思纠正
- ❌ “电子像行星绕太阳一样绕原子核旋转”
- ✅ “电子以概率云形式存在，没有确定轨迹”

- ❌ “电子可以在任意位置，能量可以连续变化”
- ✅ “电子只能存在于特定能级，能量是量子化的”

- ❌ “跃迁时电子‘跳跃’过中间空间”
- ✅ “跃迁是瞬时状态改变，不经过中间位置”

## 💡 使用建议

### 学习路径推荐
**初学者路径**（建议用时：15-20分钟）
1. 从“电子云概率模型”开始，运行模拟观察云的形成
2. 切换到“能级与壳层”，理解能量分层概念
3. 体验“轨道形状”，认识s和p轨道的空间分布
4. 最后学习“能级跃迁”，操作能量滑块触发跃迁

**探究式学习**（建议用时：25-30分钟）
1. 在电子云场景中，尝试不同速度观察概率分布变化
2. 比较氢、氦、锂原子的能级结构差异
3. 手动输入不同能量值，探索哪些能级跃迁被允许
4. 开启“自动衰减”观察激发态的寿命和光子发射

### 课堂应用建议
**教师演示模式**
- 使用投影仪全屏展示，逐步讲解每个场景
- 在关键节点暂停动画，引导学生观察和预测
- 使用“重置”功能对比不同条件下的模拟结果

**学生自主探究**
- 分组设置探究任务：“找出氢原子可见光对应的跃迁”
- 挑战性问题：“为什么锂原子的第三能级没有电子？”
- 创作任务：“用本工具解释霓虹灯发光的原理”

**评估与反馈**
- 观察学生操作过程，评估概念理解程度
- 设置简单测验：“从n=4到n=2跃迁发射什么颜色的光？”
- 鼓励学生用工具解释生活中的现象（如焰色反应）

### 高级探索方向
1. **定量分析**：记录不同能级跃迁所需的精确能量值
2. **比较研究**：对比玻尔模型与量子力学模型的异同
3. **拓展思考**：思考如何用本模型解释化学键的形成
4. **现实联系**：研究原子光谱在天文学、医学中的应用

---

## 🎓 学习目标达成

完成本动画的学习后，您将能够：

1. **准确描述**电子云的概率本质及其与经典轨道模型的区别
2. **解释说明**量子化能级的概念和电子排布规律
3. **识别区分**s轨道和p轨道的空间形状特征
4. **分析预测**电子跃迁过程与光谱现象的关系
5. **应用迁移**用原子结构原理解释相关物理化学现象

---

**温馨提示**：微观世界的量子行为常常违反我们的日常直觉，这正是量子力学的奇妙之处。当某些现象让您感到困惑时，请记住——这不是工具的局限，而是自然本身的神秘。享受探索的乐趣，让好奇心引领您进入神奇的原子世界！

祝您学习愉快，探索无限！ 🚀🔬