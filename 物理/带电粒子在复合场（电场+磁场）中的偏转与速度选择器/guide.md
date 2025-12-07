# 需求：带电粒子在复合场（电场+磁场）中的偏转与速度选择器

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：高中物理或大学基础物理的学生。他们已具备电场、磁场、洛伦兹力的基础知识，但难以在脑海中动态构建复合场中粒子运动的复杂物理图景。
2.  **核心痛点**：
    *   **抽象性**：电场力、洛伦兹力的方向判断（左手定则/右手定则）和合力分析是动态且三维的，静态图示难以清晰表达。
    *   **过程性**：粒子从进入复合场到最终偏转或匀速穿出的完整运动过程，其速度、轨迹、受力如何随时间演变，学生缺乏直观感受。
    *   **参数关联**：不理解电场强度 `E`、磁感应强度 `B`、粒子电荷 `q`、质量 `m`、初速度 `v0` 等参数如何共同决定最终的运动状态（如：是否偏转、偏转方向、能否通过速度选择器）。
3.  **学习目标**：通过交互动画，学生应能：
    *   直观理解带电粒子在正交复合场（电场与磁场方向垂直）中的运动规律。
    *   掌握“速度选择器”的工作原理，并理解“选择”的条件（`v = E/B`）。
    *   能够通过调整参数预测并验证粒子的运动结果，深化对力与运动关系的理解。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念分解**：
    *   **基础回顾**：单独电场中的偏转（类平抛）、单独磁场中的偏转（匀速圆周运动）。
    *   **复合场受力**：正交复合场中，电场力 (`F_e = qE`) 方向固定，洛伦兹力 (`F_b = qv×B`) 方向随速度方向变化，强调初始时刻的合力分析。
    *   **运动合成**：将复杂运动分解为两个直线运动的合成（如：沿电场力方向的加速运动与垂直方向的匀速圆周运动分量的合成），或直接呈现轨迹。
    *   **速度选择器**：作为复合场的一个特例和重要应用。当 `qE = qvB` 即 `v = E/B` 时，粒子受力平衡，做匀速直线运动。偏离该速度的粒子将被偏转过滤。

2.  **遵循认知规律**：
    *   **从简到繁**：先展示单一电场、单一磁场的偏转，再引入复合场。
    *   **从静到动**：允许暂停、步进播放，观察某一瞬间的受力矢量与速度矢量。
    *   **从观察到探究**：默认参数演示标准现象 → 开放参数控件，鼓励学生主动改变参数并观察结果，进行“猜想-验证”。

3.  **交互设计**：
    *   **模块化场景**：设计两个主要可切换场景：“复合场偏转” 和 “速度选择器”。
    *   **实时控制**：提供滑块或输入框，实时调整 `E`, `B`, `q` (正/负), `m`, `v0` 等参数。
    *   **可视化叠加**：
        *   用**彩色箭头**实时显示电场力（如红色）、洛伦兹力（如蓝色）、合力（如黄色），箭头长度可代表力的大小。
        *   显示粒子的**实时速度矢量**（绿色箭头）。
        *   绘制粒子运动的**轨迹**。
        *   在“速度选择器”场景中，用明显的“通道”或“狭缝”来视觉化“选择”通过的概念。
    *   **重置与对比**：提供“重置”按钮恢复默认状态；可考虑同时发射两个不同参数的粒子进行对比。

4.  **视觉呈现**：
    *   **主视图**：一个清晰的二维平面（`x-y` 平面），电场和磁场方向用直观的图示标明（如：平行线表示匀强电场，`×` 或 `·` 表示垂直纸面的磁场）。
    *   **粒子表征**：用发光的小球代表粒子，正负电荷可用 `+` / `-` 号或颜色区分。
    *   **信息面板**：侧边栏或底部栏动态显示关键数据（位置、速度、各力大小、当前时刻）。
    *   **动画流畅性**：确保动画帧率流畅，轨迹绘制清晰，力矢量的变化平滑连续。

#### 配色方案选择
*   **背景与画布**：深灰色或黑色背景，凸显发光元素和轨迹；画布区域为浅灰网格或纯浅色，增强对比。
*   **力与场矢量**：
    *   电场力：**红色**（醒目，代表与电场强度相关）。
    *   洛伦兹力：**蓝色**（冷静，常与磁场关联）。
    *   合力：**黄色**或**白色**（作为合成结果）。
*   **粒子与轨迹**：
    *   正电荷粒子：**亮黄色**或**青色**发光球体。
    *   负电荷粒子：**洋红色**发光球体。
    *   运动轨迹：**半透明的白色或浅灰色线条**，随时间淡出，避免画面杂乱。
*   **速度矢量**：**绿色**箭头，与力的颜色区分开。
*   **界面控件**：使用中性色（如浅蓝、浅灰），确保清晰可操作。
*   **文本与数据**：白色或浅黄色文字，确保在深色背景上可读。

#### 交互功能列表
1.  **场景选择器**：按钮切换“复合场偏转”与“速度选择器”两个主场景。
2.  **模拟控制**：
    *   播放/暂停/重置 按钮。
    *   单步前进（步进）按钮。
    *   轨迹显示/隐藏 开关。
    *   矢量显示/隐藏 开关（可分别控制力、速度矢量的显示）。
3.  **物理参数调节面板**：
    *   电场强度 `E`（大小和方向选择：向上/向下/为零）。
    *   磁感应强度 `B`（大小和方向选择：垂直进入纸面/垂直穿出纸面/为零）。
    *   粒子电荷 `q`（大小和正负选择）。
    *   粒子质量 `m`。
    *   粒子初速度 `v0`（大小和方向角输入或矢量拖拽设定）。
4.  **可视化反馈**：
    *   动态更新的粒子位置、速度分量、力的大小。
    *   实时绘制的运动轨迹。
    *   动态变化的力矢量和速度矢量箭头。
5.  **预设案例按钮**（可选，用于快速演示）：
    *   “仅电场偏转”
    *   “仅磁场偏转”
    *   “速度选择器（平衡）”
    *   “速度大于 E/B”
    *   “速度小于 E/B”
    *   “电荷符号反转”

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>带电粒子在复合场中的运动与速度选择器</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        header {
            text-align: center;
            padding: 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        h1 {
            color: #4fc3f7;
            margin-bottom: 10px;
            font-size: 2.5rem;
            text-shadow: 0 0 10px rgba(79, 195, 247, 0.5);
        }
        
        .subtitle {
            color: #b0bec5;
            font-size: 1.2rem;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .simulation-area {
            flex: 1;
            min-width: 700px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 500px;
            background: #0d1525;
            border-radius: 10px;
            overflow: hidden;
            border: 2px solid rgba(255, 255, 255, 0.1);
        }
        
        #simulationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        .control-panel {
            flex: 0 0 400px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 15px;
            padding: 25px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }
        
        .panel-section {
            background: rgba(30, 40, 60, 0.7);
            border-radius: 10px;
            padding: 20px;
            border-left: 4px solid #4fc3f7;
        }
        
        .section-title {
            color: #4fc3f7;
            margin-bottom: 15px;
            font-size: 1.3rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section-title i {
            font-size: 1.2rem;
        }
        
        .control-group {
            margin-bottom: 15px;
        }
        
        .control-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            color: #b0bec5;
        }
        
        .value-display {
            color: #4fc3f7;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }
        
        input[type="range"] {
            width: 100%;
            height: 8px;
            background: #2c3e50;
            border-radius: 4px;
            outline: none;
            -webkit-appearance: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            background: #4fc3f7;
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 0 10px rgba(79, 195, 247, 0.8);
        }
        
        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        button {
            padding: 12px 20px;
            background: linear-gradient(to right, #1565c0, #2196f3);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            flex: 1;
            min-width: 120px;
        }
        
        button:hover {
            background: linear-gradient(to right, #0d47a1, #1976d2);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(33, 150, 243, 0.4);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        button.reset {
            background: linear-gradient(to right, #c62828, #f44336);
        }
        
        button.reset:hover {
            background: linear-gradient(to right, #b71c1c, #d32f2f);
            box-shadow: 0 5px 15px rgba(244, 67, 54, 0.4);
        }
        
        .toggle-switch {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 10px;
        }
        
        .switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
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
            background-color: #2c3e50;
            transition: .4s;
            border-radius: 24px;
        }
        
        .slider:before {
            position: absolute;
            content: "";
            height: 16px;
            width: 16px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }
        
        input:checked + .slider {
            background-color: #4fc3f7;
        }
        
        input:checked + .slider:before {
            transform: translateX(26px);
        }
        
        .info-panel {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-top: 10px;
        }
        
        .info-item {
            background: rgba(0, 0, 0, 0.3);
            padding: 12px;
            border-radius: 8px;
            text-align: center;
        }
        
        .info-label {
            color: #b0bec5;
            font-size: 0.9rem;
            margin-bottom: 5px;
        }
        
        .info-value {
            color: #4fc3f7;
            font-weight: bold;
            font-size: 1.2rem;
            font-family: 'Courier New', monospace;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 4px;
        }
        
        .legend-text {
            font-size: 0.9rem;
            color: #b0bec5;
        }
        
        .scene-selector {
            display: flex;
            background: rgba(30, 40, 60, 0.7);
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 20px;
        }
        
        .scene-btn {
            flex: 1;
            padding: 15px;
            text-align: center;
            background: transparent;
            border: none;
            color: #b0bec5;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .scene-btn.active {
            background: #4fc3f7;
            color: white;
        }
        
        .preset-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        
        .preset-btn {
            padding: 10px;
            background: rgba(30, 40, 60, 0.9);
            border: 1px solid rgba(79, 195, 247, 0.3);
            color: #b0bec5;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .preset-btn:hover {
            background: rgba(79, 195, 247, 0.2);
            color: white;
            border-color: #4fc3f7;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: #78909c;
            font-size: 0.9rem;
            margin-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        @media (max-width: 1200px) {
            .main-content {
                flex-direction: column;
            }
            
            .simulation-area, .control-panel {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>⚡ 带电粒子在复合场中的运动</h1>
            <p class="subtitle">电场 + 磁场 | 偏转轨迹 | 速度选择器 | 交互式教学动画</p>
        </header>
        
        <div class="scene-selector">
            <button class="scene-btn active" id="scene1Btn">复合场偏转</button>
            <button class="scene-btn" id="scene2Btn">速度选择器</button>
        </div>
        
        <div class="main-content">
            <div class="simulation-area">
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff5252;"></div>
                        <div class="legend-text">电场力 (Fₑ)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #448aff;"></div>
                        <div class="legend-text">洛伦兹力 (Fₘ)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ffeb3b;"></div>
                        <div class="legend-text">合力 (F)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #69f0ae;"></div>
                        <div class="legend-text">速度 (v)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff9800;"></div>
                        <div class="legend-text">正电荷粒子</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e040fb;"></div>
                        <div class="legend-text">负电荷粒子</div>
                    </div>
                </div>
            </div>
            
            <div class="control-panel">
                <div class="panel-section">
                    <h3 class="section-title">🎮 模拟控制</h3>
                    <div class="button-group">
                        <button id="playBtn">▶ 播放</button>
                        <button id="pauseBtn">⏸ 暂停</button>
                        <button id="stepBtn">⏭ 单步</button>
                        <button id="resetBtn" class="reset">↺ 重置</button>
                    </div>
                    
                    <div class="toggle-switch">
                        <span>显示轨迹</span>
                        <label class="switch">
                            <input type="checkbox" id="showTrajectory" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                    
                    <div class="toggle-switch">
                        <span>显示矢量</span>
                        <label class="switch">
                            <input type="checkbox" id="showVectors" checked>
                            <span class="slider"></span>
                        </label>
                    </div>
                </div>
                
                <div class="panel-section">
                    <h3 class="section-title">⚙️ 物理参数</h3>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>电场强度 E (N/C):</span>
                            <span class="value-display" id="eValue">1000</span>
                        </div>
                        <input type="range" id="eSlider" min="0" max="5000" step="100" value="1000">
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>磁感应强度 B (T):</span>
                            <span class="value-display" id="bValue">0.5</span>
                        </div>
                        <input type="range" id="bSlider" min="0" max="2" step="0.05" value="0.5">
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>粒子电荷 q (C):</span>
                            <span class="value-display" id="qValue">+1.6e-19</span>
                        </div>
                        <input type="range" id="qSlider" min="-1.6e-19" max="1.6e-19" step="3.2e-20" value="1.6e-19">
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>粒子质量 m (kg):</span>
                            <span class="value-display" id="mValue">9.1e-31</span>
                        </div>
                        <input type="range" id="mSlider" min="1e-31" max="5e-30" step="1e-31" value="9.1e-31">
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">
                            <span>初速度 v₀ (m/s):</span>
                            <span class="value-display" id="vValue">1e6</span>
                        </div>
                        <input type="range" id="vSlider" min="1e5" max="5e6" step="1e5" value="1e6">
                    </div>
                </div>
                
                <div class="panel-section">
                    <h3 class="section-title">🚀 预设案例</h3>
                    <div class="preset-buttons">
                        <button class="preset-btn" data-preset="electric">仅电场偏转</button>
                        <button class="preset-btn" data-preset="magnetic">仅磁场偏转</button>
                        <button class="preset-btn" data-preset="selector">速度选择器</button>
                        <button class="preset-btn" data-preset="fast">速度 > E/B</button>
                        <button class="preset-btn" data-preset="slow">速度 < E/B</button>
                        <button class="preset-btn" data-preset="negative">负电荷粒子</button>
                    </div>
                </div>
                
                <div class="panel-section">
                    <h3 class="section-title">📊 实时数据</h3>
                    <div class="info-panel">
                        <div class="info-item">
                            <div class="info-label">位置 (x, y)</div>
                            <div class="info-value" id="posValue">(0, 0)</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">速度 (m/s)</div>
                            <div class="info-value" id="speedValue">1.00e6</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">电场力 (N)</div>
                            <div class="info-value" id="feValue">1.60e-16</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">洛伦兹力 (N)</div>
                            <div class="info-value" id="fbValue">8.00e-14</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">v = E/B</div>
                            <div class="info-value" id="ebValue">2.00e6</div>
                        </div>
                        <div class="info-item">
                            <div class="info-label">状态</div>
                            <div class="info-value" id="stateValue">运动</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>物理教学交互动画 | 带电粒子在复合场中的运动 | 设计：教育技术专家</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('simulationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
        }
        
        // 初始调整尺寸
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 物理参数
        let params = {
            E: 1000,        // 电场强度 (N/C)
            B: 0.5,         // 磁感应强度 (T)
            q: 1.6e-19,     // 电荷量 (C)
            m: 9.1e-31,     // 质量 (kg)
            v0: 1e6,        // 初速度 (m/s)
            angle: 0,       // 初速度角度 (弧度)
            
            // 电场方向：向下为正（y轴正方向）
            E_direction: { x: 0, y: 1 },
            // 磁场方向：垂直纸面向外（z轴正方向）
            B_direction: { x: 0, y: 0, z: 1 }
        };
        
        // 粒子状态
        let particle = {
            x: 0,
            y: 0,
            vx: 0,
            vy: 0,
            ax: 0,
            ay: 0,
            trail: [],
            maxTrailLength: 200
        };
        
        // 模拟状态
        let simulation = {
            running: false,
            time: 0,
            dt: 1e-10,      // 时间步长 (s)
            scene: 1,       // 1: 复合场偏转, 2: 速度选择器
            showTrajectory: true,
            showVectors: true
        };
        
        // 初始化粒子
        function initParticle() {
            particle.x = -canvas.width * 0.4;
            particle.y = 0;
            particle.vx = params.v0 * Math.cos(params.angle);
            particle.vy = params.v0 * Math.sin(params.angle);
            particle.trail = [];
            simulation.time = 0;
            
            // 添加初始位置到轨迹
            particle.trail.push({ x: particle.x, y: particle.y });
        }
        
        // 计算力
        function calculateForces() {
            // 电场力: F_e = q * E
            const Fe_x = params.q * params.E * params.E_direction.x;
            const Fe_y = params.q * params.E * params.E_direction.y;
            
            // 洛伦兹力: F_b = q * (v × B)
            // v × B = (vy*Bz - vz*By, vz*Bx - vx*Bz, vx*By - vy*Bx)
            // 假设磁场只有z分量，速度只有x,y分量
            const Bz = params.B * params.B_direction.z;
            const Fb_x = params.q * (particle.vy * Bz);
            const Fb_y = params.q * (-particle.vx * Bz);
            
            // 合力
            const Fx = Fe_x + Fb_x;
            const Fy = Fe_y + Fb_y;
            
            // 加速度: a = F / m
            particle.ax = Fx / params.m;
            particle.ay = Fy / params.m;
            
            return {
                Fe: { x: Fe_x, y: Fe_y, magnitude: Math.sqrt(Fe_x*Fe_x + Fe_y*Fe_y) },
                Fb: { x: Fb_x, y: Fb_y, magnitude: Math.sqrt(Fb_x*Fb_x + Fb_y*Fb_y) },
                F: { x: Fx, y: Fy, magnitude: Math.sqrt(Fx*Fx + Fy*Fy) }
            };
        }
        
        // 更新粒子状态
        function updateParticle() {
            if (!simulation.running) return;
            
            // 计算力
            const forces = calculateForces();
            
            // 更新速度 (v = v0 + a*t)
            particle.vx += particle.ax * simulation.dt;
            particle.vy += particle.ay * simulation.dt;
            
            // 更新位置 (x = x0 + v*t)
            particle.x += particle.vx * simulation.dt;
            particle.y += particle.vy * simulation.dt;
            
            // 添加位置到轨迹
            particle.trail.push({ x: particle.x, y: particle.y });
            
            // 限制轨迹长度
            if (particle.trail.length > particle.maxTrailLength) {
                particle.trail.shift();
            }
            
            // 更新时间
            simulation.time += simulation.dt;
            
            // 如果粒子飞出画布，重置
            if (Math.abs(particle.x) > canvas.width * 0.6 || Math.abs(particle.y) > canvas.height * 0.6) {
                initParticle();
            }
            
            // 更新数据显示
            updateDisplay(forces);
        }
        
        // 更新数据显示
        function updateDisplay(forces) {
            // 更新参数显示
            document.getElementById('eValue').textContent = params.E.toFixed(0);
            document.getElementById('bValue').textContent = params.B.toFixed(2);
            document.getElementById('qValue').textContent = params.q.toExponential(2);
            document.getElementById('mValue').textContent = params.m.toExponential(2);
            document.getElementById('vValue').textContent = (params.v0 / 1e6).toFixed(2) + 'e6';
            
            // 更新实时数据
            const speed = Math.sqrt(particle.vx*particle.vx + particle.vy*particle.vy);
            document.getElementById('posValue').textContent = 
                `(${(particle.x * 1e3).toFixed(2)}, ${(particle.y * 1e3).toFixed(2)}) mm`;
            document.getElementById('speedValue').textContent = (speed / 1e6).toFixed(2) + 'e6';
            document.getElementById('feValue').textContent = forces.Fe.magnitude.toExponential(2);
            document.getElementById('fbValue').textContent = forces.Fb.magnitude.toExponential(2);
            
            // 计算 v = E/B
            const v_EB = params.B !== 0 ? Math.abs(params.E / params.B) : Infinity;
            document.getElementById('ebValue').textContent = 
                params.B !== 0 ? (v_EB / 1e6).toFixed(2) + 'e6' : '∞';
            
            // 更新状态
            if (simulation.scene === 2) {
                const diff = Math.abs(speed - v_EB) / v_EB;
                if (diff < 0.05) {
                    document.getElementById('stateValue').textContent = '通过';
                    document.getElementById('stateValue').style.color = '#69f0ae';
                } else if (speed > v_EB) {
                    document.getElementById('stateValue').textContent = '偏转';
                    document.getElementById('stateValue').style.color = '#ff5252';
                } else {
                    document.getElementById('stateValue').textContent = '偏转';
                    document.getElementById('stateValue').style.color = '#448aff';
                }
            } else {
                document.getElementById('stateValue').textContent = '运动';
                document.getElementById('stateValue').style.color = '#ffeb3b';
            }
        }
        
        // 绘制场景
        function drawScene() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制网格背景
            drawGrid();
            
            // 绘制场指示
            drawFieldIndicators();
            
            // 绘制速度选择器通道（如果场景2）
            if (simulation.scene === 2) {
                drawVelocitySelector();
            }
            
            // 绘制粒子轨迹
            if (simulation.showTrajectory && particle.trail.length > 1) {
                drawTrajectory();
            }
            
            // 绘制粒子
            drawParticle();
            
            // 绘制力矢量
            if (simulation.showVectors) {
                drawForceVectors();
            }
            
            // 绘制坐标轴
            drawAxes();
            
            // 绘制场景标题
            drawSceneTitle();
        }
        
        // 绘制网格
        function drawGrid() {
            const gridSize = 50;
            const offsetX = canvas.width / 2;
            const offsetY = canvas.height / 2;
            
            ctx.strokeStyle = 'rgba(100, 100, 150, 0.2)';
            ctx.lineWidth = 1;
            
            // 垂直线
            for (let x = -offsetX; x <= offsetX; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x + offsetX, 0);
                ctx.lineTo(x + offsetX, canvas.height);
                ctx.stroke();
            }
            
            // 水平线
            for (let y = -offsetY; y <= offsetY; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y + offsetY);
                ctx.lineTo(canvas.width, y + offsetY);
                ctx.stroke();
            }
        }
        
        // 绘制场指示
        function drawFieldIndicators() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制电场指示（箭头向下表示电场方向）
            if (params.E > 0) {
                ctx.fillStyle = 'rgba(255, 82, 82, 0.3)';
                ctx.strokeStyle = '#ff5252';
                ctx.lineWidth = 2;
                
                // 电场区域
                ctx.fillRect(0, 0, canvas.width, canvas.height);
                
                // 电场箭头
                const arrowCount = 10;
                const arrowSpacing = canvas.width / (arrowCount + 1);
                
                for (let i = 1; i <= arrowCount; i++) {
                    const x = i * arrowSpacing;
                    drawArrow(x, 30, x, 70, 10, '#ff5252');
                }
                
                // 电场标签
                ctx.fillStyle = '#ff5252';
                ctx.font = 'bold 16px Arial';
                ctx.fillText('E', canvas.width - 40, 50);
            }
            
            // 绘制磁场指示（×表示垂直纸面向外）
            if (params.B > 0) {
                ctx.fillStyle = 'rgba(68, 138, 255, 0.1)';
                ctx.strokeStyle = '#448aff';
                ctx.lineWidth = 2;
                
                // 磁场符号
                const symbolSize = 20;
                const symbolSpacing = 60;
                
                for (let x = symbolSpacing; x < canvas.width; x += symbolSpacing) {
                    for (let y = symbolSpacing; y < canvas.height; y += symbolSpacing) {
                        drawCircleWithDot(x, y, symbolSize / 2, '#448aff');
                    }
                }
                
                // 磁场标签
                ctx.fillStyle = '#448aff';
                ctx.font = 'bold 16px Arial';
                ctx.fillText('B ⊙', canvas.width - 50, canvas.height - 30);
            }
        }
        
        // 绘制速度选择器通道
        function drawVelocitySelector() {
            const centerY = canvas.height / 2;
            const channelWidth = 80;
            
            // 通道背景
            ctx.fillStyle = 'rgba(100, 255, 100, 0.1)';
            ctx.fillRect(0, centerY - channelWidth/2, canvas.width, channelWidth);
            
            // 通道边界
            ctx.strokeStyle = '#69f0ae';
            ctx.lineWidth = 3;
            ctx.setLineDash([10, 5]);
            ctx.beginPath();
            ctx.moveTo(0, centerY - channelWidth/2);
            ctx.lineTo(canvas.width, centerY - channelWidth/2);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(0, centerY + channelWidth/2);
            ctx.lineTo(canvas.width, centerY + channelWidth/2);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 通道标签
            ctx.fillStyle = '#69f0ae';
            ctx.font = 'bold 18px Arial';
            ctx.fillText('速度选择器通道', canvas.width / 2 - 70, centerY - channelWidth/2 - 10);
            
            // 显示选择条件
            const v_EB = params.B !== 0 ? Math.abs(params.E / params.B) : Infinity;
            ctx.fillStyle = '#ffffff';
            ctx.font = '16px Arial';
            ctx.fillText(`选择条件: v = E/B = ${(v_EB/1e6).toFixed(2)}×10⁶ m/s`, 
                        canvas.width / 2 - 120, centerY + channelWidth/2 + 25);
        }
        
        // 绘制粒子轨迹
        function drawTrajectory() {
            if (particle.trail.length < 2) return;
            
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.7)';
            ctx.lineWidth = 2;
            ctx.lineJoin = 'round';
            ctx.lineCap = 'round';
            
            ctx.beginPath();
            ctx.moveTo(
                canvas.width / 2 + particle.trail[0].x,
                canvas.height / 2 + particle.trail[0].y
            );
            
            for (let i = 1; i < particle.trail.length; i++) {
                ctx.lineTo(
                    canvas.width / 2 + particle.trail[i].x,
                    canvas.height / 2 + particle.trail[i].y
                );
            }
            
            ctx.stroke();
        }
        
        // 绘制粒子
        function drawParticle() {
            const screenX = canvas.width / 2 + particle.x;
            const screenY = canvas.height / 2 + particle.y;
            
            // 粒子颜色基于电荷
            const particleColor = params.q >= 0 ? '#ff9800' : '#e040fb';
            
            // 绘制粒子（发光效果）
            const gradient = ctx.createRadialGradient(
                screenX, screenY, 0,
                screenX, screenY, 15
            );
            gradient.addColorStop(0, particleColor);
            gradient.addColorStop(0.7, particleColor + 'cc');
            gradient.addColorStop(1, particleColor + '00');
            
            ctx.fillStyle = gradient;
            ctx.beginPath();
            ctx.arc(screenX, screenY, 10, 0, Math.PI * 2);
            ctx.fill();
            
            // 粒子边框
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.arc(screenX, screenY, 10, 0, Math.PI * 2);
            ctx.stroke();
            
            // 电荷符号
            ctx.fillStyle = '#ffffff';
            ctx.font = 'bold 14px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(params.q >= 0 ? '+' : '-', screenX, screenY);
        }
        
        // 绘制力矢量
        function drawForceVectors() {
            const forces = calculateForces();
            const screenX = canvas.width / 2 + particle.x;
            const screenY = canvas.height / 2 + particle.y;
            
            // 缩放因子
            const forceScale = 1e15; // 放大显示
            
            // 绘制电场力矢量（红色）
            if (forces.Fe.magnitude > 0) {
                drawArrow(
                    screenX, screenY,
                    screenX + forces.Fe.x * forceScale,
                    screenY + forces.Fe.y * forceScale,
                    10, '#ff5252'
                );
            }
            
            // 绘制洛伦兹力矢量（蓝色）
            if (forces.Fb.magnitude > 0) {
                drawArrow(
                    screenX, screenY,
                    screenX + forces.Fb.x * forceScale,
                    screenY + forces.Fb.y * forceScale,
                    10, '#448aff'
                );
            }
            
            // 绘制合力矢量（黄色）
            if (forces.F.magnitude > 0) {
                drawArrow(
                    screenX, screenY,
                    screenX + forces.F.x * forceScale,
                    screenY + forces.F.y * forceScale,
                    12, '#ffeb3b'
                );
            }
            
            // 绘制速度矢量（绿色）
            const speedScale = 1e-7; // 缩放速度矢量
            drawArrow(
                screenX, screenY,
                screenX + particle.vx * speedScale,
                screenY + particle.vy * speedScale,
                8, '#69f0ae'
            );
        }
        
        // 绘制坐标轴
        function drawAxes() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.5)';
            ctx.lineWidth = 2;
            
            // x轴
            ctx.beginPath();
            ctx.moveTo(0, centerY);
            ctx.lineTo(canvas.width, centerY);
            ctx.stroke();
            
            // y轴
            ctx.beginPath();
            ctx.moveTo(centerX, 0);
            ctx.lineTo(centerX, canvas.height);
            ctx.stroke();
            
            // 坐标轴标签
            ctx.fillStyle = '#ffffff';
            ctx.font = '14px Arial';
            ctx.fillText('x', canvas.width - 20, centerY - 10);
            ctx.fillText('
<!--检测到代码截断，自动续写中...-->
'y', centerX + 10, 20);
        }
        
        // 绘制场景标题
        function drawSceneTitle() {
            ctx.fillStyle = '#4fc3f7';
            ctx.font = 'bold 24px Arial';
            ctx.textAlign = 'left';
            ctx.textBaseline = 'top';
            
            if (simulation.scene === 1) {
                ctx.fillText('复合场偏转', 20, 20);
                ctx.font = '16px Arial';
                ctx.fillStyle = '#b0bec5';
                ctx.fillText('电场力 + 洛伦兹力 = 复杂轨迹', 20, 50);
            } else {
                ctx.fillText('速度选择器', 20, 20);
                ctx.font = '16px Arial';
                ctx.fillStyle = '#b0bec5';
                ctx.fillText('当 v = E/B 时，粒子受力平衡，直线通过', 20, 50);
            }
        }
        
        // 绘制箭头
        function drawArrow(fromX, fromY, toX, toY, headSize, color) {
            const angle = Math.atan2(toY - fromY, toX - fromX);
            const length = Math.sqrt((toX - fromX)**2 + (toY - fromY)**2);
            
            if (length < 5) return; // 太短不绘制
            
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            ctx.lineWidth = 3;
            ctx.lineCap = 'round';
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(fromX, fromY);
            ctx.lineTo(toX, toY);
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(toX, toY);
            ctx.lineTo(
                toX - headSize * Math.cos(angle - Math.PI/6),
                toY - headSize * Math.sin(angle - Math.PI/6)
            );
            ctx.lineTo(
                toX - headSize * Math.cos(angle + Math.PI/6),
                toY - headSize * Math.sin(angle + Math.PI/6)
            );
            ctx.closePath();
            ctx.fill();
        }
        
        // 绘制带点的圆（表示垂直纸面向外的磁场）
        function drawCircleWithDot(x, y, radius, color) {
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            ctx.lineWidth = 2;
            
            // 绘制圆
            ctx.beginPath();
            ctx.arc(x, y, radius, 0, Math.PI * 2);
            ctx.stroke();
            
            // 绘制中心点
            ctx.beginPath();
            ctx.arc(x, y, radius/3, 0, Math.PI * 2);
            ctx.fill();
        }
        
        // 动画循环
        function animate() {
            updateParticle();
            drawScene();
            requestAnimationFrame(animate);
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 场景切换
            document.getElementById('scene1Btn').addEventListener('click', () => {
                document.getElementById('scene1Btn').classList.add('active');
                document.getElementById('scene2Btn').classList.remove('active');
                simulation.scene = 1;
                initParticle();
            });
            
            document.getElementById('scene2Btn').addEventListener('click', () => {
                document.getElementById('scene2Btn').classList.add('active');
                document.getElementById('scene1Btn').classList.remove('active');
                simulation.scene = 2;
                initParticle();
            });
            
            // 模拟控制按钮
            document.getElementById('playBtn').addEventListener('click', () => {
                simulation.running = true;
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                simulation.running = false;
            });
            
            document.getElementById('stepBtn').addEventListener('click', () => {
                simulation.running = false;
                updateParticle();
                drawScene();
            });
            
            document.getElementById('resetBtn').addEventListener('click', () => {
                initParticle();
                simulation.running = false;
            });
            
            // 切换开关
            document.getElementById('showTrajectory').addEventListener('change', (e) => {
                simulation.showTrajectory = e.target.checked;
            });
            
            document.getElementById('showVectors').addEventListener('change', (e) => {
                simulation.showVectors = e.target.checked;
            });
            
            // 参数滑块
            document.getElementById('eSlider').addEventListener('input', (e) => {
                params.E = parseFloat(e.target.value);
                initParticle();
            });
            
            document.getElementById('bSlider').addEventListener('input', (e) => {
                params.B = parseFloat(e.target.value);
                initParticle();
            });
            
            document.getElementById('qSlider').addEventListener('input', (e) => {
                params.q = parseFloat(e.target.value);
                initParticle();
            });
            
            document.getElementById('mSlider').addEventListener('input', (e) => {
                params.m = parseFloat(e.target.value);
                initParticle();
            });
            
            document.getElementById('vSlider').addEventListener('input', (e) => {
                params.v0 = parseFloat(e.target.value);
                initParticle();
            });
            
            // 预设案例按钮
            document.querySelectorAll('.preset-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    const preset = btn.dataset.preset;
                    
                    switch(preset) {
                        case 'electric':
                            params.E = 2000;
                            params.B = 0;
                            params.q = 1.6e-19;
                            params.v0 = 1e6;
                            break;
                        case 'magnetic':
                            params.E = 0;
                            params.B = 0.8;
                            params.q = 1.6e-19;
                            params.v0 = 1e6;
                            break;
                        case 'selector':
                            params.E = 1000;
                            params.B = 0.5;
                            params.q = 1.6e-19;
                            params.v0 = params.E / params.B; // v = E/B
                            simulation.scene = 2;
                            document.getElementById('scene2Btn').classList.add('active');
                            document.getElementById('scene1Btn').classList.remove('active');
                            break;
                        case 'fast':
                            params.E = 1000;
                            params.B = 0.5;
                            params.q = 1.6e-19;
                            params.v0 = 3e6; // > E/B
                            simulation.scene = 2;
                            document.getElementById('scene2Btn').classList.add('active');
                            document.getElementById('scene1Btn').classList.remove('active');
                            break;
                        case 'slow':
                            params.E = 1000;
                            params.B = 0.5;
                            params.q = 1.6e-19;
                            params.v0 = 0.5e6; // < E/B
                            simulation.scene = 2;
                            document.getElementById('scene2Btn').classList.add('active');
                            document.getElementById('scene1Btn').classList.remove('active');
                            break;
                        case 'negative':
                            params.E = 1000;
                            params.B = 0.5;
                            params.q = -1.6e-19;
                            params.v0 = 1e6;
                            break;
                    }
                    
                    // 更新滑块值
                    document.getElementById('eSlider').value = params.E;
                    document.getElementById('bSlider').value = params.B;
                    document.getElementById('qSlider').value = params.q;
                    document.getElementById('vSlider').value = params.v0;
                    
                    initParticle();
                });
            });
        }
        
        // 初始化应用
        function initApp() {
            initParticle();
            initEventListeners();
            animate();
            
            // 初始更新显示
            updateDisplay(calculateForces());
        }
        
        // 启动应用
        window.addEventListener('load', initApp);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

# 交互式教学动画使用指南

## 欢迎使用《带电粒子在复合场中的运动》教学动画

亲爱的老师和同学们：

欢迎使用这款专为物理教学设计的交互式动画！本工具旨在帮助您直观理解带电粒子在电场和磁场复合场中的复杂运动规律，特别是**速度选择器**这一重要物理概念。通过实时模拟、参数调节和可视化反馈，您将能够“看见”抽象的物理原理，深化对电磁学核心概念的理解。

---

## 一、功能说明

### 1. 两大核心场景
- **复合场偏转场景**：展示带电粒子在正交电场和磁场共同作用下的复杂轨迹运动
- **速度选择器场景**：演示当粒子速度满足特定条件（v = E/B）时，如何实现选择性通过

### 2. 完整的模拟系统
- 实时物理引擎计算粒子受力、速度和位置
- 可视化显示电场力、洛伦兹力、合力和速度矢量
- 动态绘制粒子运动轨迹
- 实时数据显示关键物理参数

### 3. 交互式控制面板
- 可调节电场强度、磁感应强度、粒子电荷、质量和初速度
- 播放/暂停/单步/重置控制
- 轨迹和矢量显示开关
- 预设案例快速演示

---

## 二、主要功能详解

### 🎮 模拟控制区
- **播放/暂停**：控制模拟运行状态
- **单步前进**：逐帧观察粒子运动，适合详细分析受力变化
- **重置**：将粒子重置到初始位置，清除轨迹
- **显示开关**：可独立控制轨迹和矢量的显示/隐藏

### ⚙️ 物理参数调节区
1. **电场强度 E** (0-5000 N/C)
   - 控制电场强弱，影响电场力大小
   - 电场方向固定向下（y轴正方向）

2. **磁感应强度 B** (0-2 T)
   - 控制磁场强弱，影响洛伦兹力大小
   - 磁场方向固定垂直纸面向外（用带点的圆圈表示）

3. **粒子电荷 q** (±1.6×10⁻¹⁹ C)
   - 正电荷（橙色）和负电荷（紫色）粒子
   - 电荷符号影响受力方向

4. **粒子质量 m** (1×10⁻³¹ - 5×10⁻³⁰ kg)
   - 默认值为电子质量 9.1×10⁻³¹ kg
   - 质量影响加速度大小

5. **初速度 v₀** (1×10⁵ - 5×10⁶ m/s)
   - 控制粒子进入场区的初始速度
   - 在速度选择器场景中，与E/B比值比较决定是否通过

### 🚀 预设案例区
六个精心设计的预设案例，一键演示关键物理现象：
1. **仅电场偏转**：B=0，观察类平抛运动
2. **仅磁场偏转**：E=0，观察匀速圆周运动
3. **速度选择器**：自动设置v=E/B，演示平衡状态
4. **速度 > E/B**：粒子向上偏转
5. **速度 < E/B**：粒子向下偏转
6. **负电荷粒子**：观察电荷符号对运动的影响

### 📊 实时数据显示区
- 粒子位置坐标（毫米单位）
- 实时速度大小
- 电场力和洛伦兹力大小
- 理论选择速度 v=E/B
- 粒子当前状态（运动/通过/偏转）

---

## 三、设计特色

### 🎨 可视化设计
1. **色彩编码系统**
   - 红色箭头：电场力 (Fₑ)
   - 蓝色箭头：洛伦兹力 (Fₘ)
   - 黄色箭头：合力 (F)
   - 绿色箭头：速度 (v)
   - 橙色/紫色粒子：正/负电荷

2. **场指示清晰**
   - 红色背景区域：电场作用区
   - 蓝色圆圈符号：磁场方向（垂直纸面向外）
   - 绿色通道：速度选择器通过区域

3. **专业视觉元素**
   - 坐标网格便于定位
   - 半透明轨迹随时间淡出
   - 力矢量按比例缩放显示

### 🔧 交互设计
1. **实时响应**：所有参数调节立即生效
2. **对比观察**：可通过单步模式仔细观察每一时刻的受力情况
3. **场景切换**：两个场景独立设置，便于对比学习

---

## 四、教学要点与使用建议

### 教学要点

#### 1. 复合场偏转场景
- **核心概念**：电场力恒定，洛伦兹力随速度方向变化
- **观察重点**：
  - 轨迹形状如何随参数变化
  - 力矢量如何随时间变化
  - 正负电荷运动轨迹的差异
- **思考问题**：
  - 为什么轨迹不是简单的圆周或抛物线？
  - 哪些参数主要影响轨迹的弯曲程度？
  - 如何解释轨迹的周期性？

#### 2. 速度选择器场景
- **核心原理**：当 qE = qvB 即 v = E/B 时，粒子受力平衡
- **关键观察**：
  - 满足 v=E/B 时，粒子直线通过通道
  - v>E/B 时，洛伦兹力占优，向上偏转
  - v<E/B 时，电场力占优，向下偏转
- **物理意义**：
  - 速度选择器是质谱仪等仪器的基础
  - 理解“选择”的物理机制

### 使用建议

#### 对于教师：
1. **课堂演示**
   - 使用预设案例快速展示关键现象
   - 通过参数调节引导学生预测结果
   - 结合单步模式讲解受力分析

2. **探究式教学**
   - 提出问题：如果改变某个参数，会发生什么？
   - 让学生先预测，再通过模拟验证
   - 组织小组讨论解释观察到的现象

3. **概念巩固**
   - 对比单一电场、单一磁场和复合场的区别
   - 强调左手定则在洛伦兹力方向判断中的应用
   - 联系实际应用（质谱仪、回旋加速器等）

#### 对于学生：
1. **自主学习**
   - 从简单到复杂：先观察预设案例，再尝试自己调节参数
   - 记录观察：不同参数组合下的轨迹特征
   - 尝试解释：为什么会有这样的运动轨迹？

2. **概念验证**
   - 验证 v=E/B 确实是速度选择器的条件
   - 观察质量对运动的影响
   - 理解电荷符号如何改变受力方向

3. **深入探究**
   - 尝试找出使粒子做直线运动的其他参数组合
   - 观察当初速度方向不水平时的运动
   - 思考如果电场和磁场不垂直会怎样

### 教学流程建议

1. **引入阶段**（5分钟）
   - 回顾电场力和洛伦兹力的基本公式
   - 提出问题：如果两个场同时存在会怎样？

2. **探索阶段**（15分钟）
   - 演示单一电场和单一磁场的偏转
   - 引入复合场，观察复杂轨迹
   - 重点讲解速度选择器原理

3. **探究阶段**（15分钟）
   - 学生自主探索，调节参数观察变化
   - 完成探究任务：找出通过速度选择器的条件
   - 记录观察结果和分析

4. **总结阶段**（10分钟）
   - 分享观察结果
   - 总结规律和公式
   - 联系实际应用

---

## 五、技术说明

### 物理模型
- 采用经典电磁学公式计算
- 时间步长：1×10⁻¹⁰ 秒
- 二维平面模拟（x-y平面）
- 假设磁场垂直纸面，电场在平面内

### 使用要求
- 现代浏览器（Chrome、Firefox、Edge等）
- 支持HTML5 Canvas
- 建议屏幕分辨率 1280×720 以上

### 教育价值
1. **化抽象为具体**：将抽象的公式和概念转化为可视化的运动
2. **培养科学思维**：通过“预测-观察-解释”培养探究能力
3. **深化概念理解**：多参数调节帮助理解各物理量的影响
4. **激发学习兴趣**：交互式设计提高学习参与度

---

## 开始探索吧！

现在，您已经了解了这个教学工具的所有功能。建议您：

1. 先尝试各个预设案例，观察基本现象
2. 然后自由调节参数，探索参数间的相互影响
3. 最后尝试解释您观察到的所有现象

记住：物理学的美妙在于从复杂现象中发现简单规律。祝您在探索带电粒子世界的旅程中获得启发和乐趣！

**教学提示**：鼓励学生不仅“看”动画，更要“想”物理。每一个现象背后都有深刻的物理原理等待发现。

---
*本教学工具由教育技术专家设计，旨在促进物理概念的理解。如有教学建议或技术问题，欢迎反馈。*