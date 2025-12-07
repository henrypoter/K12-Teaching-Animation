# 需求：电磁波的产生与传播（振荡电偶极子辐射电磁波）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中物理或大学普通物理的学生。用户的核心需求是：
1.  **理解抽象过程**：电磁波的产生与传播是一个肉眼不可见、高度抽象的物理过程。用户需要一个直观、动态的模型来“看见”这一过程。
2.  **建立因果关系**：理解振荡电偶极子（变化的电场和磁场）如何作为“源头”辐射出电磁波，以及电场、磁场、传播方向三者之间的空间关系。
3.  **掌握核心规律**：掌握电磁波是横波、电场与磁场同相振荡且相互垂直、传播速度等于光速等核心规律。
4.  **降低认知负荷**：避免一次性呈现过多复杂信息（如严格的数学推导），通过分层、可控的视觉呈现，引导用户逐步构建知识。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念聚焦**：
    *   **源**：振荡电偶极子（简化为一个电荷间距周期性变化的模型）。
    *   **场**：变化的电场产生磁场，变化的磁场产生电场（麦克斯韦方程组的核心思想）。
    *   **波**：电场和磁场相互激发，脱离波源，在空间中传播形成电磁波。
    *   **关系**：电场矢量 (**E**)、磁场矢量 (**B**)、波传播方向 (**k**) 三者两两垂直，构成右手螺旋关系。

*   **认知规律遵循**：
    1.  **从静态到动态**：先展示静态电偶极子的电场线分布，再引入电荷振荡，最后展示波的传播。
    2.  **从近场到远场**：动画应能清晰区分近场区（场线复杂，与源强耦合）和远场区（形成稳定的平面横波）。
    3.  **从单一到整体**：先分别观察电场和磁场的变化，再观察它们如何耦合在一起形成完整的电磁波。
    4.  **从定性到定量**：主要进行定性展示，但可通过交互控件（如调节频率）观察现象变化，并可选择性地显示关键物理量（如波长λ）。

*   **交互设计**：
    *   **控制面板**：提供播放/暂停、重置、速度调节等基础控制。
    *   **视图切换**：允许用户选择仅显示“电场”、“磁场”或“电磁波（两者叠加）”。
    *   **参数调节**：调节电偶极子的振荡频率，直观观察波长与频率的反比关系（λ = c/f）。
    *   **探测工具**：允许用户在传播路径上放置一个“虚拟探测器”，显示该点的电场和磁场随时间变化的曲线图，将空间分布与时间变化联系起来。
    *   **提示与标注**：关键位置（如波峰、波谷、传播方向）应有清晰的动态标注或提示线。

*   **视觉呈现**：
    *   **电偶极子**：用两个颜色鲜明（如红+、蓝-）的球体表示正负电荷，中间用细线或弹簧连接，直观展示其简谐振荡。
    *   **电场**：用**连续的、动态变化的蓝色线条或管状面**表示电场线。线条的疏密表示场强，箭头方向表示场的方向。线条从正电荷发出，终止于负电荷，并随振荡向外“甩出”形成波。
    *   **磁场**：用**环绕的、动态变化的绿色圆圈或环状面**表示磁感线。磁场方向垂直于电场和传播方向，用圆环上的箭头表示。
    *   **电磁波**：当电场和磁场视图叠加时，形成蓝绿交织的、向前传播的波形结构。在远场区，应呈现为规整的、正弦形式的平面波前。
    *   **空间网格**：使用半透明的浅灰色参考网格，帮助用户建立三维空间感，并清晰展示波的传播方向。

#### 配色方案选择
*   **主色调**：深空蓝或深灰色作为画布背景，模拟深邃的宇宙空间感，突出前景的发光元素。
*   **电场**：采用**蓝色系**。例如，亮蓝色 (#4FC3F7) 或青色 (#00E5FF) 用于电场线和波面，具有科技感和清晰度。
*   **磁场**：采用**绿色系**。例如，亮绿色 (#69F0AE) 或黄绿色 (#C6FF00)，与蓝色形成鲜明对比，易于区分。
*   **电荷与源**：正电荷用**红色** (#FF5252)，负电荷用**橙色** (#FFAB40) 或**紫色** (#E040FB)，与场的颜色区分开。
*   **辅助元素**：坐标轴、网格用浅灰色 (#CCCCCC)。文本、按钮、控制面板用白色或浅灰色，确保可读性。
*   **高亮与提示**：使用**黄色** (#FFEB3B) 或**粉色** (#FF4081) 进行关键标注和动态追踪，吸引注意力。

#### 交互功能列表
1.  **动画控制区**：
    *   播放 / 暂停 / 重置 按钮。
    *   动画速度滑块（从慢速到快速）。
2.  **视图选择区**（单选按钮或图标切换）：
    *   “仅电场”视图。
    *   “仅磁场”视图。
    *   “电磁波”视图（电场+磁场叠加）。
3.  **参数调节区**：
    *   “振荡频率 (f)”滑块：调节电偶极子的振荡快慢。
    *   （可选）“偶极矩大小”滑块：调节电荷量或间距。
4.  **探测与测量区**：
    *   一个可拖放的“虚拟探测器”图标。
    *   放置后，弹出一个小图表窗口，分别绘制该点 **E-t** 和 **B-t** 的正弦曲线，并显示相位关系。
5.  **显示选项区**（复选框）：
    *   “显示/隐藏 空间网格”。
    *   “显示/隐藏 场线箭头”。
    *   “显示/隐藏 波前标记”（如等相位面）。
    *   “显示/隐藏 关键物理量”（如波长λ、传播方向k）。
6.  **教学提示**：
    *   一个“？”帮助按钮，点击可显示当前视图的简要文字说明。
    *   关键步骤或关系出现时，有非侵入性的浮动文字提示（可关闭）。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>电磁波的产生与传播 - 振荡电偶极子辐射</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0c0e2a 0%, #1a1d3c 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 20px;
            padding: 20px;
            background: rgba(30, 33, 64, 0.7);
            border-radius: 12px;
            border: 1px solid rgba(76, 195, 247, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        h1 {
            color: #4FC3F7;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 0 10px rgba(79, 195, 247, 0.5);
        }
        
        .subtitle {
            color: #69F0AE;
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .canvas-container {
            flex: 1;
            min-width: 600px;
            background: rgba(20, 22, 45, 0.8);
            border-radius: 12px;
            padding: 15px;
            border: 1px solid rgba(76, 195, 247, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        #animationCanvas {
            width: 100%;
            height: 500px;
            display: block;
            background: transparent;
        }
        
        .controls-panel {
            flex: 0 0 300px;
            background: rgba(30, 33, 64, 0.7);
            border-radius: 12px;
            padding: 20px;
            border: 1px solid rgba(105, 240, 174, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .control-section {
            background: rgba(40, 44, 80, 0.6);
            padding: 15px;
            border-radius: 8px;
            border-left: 4px solid #4FC3F7;
        }
        
        .control-section.magnetic {
            border-left-color: #69F0AE;
        }
        
        .control-section.other {
            border-left-color: #FFEB3B;
        }
        
        h2 {
            color: #4FC3F7;
            font-size: 1.3rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        h2.magnetic {
            color: #69F0AE;
        }
        
        h2.other {
            color: #FFEB3B;
        }
        
        .button-group {
            display: flex;
            gap: 10px;
            margin-bottom: 15px;
        }
        
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 6px;
            background: rgba(76, 195, 247, 0.2);
            color: #e0e0e0;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            flex: 1;
        }
        
        button:hover {
            background: rgba(76, 195, 247, 0.4);
            transform: translateY(-2px);
        }
        
        button.active {
            background: rgba(76, 195, 247, 0.7);
            color: white;
            box-shadow: 0 0 10px rgba(76, 195, 247, 0.5);
        }
        
        .magnetic-btn {
            background: rgba(105, 240, 174, 0.2);
        }
        
        .magnetic-btn:hover {
            background: rgba(105, 240, 174, 0.4);
        }
        
        .magnetic-btn.active {
            background: rgba(105, 240, 174, 0.7);
            box-shadow: 0 0 10px rgba(105, 240, 174, 0.5);
        }
        
        .slider-container {
            margin-bottom: 15px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            color: #b0b0b0;
            font-size: 0.95rem;
        }
        
        .slider-value {
            color: #FFEB3B;
            font-weight: bold;
            float: right;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: rgba(100, 100, 120, 0.5);
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4FC3F7;
            cursor: pointer;
            box-shadow: 0 0 5px rgba(79, 195, 247, 0.8);
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
        
        input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }
        
        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.9rem;
        }
        
        .legend-color {
            width: 20px;
            height: 10px;
            border-radius: 2px;
        }
        
        .legend-color.electric {
            background: #4FC3F7;
        }
        
        .legend-color.magnetic {
            background: #69F0AE;
        }
        
        .legend-color.positive {
            background: #FF5252;
        }
        
        .legend-color.negative {
            background: #FFAB40;
        }
        
        .legend-color.grid {
            background: #CCCCCC;
        }
        
        .instructions {
            background: rgba(30, 33, 64, 0.7);
            border-radius: 12px;
            padding: 20px;
            margin-top: 20px;
            border: 1px solid rgba(255, 235, 59, 0.2);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .instructions h2 {
            color: #FFEB3B;
            margin-bottom: 10px;
        }
        
        .instructions p {
            line-height: 1.6;
            margin-bottom: 10px;
        }
        
        .instructions ul {
            padding-left: 20px;
            margin-bottom: 15px;
        }
        
        .instructions li {
            margin-bottom: 8px;
            line-height: 1.5;
        }
        
        .key-point {
            color: #FFEB3B;
            font-weight: bold;
        }
        
        .detector-info {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(0, 0, 0, 0.7);
            padding: 10px;
            border-radius: 6px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 235, 59, 0.3);
            max-width: 250px;
            display: none;
        }
        
        .detector-info.active {
            display: block;
        }
        
        @media (max-width: 1000px) {
            .main-content {
                flex-direction: column;
            }
            
            .canvas-container, .controls-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>电磁波的产生与传播</h1>
            <div class="subtitle">振荡电偶极子辐射电磁波 - 交互式教学动画</div>
        </header>
        
        <div class="main-content">
            <div class="canvas-container">
                <canvas id="animationCanvas"></canvas>
                <div class="detector-info" id="detectorInfo">
                    <div>探测器位置: (<span id="detectorX">0</span>, <span id="detectorY">0</span>)</div>
                    <div>电场强度 E: <span id="detectorE">0.00</span></div>
                    <div>磁场强度 B: <span id="detectorB">0.00</span></div>
                    <div>相位差: <span id="detectorPhase">0.00</span> π</div>
                </div>
            </div>
            
            <div class="controls-panel">
                <div class="control-section">
                    <h2>📊 动画控制</h2>
                    <div class="button-group">
                        <button id="playBtn">▶ 播放</button>
                        <button id="pauseBtn">⏸ 暂停</button>
                        <button id="resetBtn">↺ 重置</button>
                    </div>
                    
                    <div class="slider-container">
                        <label>动画速度: <span class="slider-value" id="speedValue">1.0x</span></label>
                        <input type="range" id="speedSlider" min="0.1" max="3" step="0.1" value="1">
                    </div>
                </div>
                
                <div class="control-section">
                    <h2>👁️ 视图选择</h2>
                    <div class="button-group">
                        <button id="viewElectric" class="active">仅电场</button>
                        <button id="viewMagnetic" class="magnetic-btn">仅磁场</button>
                        <button id="viewBoth">电磁波</button>
                    </div>
                </div>
                
                <div class="control-section">
                    <h2>⚙️ 参数调节</h2>
                    <div class="slider-container">
                        <label>振荡频率 (f): <span class="slider-value" id="freqValue">1.0 Hz</span></label>
                        <input type="range" id="freqSlider" min="0.5" max="3" step="0.1" value="1">
                    </div>
                    
                    <div class="slider-container">
                        <label>偶极矩大小: <span class="slider-value" id="dipoleValue">1.0</span></label>
                        <input type="range" id="dipoleSlider" min="0.5" max="2" step="0.1" value="1">
                    </div>
                </div>
                
                <div class="control-section other">
                    <h2 class="other">🔧 显示选项</h2>
                    <div class="checkbox-group">
                        <div class="checkbox-item">
                            <input type="checkbox" id="showGrid" checked>
                            <label for="showGrid">空间网格</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showArrows" checked>
                            <label for="showArrows">场线箭头</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showWavefront">
                            <label for="showWavefront">波前标记</label>
                        </div>
                        <div class="checkbox-item">
                            <input type="checkbox" id="showLabels" checked>
                            <label for="showLabels">物理量标签</label>
                        </div>
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color electric"></div>
                        <span>电场 (E)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color magnetic"></div>
                        <span>磁场 (B)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color positive"></div>
                        <span>正电荷 (+)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color negative"></div>
                        <span>负电荷 (-)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color grid"></div>
                        <span>参考网格</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="instructions">
            <h2>📚 教学说明</h2>
            <p>本动画展示了振荡电偶极子如何产生并辐射电磁波的过程：</p>
            <ul>
                <li><span class="key-point">红色和橙色球体</span>分别代表正负电荷，它们以简谐运动方式振荡，形成振荡电偶极子。</li>
                <li><span class="key-point">蓝色线条/波面</span>表示电场线，其疏密代表电场强度大小。</li>
                <li><span class="key-point">绿色圆圈/环状面</span>表示磁感线，环绕在电场周围。</li>
                <li>在近场区（靠近偶极子），电场和磁场分布复杂；在远场区，形成稳定的<span class="key-point">横电磁波</span>。</li>
                <li>电磁波传播方向、电场方向、磁场方向三者<span class="key-point">两两垂直</span>，符合右手螺旋定则。</li>
                <li>调节频率可观察波长变化：频率越高，波长越短（λ = c/f）。</li>
            </ul>
            <p><span class="key-point">交互提示：</span>点击画布任意位置可放置虚拟探测器，显示该点的电场和磁场实时数值。</p>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = 500;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let animationId = null;
        let isPlaying = true;
        let time = 0;
        let speed = 1.0;
        
        // 视图模式：0=仅电场，1=仅磁场，2=电磁波
        let viewMode = 0;
        
        // 物理参数
        let frequency = 1.0; // Hz
        let dipoleMoment = 1.0;
        
        // 显示选项
        let showGrid = true;
        let showArrows = true;
        let showWavefront = false;
        let showLabels = true;
        
        // 探测器位置
        let detector = null;
        
        // 颜色定义
        const colors = {
            background: '#0c0e2a',
            electric: '#4FC3F7',
            magnetic: '#69F0AE',
            positive: '#FF5252',
            negative: '#FFAB40',
            grid: 'rgba(204, 204, 204, 0.3)',
            wavefront: 'rgba(255, 235, 59, 0.6)',
            text: '#e0e0e0',
            highlight: '#FFEB3B'
        };
        
        // 初始化UI控件
        document.getElementById('playBtn').addEventListener('click', () => {
            isPlaying = true;
            if (!animationId) animate();
        });
        
        document.getElementById('pauseBtn').addEventListener('click', () => {
            isPlaying = false;
        });
        
        document.getElementById('resetBtn').addEventListener('click', () => {
            time = 0;
            detector = null;
            document.getElementById('detectorInfo').classList.remove('active');
        });
        
        document.getElementById('speedSlider').addEventListener('input', (e) => {
            speed = parseFloat(e.target.value);
            document.getElementById('speedValue').textContent = speed.toFixed(1) + 'x';
        });
        
        document.getElementById('viewElectric').addEventListener('click', () => {
            viewMode = 0;
            updateViewButtons();
        });
        
        document.getElementById('viewMagnetic').addEventListener('click', () => {
            viewMode = 1;
            updateViewButtons();
        });
        
        document.getElementById('viewBoth').addEventListener('click', () => {
            viewMode = 2;
            updateViewButtons();
        });
        
        document.getElementById('freqSlider').addEventListener('input', (e) => {
            frequency = parseFloat(e.target.value);
            document.getElementById('freqValue').textContent = frequency.toFixed(1) + ' Hz';
        });
        
        document.getElementById('dipoleSlider').addEventListener('input', (e) => {
            dipoleMoment = parseFloat(e.target.value);
            document.getElementById('dipoleValue').textContent = dipoleMoment.toFixed(1);
        });
        
        document.getElementById('showGrid').addEventListener('change', (e) => {
            showGrid = e.target.checked;
        });
        
        document.getElementById('showArrows').addEventListener('change', (e) => {
            showArrows = e.target.checked;
        });
        
        document.getElementById('showWavefront').addEventListener('change', (e) => {
            showWavefront = e.target.checked;
        });
        
        document.getElementById('showLabels').addEventListener('change', (e) => {
            showLabels = e.target.checked;
        });
        
        // 点击Canvas放置探测器
        canvas.addEventListener('click', (e) => {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 转换为物理坐标（原点在画布中心）
            const physX = (x - canvas.width/2) / 50;
            const physY = (canvas.height/2 - y) / 50;
            
            detector = {x: physX, y: physY};
            
            // 更新探测器信息显示
            const detectorInfo = document.getElementById('detectorInfo');
            detectorInfo.classList.add('active');
            document.getElementById('detectorX').textContent = physX.toFixed(2);
            document.getElementById('detectorY').textContent = physY.toFixed(2);
        });
        
        // 更新视图按钮状态
        function updateViewButtons() {
            const electricBtn = document.getElementById('viewElectric');
            const magneticBtn = document.getElementById('viewMagnetic');
            const bothBtn = document.getElementById('viewBoth');
            
            electricBtn.classList.toggle('active', viewMode === 0);
            magneticBtn.classList.toggle('active', viewMode === 1);
            bothBtn.classList.toggle('active', viewMode === 2);
        }
        
        // 计算电场和磁场
        function calculateFields(x, y, t) {
            // 简化模型：振荡电偶极子位于原点，沿y轴方向振荡
            const r = Math.sqrt(x*x + y*y);
            if (r < 0.1) return {E: 0, B: 0, Ex: 0, Ey: 0, Bz: 0};
            
            const theta = Math.atan2(y, x);
            const k = 2 * Math.PI * frequency / 3; // 波数（简化，光速c=3单位）
            const omega = 2 * Math.PI * frequency;
            
            // 振荡偶极矩 p = p0 * cos(ωt)
            const p = dipoleMoment * Math.cos(omega * t);
            
            // 远场近似下的电场和磁场（简化模型）
            const E0 = p * Math.sin(theta) / (r * r);
            const B0 = p * Math.sin(theta) / (r * r);
            
            // 考虑波动性：cos(kr - ωt) / r
            const waveFactor = Math.cos(k * r - omega * t) / Math.max(r, 1);
            
            // 电场分量（在xy平面内，垂直于传播方向）
            const Ex = -E0 * Math.sin(theta) * waveFactor;
            const Ey = E0 * Math.cos(theta) * waveFactor;
            
            // 磁场分量（垂直于屏幕，z方向）
            const Bz = B0 * waveFactor;
            
            // 总场强（用于显示）
            const E = Math.sqrt(Ex*Ex + Ey*Ey);
            const B = Math.abs(Bz);
            
            return {E, B, Ex, Ey, Bz, r, theta};
        }
        
        // 绘制网格
        function drawGrid() {
            if (!showGrid) return;
            
            ctx.strokeStyle = colors.grid;
            ctx.lineWidth = 0.5;
            ctx.setLineDash([2, 2]);
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const gridSize = 50; // 像素/单位
            
            // 垂直线
            for (let x = -5; x <= 5; x++) {
                ctx.beginPath();
                ctx.moveTo(centerX + x * gridSize, 0);
                ctx.lineTo(centerX + x * gridSize, canvas.height);
                ctx.stroke();
            }
            
            // 水平线
            for (let y = -5; y <= 5; y++) {
                ctx.beginPath();
                ctx.moveTo(0, centerY + y * gridSize);
                ctx.lineTo(canvas.width, centerY + y * gridSize);
                ctx.stroke();
            }
            
            ctx.setLineDash([]);
            
            // 坐标轴
            ctx.strokeStyle = colors.text;
            ctx.lineWidth = 1.5;
            
            // X轴
            ctx.beginPath();
            ctx.moveTo(0, centerY);
            ctx.lineTo(canvas.width, centerY);
            ctx.stroke();
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(centerX, 0);
            ctx.lineTo(centerX, canvas.height);
            ctx.stroke();
            
            // 坐标轴标签
            if (showLabels) {
                ctx.fillStyle = colors.text;
                ctx.font = '12px Arial';
                ctx.fillText('x (传播方向)', canvas.width - 60, centerY - 10);
                ctx.fillText('y', centerX + 10, 20);
            }
        }
        
        // 绘制电偶极子
        function drawDipole(t) {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const gridSize = 50;
            
            // 计算电荷位置（沿y轴振荡）
            const amplitude = 0.8 * dipoleMoment;
            const omega = 2 * Math.PI * frequency;
            const dy = amplitude * Math.cos(omega * t);
            
            // 正电荷（红色）
            const posY = centerY - dy * gridSize;
            ctx.fillStyle = colors.positive;
            ctx.beginPath();
            ctx.arc(centerX, posY, 10, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = 'white';
            ctx.font = 'bold 12px Arial';
            ctx.fillText('+', centerX - 4, posY + 4);
            
            // 负电荷（橙色）
            const negY = centerY + dy * gridSize;
            ctx.fillStyle = colors.negative;
            ctx.beginPath();
            ctx.arc(centerX, negY, 10, 0, Math.PI * 2);
            ctx.fill();
            ctx.fillStyle = 'white';
            ctx.font = 'bold 12px Arial';
            ctx.fillText('-', centerX - 4, negY + 4);
            
            // 连接线
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(centerX, posY);
            ctx.lineTo(centerX, negY);
            ctx.stroke();
            
            // 标签
            if (showLabels) {
                ctx.fillStyle = colors.highlight;
                ctx.font = '14px Arial';
                ctx.fillText('振荡电偶极子', centerX - 50, Math.min(posY, negY) - 15);
            }
        }
        
        // 绘制电场
        function drawElectricField(t) {
            if (viewMode === 1) return; // 仅磁场视图时不绘制
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const gridSize = 50;
            
            ctx.strokeStyle = colors.electric;
            ctx.lineWidth = 1.5;
            ctx.globalAlpha = 0.7;
            
            // 绘制电场线/波面
            for (let r = 1; r <= 4; r += 0.5) {
                for (let theta = 0; theta < Math.PI * 2; theta += Math.PI / 8) {
                    const x = r * Math.cos(theta);
                    const y = r * Math.sin(theta);
                    
                    const fields = calculateFields(x, y, t);
                    if (fields.E < 0.01) continue;
                    
                    // 转换为画布坐标
                    const canvasX = centerX + x * gridSize;
                    const canvasY = centerY - y * gridSize;
                    
                    // 电场方向
                    const angle = Math.atan2(fields.Ey, fields.Ex);
                    const length = 15 * fields.E;
                    
                    // 绘制电场线片段
                    ctx.beginPath();
                    ctx.moveTo(canvasX, canvasY);
                    ctx.lineTo(
                        canvasX + length * Math.cos(angle),
                        canvasY - length * Math.sin(angle)
                    );
                    ctx.stroke();
                    
                    // 绘制箭头
                    if (showArrows && fields.E > 0.05) {
                        drawArrow(canvasX, canvasY, angle, length, colors.electric);
                    }
                }
            }
            
            // 绘制波前（等相位面）
            if (showWavefront && (viewMode === 0 || viewMode === 2)) {
                ctx.strokeStyle = colors.wavefront;
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                
                const omega = 2 * Math.PI * frequency;
                const phase = omega * t;
                
                for (let r = 1; r <= 4; r += 1) {
                    ctx.beginPath();
                    for (let theta = 0; theta < Math.PI * 2; theta += 0.1) {
                        const x = r * Math.cos(theta);
                        const y = r * Math.sin(theta);
                        
                        const canvasX = centerX + x * gridSize;
                        const canvasY = centerY - y * gridSize;
                        
                        if (theta === 0) {
                            ctx.moveTo(canvasX, canvasY);
                        } else {
                            ctx.lineTo(canvasX, canvasY);
                        }
                    }
                    ctx.closePath();
                    ctx.stroke();
                }
                
                ctx.setLineDash([]);
            }
            
            ctx.globalAlpha = 1.0;
        }
        
        // 绘制磁场
        function drawMagneticField(t) {
            if (viewMode === 0) return; // 仅电场视图时不绘制
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const gridSize = 50;
            
            ctx.strokeStyle = colors.magnetic;
            ctx.lineWidth = 1.5;
            ctx.globalAlpha = 0.7;
            
            // 绘制磁感线环
            for (let r = 1; r <= 4; r += 0.5) {
                for (let theta = 0; theta < Math.PI * 2; theta += Math.PI / 8) {
                    const x = r * Math.cos(theta);
                    const y = r * Math.sin(theta);
                    
                    const fields = calculateFields(x, y, t);
                    if (fields.B < 0.01) continue;
                    
                    // 转换为画布坐标
                    const canvasX = centerX + x * gridSize;
                    const canvasY = centerY - y * gridSize;
                    
                    // 磁场环半径与磁场强度成正比
                    const ringRadius = 8 * fields.B;
                    
                    // 绘制磁场环
                    ctx.beginPath();
                    ctx.arc(canvasX, canvasY, ringRadius, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 绘制磁场方向箭头（垂直于屏幕，用环上的箭头表示）
                    if (showArrows && fields.B > 0.05) {
                        // 根据Bz的正负决定箭头方向
                        const direction = fields.Bz > 0 ? 1 : -1;
                        const arrowAngle = theta + direction * Math.PI / 2;
                        
                        drawArrow(
                            canvasX + ringRadius * Math.cos(arrowAngle),
                            canvasY - ringRadius * Math.sin(arrowAngle),
                            arrowAngle + Math.PI / 2,
                            6,
                            colors.magnetic
                        );
                    }
                }
            }
            
            ctx.globalAlpha = 1.0;
        }
        
        // 绘制箭头
        function drawArrow(x, y, angle, length, color) {
            ctx.save();
            ctx.translate(x, y);
            ctx.rotate(-angle); // 注意：Canvas的y轴向下，所以需要调整
            
            ctx.fillStyle = color;
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(length, 0);
            ctx.lineTo(length - 6, -4);
            ctx.lineTo(length - 6, 4);
            ctx.closePath();
            ctx.fill();
            
            ctx.restore();
        }
        
        // 绘制探测器
        function drawDetector() {
            if (!detector) return;
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const gridSize = 50;
            
            // 转换为画布坐标
            const canvasX = centerX + detector.x * gridSize;
            const canvasY = centerY - detector.y * gridSize;
            
            // 绘制探测器图标
            ctx.fillStyle = colors.highlight;
            ctx.beginPath();
            ctx.arc(canvasX, canvasY, 8, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.strokeStyle = colors.highlight;
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(canvasX - 12, canvasY);
            ctx.lineTo(canvasX + 12, canvasY);
            ctx.moveTo(canvasX, canvasY - 12);
            ctx.lineTo(canvasX, canvasY + 12);
            ctx.stroke();
            
            // 计算并显示探测器处的场值
            const fields = calculateFields(detector.x, detector.y, time);
            
            // 更新探测器信息显示
            document.getElementById('detectorE').textContent = fields.E.toFixed(2);
            document.getElementById('detectorB').textContent = fields.B.toFixed(2);
            
            // 计算相位差（理想情况下应为0）
            const phaseDiff = 0; // 简化模型中同相
            document.getElementById('detectorPhase').textContent = phaseDiff.toFixed(2);
        }
        
        // 绘制物理量标签
        function drawLabels() {
            if (!showLabels) return;
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            
            // 波长标签
            const wavelength = 3 / frequency; // λ = c/f，c=3单位
            ctx.fillText(`波长 λ = ${wavelength.toFixed(2)} 单位`, 20, 30);
            
            // 频率标签
            ctx.fillText(`频率 f = ${frequency.toFixed(2)} Hz`, 20, 55);
            
            // 传播方向指示
            ctx.fillStyle = colors.highlight;
            ctx.font = 'bold 16px Arial';
            ctx.fillText('→ 电磁波传播方向', centerX + 100, centerY - 20);
            
            // 右手螺旋定则提示
            ctx.fillStyle = colors.text;
            ctx.font = '12px Arial';
            ctx.fillText('E ⊥ B ⊥ k (右手螺旋定则)', centerX - 100, 30);
        }
        
        // 绘制函数
        function draw() {
            // 清空画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制各个组件
            drawGrid();
            drawDipole(time);
            
            if (viewMode === 0 || viewMode === 2) {
                drawElectricField(time);
            }
            
            if (viewMode === 1 || viewMode === 2) {
                drawMagneticField(time);
            }
            
            drawDetector();
            drawLabels();
            
            // 绘制时间指示
            ctx.fillStyle = colors.text;
            ctx.font = '14px Arial';
            ctx.fillText(`时间 t = ${time.toFixed(2)} s`, canvas.width - 150, 30);
        }
        
        // 动画循环
        function animate() {
            if (isPlaying) {
                time += 0.02 * speed;
            }
            
            draw();
            
            animationId = requestAnimationFrame(animate);
        }
        
        // 启动动画
        animate();
        
        // 初始更新视图按钮状态
        updateViewButtons();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 电磁波的产生与传播 - 交互式教学动画使用指南

欢迎使用“电磁波的产生与传播”交互式教学动画！本动画旨在通过直观、动态的可视化方式，帮助您深入理解振荡电偶极子如何产生并辐射电磁波这一重要的物理现象。无论您是高中物理学生、大学普通物理学习者，还是对电磁学感兴趣的爱好者，本工具都将为您提供独特的探索体验。

---

### 一、功能概览

本动画采用**分层可视化**和**交互控制**的设计理念，将抽象的电磁波产生过程转化为直观的视觉体验。您将能够：

1. **观察动态过程**：实时观看电荷振荡如何激发电场和磁场，并形成向外传播的电磁波
2. **控制实验参数**：调节物理参数，观察现象变化规律
3. **切换观察视角**：从不同角度理解电场、磁场及其相互作用
4. **进行虚拟测量**：在任意位置探测场强数值，建立定量概念

---

### 二、主要功能详解

#### 1. 动画控制区（📊 动画控制）
- **播放/暂停**：控制动画运行状态，便于仔细观察关键瞬间
- **重置**：将动画恢复到初始状态，时间归零
- **速度调节**：通过滑块控制动画播放速度（0.1x - 3.0x），适合不同学习节奏

#### 2. 视图选择区（👁️ 视图选择）
- **仅电场视图**：专注观察蓝色电场线的分布和变化
- **仅磁场视图**：专注观察绿色磁感线的环绕和振荡
- **电磁波视图**：同时显示电场和磁场，观察完整的电磁波结构

#### 3. 参数调节区（⚙️ 参数调节）
- **振荡频率 (f)**：调节电偶极子的振荡快慢
  - *教学提示*：观察频率变化如何影响波长（λ = c/f）
  - *实验发现*：频率越高 → 波长越短，波峰更密集
- **偶极矩大小**：调节电荷振荡的幅度
  - *教学提示*：观察辐射强度与偶极矩的关系
  - *实验发现*：偶极矩越大 → 辐射的电磁波越强

#### 4. 显示选项区（🔧 显示选项）
- **空间网格**：显示参考坐标系，帮助建立空间概念
- **场线箭头**：显示电场和磁场的方向指示
- **波前标记**：显示等相位面，理解波的传播特性
- **物理量标签**：显示波长、频率等关键物理量

#### 5. 虚拟探测器功能
- **放置探测器**：点击画布任意位置，放置虚拟探测器
- **实时数据显示**：显示该点的电场强度(E)、磁场强度(B)和相位关系
- **动态追踪**：随着动画运行，数据实时更新

---

### 三、设计特色与教学价值

#### 1. 分层可视化设计
- **近场与远场区分**：清晰展示靠近偶极子的复杂场分布和远处的规则平面波
- **颜色编码系统**：
  - 🔵 蓝色 = 电场（E场）
  - 🟢 绿色 = 磁场（B场）
  - 🔴 红色 = 正电荷
  - 🟠 橙色 = 负电荷
- **动态场线表示**：场线疏密表示场强大小，运动方向表示场的变化趋势

#### 2. 三维空间感的二维呈现
- 通过网格和透视效果，在二维平面上建立三维空间概念
- 电场在平面内振荡，磁场垂直于平面（用环绕的圆圈表示）

#### 3. 物理准确性保障
- 基于振荡电偶极子辐射的基本物理模型
- 正确体现电场、磁场、传播方向的三维正交关系
- 符合右手螺旋定则的场方向设定

---

### 四、核心教学要点

#### 1. 电磁波的产生机制
- **源头**：振荡的电荷（电偶极子）是电磁波的源
- **过程**：变化的电场产生磁场，变化的磁场产生电场，相互激发
- **脱离**：电磁场脱离波源，在空间中独立传播

#### 2. 电磁波的基本特性
- **横波特性**：振动方向与传播方向垂直
- **正交关系**：E ⊥ B ⊥ k（传播方向）
- **同相振荡**：电场和磁场同时达到最大值和最小值
- **速度恒定**：在真空中以光速传播（c ≈ 3×10⁸ m/s）

#### 3. 重要物理关系
- **波长-频率关系**：λ = c/f（调节频率滑块直观验证）
- **辐射强度**：与频率的四次方和偶极矩的平方成正比
- **方向特性**：沿偶极子轴线方向辐射最弱，垂直方向最强

---

### 五、使用建议与学习路径

#### 建议学习流程：

**第一阶段：观察与熟悉（约5分钟）**
1. 保持默认设置，点击“播放”观察完整过程
2. 分别切换三种视图模式，理解电场和磁场的单独表现
3. 使用“暂停”功能，在关键位置仔细分析场分布

**第二阶段：探索与实验（约10分钟）**
1. 调节频率滑块，观察波长变化，验证 λ ∝ 1/f
2. 调节偶极矩大小，观察辐射强度变化
3. 在不同位置放置探测器，比较近场和远场的场强差异

**第三阶段：分析与总结（约5分钟）**
1. 打开“波前标记”，观察等相位面的传播
2. 结合右侧教学说明，对照动画验证每个知识点
3. 思考：如果偶极子沿x轴振荡，电磁波会如何变化？

#### 教学场景建议：
- **课堂演示**：教师可逐步展示不同参数下的现象，引导学生发现规律
- **自主学习**：学生可按照建议流程自主探索，建立直观理解
- **小组探究**：分组设置不同参数，比较结果，讨论物理规律
- **复习巩固**：在学习相关理论后，通过动画加深对抽象概念的理解

---

### 六、技术提示

1. **最佳观看环境**：在光线较暗的环境下，颜色对比更明显
2. **浏览器要求**：建议使用Chrome、Edge等现代浏览器
3. **性能优化**：如果动画卡顿，可适当降低动画速度或关闭部分显示选项
4. **全屏模式**：按F11键可进入全屏模式，获得更佳观看体验

---

### 七、扩展思考

在掌握基本操作后，您可以尝试思考以下问题：

1. 如果电偶极子停止振荡，电磁波会立即消失吗？为什么？
2. 实际天线（如无线电发射塔）与这个简化模型有何异同？
3. 电磁波的能量是如何传播的？与机械波的能量传播有何不同？
4. 如何从麦克斯韦方程组推导出电磁波的存在？

---

**祝您探索愉快！** 通过这个交互式动画，我们希望您不仅能“看到”电磁波，更能“理解”电磁波，感受物理学的简洁与美妙。如果您有任何发现或疑问，欢迎与同学、老师一起讨论分享！

*“从振荡的电荷到穿越宇宙的电磁波，科学让我们看见不可见的世界。”*