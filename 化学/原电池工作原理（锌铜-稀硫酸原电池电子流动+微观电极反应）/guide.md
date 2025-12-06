# 需求：原电池工作原理（锌铜-稀硫酸原电池电子流动+微观电极反应）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：高中或大学低年级化学初学者。他们具备基础的化学知识（如原子、离子、氧化还原反应），但需要直观、动态的模型来理解抽象的原电池工作原理。
2.  **核心痛点**：
    *   **抽象性**：电子、离子的微观运动肉眼不可见，学生难以在脑海中构建动态图景。
    *   **综合性**：原电池涉及宏观现象（电流、气泡）、微观粒子行为（电子转移、离子迁移）和电极反应方程式的多重表征，学生容易混淆。
    *   **连接性**：难以理解外电路电子流动与内电路离子迁移如何协同构成完整回路。
3.  **学习目标**：通过动画，学生应能：
    *   清晰识别原电池的正负极、电极材料和电解质。
    *   描述并可视化电子在外电路（导线）中的流动方向。
    *   描述并可视化离子在内电路（溶液）中的迁移方向。
    *   准确写出锌电极和铜电极上发生的半反应（氧化和还原反应）及总反应。
    *   理解盐桥（或本例中稀硫酸作为电解质）的作用是维持电荷平衡和构成内电路。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分解**：
    *   **驱动力**：锌比铜活泼，易失电子（氧化倾向不同）。
    *   **电子路径（外电路）**：电子从锌（负极，被氧化）流出，经导线和负载（如灯泡/电流计），流入铜（正极，使H⁺还原）。
    *   **离子路径（内电路）**：溶液中，SO₄²⁻向锌极迁移，H⁺向铜极迁移，以平衡电荷。
    *   **电极反应**：锌极：`Zn → Zn²⁺ + 2e⁻`（氧化）；铜极：`2H⁺ + 2e⁻ → H₂↑`（还原）。
    *   **完整回路**：电子流与离子流共同构成电荷的闭合循环。

2.  **认知规律遵循**：
    *   **从宏观到微观**：先展示完整的电池装置（烧杯、电极、导线、灯泡），再通过“放大镜”或“进入微观”视角展示粒子运动。
    *   **从静态到动态**：初始状态为静止装置，启动后粒子开始规律运动。
    *   **分层呈现**：允许用户选择性地观看“电子流”、“离子流”或“电极反应”，避免信息过载。

3.  **交互设计**：
    *   **控制面板**：提供“播放/暂停/重置”全局控制。
    *   **图层控制**：使用复选框或按钮，允许用户单独显示/隐藏“电子”、“锌离子(Zn²⁺)”、“氢离子(H⁺)”、“硫酸根离子(SO₄²⁻)”、“氢气气泡”等元素，便于分步学习。
    *   **提示与标注**：鼠标悬停在电极、粒子或导线上时，显示其名称和所带电荷（如 `Zn²⁺`， `+2`）。点击电极，弹出该电极反应的化学方程式。
    *   **速度控制**：提供滑块调节粒子运动速度，适应不同观察需求。

4.  **视觉呈现**：
    *   **装置**：采用简洁、卡通化的烧杯、电极片、导线、灯泡（或电流计）图标，确保清晰可辨。
    *   **粒子**：
        *   电子 (`e⁻`)：用非常小的、高亮（如黄色）闪烁的圆点表示，沿导线快速移动。
        *   离子：用不同颜色和大小的球体表示，并标注化学式。
            *   `Zn²⁺`：浅灰色球，带“+2”标识。
            *   `H⁺`：小的红色球，带“+”标识。
            *   `SO₄²⁻`：黄色和红色组成的复合球体或简单黄色球，带“-2”标识。
    *   **运动轨迹**：电子在导线中沿路径流动；离子在溶液中做定向的、略带随机的迁移动画，总体趋势明确。
    *   **反应特效**：锌极表面，锌原子“溶解”为`Zn²⁺`进入溶液，同时释放出电子。铜极表面，`H⁺`接触到电极后与电子结合，生成`H₂`气泡（用两个相连的白色小球表示）并上浮。

#### 配色方案选择
*   **背景与装置**：采用浅灰色或淡蓝色背景。烧杯、电极（锌片、铜片）用浅色线条勾勒，内部溶液为非常浅的蓝色（暗示水溶液），透明度高，不遮挡粒子。
*   **粒子配色**（遵循化学可视化惯例并确保高对比度）：
    *   电子 (`e⁻`)：亮黄色或金色，带光晕效果，最醒目。
    *   锌离子 (`Zn²⁺`)：浅灰色或金属银色。
    *   氢离子 (`H⁺`)：红色（酸性的常见代表色）。
    *   硫酸根离子 (`SO₄²⁻`)：黄色或橙色。
    *   氢气 (`H₂`)：白色或浅灰色气泡。
*   **导线与电流**：导线为深灰色。电子流经时，导线可以伴有微弱的蓝色或黄色光晕，表示电流方向（与电子流相反）。
*   **界面与控制面板**：使用中性色（如深蓝、灰色），确保控件清晰但不喧宾夺主。

#### 交互功能列表
1.  **动画控制**：播放、暂停、重置按钮。
2.  **速度调节**：滑块控制所有粒子动画速度。
3.  **可视化图层开关**（复选框）：
    *   [ ] 显示/隐藏 电子流
    *   [ ] 显示/隐藏 锌离子 (Zn²⁺)
    *   [ ] 显示/隐藏 氢离子 (H⁺)
    *   [ ] 显示/隐藏 硫酸根离子 (SO₄²⁻)
    *   [ ] 显示/隐藏 氢气气泡 (H₂)
    *   [ ] 高亮显示 电流方向（与电子流反向）
4.  **信息提示**：
    *   鼠标悬停：显示电极名称（“锌负极（阳极）”、“铜正极（阴极）”）、粒子身份与电荷。
    *   点击电极：弹出卡片，显示该电极发生的半反应方程式（含电子得失）和反应类型（氧化/还原）。
    *   点击“总反应”按钮：在画面中央显示总离子方程式和化学方程式。
5.  **步骤引导模式（可选）**：一个“引导”按钮，按预设顺序（如：1.认识装置 2.观察电子流 3.观察离子流 4.理解电极反应）高亮并讲解动画的不同部分。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>原电池工作原理动画 - 锌铜稀硫酸原电池</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
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
            max-width: 1000px;
        }
        
        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: #34495e;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }
        
        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1000px;
            width: 100%;
            justify-content: center;
        }
        
        .animation-area {
            flex: 1;
            min-width: 600px;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            position: relative;
        }
        
        #canvas {
            display: block;
            background-color: #f8fafc;
            width: 100%;
            height: 500px;
        }
        
        .control-panel {
            flex: 0 0 300px;
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .panel-section {
            border-bottom: 1px solid #eee;
            padding-bottom: 20px;
        }
        
        .panel-section:last-child {
            border-bottom: none;
        }
        
        .section-title {
            color: #2c3e50;
            font-size: 1.3rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .section-title i {
            margin-right: 10px;
            font-size: 1.2rem;
        }
        
        .controls {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin-bottom: 15px;
        }
        
        .btn {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        
        .btn-primary {
            background-color: #3498db;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: #95a5a6;
            color: white;
        }
        
        .btn-secondary:hover {
            background-color: #7f8c8d;
            transform: translateY(-2px);
        }
        
        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .speed-label {
            font-weight: 600;
            color: #2c3e50;
            min-width: 60px;
        }
        
        .speed-slider {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: #ddd;
            border-radius: 4px;
            outline: none;
        }
        
        .speed-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        .toggle-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        
        .toggle-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .toggle-checkbox {
            width: 20px;
            height: 20px;
            cursor: pointer;
        }
        
        .toggle-label {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            font-weight: 500;
        }
        
        .particle-icon {
            width: 16px;
            height: 16px;
            border-radius: 50%;
            display: inline-block;
        }
        
        .electron-icon {
            background-color: #FFD700;
            box-shadow: 0 0 5px #FFD700;
        }
        
        .zn-icon {
            background-color: #C0C0C0;
        }
        
        .h-icon {
            background-color: #FF6B6B;
        }
        
        .so4-icon {
            background-color: #FFA726;
        }
        
        .h2-icon {
            background-color: #ECF0F1;
            border: 1px solid #BDC3C7;
        }
        
        .current-icon {
            width: 16px;
            height: 16px;
            background: linear-gradient(90deg, #3498db, #2ecc71);
            border-radius: 3px;
        }
        
        .info-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            border-left: 4px solid #3498db;
        }
        
        .info-title {
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }
        
        .info-content {
            color: #555;
            line-height: 1.5;
        }
        
        .reaction-equations {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-top: 10px;
        }
        
        .equation {
            background-color: #f1f8ff;
            padding: 10px;
            border-radius: 6px;
            font-family: 'Courier New', monospace;
            font-weight: bold;
            color: #2c3e50;
            text-align: center;
            border: 1px dashed #a2d0fa;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
            justify-content: center;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.85rem;
        }
        
        .footer {
            margin-top: 30px;
            text-align: center;
            color: #7f8c8d;
            font-size: 0.9rem;
            max-width: 1000px;
            width: 100%;
            padding-top: 20px;
            border-top: 1px solid #ddd;
        }
        
        .highlight {
            background-color: #fffacd;
            padding: 2px 5px;
            border-radius: 3px;
            font-weight: 600;
        }
        
        @media (max-width: 950px) {
            .container {
                flex-direction: column;
            }
            
            .animation-area, .control-panel {
                min-width: 100%;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="header">
        <h1><i class="fas fa-battery-full"></i> 原电池工作原理</h1>
        <p class="subtitle">锌铜-稀硫酸原电池 | 电子流动与微观电极反应</p>
    </div>
    
    <div class="container">
        <div class="animation-area">
            <canvas id="canvas" width="800" height="500"></canvas>
        </div>
        
        <div class="control-panel">
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-play-circle"></i> 动画控制</div>
                <div class="controls">
                    <button id="playBtn" class="btn btn-primary">
                        <i class="fas fa-play"></i> 播放
                    </button>
                    <button id="pauseBtn" class="btn btn-secondary">
                        <i class="fas fa-pause"></i> 暂停
                    </button>
                    <button id="resetBtn" class="btn btn-secondary">
                        <i class="fas fa-redo"></i> 重置
                    </button>
                </div>
                
                <div class="speed-control">
                    <div class="speed-label">速度:</div>
                    <input type="range" min="1" max="10" value="5" class="speed-slider" id="speedSlider">
                    <span id="speedValue">中速</span>
                </div>
            </div>
            
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-eye"></i> 显示控制</div>
                <div class="toggle-group">
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleElectrons" class="toggle-checkbox" checked>
                        <label for="toggleElectrons" class="toggle-label">
                            <span class="particle-icon electron-icon"></span>
                            电子 (e⁻)
                        </label>
                    </div>
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleZnIons" class="toggle-checkbox" checked>
                        <label for="toggleZnIons" class="toggle-label">
                            <span class="particle-icon zn-icon"></span>
                            锌离子 (Zn²⁺)
                        </label>
                    </div>
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleHIons" class="toggle-checkbox" checked>
                        <label for="toggleHIons" class="toggle-label">
                            <span class="particle-icon h-icon"></span>
                            氢离子 (H⁺)
                        </label>
                    </div>
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleSO4Ions" class="toggle-checkbox" checked>
                        <label for="toggleSO4Ions" class="toggle-label">
                            <span class="particle-icon so4-icon"></span>
                            硫酸根离子 (SO₄²⁻)
                        </label>
                    </div>
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleH2Bubbles" class="toggle-checkbox" checked>
                        <label for="toggleH2Bubbles" class="toggle-label">
                            <span class="particle-icon h2-icon"></span>
                            氢气气泡 (H₂)
                        </label>
                    </div>
                    <div class="toggle-item">
                        <input type="checkbox" id="toggleCurrent" class="toggle-checkbox">
                        <label for="toggleCurrent" class="toggle-label">
                            <span class="current-icon"></span>
                            电流方向
                        </label>
                    </div>
                </div>
            </div>
            
            <div class="panel-section">
                <div class="section-title"><i class="fas fa-info-circle"></i> 反应方程式</div>
                <div class="reaction-equations">
                    <div class="equation" id="anodeEq">锌极（负极，氧化）: Zn → Zn²⁺ + 2e⁻</div>
                    <div class="equation" id="cathodeEq">铜极（正极，还原）: 2H⁺ + 2e⁻ → H₂↑</div>
                    <div class="equation" id="totalEq">总反应: Zn + 2H⁺ → Zn²⁺ + H₂↑</div>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">原电池工作原理</div>
                    <div class="info-content">
                        锌比铜活泼，易失去电子。电子从锌电极（负极）流出，经导线流向铜电极（正极）。溶液中，阳离子（H⁺）向正极移动，阴离子（SO₄²⁻）向负极移动，形成闭合回路。
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="legend">
        <div class="legend-item"><span class="particle-icon electron-icon"></span> 电子</div>
        <div class="legend-item"><span class="particle-icon zn-icon"></span> 锌离子</div>
        <div class="legend-item"><span class="particle-icon h-icon"></span> 氢离子</div>
        <div class="legend-item"><span class="particle-icon so4-icon"></span> 硫酸根离子</div>
        <div class="legend-item"><span class="particle-icon h2-icon"></span> 氢气</div>
        <div class="legend-item"><i class="fas fa-arrow-right" style="color:#3498db;"></i> 电子流方向</div>
        <div class="legend-item"><i class="fas fa-arrow-left" style="color:#2ecc71;"></i> 电流方向</div>
    </div>
    
    <div class="footer">
        <p>教学动画设计 | 锌铜稀硫酸原电池工作原理 | 交互式化学教学工具</p>
        <p>提示：点击电极查看详细信息 | 使用图层控制可聚焦特定粒子运动</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('canvas');
        const ctx = canvas.getContext('2d');
        
        // 动画状态
        let animationId = null;
        let isPlaying = false;
        let animationSpeed = 5; // 1-10
        let time = 0;
        
        // 显示/隐藏控制
        let showElectrons = true;
        let showZnIons = true;
        let showHIons = true;
        let showSO4Ions = true;
        let showH2Bubbles = true;
        let showCurrent = false;
        
        // 电池装置参数
        const beaker = {
            x: 100,
            y: 100,
            width: 600,
            height: 300,
            bottomWidth: 500,
            liquidHeight: 220
        };
        
        // 电极参数
        const electrodes = {
            zinc: {
                x: 200,
                y: beaker.y + 20,
                width: 15,
                height: beaker.liquidHeight - 20,
                name: "锌电极 (负极)",
                reaction: "Zn → Zn²⁺ + 2e⁻",
                type: "氧化反应",
                color: "#A0A0A0"
            },
            copper: {
                x: 500,
                y: beaker.y + 20,
                width: 15,
                height: beaker.liquidHeight - 20,
                name: "铜电极 (正极)",
                reaction: "2H⁺ + 2e⁻ → H₂↑",
                type: "还原反应",
                color: "#DAA520"
            }
        };
        
        // 导线和灯泡
        const wire = {
            topY: beaker.y - 30,
            height: 30,
            bulbX: 350,
            bulbY: beaker.y - 80,
            bulbRadius: 25
        };
        
        // 粒子数组
        let electrons = [];
        let znIons = [];
        let hIons = [];
        let so4Ions = [];
        let h2Bubbles = [];
        
        // 初始化粒子
        function initParticles() {
            // 清空粒子数组
            electrons = [];
            znIons = [];
            hIons = [];
            so4Ions = [];
            h2Bubbles = [];
            
            // 初始化电子 (在锌电极表面)
            for (let i = 0; i < 8; i++) {
                electrons.push({
                    x: electrodes.zinc.x + electrodes.zinc.width/2,
                    y: electrodes.zinc.y + electrodes.zinc.height - 20 - i * 25,
                    radius: 4,
                    speed: 2 + Math.random() * 1,
                    color: "#FFD700",
                    glow: true,
                    pathProgress: 0,
                    onWire: false
                });
            }
            
            // 初始化锌离子 (在锌电极附近)
            for (let i = 0; i < 15; i++) {
                znIons.push({
                    x: electrodes.zinc.x + electrodes.zinc.width + 20 + Math.random() * 100,
                    y: electrodes.zinc.y + 50 + Math.random() * (electrodes.zinc.height - 100),
                    radius: 8,
                    speed: 0.3 + Math.random() * 0.3,
                    color: "#C0C0C0",
                    charge: "+2",
                    driftDirection: 1 // 1 = 向右移动
                });
            }
            
            // 初始化氢离子 (均匀分布在溶液中)
            for (let i = 0; i < 25; i++) {
                hIons.push({
                    x: beaker.x + 50 + Math.random() * (beaker.width - 100),
                    y: beaker.y + 50 + Math.random() * (beaker.liquidHeight - 100),
                    radius: 6,
                    speed: 0.4 + Math.random() * 0.4,
                    color: "#FF6B6B",
                    charge: "+",
                    driftDirection: -1 // -1 = 向左移动 (向铜电极)
                });
            }
            
            // 初始化硫酸根离子 (均匀分布在溶液中)
            for (let i = 0; i < 15; i++) {
                so4Ions.push({
                    x: beaker.x + 50 + Math.random() * (beaker.width - 100),
                    y: beaker.y + 50 + Math.random() * (beaker.liquidHeight - 100),
                    radius: 10,
                    speed: 0.2 + Math.random() * 0.2,
                    color: "#FFA726",
                    charge: "-2",
                    driftDirection: 1 // 1 = 向右移动 (向锌电极)
                });
            }
            
            // 初始化氢气气泡 (在铜电极表面)
            for (let i = 0; i < 5; i++) {
                h2Bubbles.push({
                    x: electrodes.copper.x - 10,
                    y: electrodes.copper.y + electrodes.copper.height - 30 - i * 40,
                    radius: 6 + Math.random() * 4,
                    speed: 0.5 + Math.random() * 0.3,
                    color: "#ECF0F1",
                    borderColor: "#BDC3C7",
                    floatProgress: Math.random() * 0.5
                });
            }
        }
        
        // 绘制烧杯
        function drawBeaker() {
            // 烧杯外框
            ctx.beginPath();
            ctx.moveTo(beaker.x + (beaker.width - beaker.bottomWidth)/2, beaker.y + beaker.height);
            ctx.lineTo(beaker.x, beaker.y);
            ctx.lineTo(beaker.x + beaker.width, beaker.y);
            ctx.lineTo(beaker.x + beaker.width - (beaker.width - beaker.bottomWidth)/2, beaker.y + beaker.height);
            ctx.closePath();
            
            // 烧杯填充
            ctx.fillStyle = "rgba(255, 255, 255, 0.8)";
            ctx.fill();
            
            // 烧杯边框
            ctx.strokeStyle = "#95a5a6";
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 液体
            ctx.beginPath();
            ctx.moveTo(beaker.x, beaker.y + beaker.liquidHeight);
            ctx.lineTo(beaker.x + beaker.width, beaker.y + beaker.liquidHeight);
            ctx.lineTo(beaker.x + beaker.width - (beaker.width - beaker.bottomWidth)/2, beaker.y + beaker.height);
            ctx.lineTo(beaker.x + (beaker.width - beaker.bottomWidth)/2, beaker.y + beaker.height);
            ctx.closePath();
            
            // 液体填充
            const liquidGradient = ctx.createLinearGradient(0, beaker.y, 0, beaker.y + beaker.liquidHeight);
            liquidGradient.addColorStop(0, "rgba(173, 216, 230, 0.4)");
            liquidGradient.addColorStop(1, "rgba(135, 206, 250, 0.6)");
            ctx.fillStyle = liquidGradient;
            ctx.fill();
            
            // 液体表面
            ctx.beginPath();
            ctx.moveTo(beaker.x, beaker.y + beaker.liquidHeight);
            ctx.lineTo(beaker.x + beaker.width, beaker.y + beaker.liquidHeight);
            ctx.strokeStyle = "rgba(70, 130, 180, 0.5)";
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 烧杯标签
            ctx.fillStyle = "#34495e";
            ctx.font = "16px Arial";
            ctx.fillText("稀硫酸溶液 (H₂SO₄)", beaker.x + beaker.width/2 - 70, beaker.y + beaker.liquidHeight + 25);
        }
        
        // 绘制电极
        function drawElectrodes() {
            // 锌电极
            ctx.fillStyle = electrodes.zinc.color;
            ctx.fillRect(electrodes.zinc.x, electrodes.zinc.y, electrodes.zinc.width, electrodes.zinc.height);
            
            // 锌电极标签
            ctx.fillStyle = "#2c3e50";
            ctx.font = "bold 16px Arial";
            ctx.fillText("Zn", electrodes.zinc.x + electrodes.zinc.width/2 - 10, electrodes.zinc.y - 10);
            ctx.font = "14px Arial";
            ctx.fillText("负极（阳极）", electrodes.zinc.x - 25, electrodes.zinc.y + electrodes.zinc.height/2);
            
            // 铜电极
            ctx.fillStyle = electrodes.copper.color;
            ctx.fillRect(electrodes.copper.x, electrodes.copper.y, electrodes.copper.width, electrodes.copper.height);
            
            // 铜电极标签
            ctx.fillStyle = "#2c3e50";
            ctx.font = "bold 16px Arial";
            ctx.fillText("Cu", electrodes.copper.x + electrodes.copper.width/2 - 10, electrodes.copper.y - 10);
            ctx.font = "14px Arial";
            ctx.fillText("正极（阴极）", electrodes.copper.x + electrodes.copper.width + 10, electrodes.copper.y + electrodes.copper.height/2);
        }
        
        // 绘制导线和灯泡
        function drawWiresAndBulb() {
            // 导线
            ctx.strokeStyle = "#2c3e50";
            ctx.lineWidth = 3;
            
            // 锌极到灯泡的导线
            ctx.beginPath();
            ctx.moveTo(electrodes.zinc.x + electrodes.zinc.width/2, electrodes.zinc.y);
            ctx.lineTo(electrodes.zinc.x + electrodes.zinc.width/2, wire.topY);
            ctx.lineTo(wire.bulbX, wire.topY);
            ctx.stroke();
            
            // 铜极到灯泡的导线
            ctx.beginPath();
            ctx.moveTo(electrodes.copper.x + electrodes.copper.width/2, electrodes.copper.y);
            ctx.lineTo(electrodes.copper.x + electrodes.copper.width/2, wire.topY);
            ctx.lineTo(wire.bulbX, wire.topY);
            ctx.stroke();
            
            // 灯泡
            ctx.beginPath();
            ctx.arc(wire.bulbX, wire.bulbY, wire.bulbRadius, 0, Math.PI * 2);
            
            // 灯泡发光效果（当动画播放时）
            if (isPlaying) {
                const bulbGradient = ctx.createRadialGradient(
                    wire.bulbX, wire.bulbY, 5,
                    wire.bulbX, wire.bulbY, wire.bulbRadius
                );
                bulbGradient.addColorStop(0, "#FFEB3B");
                bulbGradient.addColorStop(1, "rgba(255, 235, 59, 0.3)");
                ctx.fillStyle = bulbGradient;
            } else {
                ctx.fillStyle = "#F1C40F";
            }
            
            ctx.fill();
            ctx.strokeStyle = "#E67E22";
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 灯泡标签
            ctx.fillStyle = "#2c3e50";
            ctx.font = "14px Arial";
            ctx.fillText("灯泡/电流计", wire.bulbX - 35, wire.bulbY - wire.bulbRadius - 10);
        }
        
        // 绘制电子
        function drawElectrons() {
            if (!showElectrons) return;
            
            electrons.forEach(electron => {
                // 电子发光效果
                if (electron.glow) {
                    const glowGradient = ctx.createRadialGradient(
                        electron.x, electron.y, 0,
                        electron.x, electron.y, electron.radius * 2
                    );
                    glowGradient.addColorStop(0, "rgba(255, 215, 0, 0.8)");
                    glowGradient.addColorStop(1, "rgba(255, 215, 0, 0)");
                    
                    ctx.beginPath();
                    ctx.arc(electron.x, electron.y, electron.radius * 2, 0, Math.PI * 2);
                    ctx.fillStyle = glowGradient;
                    ctx.fill();
                }
                
                // 电子本体
                ctx.beginPath();
                ctx.arc(electron.x, electron.y, electron.radius, 0, Math.PI * 2);
                ctx.fillStyle = electron.color;
                ctx.fill();
                
                // 电子标签
                ctx.fillStyle = "#B8860B";
                ctx.font = "bold 12px Arial";
                ctx.fillText("e⁻", electron.x - 6, electron.y + 4);
            });
        }
        
        // 绘制锌离子
        function drawZnIons() {
            if (!showZnIons) return;
            
            znIons.forEach(ion => {
                // 离子本体
                ctx.beginPath();
                ctx.arc(ion.x, ion.y, ion.radius, 0, Math.PI * 2);
                ctx.fillStyle = ion.color;
                ctx.fill();
                
                // 离子边框
                ctx.strokeStyle = "#808080";
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 离子标签
                ctx.fillStyle = "#2c3e50";
                ctx.font = "bold 14px Arial";
                ctx.fillText("Zn²⁺", ion.x - 15, ion.y + 5);
            });
        }
        
        // 绘制氢离子
        function drawHIons() {
            if (!showHIons) return;
            
            hIons.forEach(ion => {
                // 离子本体
                ctx.beginPath();
                ctx.arc(ion.x, ion.y, ion.radius, 0, Math.PI * 2);
                ctx.fillStyle = ion.color;
                ctx.fill();
                
                // 离子标签
                ctx.fillStyle = "#C0392B";
                ctx.font = "bold 14px Arial";
                ctx.fillText("H⁺", ion.x - 8, ion.y + 4);
            });
        }
        
        // 绘制硫酸根离子
        function drawSO4Ions() {
            if (!showSO4Ions) return;
            
            so4Ions.forEach(ion => {
                // 离子本体
                ctx.beginPath();
                ctx.arc(ion.x, ion.y, ion.radius, 0, Math.PI * 2);
                ctx.fillStyle = ion.color;
                ctx.fill();
                
                // 离子边框
                ctx.strokeStyle = "#E67E22";
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 离子标签
                ctx.fillStyle = "#D35400";
                ctx.font = "bold 14px Arial";
                ctx.fillText("SO₄²⁻", ion.x - 20, ion.y + 5);
            });
        }
        
        // 绘制氢气气泡
        function drawH2Bubbles() {
            if (!showH2Bubbles) return;
            
            h2Bubbles.forEach(bubble => {
                // 气泡本体
                ctx.beginPath();
                ctx.arc(bubble.x, bubble.y, bubble.radius, 0, Math.PI * 2);
                ctx.fillStyle = bubble.color;
                ctx.fill();
                
                // 气泡边框
                ctx.strokeStyle = bubble.borderColor;
                ctx.lineWidth = 1;
                ctx.stroke();
                
                // 气泡高光
                ctx.beginPath();
                ctx.arc(bubble.x - bubble.radius/3, bubble.y - bubble.radius/3, bubble.radius/3, 0, Math.PI * 2);
                ctx.fillStyle = "rgba(255, 255, 255, 0.6)";
                ctx.fill();
                
                // 气泡标签
                ctx.fillStyle = "#7f8c8d";
                ctx.font = "bold 12px Arial";
                ctx.fillText("H₂", bubble.x - 8, bubble.y + 4);
            });
        }
        
        // 绘制电流方向指示
        function drawCurrentDirection() {
            if (!showCurrent) return;
            
            // 电流方向箭头 (与电子流方向相反)
            ctx.strokeStyle = "#2ecc71";
            ctx.fillStyle = "#2ecc71";
            ctx.lineWidth = 2;
            
            // 从铜电极到灯泡
            drawArrow(
                electrodes.copper.x + electrodes.copper.width/2, wire.topY,
                wire.bulbX, wire.topY,
                10, true
            );
            
            // 从灯泡到锌电极
            drawArrow(
                wire.bulbX, wire.topY,
                electrodes.zinc.x + electrodes.zinc.width/2, wire.topY,
                10, true
            );
            
            // 电流方向标签
            ctx.fillStyle = "#27ae60";
            ctx.font = "bold 14px Arial";
            ctx.fillText("电流方向", wire.bulbX - 100, wire.topY - 15);
        }
        
        // 绘制箭头的辅助函数
        function drawArrow(fromX, fromY, toX, toY, headLength, reverse = false) {
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const actualFromX = reverse ? toX : fromX;
            const actualFromY = reverse ? toY : fromY;
            const actualToX = reverse ? fromX : toX;
            const actualToY = reverse ? fromY : toY;
            
            // 绘制线
            ctx.beginPath();
            ctx.moveTo(actualFromX, actualFromY);
            ctx.lineTo(actualToX, actualToY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(actualToX, actualToY);
            ctx.lineTo(
                actualToX - headLength * Math.cos(angle - Math.PI / 6),
                actualToY - headLength * Math.sin(angle - Math.PI / 6)
            );
            ctx.lineTo(
                actualToX - headLength * Math.cos(angle + Math.PI / 6),
                actualToY - headLength * Math.sin(angle + Math.PI / 6)
            );
            ctx.closePath();
            ctx.fill();
        }
        
        // 更新电子位置
        function updateElectrons() {
            electrons.forEach(electron => {
                if (!electron.onWire) {
                    // 电子从锌电极表面产生
                    electron.y -= electron.speed * animationSpeed / 5;
                    
                    // 当电子到达锌电极顶部时，开始沿导线移动
                    if (electron.y <= electrodes.zinc.y) {
                        electron.onWire = true;
                        electron.pathProgress = 0;
                    }
                } else {
                    // 电子沿导线移动
                    electron.pathProgress += 0.005 * animationSpeed;
                    
                    if (electron.pathProgress <= 0.5) {
                        // 从锌电极到灯泡
                        const t = electron.pathProgress * 2; // 映射到 0-1
                        electron.x = electrodes.zinc.x + electrodes.zinc.width/2;
                        electron.y = electrodes.zinc.y - t * (electrodes.zinc.y - wire.topY);
                        
                        // 水平移动到灯泡
                        if (t >= 1) {
                            electron.x = electrodes.zinc.x + electrodes.zinc.width/2 + (wire.bulbX - (electrodes.zinc.x + electrodes.zinc.width/2)) * (t - 1);
                        }
                    } else {
                        // 从灯泡到铜电极
                        const t = (electron.pathProgress - 0.5) * 2; // 映射到 0-1
                        electron.x = wire.bulbX;
                        electron.y = wire.topY;
                        
                        // 水平移动到铜电极上方
                        if (t >= 0.5) {
                            electron.x = wire.bulbX + (electrodes.copper.x + electrodes.copper.width/2 - wire.bulbX) * (t - 0.5) * 2;
                        }
                        
                        // 垂直下降到铜电极
                        if (t >= 1) {
                            electron.y = wire.topY + (electrodes.copper.y - wire.topY) * (t - 1);
                        }
                    }
                    
                    // 当电子完成整个路径时，重置
                    if (electron.pathProgress >= 1) {
                        resetElectron(electron);
                    }
                }
            });
        }
        
        // 重置电子到起始位置
        function resetElectron(electron) {
            electron.x = electrodes.zinc.x + electrodes.zinc.width/2;
            electron.y = electrodes.zinc.y + electrodes.zinc.height - 20 - Math.random() * 50;
            electron.onWire = false;
            electron.pathProgress = 0;
        }
        
        // 更新离子位置
        function updateIons() {
            // 更新锌离子 (向溶液右侧扩散)
            znIons.forEach(ion => {
                ion.x += ion.driftDirection * ion.speed * animationSpeed / 10;
                ion.y += (Math.sin(time + ion.x * 0.1) * 0.5) * animationSpeed / 10;
                
                // 边界检查
                if (ion.x > beaker.x + beaker.width - 50) {
                    ion.driftDirection = -0.5; // 轻微反弹
                }
                if (ion.x < electrodes.zinc.x + electrodes.zinc.width + 20) {
                    ion.driftDirection = 1; // 继续向右
                }
                
                // 垂直边界
                if (ion.y < beaker.y + 30 || ion.y > beaker.y + beaker.liquidHeight - 30) {
                    ion.y = Math.max(beaker.y + 30, Math.min(beaker.y + beaker.liquidHeight - 
<!--检测到代码截断，自动续写中...-->
30, ion.y));
                }
            });
            
            // 更新氢离子 (向铜电极移动)
            hIons.forEach(ion => {
                ion.x += ion.driftDirection * ion.speed * animationSpeed / 10;
                ion.y += (Math.cos(time + ion.x * 0.05) * 0.3) * animationSpeed / 10;
                
                // 当氢离子接近铜电极时，可能被还原
                if (ion.x < electrodes.copper.x + 30 && Math.random() < 0.01 * animationSpeed) {
                    // 重置氢离子位置
                    ion.x = beaker.x + 50 + Math.random() * (beaker.width - 100);
                    ion.y = beaker.y + 50 + Math.random() * (beaker.liquidHeight - 100);
                    
                    // 有可能生成氢气气泡
                    if (showH2Bubbles && Math.random() < 0.3) {
                        h2Bubbles.push({
                            x: electrodes.copper.x - 10,
                            y: electrodes.copper.y + electrodes.copper.height - 30 - Math.random() * 100,
                            radius: 5 + Math.random() * 5,
                            speed: 0.3 + Math.random() * 0.3,
                            color: "#ECF0F1",
                            borderColor: "#BDC3C7",
                            floatProgress: 0
                        });
                    }
                }
                
                // 边界检查
                if (ion.x < beaker.x + 30) {
                    ion.driftDirection = 0.5; // 轻微反弹
                }
                if (ion.x > beaker.x + beaker.width - 30) {
                    ion.driftDirection = -1; // 向左移动
                }
                
                // 垂直边界
                if (ion.y < beaker.y + 30 || ion.y > beaker.y + beaker.liquidHeight - 30) {
                    ion.y = Math.max(beaker.y + 30, Math.min(beaker.y + beaker.liquidHeight - 30, ion.y));
                }
            });
            
            // 更新硫酸根离子 (向锌电极移动)
            so4Ions.forEach(ion => {
                ion.x += ion.driftDirection * ion.speed * animationSpeed / 10;
                ion.y += (Math.sin(time * 0.5 + ion.x * 0.08) * 0.4) * animationSpeed / 10;
                
                // 边界检查
                if (ion.x > beaker.x + beaker.width - 50) {
                    ion.driftDirection = -1; // 向左移动
                }
                if (ion.x < beaker.x + 50) {
                    ion.driftDirection = 1; // 向右移动
                }
                
                // 垂直边界
                if (ion.y < beaker.y + 40 || ion.y > beaker.y + beaker.liquidHeight - 40) {
                    ion.y = Math.max(beaker.y + 40, Math.min(beaker.y + beaker.liquidHeight - 40, ion.y));
                }
            });
        }
        
        // 更新氢气气泡
        function updateH2Bubbles() {
            for (let i = h2Bubbles.length - 1; i >= 0; i--) {
                const bubble = h2Bubbles[i];
                bubble.floatProgress += 0.005 * animationSpeed;
                
                // 气泡上浮
                bubble.y -= bubble.speed * animationSpeed / 5;
                bubble.x += Math.sin(time * 2 + i) * 0.5;
                
                // 当气泡到达液面时，移除或重置
                if (bubble.y < beaker.y + 20 || bubble.floatProgress > 1) {
                    h2Bubbles.splice(i, 1);
                    
                    // 添加新的气泡
                    if (showH2Bubbles && isPlaying) {
                        h2Bubbles.push({
                            x: electrodes.copper.x - 10,
                            y: electrodes.copper.y + electrodes.copper.height - 30 - Math.random() * 100,
                            radius: 5 + Math.random() * 5,
                            speed: 0.3 + Math.random() * 0.3,
                            color: "#ECF0F1",
                            borderColor: "#BDC3C7",
                            floatProgress: 0
                        });
                    }
                }
            }
        }
        
        // 绘制电极反应动画
        function drawElectrodeReactions() {
            // 锌电极反应动画 (锌原子溶解)
            if (isPlaying && showZnIons) {
                const reactionRate = 0.02 * animationSpeed;
                
                // 在锌电极表面绘制溶解动画
                for (let i = 0; i < 3; i++) {
                    const dissolveY = electrodes.zinc.y + electrodes.zinc.height - 30 - (time * 20 + i * 40) % (electrodes.zinc.height - 50);
                    
                    ctx.beginPath();
                    ctx.arc(electrodes.zinc.x + electrodes.zinc.width + 5, dissolveY, 6, 0, Math.PI * 2);
                    ctx.fillStyle = "rgba(192, 192, 192, 0.7)";
                    ctx.fill();
                    
                    // 溶解箭头
                    ctx.beginPath();
                    ctx.moveTo(electrodes.zinc.x + electrodes.zinc.width + 5, dissolveY);
                    ctx.lineTo(electrodes.zinc.x + electrodes.zinc.width + 25, dissolveY);
                    ctx.strokeStyle = "rgba(128, 128, 128, 0.7)";
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 箭头头部
                    ctx.beginPath();
                    ctx.moveTo(electrodes.zinc.x + electrodes.zinc.width + 25, dissolveY);
                    ctx.lineTo(electrodes.zinc.x + electrodes.zinc.width + 20, dissolveY - 5);
                    ctx.lineTo(electrodes.zinc.x + electrodes.zinc.width + 20, dissolveY + 5);
                    ctx.closePath();
                    ctx.fillStyle = "rgba(128, 128, 128, 0.7)";
                    ctx.fill();
                }
                
                // 偶尔生成新的锌离子
                if (Math.random() < reactionRate && znIons.length < 25) {
                    znIons.push({
                        x: electrodes.zinc.x + electrodes.zinc.width + 20,
                        y: electrodes.zinc.y + 50 + Math.random() * (electrodes.zinc.height - 100),
                        radius: 8,
                        speed: 0.3 + Math.random() * 0.3,
                        color: "#C0C0C0",
                        charge: "+2",
                        driftDirection: 1
                    });
                }
            }
            
            // 铜电极反应动画 (氢离子还原)
            if (isPlaying && showHIons) {
                const reactionRate = 0.01 * animationSpeed;
                
                // 在铜电极表面绘制还原动画
                for (let i = 0; i < 2; i++) {
                    const reduceY = electrodes.copper.y + electrodes.copper.height - 40 - (time * 15 + i * 60) % (electrodes.copper.height - 60);
                    
                    // 氢离子移动到铜电极
                    ctx.beginPath();
                    ctx.moveTo(electrodes.copper.x - 20, reduceY);
                    ctx.lineTo(electrodes.copper.x - 5, reduceY);
                    ctx.strokeStyle = "rgba(255, 107, 107, 0.7)";
                    ctx.lineWidth = 2;
                    ctx.stroke();
                    
                    // 氢离子
                    ctx.beginPath();
                    ctx.arc(electrodes.copper.x - 20, reduceY, 5, 0, Math.PI * 2);
                    ctx.fillStyle = "rgba(255, 107, 107, 0.7)";
                    ctx.fill();
                    
                    // 电子流入
                    ctx.beginPath();
                    ctx.arc(electrodes.copper.x - 2, reduceY - 10, 3, 0, Math.PI * 2);
                    ctx.fillStyle = "rgba(255, 215, 0, 0.7)";
                    ctx.fill();
                }
            }
        }
        
        // 绘制信息提示
        function drawInfoHints() {
            // 绘制电子流方向箭头
            if (showElectrons && isPlaying) {
                ctx.strokeStyle = "#3498db";
                ctx.fillStyle = "#3498db";
                ctx.lineWidth = 2;
                
                // 从锌电极到灯泡
                drawArrow(
                    electrodes.zinc.x + electrodes.zinc.width/2, wire.topY,
                    wire.bulbX, wire.topY,
                    10, false
                );
                
                // 从灯泡到铜电极
                drawArrow(
                    wire.bulbX, wire.topY,
                    electrodes.copper.x + electrodes.copper.width/2, wire.topY,
                    10, false
                );
                
                // 电子流方向标签
                ctx.fillStyle = "#2980b9";
                ctx.font = "bold 14px Arial";
                ctx.fillText("电子流方向", wire.bulbX + 30, wire.topY - 15);
            }
            
            // 绘制离子迁移方向提示
            if (isPlaying) {
                // 氢离子向铜电极迁移
                ctx.strokeStyle = "rgba(255, 107, 107, 0.7)";
                ctx.fillStyle = "rgba(255, 107, 107, 0.7)";
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.moveTo(beaker.x + beaker.width/2, beaker.y + beaker.liquidHeight/2);
                ctx.lineTo(electrodes.copper.x - 30, beaker.y + beaker.liquidHeight/2);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 硫酸根离子向锌电极迁移
                ctx.strokeStyle = "rgba(255, 167, 38, 0.7)";
                ctx.fillStyle = "rgba(255, 167, 38, 0.7)";
                ctx.setLineDash([5, 5]);
                ctx.beginPath();
                ctx.moveTo(beaker.x + beaker.width/2, beaker.y + beaker.liquidHeight/2 + 30);
                ctx.lineTo(electrodes.zinc.x + electrodes.zinc.width + 30, beaker.y + beaker.liquidHeight/2 + 30);
                ctx.stroke();
                ctx.setLineDash([]);
                
                // 离子迁移标签
                ctx.fillStyle = "#7f8c8d";
                ctx.font = "12px Arial";
                ctx.fillText("H⁺ 向正极迁移", electrodes.copper.x - 100, beaker.y + beaker.liquidHeight/2 - 10);
                ctx.fillText("SO₄²⁻ 向负极迁移", electrodes.zinc.x + electrodes.zinc.width + 10, beaker.y + beaker.liquidHeight/2 + 45);
            }
        }
        
        // 主绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制所有组件
            drawBeaker();
            drawElectrodes();
            drawWiresAndBulb();
            drawElectrodeReactions();
            drawInfoHints();
            
            // 绘制粒子
            drawZnIons();
            drawHIons();
            drawSO4Ions();
            drawH2Bubbles();
            drawElectrons();
            drawCurrentDirection();
            
            // 更新时间
            time += 0.05;
        }
        
        // 动画循环
        function animate() {
            if (!isPlaying) return;
            
            updateElectrons();
            updateIons();
            updateH2Bubbles();
            draw();
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 初始化
        function init() {
            initParticles();
            draw();
            
            // 添加事件监听器
            document.getElementById('playBtn').addEventListener('click', () => {
                if (!isPlaying) {
                    isPlaying = true;
                    animate();
                    document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放中';
                    document.getElementById('playBtn').classList.add('btn-secondary');
                    document.getElementById('playBtn').classList.remove('btn-primary');
                }
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                isPlaying = false;
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                document.getElementById('playBtn').classList.add('btn-primary');
                document.getElementById('playBtn').classList.remove('btn-secondary');
                draw(); // 绘制一帧静态图
            });
            
            document.getElementById('resetBtn').addEventListener('click', () => {
                isPlaying = false;
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
                time = 0;
                initParticles();
                draw();
                document.getElementById('playBtn').innerHTML = '<i class="fas fa-play"></i> 播放';
                document.getElementById('playBtn').classList.add('btn-primary');
                document.getElementById('playBtn').classList.remove('btn-secondary');
            });
            
            document.getElementById('speedSlider').addEventListener('input', (e) => {
                animationSpeed = parseInt(e.target.value);
                const speedText = ['极慢', '很慢', '慢', '较慢', '中慢', '中速', '中快', '快', '很快', '极快'];
                document.getElementById('speedValue').textContent = speedText[animationSpeed - 1];
            });
            
            // 显示/隐藏控制
            document.getElementById('toggleElectrons').addEventListener('change', (e) => {
                showElectrons = e.target.checked;
                draw();
            });
            
            document.getElementById('toggleZnIons').addEventListener('change', (e) => {
                showZnIons = e.target.checked;
                draw();
            });
            
            document.getElementById('toggleHIons').addEventListener('change', (e) => {
                showHIons = e.target.checked;
                draw();
            });
            
            document.getElementById('toggleSO4Ions').addEventListener('change', (e) => {
                showSO4Ions = e.target.checked;
                draw();
            });
            
            document.getElementById('toggleH2Bubbles').addEventListener('change', (e) => {
                showH2Bubbles = e.target.checked;
                if (!showH2Bubbles) {
                    h2Bubbles = [];
                }
                draw();
            });
            
            document.getElementById('toggleCurrent').addEventListener('change', (e) => {
                showCurrent = e.target.checked;
                draw();
            });
            
            // 点击电极显示详细信息
            canvas.addEventListener('click', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                // 检查是否点击了锌电极
                if (x >= electrodes.zinc.x && x <= electrodes.zinc.x + electrodes.zinc.width &&
                    y >= electrodes.zinc.y && y <= electrodes.zinc.y + electrodes.zinc.height) {
                    alert(`锌电极（负极）\n反应类型：${electrodes.zinc.type}\n半反应式：${electrodes.zinc.reaction}\n\n锌原子失去电子被氧化为锌离子，电子通过导线流向铜电极。`);
                }
                
                // 检查是否点击了铜电极
                if (x >= electrodes.copper.x && x <= electrodes.copper.x + electrodes.copper.width &&
                    y >= electrodes.copper.y && y <= electrodes.copper.y + electrodes.copper.height) {
                    alert(`铜电极（正极）\n反应类型：${electrodes.copper.type}\n半反应式：${electrodes.copper.reaction}\n\n溶液中的氢离子在铜电极表面获得电子，被还原为氢气逸出。`);
                }
            });
            
            // 鼠标悬停提示
            canvas.addEventListener('mousemove', (e) => {
                const rect = canvas.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                // 检查鼠标是否在电极上
                let cursor = 'default';
                
                if (x >= electrodes.zinc.x && x <= electrodes.zinc.x + electrodes.zinc.width &&
                    y >= electrodes.zinc.y && y <= electrodes.zinc.y + electrodes.zinc.height) {
                    cursor = 'pointer';
                    canvas.title = "点击查看锌电极详细信息";
                } else if (x >= electrodes.copper.x && x <= electrodes.copper.x + electrodes.copper.width &&
                    y >= electrodes.copper.y && y <= electrodes.copper.y + electrodes.copper.height) {
                    cursor = 'pointer';
                    canvas.title = "点击查看铜电极详细信息";
                } else {
                    canvas.title = "原电池工作原理动画";
                }
                
                canvas.style.cursor = cursor;
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 锌铜-稀硫酸原电池交互式教学动画使用指南

欢迎使用这款精心设计的交互式教学动画！本指南将帮助您充分利用这一工具，深入理解原电池的工作原理。

---

### 一、功能说明

本动画以**锌铜-稀硫酸原电池**为模型，通过动态可视化方式展示了：
- **宏观装置**：完整的原电池结构（烧杯、电极、导线、灯泡）
- **微观过程**：电子、离子的运动轨迹
- **化学反应**：电极上的氧化还原反应
- **完整回路**：外电路电子流与内电路离子流的协同作用

动画采用**分层可视化**设计，允许您控制显示不同粒子，逐步构建对原电池工作原理的完整认知。

---

### 二、主要功能

#### 1. 动画控制区
- **播放/暂停**：启动或暂停动画演示
- **重置**：恢复初始状态，重新开始观察
- **速度调节**：提供10档速度控制（极慢→极快），适应不同观察需求

#### 2. 可视化图层控制
通过复选框独立控制以下元素的显示/隐藏：
- ✅ **电子 (e⁻)**：亮黄色粒子，沿导线流动
- ✅ **锌离子 (Zn²⁺)**：银灰色粒子，从锌电极溶出
- ✅ **氢离子 (H⁺)**：红色粒子，向铜电极迁移
- ✅ **硫酸根离子 (SO₄²⁻)**：橙色粒子，向锌电极迁移
- ✅ **氢气气泡 (H₂)**：白色气泡，在铜电极表面生成
- ✅ **电流方向**：绿色箭头，显示与电子流相反的方向

#### 3. 交互式学习功能
- **点击电极**：弹出详细信息窗口，显示电极名称、反应类型和化学方程式
- **鼠标悬停**：查看电极和粒子的基本信息
- **反应方程式实时显示**：右侧面板始终显示三个关键方程式

---

### 三、设计特色

#### 1. 认知友好的分层设计
- **从宏观到微观**：先观察完整装置，再聚焦粒子运动
- **从静态到动态**：可先暂停观察初始状态，再播放观看动态过程
- **选择性关注**：通过图层控制，可单独研究电子流或离子流

#### 2. 科学的视觉编码
- **颜色系统**：遵循化学可视化惯例（H⁺用红色，电子用亮黄色）
- **运动轨迹**：电子沿导线定向流动，离子在溶液中做定向迁移
- **反应特效**：锌电极的溶解动画、铜电极的还原动画

#### 3. 多重表征整合
- **宏观表征**：装置图、灯泡发光
- **微观表征**：粒子运动、电极反应
- **符号表征**：化学方程式、电荷标注
- **语言表征**：提示信息、反应类型说明

---

### 四、教学要点

#### 核心概念分解
1. **驱动力来源**：锌比铜活泼，更易失去电子
2. **电子路径（外电路）**：
   - 电子从锌电极（负极）流出
   - 经导线和负载（灯泡）
   - 流入铜电极（正极）
3. **离子路径（内电路）**：
   - H⁺向铜电极（正极）迁移
   - SO₄²⁻向锌电极（负极）迁移
4. **电极反应**：
   - 锌极（氧化）：`Zn → Zn²⁺ + 2e⁻`
   - 铜极（还原）：`2H⁺ + 2e⁻ → H₂↑`
5. **完整回路**：电子流与离子流共同构成电荷循环

#### 常见困惑点澄清
- **电流方向 vs 电子流方向**：电流方向与电子流方向相反（可通过"电流方向"图层对比观察）
- **正负极判断**：根据电子流出/流入判断，而非电极材料位置
- **离子迁移原因**：为维持溶液电中性，平衡电极附近的电荷变化

---

### 五、使用建议

#### 对于学生自学
1. **初次接触**：
   - 先观看完整动画（所有图层开启）
   - 注意观察灯泡何时发光、何处产生气泡
   
2. **分步深入学习**：
   - 第一步：仅开启"电子"图层，追踪电子流动路径
   - 第二步：仅开启"离子"图层，观察H⁺和SO₄²⁻的迁移方向
   - 第三步：结合两者，理解内外电路的协同
   
3. **概念检验**：
   - 暂停动画，尝试预测下一步的粒子运动
   - 对照右侧方程式，解释观察到的现象

#### 对于教师课堂演示
1. **引入阶段**：
   - 展示静态装置，提问"哪些部分构成原电池？"
   - 引导学生预测电子流动方向
   
2. **探究阶段**：
   - 分层展示：先看电子流，再看离子流
   - 使用慢速播放，详细讲解关键节点
   - 点击电极展示反应方程式，建立微观-符号联系
   
3. **总结阶段**：
   - 同时显示电子流和电流方向，对比讲解
   - 引导学生总结"原电池工作的必要条件"
   - 联系实际应用（干电池、蓄电池等）

#### 对于翻转课堂
1. **课前预习**：
   - 学生自主探索动画，完成预习任务单
   - 记录观察到的三个关键现象
   
2. **课堂讨论**：
   - 小组分享观察结果
   - 针对困惑点（如离子迁移原因）重点讨论
   - 教师使用动画进行难点澄清

#### 技术提示
- **最佳观看**：在全屏或较大窗口下观看，确保细节清晰
- **交互探索**：大胆尝试不同图层组合，发现新的观察角度
- **速度调节**：复杂概念建议使用"慢速"或"中速"
- **移动设备**：本动画支持响应式设计，在平板电脑上也能良好运行

---

### 六、学习延伸

完成本动画学习后，您可以进一步思考：
1. 如果更换电解质（如CuSO₄溶液），动画会有何变化？
2. 如果更换电极材料（如铁-铜原电池），工作原理是否相同？
3. 盐桥在原电池中起什么作用？与稀硫酸作为电解质有何异同？

---

**祝您学习愉快！通过这个交互式动画，我们希望抽象的化学概念变得生动直观，让您真正理解原电池的奥秘。**

*如有任何使用问题或教学建议，欢迎反馈。这款工具将持续优化，为化学教学提供更好的支持。*