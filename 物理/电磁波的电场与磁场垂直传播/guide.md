# 需求：电磁波的电场与磁场垂直传播

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：高中或大学低年级的物理学习者。他们已具备基础的波和电磁学知识（如横波、电场、磁场概念），但需要直观理解电磁波作为一种横波，其电场（E）、磁场（B）与传播方向（k）三者之间的空间正交关系。
2.  **核心痛点**：
    *   **抽象性**：电磁波看不见摸不着，其三维空间中的矢量关系难以在静态二维图或脑海中构建。
    *   **动态性**：电磁波是传播的，电场和磁场是同步振荡且相互激发的，这个动态过程需要可视化。
    *   **空间关系**：理解“相互垂直”且“都垂直于传播方向”这一双重垂直关系是关键难点。
3.  **学习目标**：
    *   **知识层面**：确认电磁波是横波，E、B、k两两垂直。
    *   **过程层面**：观察电场和磁场如何随时间变化并沿空间传播。
    *   **应用层面**：能够判断给定电磁波模型中各矢量的方向。

#### 教学设计思路
1.  **核心概念**：
    *   **横波特性**：振动方向与传播方向垂直。
    *   **矢量场**：电场E和磁场B是矢量，具有方向和大小。
    *   **正交关系**：E ⊥ B，且 E ⊥ k， B ⊥ k（k为波矢，指示传播方向）。
    *   **同相振荡**：在自由空间传播的平面电磁波中，E和B的幅值同时达到最大、同时过零。
    *   **右手定则**：E × B 的方向（叉积方向）即为波的传播方向k。

2.  **认知规律（支架式教学）**：
    *   **从已知到未知**：先回顾机械横波（如绳子上的波），建立“振动方向垂直传播方向”的直观印象。
    *   **分解与聚焦**：将三维动画分解，允许用户单独查看电场、磁场的分布和变化，再组合观察。
    *   **从静态到动态**：先展示某一时刻的“快照”，理解空间分布；再启动动画，观察时间上的传播与振荡。
    *   **交互探索**：允许用户从不同视角（正面、侧面、三维透视）观察，主动构建空间认知。

3.  **交互设计**：
    *   **模块化控制面板**：清晰划分“视图控制”、“波形控制”和“矢量显示控制”。
    *   **渐进式揭示**：初始状态可能只显示传播的波和电场，用户可通过勾选逐步加入磁场、网格、矢量箭头等元素。
    *   **关键点提示与探测**：鼠标悬停或点击波上某一点，可突出显示该点的E、B矢量，并显示实时数值和方向信息。
    *   **情景化挑战**：设置一个小测验模块，如“给定E方向，请指出正确的B和k方向”，让用户应用右手定则。

4.  **视觉呈现**：
    *   **主视图**：一个三维笛卡尔坐标系空间，电磁波沿+x方向传播。
    *   **电场E**：用**洋红色**箭头或正弦曲线表示。箭头直观显示矢量方向与大小，曲线显示空间分布。电场方向固定沿y轴方向振荡。
    *   **磁场B**：用**青色**箭头或正弦曲线表示。方向固定沿z轴方向振荡。颜色上与电场形成鲜明对比。
    *   **传播与波形**：用一条沿x轴延伸的**亮白色或淡灰色**“光带”或密集点阵表示波传播的路径和波前。E和B的正弦曲线绘制在这个路径上。
    *   **空间参考**：提供半透明的坐标平面（如x-y平面）和网格，辅助用户进行空间定位。

#### 配色方案选择
*   **主旨**：清晰、对比度高、符合科学可视化惯例、减少视觉疲劳。
*   **电场（E）**：**洋红色 (#FF00FF)** 或 **红色 (#FF3333)**。在物理可视化中常用红色代表电场。
*   **磁场（B）**：**青色 (#00FFFF)** 或 **蓝色 (#3399FF)**。常用蓝色或青色代表磁场。
*   **传播轴/波形路径**：**浅灰色 (#CCCCCC)** 或 **白色 (#FFFFFF)**，低调且不喧宾夺主。
*   **坐标系与网格**：**深灰色 (#444444)**，半透明，提供参考但不干扰前景。
*   **背景**：**深空蓝 (#0A0A2A)** 或 **纯黑 (#000000)**。模拟空间感，能极大突出发光色的矢量与波形。
*   **界面UI**：浅色文字和控件（浅灰 #EEEEEE），置于深色半透明面板上，确保可读性。

#### 交互功能列表
1.  **动画控制**：
    *   播放/暂停按钮。
    *   重置动画按钮。
    *   动画速度滑块。
2.  **视图控制**：
    *   三维视图旋转（通过鼠标拖拽）。
    *   预设视角按钮（如：正视图、侧视图、等轴视图）。
    *   缩放滑块。
3.  **可视化元素开关**：
    *   ✅ 显示/隐藏 电场（E）矢量与波形。
    *   ✅ 显示/隐藏 磁场（B）矢量与波形。
    *   ✅ 显示/隐藏 传播路径/波前。
    *   ✅ 显示/隐藏 参考坐标系与网格。
    *   ✅ 显示/隐藏 某时刻的“瞬时快照”（冻结的波形）。
4.  **探测与提示**：
    *   鼠标悬停在空间任意点，显示该点（或最近计算点）的E、B矢量（临时出现）及其数值。
    *   点击波上某点，将该点固定显示其E、B矢量，并可能显示“此处E最大，B也最大”等文字说明。
5.  **教学辅助模块**：
    *   **步骤演示**：一个分步引导按钮，自动按教学顺序展示从机械横波到电磁波，从单独E到E+B的过程。
    *   **右手定则辅助**：一个动态图示区域，当用户选择E和B方向后，自动生成并高亮显示叉乘得到的传播方向k。
    *   **小测验**：一个弹出式问题，让用户调整三维模型中的箭头方向来完成方向关系判断。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>电磁波：电场与磁场的垂直传播</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(to bottom, #0A0A2A, #1a1a40);
            color: #EEEEEE;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid rgba(255, 255, 255, 0.1);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #FF00FF, #00FFFF);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }

        .subtitle {
            font-size: 1.1rem;
            opacity: 0.8;
            max-width: 800px;
            margin: 0 auto;
        }

        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            margin-bottom: 30px;
        }

        .canvas-container {
            flex: 3;
            min-width: 300px;
            background-color: rgba(0, 0, 0, 0.4);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
        }

        #waveCanvas {
            display: block;
            width: 100%;
            height: 600px;
            cursor: grab;
        }

        #waveCanvas:active {
            cursor: grabbing;
        }

        .controls-panel {
            flex: 1;
            min-width: 300px;
            background-color: rgba(20, 20, 40, 0.8);
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.4);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .control-section {
            background-color: rgba(30, 30, 60, 0.6);
            border-radius: 10px;
            padding: 20px;
            border-left: 4px solid #00FFFF;
        }

        .control-section:nth-child(2) {
            border-left-color: #FF00FF;
        }

        .control-section:nth-child(3) {
            border-left-color: #FFCC00;
        }

        h2 {
            font-size: 1.4rem;
            margin-bottom: 18px;
            color: #FFFFFF;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        h2 i {
            font-size: 1.2rem;
        }

        .control-group {
            margin-bottom: 18px;
        }

        .control-group:last-child {
            margin-bottom: 0;
        }

        .control-label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: #CCCCCC;
        }

        .checkbox-group {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .checkbox-item {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            padding: 5px 0;
        }

        .checkbox-item input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .color-indicator {
            width: 16px;
            height: 16px;
            border-radius: 3px;
            display: inline-block;
        }

        .color-e {
            background-color: #FF00FF;
        }

        .color-b {
            background-color: #00FFFF;
        }

        .color-path {
            background-color: #CCCCCC;
        }

        .color-grid {
            background-color: #444444;
        }

        button {
            background-color: #3399FF;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 600;
            font-size: 1rem;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            width: 100%;
        }

        button:hover {
            background-color: #4DA6FF;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(51, 153, 255, 0.4);
        }

        button:active {
            transform: translateY(0);
        }

        #resetBtn {
            background-color: #6666CC;
        }

        #resetBtn:hover {
            background-color: #7777DD;
        }

        .slider-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        input[type="range"] {
            flex: 1;
            height: 8px;
            -webkit-appearance: none;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #00FFFF;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(0, 255, 255, 0.5);
        }

        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: 600;
            color: #00FFFF;
        }

        .view-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
        }

        .view-btn {
            background-color: rgba(60, 60, 100, 0.7);
            padding: 10px;
            font-size: 0.9rem;
        }

        .view-btn:hover {
            background-color: rgba(80, 80, 120, 0.9);
        }

        .info-panel {
            background-color: rgba(0, 0, 0, 0.5);
            border-radius: 10px;
            padding: 20px;
            margin-top: 10px;
            border-top: 2px solid rgba(255, 255, 255, 0.1);
        }

        .info-title {
            font-weight: 600;
            color: #FFCC00;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .info-content {
            font-size: 0.95rem;
            color: #DDDDDD;
        }

        .info-content p {
            margin-bottom: 8px;
        }

        .highlight {
            color: #FF00FF;
            font-weight: 600;
        }

        .highlight-b {
            color: #00FFFF;
            font-weight: 600;
        }

        .highlight-k {
            color: #FFFFFF;
            font-weight: 600;
        }

        .coordinate-info {
            position: absolute;
            bottom: 15px;
            left: 15px;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 10px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
            border-left: 3px solid #FFCC00;
        }

        .point-info {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 12px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
            max-width: 250px;
            border-left: 3px solid #3399FF;
            display: none;
        }

        .point-info.active {
            display: block;
        }

        .legend {
            position: absolute;
            bottom: 15px;
            right: 15px;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 12px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 8px;
        }

        .legend-item:last-child {
            margin-bottom: 0;
        }

        @media (max-width: 1100px) {
            .main-content {
                flex-direction: column;
            }
            
            .canvas-container, .controls-panel {
                width: 100%;
            }
            
            #waveCanvas {
                height: 500px;
            }
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 2rem;
            }
            
            #waveCanvas {
                height: 400px;
            }
            
            .controls-panel {
                padding: 15px;
            }
            
            .control-section {
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>电磁波：电场与磁场的垂直传播</h1>
            <p class="subtitle">可视化电磁波作为横波的三维特性：电场(E)、磁场(B)与传播方向(k)两两垂直，且同步振荡传播。</p>
        </header>

        <div class="main-content">
            <div class="canvas-container">
                <canvas id="waveCanvas"></canvas>
                <div class="coordinate-info">
                    <div>X轴: 传播方向 (k)</div>
                    <div>Y轴: 电场方向 (E) <span style="color:#FF00FF;">●</span></div>
                    <div>Z轴: 磁场方向 (B) <span style="color:#00FFFF;">●</span></div>
                </div>
                <div class="point-info" id="pointInfo">
                    <div class="info-title">探测点信息</div>
                    <div>位置: <span id="posX">0</span>, <span id="posY">0</span>, <span id="posZ">0</span></div>
                    <div>电场 E: <span id="eValue" class="highlight">0</span> (Y方向)</div>
                    <div>磁场 B: <span id="bValue" class="highlight-b">0</span> (Z方向)</div>
                    <div>相位: <span id="phaseValue">0</span>°</div>
                </div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="color-indicator color-e"></div>
                        <span>电场 (E)</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-indicator color-b"></div>
                        <span>磁场 (B)</span>
                    </div>
                    <div class="legend-item">
                        <div class="color-indicator color-path"></div>
                        <span>传播路径</span>
                    </div>
                </div>
            </div>

            <div class="controls-panel">
                <div class="control-section">
                    <h2>📊 动画控制</h2>
                    
                    <div class="control-group">
                        <div class="slider-container">
                            <span class="control-label">动画速度</span>
                            <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                            <span class="slider-value" id="speedValue">1.0x</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="slider-container">
                            <span class="control-label">波长</span>
                            <input type="range" id="wavelengthSlider" min="50" max="200" step="10" value="100">
                            <span class="slider-value" id="wavelengthValue">100</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <button id="playPauseBtn">
                            <span id="playIcon">⏸️</span>
                            <span id="playText">暂停动画</span>
                        </button>
                    </div>
                    
                    <div class="control-group">
                        <button id="resetBtn">🔄 重置视图与动画</button>
                    </div>
                </div>

                <div class="control-section">
                    <h2>👁️ 可视化选项</h2>
                    
                    <div class="control-group">
                        <div class="control-label">显示/隐藏元素</div>
                        <div class="checkbox-group">
                            <label class="checkbox-item">
                                <input type="checkbox" id="showE" checked>
                                <div class="color-indicator color-e"></div>
                                <span>电场 (E)</span>
                            </label>
                            <label class="checkbox-item">
                                <input type="checkbox" id="showB" checked>
                                <div class="color-indicator color-b"></div>
                                <span>磁场 (B)</span>
                            </label>
                            <label class="checkbox-item">
                                <input type="checkbox" id="showPath" checked>
                                <div class="color-indicator color-path"></div>
                                <span>传播路径</span>
                            </label>
                            <label class="checkbox-item">
                                <input type="checkbox" id="showGrid" checked>
                                <div class="color-indicator color-grid"></div>
                                <span>坐标网格</span>
                            </label>
                            <label class="checkbox-item">
                                <input type="checkbox" id="showVectors">
                                <span>矢量箭头</span>
                            </label>
                            <label class="checkbox-item">
                                <input type="checkbox" id="showSnapshot">
                                <span>瞬时快照</span>
                            </label>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">预设视图</div>
                        <div class="view-buttons">
                            <button class="view-btn" id="frontView">正视图 (X-Y平面)</button>
                            <button class="view-btn" id="sideView">侧视图 (X-Z平面)</button>
                            <button class="view-btn" id="topView">俯视图 (Y-Z平面)</button>
                            <button class="view-btn" id="isoView">等轴视图</button>
                        </div>
                    </div>
                </div>

                <div class="control-section">
                    <h2>🎓 教学辅助</h2>
                    
                    <div class="control-group">
                        <button id="stepDemoBtn">▶️ 启动分步演示</button>
                    </div>
                    
                    <div class="control-group">
                        <button id="rightHandBtn">🖐️ 显示右手定则</button>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">探测模式</div>
                        <div class="checkbox-group">
                            <label class="checkbox-item">
                                <input type="checkbox" id="probeMode">
                                <span>启用点探测 (点击画布)</span>
                            </label>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="info-panel">
            <div class="info-title">📚 核心概念</div>
            <div class="info-content">
                <p>1. 电磁波是<strong>横波</strong>：电场 <span class="highlight">E</span> 和磁场 <span class="highlight-b">B</span> 的振动方向都与波的传播方向 <span class="highlight-k">k</span> 垂直。</p>
                <p>2. <strong>正交关系</strong>：<span class="highlight">E</span> ⊥ <span class="highlight-b">B</span>，且 <span class="highlight">E</span> ⊥ <span class="highlight-k">k</span>，<span class="highlight-b">B</span> ⊥ <span class="highlight-k">k</span>，三者两两垂直。</p>
                <p>3. <strong>同相振荡</strong>：在自由空间中，<span class="highlight">E</span> 和 <span class="highlight-b">B</span> 同时达到最大值，同时过零点，相位相同。</p>
                <p>4. <strong>右手定则</strong>：右手四指从 <span class="highlight">E</span> 方向弯向 <span class="highlight-b">B</span> 方向，拇指指向即为波的传播方向 <span class="highlight-k">k</span>。</p>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('waveCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.clientWidth;
            canvas.height = canvas.clientHeight;
        }
        
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
        
        // 动画状态
        let animationId = null;
        let isPlaying = true;
        let time = 0;
        
        // 视图参数
        let viewRotationX = -30 * Math.PI / 180;
        let viewRotationY = 30 * Math.PI / 180;
        let zoom = 1.0;
        let offsetX = 0;
        let offsetY = 0;
        
        // 波形参数
        let wavelength = 100;
        let amplitude = 40;
        let speed = 1.0;
        
        // 显示选项
        let showE = true;
        let showB = true;
        let showPath = true;
        let showGrid = true;
        let showVectors = false;
        let showSnapshot = false;
        let probeMode = false;
        
        // 探测点信息
        let probePoint = null;
        
        // 鼠标交互
        let isDragging = false;
        let lastMouseX = 0;
        let lastMouseY = 0;
        
        // 分步演示状态
        let stepDemoActive = false;
        let stepDemoPhase = 0;
        let stepDemoTimer = null;
        
        // 右手定则显示
        let showRightHandRule = false;
        
        // 初始化控件状态
        document.getElementById('showE').checked = showE;
        document.getElementById('showB').checked = showB;
        document.getElementById('showPath').checked = showPath;
        document.getElementById('showGrid').checked = showGrid;
        document.getElementById('showVectors').checked = showVectors;
        document.getElementById('showSnapshot').checked = showSnapshot;
        document.getElementById('probeMode').checked = probeMode;
        
        // 更新滑块显示值
        document.getElementById('speedValue').textContent = speed.toFixed(1) + 'x';
        document.getElementById('wavelengthValue').textContent = wavelength;
        
        // 控件事件监听
        document.getElementById('speedSlider').addEventListener('input', function() {
            speed = parseFloat(this.value);
            document.getElementById('speedValue').textContent = speed.toFixed(1) + 'x';
        });
        
        document.getElementById('wavelengthSlider').addEventListener('input', function() {
            wavelength = parseInt(this.value);
            document.getElementById('wavelengthValue').textContent = wavelength;
        });
        
        document.getElementById('playPauseBtn').addEventListener('click', function() {
            isPlaying = !isPlaying;
            document.getElementById('playText').textContent = isPlaying ? '暂停动画' : '播放动画';
            document.getElementById('playIcon').textContent = isPlaying ? '⏸️' : '▶️';
            
            if (isPlaying) {
                animate();
            } else {
                if (animationId) {
                    cancelAnimationFrame(animationId);
                }
            }
        });
        
        document.getElementById('resetBtn').addEventListener('click', function() {
            viewRotationX = -30 * Math.PI / 180;
            viewRotationY = 30 * Math.PI / 180;
            zoom = 1.0;
            offsetX = 0;
            offsetY = 0;
            time = 0;
            probePoint = null;
            document.getElementById('pointInfo').classList.remove('active');
            showRightHandRule = false;
            
            if (!isPlaying) {
                isPlaying = true;
                document.getElementById('playText').textContent = '暂停动画';
                document.getElementById('playIcon').textContent = '⏸️';
                animate();
            }
        });
        
        document.getElementById('showE').addEventListener('change', function() {
            showE = this.checked;
        });
        
        document.getElementById('showB').addEventListener('change', function() {
            showB = this.checked;
        });
        
        document.getElementById('showPath').addEventListener('change', function() {
            showPath = this.checked;
        });
        
        document.getElementById('showGrid').addEventListener('change', function() {
            showGrid = this.checked;
        });
        
        document.getElementById('showVectors').addEventListener('change', function() {
            showVectors = this.checked;
        });
        
        document.getElementById('showSnapshot').addEventListener('change', function() {
            showSnapshot = this.checked;
        });
        
        document.getElementById('probeMode').addEventListener('change', function() {
            probeMode = this.checked;
        });
        
        // 视图按钮
        document.getElementById('frontView').addEventListener('click', function() {
            viewRotationX = 0;
            viewRotationY = 0;
        });
        
        document.getElementById('sideView').addEventListener('click', function() {
            viewRotationX = 0;
            viewRotationY = 90 * Math.PI / 180;
        });
        
        document.getElementById('topView').addEventListener('click', function() {
            viewRotationX = -90 * Math.PI / 180;
            viewRotationY = 0;
        });
        
        document.getElementById('isoView').addEventListener('click', function() {
            viewRotationX = -30 * Math.PI / 180;
            viewRotationY = 30 * Math.PI / 180;
        });
        
        // 教学辅助按钮
        document.getElementById('stepDemoBtn').addEventListener('click', function() {
            startStepDemo();
        });
        
        document.getElementById('rightHandBtn').addEventListener('click', function() {
            showRightHandRule = !showRightHandRule;
            this.textContent = showRightHandRule ? '🖐️ 隐藏右手定则' : '🖐️ 显示右手定则';
        });
        
        // 鼠标事件
        canvas.addEventListener('mousedown', function(e) {
            isDragging = true;
            lastMouseX = e.clientX;
            lastMouseY = e.clientY;
            
            // 如果探测模式开启，处理点击探测
            if (probeMode) {
                handleCanvasClick(e);
            }
        });
        
        canvas.addEventListener('mousemove', function(e) {
            if (isDragging && !probeMode) {
                const deltaX = e.clientX - lastMouseX;
                const deltaY = e.clientY - lastMouseY;
                
                viewRotationY += deltaX * 0.01;
                viewRotationX += deltaY * 0.01;
                
                lastMouseX = e.clientX;
                lastMouseY = e.clientY;
            }
        });
        
        canvas.addEventListener('mouseup', function() {
            isDragging = false;
        });
        
        canvas.addEventListener('mouseleave', function() {
            isDragging = false;
        });
        
        // 鼠标滚轮缩放
        canvas.addEventListener('wheel', function(e) {
            e.preventDefault();
            zoom += e.deltaY * -0.001;
            zoom = Math.max(0.5, Math.min(3, zoom));
        });
        
        // 处理画布点击（探测模式）
        function handleCanvasClick(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 将屏幕坐标转换为3D空间坐标（简化版）
            // 这里我们假设点击的是传播路径上的点
            const canvasX = (x - canvas.width/2) / zoom;
            const canvasY = (y - canvas.height/2) / zoom;
            
            // 逆向旋转到3D空间（简化计算）
            const cosX = Math.cos(viewRotationX);
            const sinX = Math.sin(viewRotationX);
            const cosY = Math.cos(viewRotationY);
            const sinY = Math.sin(viewRotationY);
            
            // 简化：假设点击点在z=0平面上
            let worldX = canvasX * cosY - canvasY * sinX * sinY;
            let worldY = canvasY * cosX;
            
            // 限制在合理范围内
            worldX = Math.max(-200, Math.min(200, worldX));
            worldY = Math.max(-100, Math.min(100, worldY));
            
            // 设置探测点
            probePoint = {
                x: worldX,
                y: worldY,
                z: 0
            };
            
            // 更新显示信息
            updateProbeInfo();
            document.getElementById('pointInfo').classList.add('active');
        }
        
        // 更新探测点信息
        function updateProbeInfo() {
            if (!probePoint) return;
            
            const k = 2 * Math.PI / wavelength;
            const phase = k * probePoint.x - time * 0.05 * speed;
            
            const eValue = amplitude * Math.sin(phase);
            const bValue = amplitude * Math.sin(phase);
            
            document.getElementById('posX').textContent = probePoint.x.toFixed(1);
            document.getElementById('posY').textContent = probePoint.y.toFixed(1);
            document.getElementById('posZ').textContent = probePoint.z.toFixed(1);
            document.getElementById('eValue').textContent = eValue.toFixed(1);
            document.getElementById('bValue').textContent = bValue.toFixed(1);
            document.getElementById('phaseValue').textContent = ((phase * 180 / Math.PI) % 360).toFixed(0);
        }
        
        // 3D投影函数
        function projectPoint(x, y, z) {
            // 应用视图旋转
            const cosX = Math.cos(viewRotationX);
            const sinX = Math.sin(viewRotationX);
            const cosY = Math.cos(viewRotationY);
            const sinY = Math.sin(viewRotationY);
            
            // 绕Y轴旋转
            let x1 = x * cosY + z * sinY;
            let z1 = z * cosY - x * sinY;
            
            // 绕X轴旋转
            let y1 = y * cosX - z1 * sinX;
            z1 = z1 * cosX + y * sinX;
            
            // 应用缩放和偏移
            const scale = 2 * zoom;
            const screenX = canvas.width/2 + (x1 + offsetX) * scale;
            const screenY = canvas.height/2 + (y1 + offsetY) * scale;
            
            return {x: screenX, y: screenY, z: z1};
        }
        
        // 绘制坐标系网格
        function drawGrid() {
            if (!showGrid) return;
            
            ctx.strokeStyle = 'rgba(68, 68, 68, 0.6)';
            ctx.lineWidth = 1;
            
            // 绘制X-Y平面网格
            for (let x = -200; x <= 200; x += 50) {
                const p1 = projectPoint(x, -100, 0);
                const p2 = projectPoint(x, 100, 0);
                
                ctx.beginPath();
                ctx.moveTo(p1.x, p1.y);
                ctx.lineTo(p2.x, p2.y);
                ctx.stroke();
            }
            
            for (let y = -100; y <= 100; y += 50) {
                const p1 = projectPoint(-200, y, 0);
                const p2 = projectPoint(200, y, 0);
                
                ctx.beginPath();
                ctx.moveTo(p1.x, p1.y);
                ctx.lineTo(p2.x, p2.y);
                ctx.stroke();
            }
            
            // 绘制坐标轴
            ctx.lineWidth = 2;
            
            // X轴 (红色)
            const xStart = projectPoint(-220, 0, 0);
            const xEnd = projectPoint(220, 0, 0);
            ctx.strokeStyle = '#FF3333';
            ctx.beginPath();
            ctx.moveTo(xStart.x, xStart.y);
            ctx.lineTo(xEnd.x, xEnd.y);
            ctx.stroke();
            
            // Y轴 (绿色)
            const yStart = projectPoint(0, -120, 0);
            const yEnd = projectPoint(0, 120, 0);
            ctx.strokeStyle = '#33FF33';
            ctx.beginPath();
            ctx.moveTo(yStart.x, yStart.y);
            ctx.lineTo(yEnd.x, yEnd.y);
            ctx.stroke();
            
            // Z轴 (蓝色)
            const zStart = projectPoint(0, 0, -120);
            const zEnd = projectPoint(0, 0, 120);
            ctx.strokeStyle = '#3399FF';
            ctx.beginPath();
            ctx.moveTo(zStart.x, zStart.y);
            ctx.lineTo(zEnd.x, zEnd.y);
            ctx.stroke();
            
            // 坐标轴标签
            ctx.font = '14px Arial';
            ctx.fillStyle = '#FF3333';
            ctx.fillText('X (传播方向 k)', xEnd.x + 5, xEnd.y + 5);
            
            ctx.fillStyle = '#33FF33';
            ctx.fillText('Y (电场 E)', yEnd.x + 5, yEnd.y - 10);
            
            ctx.fillStyle = '#3399FF';
            ctx.fillText('Z (磁场 B)', zEnd.x + 5, zEnd.y + 5);
        }
        
        // 绘制传播路径
        function drawPropagationPath() {
            if (!showPath) return;
            
            ctx.strokeStyle = 'rgba(204, 204, 204, 0.7)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            
            const points = [];
            for (let x = -200; x <= 200; x += 5) {
                points.push(projectPoint(x, 0, 0));
            }
            
            ctx.beginPath();
            ctx.moveTo(points[0].x, points[0].y);
            for (let i = 1; i < points.length; i++) {
                ctx.lineTo(points[i].x, points[i].y);
            }
            ctx.stroke();
            
            ctx.setLineDash([]);
        }
        
        // 绘制电场波形
        function drawElectricField() {
            if (!showE) return;
            
            const k = 2 * Math.PI / wavelength;
            
            // 绘制电场波形线
            ctx.strokeStyle = '#FF00FF';
            ctx.lineWidth = 2;
            
            const points = [];
            for (let x = -200; x <= 200; x += 2) {
                const y = amplitude * Math.sin(k * x - time * 0.05 * speed);
                points.push(projectPoint(x, y, 0));
            }
            
            ctx.beginPath();
            ctx.moveTo(points[0].x, points[0].y);
            for (let i = 1; i < points.length; i++) {
                ctx.lineTo(points[i].x, points[i].y);
            }
            ctx.stroke();
            
            // 绘制电场矢量箭头
            if (showVectors) {
                ctx.fillStyle = '#FF00FF';
                for (let x = -180; x <= 180; x += 40) {
                    const y = amplitude * Math.sin(k * x - time * 0.05 * speed);
                    const p = projectPoint(x, 0, 0);
                    const p2 = projectPoint(x, y, 0);
                    
                    drawArrow(p.x, p.y, p2.x, p2.y, '#FF00FF');
                    
                    // 在箭头中点绘制圆点
                    ctx.beginPath();
                    ctx.arc(p2.x, p2.y, 4, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制瞬时快照
            if (showSnapshot) {
                ctx.strokeStyle = 'rgba(255, 0, 255, 0.4)';
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                
                const snapshotPoints = [];
                for (let x = -200; x <= 200; x += 2) {
                    const y = amplitude * Math.sin(k * x - (time - 10) * 0.05 * speed);
                    snapshotPoints.push(projectPoint(x, y, 0));
                }
                
                ctx.beginPath();
                ctx.moveTo(snapshotPoints[0].x, snapshotPoints[0].y);
                for (let i = 1; i < snapshotPoints.length; i++) {
                    ctx.lineTo(snapshotPoints[i].x, snapshotPoints[i].y);
                }
                ctx.stroke();
                
                ctx.setLineDash([]);
            }
        }
        
        // 绘制磁场波形
        function drawMagneticField() {
            if (!showB) return;
            
            const k = 2 * Math.PI / wavelength;
            
            // 绘制磁场波形线
            ctx.strokeStyle = '#00FFFF';
            ctx.lineWidth = 2;
            
            const points = [];
            for (let x = -200; x <= 200; x += 2) {
                const z = amplitude * Math.sin(k * x - time * 0.05 * speed);
                points.push(projectPoint(x, 0, z));
            }
            
            ctx.beginPath();
            ctx.moveTo(points[0].x, points[0].y);
            for (let i = 1; i < points.length; i++) {
                ctx.lineTo(points[i].x, points[i].y);
            }
            ctx.stroke();
            
            // 绘制磁场矢量箭头
            if (showVectors) {
                ctx.fillStyle = '#00FFFF';
                for (let x = -180; x <= 180; x += 40) {
                    const z = amplitude * Math.sin(k * x - time * 0.05 * speed);
                    const p = projectPoint(x, 0, 0);
                    const p2 = projectPoint(x, 0, z);
                    
                    drawArrow(p.x, p.y, p2.x, p2.y, '#00FFFF');
                    
                    // 在箭头中点绘制圆点
                    ctx.beginPath();
                    ctx.arc(p2.x, p2.y, 4, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制瞬时快照
            if (showSnapshot) {
                ctx.strokeStyle = 'rgba(0, 255, 255, 0.4)';
                ctx.lineWidth = 1;
                ctx.setLineDash([3, 3]);
                
                const snapshotPoints = [];
                for (let x = -200; x <= 200; x += 2) {
                    const z = amplitude * Math.sin(k * x - (time - 10) * 0.05 * speed);
                    snapshotPoints.push(projectPoint(x, 0, z));
                }
                
                ctx.beginPath();
                ctx.moveTo(snapshotPoints[0].x, snapshot
<!--检测到代码截断，自动续写中...-->
                ctx.moveTo(snapshotPoints[0].x, snapshotPoints[0].y);
                for (let i = 1; i < snapshotPoints.length; i++) {
                    ctx.lineTo(snapshotPoints[i].x, snapshotPoints[i].y);
                }
                ctx.stroke();
                
                ctx.setLineDash([]);
            }
        }
        
        // 绘制探测点
        function drawProbePoint() {
            if (!probePoint) return;
            
            const p = projectPoint(probePoint.x, probePoint.y, probePoint.z);
            
            // 绘制探测点
            ctx.fillStyle = '#FFCC00';
            ctx.beginPath();
            ctx.arc(p.x, p.y, 8, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制从探测点到波形的连线
            const k = 2 * Math.PI / wavelength;
            const phase = k * probePoint.x - time * 0.05 * speed;
            
            const eValue = amplitude * Math.sin(phase);
            const bValue = amplitude * Math.sin(phase);
            
            // 电场连线
            const pE = projectPoint(probePoint.x, eValue, 0);
            ctx.strokeStyle = 'rgba(255, 0, 255, 0.6)';
            ctx.lineWidth = 1;
            ctx.setLineDash([2, 2]);
            ctx.beginPath();
            ctx.moveTo(p.x, p.y);
            ctx.lineTo(pE.x, pE.y);
            ctx.stroke();
            
            // 磁场连线
            const pB = projectPoint(probePoint.x, 0, bValue);
            ctx.strokeStyle = 'rgba(0, 255, 255, 0.6)';
            ctx.beginPath();
            ctx.moveTo(p.x, p.y);
            ctx.lineTo(pB.x, pB.y);
            ctx.stroke();
            
            ctx.setLineDash([]);
            
            // 在探测点处绘制E和B矢量
            drawArrow(p.x, p.y, pE.x, pE.y, '#FF00FF');
            drawArrow(p.x, p.y, pB.x, pB.y, '#00FFFF');
        }
        
        // 绘制右手定则示意图
        function drawRightHandRule() {
            if (!showRightHandRule) return;
            
            // 在画布右上角绘制示意图
            const centerX = canvas.width - 150;
            const centerY = 150;
            const size = 80;
            
            // 绘制E矢量 (洋红色)
            ctx.strokeStyle = '#FF00FF';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.moveTo(centerX, centerY);
            ctx.lineTo(centerX, centerY - size);
            ctx.stroke();
            
            // 绘制B矢量 (青色)
            ctx.strokeStyle = '#00FFFF';
            ctx.beginPath();
            ctx.moveTo(centerX, centerY);
            ctx.lineTo(centerX + size, centerY);
            ctx.stroke();
            
            // 绘制k矢量 (白色)
            ctx.strokeStyle = '#FFFFFF';
            ctx.beginPath();
            ctx.moveTo(centerX, centerY);
            ctx.lineTo(centerX, centerY + size);
            ctx.stroke();
            
            // 绘制右手示意图
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.lineWidth = 2;
            ctx.beginPath();
            
            // 手掌部分
            ctx.arc(centerX, centerY, 25, 0, Math.PI * 2);
            ctx.stroke();
            
            // 拇指 (k方向)
            ctx.beginPath();
            ctx.moveTo(centerX, centerY);
            ctx.lineTo(centerX, centerY + 35);
            ctx.stroke();
            
            // 四指 (从E弯向B)
            ctx.beginPath();
            ctx.arc(centerX, centerY, 20, -Math.PI/2, 0, false);
            ctx.stroke();
            
            // 标签
            ctx.font = 'bold 14px Arial';
            ctx.fillStyle = '#FF00FF';
            ctx.fillText('E', centerX - 10, centerY - size - 5);
            
            ctx.fillStyle = '#00FFFF';
            ctx.fillText('B', centerX + size + 5, centerY + 5);
            
            ctx.fillStyle = '#FFFFFF';
            ctx.fillText('k', centerX - 10, centerY + size + 15);
            
            ctx.fillStyle = '#FFCC00';
            ctx.font = '12px Arial';
            ctx.fillText('右手定则: E → B = k', centerX - 50, centerY + size + 35);
        }
        
        // 绘制箭头函数
        function drawArrow(fromX, fromY, toX, toY, color) {
            const headlen = 10;
            const angle = Math.atan2(toY - fromY, toX - fromX);
            
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            ctx.lineWidth = 2;
            
            // 绘制线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(toX - headlen * Math.cos(angle - Math.PI/6), toY - headlen * Math.sin(angle - Math.PI/6));
            ctx.lineTo(toX - headlen * Math.cos(angle + Math.PI/6), toY - headlen * Math.sin(angle + Math.PI/6));
            ctx.closePath();
            ctx.fill();
        }
        
        // 开始分步演示
        function startStepDemo() {
            if (stepDemoActive) return;
            
            stepDemoActive = true;
            stepDemoPhase = 0;
            
            // 重置显示选项
            showE = false;
            showB = false;
            showPath = false;
            showVectors = false;
            showSnapshot = false;
            
            document.getElementById('showE').checked = false;
            document.getElementById('showB').checked = false;
            document.getElementById('showPath').checked = false;
            document.getElementById('showVectors').checked = false;
            document.getElementById('showSnapshot').checked = false;
            
            // 开始演示序列
            stepDemoTimer = setInterval(() => {
                stepDemoPhase++;
                
                switch(stepDemoPhase) {
                    case 1:
                        // 步骤1: 显示传播轴
                        showPath = true;
                        document.getElementById('showPath').checked = true;
                        break;
                    case 2:
                        // 步骤2: 显示电场
                        showE = true;
                        document.getElementById('showE').checked = true;
                        break;
                    case 3:
                        // 步骤3: 显示电场矢量
                        showVectors = true;
                        document.getElementById('showVectors').checked = true;
                        break;
                    case 4:
                        // 步骤4: 显示磁场
                        showB = true;
                        document.getElementById('showB').checked = true;
                        break;
                    case 5:
                        // 步骤5: 显示磁场矢量
                        // (已经显示)
                        break;
                    case 6:
                        // 步骤6: 显示瞬时快照
                        showSnapshot = true;
                        document.getElementById('showSnapshot').checked = true;
                        break;
                    case 7:
                        // 步骤7: 演示结束
                        clearInterval(stepDemoTimer);
                        stepDemoActive = false;
                        break;
                }
            }, 1500);
        }
        
        // 主绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制黑色背景
            ctx.fillStyle = '#000000';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制各个组件
            drawGrid();
            drawPropagationPath();
            drawElectricField();
            drawMagneticField();
            
            // 绘制探测点（如果存在）
            if (probeMode && probePoint) {
                drawProbePoint();
                updateProbeInfo();
            }
            
            // 绘制右手定则
            drawRightHandRule();
            
            // 绘制波前标记
            const waveFrontX = 200 * Math.cos(time * 0.02 * speed);
            const pFront = projectPoint(waveFrontX, 0, 0);
            ctx.fillStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.beginPath();
            ctx.arc(pFront.x, pFront.y, 6, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.font = '12px Arial';
            ctx.fillStyle = '#FFFFFF';
            ctx.fillText('波前', pFront.x + 10, pFront.y);
        }
        
        // 动画循环
        function animate() {
            if (isPlaying) {
                time += 1;
                draw();
            }
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 启动动画
        animate();
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 《电磁波：电场与磁场垂直传播》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化，帮助您直观理解电磁波的核心物理特性。无论您是学生、教师还是物理爱好者，都能通过交互探索，深入掌握电场、磁场与传播方向之间的空间正交关系。

### 一、功能说明

本动画是一个基于HTML5 Canvas构建的3D可视化工具，模拟了平面电磁波在自由空间中的传播过程。它允许您从多个视角观察电场（E）和磁场（B）如何作为横波同步振荡，并沿传播方向（k）前进。所有交互功能均通过右侧控制面板实现，左侧画布区域实时呈现三维动态效果。

### 二、主要功能

1. **核心动画控制**
   * **播放/暂停**：随时控制动画的启停，便于仔细观察特定瞬间。
   * **速度调节**：通过滑块调整波的传播速度（0.1x至3.0x），适应不同的观察节奏。
   * **波长调节**：动态改变电磁波的波长，直观观察波长对波形空间分布的影响。
   * **重置**：一键恢复默认视角、动画状态和所有设置。

2. **可视化元素开关**
   * **电场（E）**：显示/隐藏洋红色的电场波形及矢量箭头。
   * **磁场（B）**：显示/隐藏青色的磁场波形及矢量箭头。
   * **传播路径**：显示/标记波传播的轴线。
   * **坐标网格**：提供三维空间参考系。
   * **矢量箭头**：在波上特定点显示E和B的瞬时方向与大小。
   * **瞬时快照**：叠加显示前一时刻的波形，清晰展示波的传播动态。

3. **视图与交互**
   * **三维视图旋转**：在画布上拖拽鼠标，可从任意角度观察电磁波。
   * **鼠标滚轮缩放**：自由缩放视图，聚焦细节或纵览全局。
   * **预设视角**：一键切换至正视图（X-Y）、侧视图（X-Z）、俯视图（Y-Z）和等轴视图。
   * **点探测模式**：启用后，点击画布上任一点，可锁定该点并实时显示其空间坐标、E/B场强及相位信息。

4. **教学辅助模块**
   * **分步演示**：自动引导您从传播轴开始，逐步叠加电场、磁场、矢量等元素，遵循从简到繁的认知规律。
   * **右手定则图示**：在画布一角动态展示E、B、k方向的右手定则关系，强化方向判断的记忆。
   * **核心概念面板**：底部常驻知识要点，随时回顾“横波特性”、“正交关系”、“同相振荡”和“右手定则”。

### 三、设计特色

1. **符合认知规律的支架式设计**：功能排列和分步演示引导用户层层深入，从已知的机械波概念过渡到抽象的电磁波模型。
2. **专业的科学可视化配色**：
   * 电场（E）：**洋红色**，高亮醒目。
   * 磁场（B）：**青色**，形成鲜明对比。
   * 背景采用**深空蓝**，有效突出发光元素，减少视觉干扰。
3. **深度交互与即时反馈**：所有操作均实时反映在动画中。点探测功能将抽象的场强数值与空间位置直接关联，提供沉浸式学习体验。
4. **响应式界面**：适配不同尺寸的屏幕，在电脑、平板等设备上均可获得良好体验。

### 四、教学要点

本动画是理解以下核心概念的理想工具：

1. **横波本质**：直观验证电场E和磁场B的振动方向均垂直于波的传播方向k。
2. **空间正交关系**：通过旋转三维视图，从各个角度确认 **E ⊥ B**， **E ⊥ k**， **B ⊥ k** 这一两两垂直的关系。
3. **同相振荡**：观察E和B的波形峰值、零点完全同步，理解它们在自由空间中相位相同。
4. **方向判断（右手定则）**：结合“右手定则”图示，学习如何由E和B的方向确定传播方向k（E × B = k）。
5. **波形参数影响**：调节波长滑块，观察波形空间疏密的变化，理解波长λ的物理意义。

### 五、使用建议

**给学生的建议：**
1. **初次探索**：先点击“分步演示”，跟随引导逐步认识各个元素。
2. **主动探究**：使用预设视角，分别从正面、侧面观察，在脑海中构建三维图像。然后尝试手动旋转，挑战自己的空间想象力。
3. **概念验证**：打开“矢量箭头”和“瞬时快照”，暂停动画，仔细比较某一点上E和B的方向，验证它们的垂直关系。
4. **自我测试**：关闭B的显示，仅看E和传播方向，尝试用右手定则推断B的方向，再打开显示进行验证。

**给教师的建议：**
1. **课堂演示**：可连接投影仪，作为讲解电磁波特性的动态板书。通过控制动画启停和视角，逐步揭示知识点。
2. **引导探究**：布置任务，如“请找出电场强度为零的点，并观察该点的磁场强度”，让学生通过操作动画自主发现“同相振荡”规律。
3. **小组讨论**：让学生使用“点探测”功能收集不同位置的数据，讨论E、B随空间位置（相位）的变化规律。

**最佳学习路径推荐：**
> **启动分步演示** → **在等轴视图中播放动画，建立整体印象** → **暂停动画，切换到正视图，观察E-k平面** → **再切换到侧视图，观察B-k平面** → **启用点探测，在波峰、波谷、零点等特征位置点击，记录数据** → **打开右手定则图示，结合动画理解方向关系** → **尝试调节波长，总结规律**。

希望本交互式动画能成为您探索电磁世界的有力助手，祝您学习愉快，收获满满！