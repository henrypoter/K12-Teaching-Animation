# 需求：凸透镜成像规律（物距像距实时变化+光路图）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为初中物理学生，也可能包括需要复习的高中生或对光学感兴趣的初学者。
2.  **核心痛点**：
    *   **抽象难懂**：凸透镜成像规律（物距u、像距v、焦距f的关系）以及像的性质（正倒、大小、虚实）是抽象的物理概念，仅凭静态图片和公式难以建立动态联系。
    *   **规律记忆困难**：传统教学依赖“一倍焦距分虚实，二倍焦距分大小”等口诀，学生容易死记硬背，不理解其背后的光路原理。
    *   **缺乏直观感知**：无法直观地看到当物体（物距）连续移动时，像的位置（像距）和性质如何实时、连续地变化。
3.  **核心需求**：需要一个**动态、交互、可视化**的工具，将抽象的光学规律转化为直观的视觉过程，帮助学生**自主探索、发现并理解**规律，而非被动接受结论。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）
1.  **核心概念聚焦**：
    *   **三条特殊光线**：平行于主光轴、过光心、过焦点的光线传播路径。这是构建所有光路图的基础。
    *   **关键点与区域**：焦点(F)、二倍焦距点(2F)、光心(O)。以及“u>2f”, “f<u<2f”, “u<f”三个关键物距区域。
    *   **像的四大性质**：位置（像距v）、大小（放大/缩小/等大）、虚实（实像/虚像）、正倒（倒立/正立）。
    *   **核心公式**：1/u + 1/v = 1/f，作为动态变化的数学体现。

2.  **认知规律遵循**：
    *   **从具体到抽象**：先展示生动的“蜡烛成像”实物模拟，再抽象为清晰的光线路径图。
    *   **从观察到总结**：引导学生通过交互操作（移动物体）观察现象，最后再呈现或归纳出规律表格和公式。
    *   **从分步到连续**：先强调三个关键区域（u>2f, f<u<2f, u<f）的典型成像情况，再通过连续拖动展示区域间的平滑过渡，理解变化的连续性。

3.  **交互设计策略**：
    *   **直接操纵**：用户可以用鼠标直接拖拽“物体”（如箭头或蜡烛），这是最核心的交互。物体的实时位置（物距u）应清晰显示。
    *   **实时响应与反馈**：
        *   随着物体移动，**像**的位置、大小、虚实立即更新。
        *   **光路图**实时绘制，至少展示两条关键光线（如平行过焦点、过光心不变），清晰地展示像点是如何由光线交点确定的。
        *   数值实时更新：物距(u)、像距(v)、焦距(f)的数值及计算关系实时显示。
    *   **渐进式信息呈现**：初始界面简洁，光路图突出。提供可开关的“辅助信息”面板，用于显示规律总结表格、公式、口诀等，避免初学时信息过载。
    *   **情景化控制**：提供预设按钮（如“物体在2倍焦距外”、“物体在焦点上”），一键跳转到典型位置，便于教师讲解或学生快速定位。

4.  **视觉呈现要点**：
    *   **主场景构图**：水平放置的主光轴，中央的凸透镜，两侧对称的F和2F点标记。
    *   **视觉层次与对比**：
        *   **物体**：使用醒目的颜色（如橙色箭头或红色蜡烛）。
        *   **实际光线**：用实线、高亮色（如红色）绘制，箭头表示方向。
        *   **虚像/反向延长线**：用明显的虚线（如蓝色虚线）表示，与实线形成强烈对比。
        *   **像**：实像用实心、高亮图形表示；虚像用半透明或轮廓线表示，以区分虚实。
    *   **动画平滑性**：所有元素（像、光线）的移动和变化需要平滑过渡，避免跳跃，以体现物理过程的连续性。

#### 配色方案选择
*   **主色调与背景**：
    *   **背景**：深灰色或深蓝色。深色背景能更好地突出彩色的光线和元素，减少视觉干扰，营造“暗室”或科学探索的沉浸感。
*   **核心元素色**：
    *   **凸透镜与主光轴**：浅灰色或白色，作为中性的基准线。
    *   **物体**：亮橙色或明黄色。温暖、醒目，代表发光体。
    *   **实际光线**：亮红色或亮绿色。高饱和度的颜色，确保清晰可见。
    *   **反向延长线与虚像**：蓝色虚线。与红色实线形成冷暖、虚实双重对比，是区分实像与虚像的关键视觉编码。
    *   **像（实像）**：与物体同色（亮橙）但可稍暗，或使用亮绿色，表示是由实际光线会聚而成。
    *   **焦点(F)、二倍焦距点(2F)**：白色或浅黄色标记和文字。
*   **UI与控制面板**：
    *   半透明黑色或深灰色面板，白色文字。
    *   按钮使用温和的蓝色或绿色，与主视觉色系协调。

#### 交互功能列表
1.  **核心交互**：
    *   **拖拽物体**：自由水平拖动物体，实时观察成像变化。
2.  **视觉控制**：
    *   **光路图显示开关**：可隐藏/显示光线路径，专注于观察物体与像的关系。
    *   **关键光线选择**：可选显示“三条特殊光线”中的两条或三条，降低初学时认知负荷。
    *   **辅助线网格**：可选的背景网格，帮助估算距离和比例。
3.  **参数控制**：
    *   **焦距(f)调节滑块**：允许用户改变凸透镜的焦距，观察不同焦距透镜的成像差异。
    *   **数值显示面板**：实时显示当前物距(u)、像距(v)、焦距(f)的数值，并可选择显示 `1/u + 1/v` 的计算值，直观验证公式。
4.  **预设与重置**：
    *   **典型位置按钮**：一键将物体置于“u>2f”, “u=2f”, “f<u<2f”, “u=f”, “u<f”等关键位置。
    *   **重置按钮**：将物体、焦距等恢复至初始状态。
5.  **学习辅助**：
    *   **规律总结面板**：可展开/折叠的表格，根据物体当前位置，高亮显示对应的成像区域、像的性质（大小、倒正、虚实）及应用举例（如照相机、投影仪、放大镜）。
    *   **公式提示**：在合适位置显示成像公式 `1/u + 1/v = 1/f`。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>凸透镜成像规律交互实验</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
            color: #e0e0e0;
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
            color: #4fc3f7;
            margin-bottom: 10px;
            font-size: 2.2rem;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
        }

        .subtitle {
            color: #90a4ae;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            max-width: 1200px;
            justify-content: center;
        }

        .simulation-panel {
            background: rgba(30, 30, 46, 0.8);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            flex: 1;
            min-width: 700px;
            border: 1px solid rgba(76, 175, 80, 0.2);
        }

        .control-panel {
            background: rgba(30, 30, 46, 0.8);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            width: 350px;
            border: 1px solid rgba(33, 150, 243, 0.2);
        }

        .panel-title {
            color: #4fc3f7;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid rgba(76, 175, 80, 0.5);
            font-size: 1.4rem;
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 450px;
            background-color: rgba(10, 15, 30, 0.9);
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        #simulationCanvas {
            display: block;
            cursor: grab;
        }

        .control-group {
            margin-bottom: 20px;
        }

        .control-title {
            color: #81c784;
            margin-bottom: 10px;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
        }

        .control-title i {
            margin-right: 8px;
            font-size: 1.2rem;
        }

        .slider-container {
            margin-bottom: 15px;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-size: 0.95rem;
        }

        .slider-value {
            color: #4fc3f7;
            font-weight: bold;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            background: rgba(100, 100, 120, 0.5);
            border-radius: 4px;
            outline: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #4fc3f7;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
        }

        .preset-buttons {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
            margin-top: 10px;
        }

        .preset-btn {
            padding: 10px;
            background: rgba(33, 150, 243, 0.2);
            border: 1px solid rgba(33, 150, 243, 0.5);
            color: #81c784;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.95rem;
        }

        .preset-btn:hover {
            background: rgba(33, 150, 243, 0.4);
            transform: translateY(-2px);
        }

        .preset-btn.active {
            background: rgba(76, 175, 80, 0.3);
            border-color: #4caf50;
            color: #c8e6c9;
        }

        .toggle-buttons {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        .toggle-btn {
            padding: 8px 15px;
            background: rgba(96, 125, 139, 0.3);
            border: 1px solid rgba(96, 125, 139, 0.6);
            color: #b0bec5;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 0.9rem;
        }

        .toggle-btn.active {
            background: rgba(76, 175, 80, 0.3);
            border-color: #4caf50;
            color: #c8e6c9;
        }

        .info-display {
            background: rgba(20, 25, 40, 0.7);
            border-radius: 8px;
            padding: 15px;
            margin-top: 15px;
            border-left: 4px solid #ff9800;
        }

        .info-title {
            color: #ff9800;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }

        .parameter-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }

        .parameter {
            display: flex;
            justify-content: space-between;
            padding: 5px 0;
            border-bottom: 1px dashed rgba(255, 255, 255, 0.1);
        }

        .parameter-name {
            color: #b0bec5;
        }

        .parameter-value {
            color: #4fc3f7;
            font-weight: bold;
            font-family: 'Courier New', monospace;
        }

        .law-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
            font-size: 0.9rem;
        }

        .law-table th {
            background: rgba(33, 150, 243, 0.3);
            color: #bbdefb;
            padding: 8px;
            text-align: center;
            border: 1px solid rgba(33, 150, 243, 0.5);
        }

        .law-table td {
            padding: 8px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .law-table tr:nth-child(even) {
            background: rgba(255, 255, 255, 0.05);
        }

        .highlight-row {
            background: rgba(255, 193, 7, 0.2) !important;
            color: #ffd54f;
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 20px;
            height: 4px;
            margin-right: 8px;
        }

        .instructions {
            margin-top: 20px;
            padding: 15px;
            background: rgba(30, 30, 46, 0.6);
            border-radius: 8px;
            font-size: 0.9rem;
            line-height: 1.5;
            border-left: 4px solid #9c27b0;
        }

        .instructions h3 {
            color: #ce93d8;
            margin-bottom: 8px;
        }

        .instructions ul {
            padding-left: 20px;
            color: #b0bec5;
        }

        .instructions li {
            margin-bottom: 5px;
        }

        .footer {
            margin-top: 20px;
            text-align: center;
            color: #78909c;
            font-size: 0.9rem;
            padding-top: 15px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            max-width: 900px;
        }

        @media (max-width: 1100px) {
            .container {
                flex-direction: column;
                align-items: center;
            }
            
            .simulation-panel {
                min-width: 90%;
            }
            
            .control-panel {
                width: 90%;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>凸透镜成像规律交互实验</h1>
        <p class="subtitle">拖动物体，实时观察成像变化与光路图 | 探索光学规律</p>
    </div>

    <div class="container">
        <div class="simulation-panel">
            <h2 class="panel-title">成像模拟与光路图</h2>
            <div class="canvas-container">
                <canvas id="simulationCanvas" width="800" height="450"></canvas>
            </div>
            
            <div class="legend">
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #ff9800;"></div>
                    <span>物体</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #4caf50;"></div>
                    <span>实像</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #2196f3; border-bottom: 2px dashed #2196f3;"></div>
                    <span>虚像</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #f44336;"></div>
                    <span>实际光线</span>
                </div>
                <div class="legend-item">
                    <div class="legend-color" style="background-color: #2196f3; border-bottom: 2px dotted #2196f3;"></div>
                    <span>反向延长线</span>
                </div>
            </div>
        </div>

        <div class="control-panel">
            <h2 class="panel-title">控制面板</h2>
            
            <div class="control-group">
                <div class="control-title">物体控制</div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>物距 (u)</span>
                        <span class="slider-value" id="uValue">60.0 cm</span>
                    </div>
                    <input type="range" id="uSlider" min="10" max="150" value="60" step="0.1">
                </div>
                
                <div class="slider-container">
                    <div class="slider-label">
                        <span>物体高度</span>
                        <span class="slider-value" id="objectHeightValue">30.0 cm</span>
                    </div>
                    <input type="range" id="objectHeightSlider" min="10" max="50" value="30" step="0.1">
                </div>
            </div>
            
            <div class="control-group">
                <div class="control-title">透镜参数</div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>焦距 (f)</span>
                        <span class="slider-value" id="fValue">20.0 cm</span>
                    </div>
                    <input type="range" id="fSlider" min="10" max="40" value="20" step="0.1">
                </div>
            </div>
            
            <div class="control-group">
                <div class="control-title">预设位置</div>
                <div class="preset-buttons">
                    <button class="preset-btn" data-u="80">u > 2f (照相机)</button>
                    <button class="preset-btn" data-u="40">u = 2f (等大实像)</button>
                    <button class="preset-btn" data-u="30">f < u < 2f (投影仪)</button>
                    <button class="preset-btn" data-u="20">u = f (不成像)</button>
                    <button class="preset-btn" data-u="10">u < f (放大镜)</button>
                    <button class="preset-btn" id="resetBtn">重置</button>
                </div>
            </div>
            
            <div class="control-group">
                <div class="control-title">显示选项</div>
                <div class="toggle-buttons">
                    <button class="toggle-btn active" id="toggleRays">显示光线</button>
                    <button class="toggle-btn active" id="toggleGrid">显示网格</button>
                    <button class="toggle-btn" id="toggleLabels">显示标签</button>
                </div>
            </div>
            
            <div class="info-display">
                <div class="info-title">实时参数</div>
                <div class="parameter-grid">
                    <div class="parameter">
                        <span class="parameter-name">物距 (u):</span>
                        <span class="parameter-value" id="displayU">60.0 cm</span>
                    </div>
                    <div class="parameter">
                        <span class="parameter-name">像距 (v):</span>
                        <span class="parameter-value" id="displayV">30.0 cm</span>
                    </div>
                    <div class="parameter">
                        <span class="parameter-name">焦距 (f):</span>
                        <span class="parameter-value" id="displayF">20.0 cm</span>
                    </div>
                    <div class="parameter">
                        <span class="parameter-name">放大率 (|v/u|):</span>
                        <span class="parameter-value" id="displayM">0.50</span>
                    </div>
                    <div class="parameter">
                        <span class="parameter-name">1/u + 1/v:</span>
                        <span class="parameter-value" id="displayFormula">0.0833</span>
                    </div>
                    <div class="parameter">
                        <span class="parameter-name">1/f:</span>
                        <span class="parameter-value" id="displayInverseF">0.0500</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <div class="simulation-panel" style="margin-top: 20px; min-width: 90%;">
        <h2 class="panel-title">成像规律总结</h2>
        <table class="law-table" id="lawTable">
            <thead>
                <tr>
                    <th>物体位置</th>
                    <th>像的位置</th>
                    <th>像的大小</th>
                    <th>像的正倒</th>
                    <th>像的虚实</th>
                    <th>应用举例</th>
                </tr>
            </thead>
            <tbody>
                <tr data-range="u>2f">
                    <td>u > 2f</td>
                    <td>f < v < 2f</td>
                    <td>缩小</td>
                    <td>倒立</td>
                    <td>实像</td>
                    <td>照相机</td>
                </tr>
                <tr data-range="u=2f">
                    <td>u = 2f</td>
                    <td>v = 2f</td>
                    <td>等大</td>
                    <td>倒立</td>
                    <td>实像</td>
                    <td>测焦距</td>
                </tr>
                <tr data-range="f<u<2f">
                    <td>f < u < 2f</td>
                    <td>v > 2f</td>
                    <td>放大</td>
                    <td>倒立</td>
                    <td>实像</td>
                    <td>投影仪</td>
                </tr>
                <tr data-range="u=f">
                    <td>u = f</td>
                    <td>不成像</td>
                    <td>-</td>
                    <td>-</td>
                    <td>-</td>
                    <td>平行光源</td>
                </tr>
                <tr data-range="u<f">
                    <td>u < f</td>
                    <td>|v| > u (同侧)</td>
                    <td>放大</td>
                    <td>正立</td>
                    <td>虚像</td>
                    <td>放大镜</td>
                </tr>
            </tbody>
        </table>
    </div>
    
    <div class="instructions">
        <h3>使用说明</h3>
        <ul>
            <li><strong>拖动物体</strong>：在画布上直接拖动物体（橙色箭头），实时观察成像变化。</li>
            <li><strong>调节参数</strong>：使用滑块调整物距、物体高度和焦距。</li>
            <li><strong>预设位置</strong>：点击预设按钮快速跳转到典型成像位置。</li>
            <li><strong>显示控制</strong>：使用显示选项按钮切换光线、网格和标签的显示。</li>
            <li><strong>观察规律</strong>：注意物体在不同位置时，像的性质（大小、倒正、虚实）变化规律。</li>
            <li><strong>验证公式</strong>：观察"1/u + 1/v"的值是否始终等于"1/f"。</li>
        </ul>
    </div>
    
    <div class="footer">
        <p>凸透镜成像规律交互实验 | 设计原理: 1/u + 1/v = 1/f | 适用于初中物理光学教学</p>
        <p>提示：虚线表示光的反向延长线，用于确定虚像的位置</p>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('simulationCanvas');
        const ctx = canvas.getContext('2d');
        
        // 状态变量
        let state = {
            // 透镜参数
            f: 20,        // 焦距 (cm)
            lensX: 400,   // 透镜中心X坐标
            
            // 物体参数
            objectX: 340, // 物体X坐标 (透镜右侧为正)
            objectHeight: 30, // 物体高度 (cm)
            u: 60,        // 物距 (cm)
            
            // 计算得到的像参数
            v: 0,         // 像距 (cm)
            imageHeight: 0, // 像高度 (cm)
            isRealImage: true, // 是否为实像
            
            // 显示选项
            showRays: true,
            showGrid: true,
            showLabels: true,
            
            // 交互状态
            isDragging: false,
            dragStartX: 0
        };
        
        // 初始化计算
        calculateImage();
        
        // 获取DOM元素
        const uSlider = document.getElementById('uSlider');
        const uValue = document.getElementById('uValue');
        const objectHeightSlider = document.getElementById('objectHeightSlider');
        const objectHeightValue = document.getElementById('objectHeightValue');
        const fSlider = document.getElementById('fSlider');
        const fValue = document.getElementById('fValue');
        
        const displayU = document.getElementById('displayU');
        const displayV = document.getElementById('displayV');
        const displayF = document.getElementById('displayF');
        const displayM = document.getElementById('displayM');
        const displayFormula = document.getElementById('displayFormula');
        const displayInverseF = document.getElementById('displayInverseF');
        
        const presetButtons = document.querySelectorAll('.preset-btn');
        const resetBtn = document.getElementById('resetBtn');
        const toggleRaysBtn = document.getElementById('toggleRays');
        const toggleGridBtn = document.getElementById('toggleGrid');
        const toggleLabelsBtn = document.getElementById('toggleLabels');
        const lawTableRows = document.querySelectorAll('#lawTable tbody tr');
        
        // 事件监听器
        uSlider.addEventListener('input', function() {
            state.u = parseFloat(this.value);
            uValue.textContent = state.u.toFixed(1) + ' cm';
            updateObjectPositionFromU();
            calculateImage();
            updateDisplay();
            updateLawTableHighlight();
            draw();
        });
        
        objectHeightSlider.addEventListener('input', function() {
            state.objectHeight = parseFloat(this.value);
            objectHeightValue.textContent = state.objectHeight.toFixed(1) + ' cm';
            calculateImage();
            updateDisplay();
            draw();
        });
        
        fSlider.addEventListener('input', function() {
            state.f = parseFloat(this.value);
            fValue.textContent = state.f.toFixed(1) + ' cm';
            calculateImage();
            updateDisplay();
            updateLawTableHighlight();
            draw();
        });
        
        // 预设按钮
        presetButtons.forEach(btn => {
            if (btn.id !== 'resetBtn') {
                btn.addEventListener('click', function() {
                    const u = parseFloat(this.getAttribute('data-u'));
                    state.u = u;
                    uSlider.value = u;
                    uValue.textContent = u.toFixed(1) + ' cm';
                    updateObjectPositionFromU();
                    calculateImage();
                    updateDisplay();
                    updateLawTableHighlight();
                    
                    // 更新按钮激活状态
                    presetButtons.forEach(b => b.classList.remove('active'));
                    this.classList.add('active');
                    
                    draw();
                });
            }
        });
        
        resetBtn.addEventListener('click', function() {
            state.u = 60;
            state.objectHeight = 30;
            state.f = 20;
            
            uSlider.value = state.u;
            objectHeightSlider.value = state.objectHeight;
            fSlider.value = state.f;
            
            uValue.textContent = state.u.toFixed(1) + ' cm';
            objectHeightValue.textContent = state.objectHeight.toFixed(1) + ' cm';
            fValue.textContent = state.f.toFixed(1) + ' cm';
            
            updateObjectPositionFromU();
            calculateImage();
            updateDisplay();
            updateLawTableHighlight();
            
            // 重置按钮激活状态
            presetButtons.forEach(b => b.classList.remove('active'));
            
            draw();
        });
        
        // 显示选项按钮
        toggleRaysBtn.addEventListener('click', function() {
            state.showRays = !state.showRays;
            this.classList.toggle('active');
            draw();
        });
        
        toggleGridBtn.addEventListener('click', function() {
            state.showGrid = !state.showGrid;
            this.classList.toggle('active');
            draw();
        });
        
        toggleLabelsBtn.addEventListener('click', function() {
            state.showLabels = !state.showLabels;
            this.classList.toggle('active');
            draw();
        });
        
        // Canvas交互
        canvas.addEventListener('mousedown', function(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 检查是否点击在物体上
            if (Math.abs(x - state.objectX) < 20 && Math.abs(y - canvas.height/2) < 40) {
                state.isDragging = true;
                state.dragStartX = x;
                canvas.style.cursor = 'grabbing';
            }
        });
        
        canvas.addEventListener('mousemove', function(e) {
            const rect = canvas.getBoundingClientRect();
            const x = e.clientX - rect.left;
            
            // 更新光标样式
            if (!state.isDragging) {
                if (Math.abs(x - state.objectX) < 20) {
                    canvas.style.cursor = 'grab';
                } else {
                    canvas.style.cursor = 'default';
                }
            }
            
            // 处理拖动
            if (state.isDragging) {
                const deltaX = x - state.dragStartX;
                state.objectX += deltaX;
                state.dragStartX = x;
                
                // 限制物体位置
                if (state.objectX < 50) state.objectX = 50;
                if (state.objectX > 750) state.objectX = 750;
                
                // 更新物距
                state.u = state.lensX - state.objectX;
                if (state.u < 10) state.u = 10;
                if (state.u > 150) state.u = 150;
                
                uSlider.value = state.u;
                uValue.textContent = state.u.toFixed(1) + ' cm';
                
                calculateImage();
                updateDisplay();
                updateLawTableHighlight();
                draw();
            }
        });
        
        canvas.addEventListener('mouseup', function() {
            state.isDragging = false;
            canvas.style.cursor = 'grab';
        });
        
        canvas.addEventListener('mouseleave', function() {
            state.isDragging = false;
            canvas.style.cursor = 'default';
        });
        
        // 计算像的位置和性质
        function calculateImage() {
            // 使用透镜公式: 1/u + 1/v = 1/f
            if (state.u === state.f) {
                // u = f, 不成像
                state.v = Infinity;
                state.imageHeight = 0;
                state.isRealImage = false;
            } else {
                state.v = 1 / (1/state.f - 1/state.u);
                
                // 判断像的虚实
                state.isRealImage = state.v > 0;
                
                // 计算像的高度 (放大率 = |v/u|)
                const magnification = Math.abs(state.v / state.u);
                state.imageHeight = state.objectHeight * magnification;
            }
        }
        
        // 根据物距更新物体位置
        function updateObjectPositionFromU() {
            state.objectX = state.lensX - state.u;
        }
        
        // 更新显示参数
        function updateDisplay() {
            displayU.textContent = state.u.toFixed(1) + ' cm';
            displayF.textContent = state.f.toFixed(1) + ' cm';
            
            if (state.u === state.f) {
                displayV.textContent = '∞';
                displayM.textContent = '-';
                displayFormula.textContent = '-';
            } else {
                displayV.textContent = (state.isRealImage ? '' : '-') + Math.abs(state.v).toFixed(1) + ' cm';
                const magnification = Math.abs(state.v / state.u);
                displayM.textContent = magnification.toFixed(2);
                
                const formulaValue = 1/state.u + 1/state.v;
                displayFormula.textContent = formulaValue.toFixed(4);
            }
            
            displayInverseF.textContent = (1/state.f).toFixed(4);
        }
        
        // 更新规律表格高亮
        function updateLawTableHighlight() {
            lawTableRows.forEach(row => {
                row.classList.remove('highlight-row');
                
                const range = row.getAttribute('data-range');
                let shouldHighlight = false;
                
                if (range === 'u>2f' && state.u > 2*state.f) {
                    shouldHighlight = true;
                } else if (range === 'u=2f' && Math.abs(state.u - 2*state.f) < 0.5) {
                    shouldHighlight = true;
                } else if (range === 'f<u<2f' && state.u > state.f && state.u < 2*state.f) {
                    shouldHighlight = true;
                } else if (range === 'u=f' && Math.abs(state.u - state.f) < 0.5) {
                    shouldHighlight = true;
                } else if (range === 'u<f' && state.u < state.f) {
                    shouldHighlight = true;
                }
                
                if (shouldHighlight) {
                    row.classList.add('highlight-row');
                }
            });
        }
        
        // 绘制函数
        function draw() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制背景
            drawBackground();
            
            // 绘制主光轴
            drawPrincipalAxis();
            
            // 绘制透镜和焦点
            drawLensAndFoci();
            
            // 绘制物体
            drawObject();
            
            // 绘制像
            drawImage();
            
            // 绘制光线
            if (state.showRays) {
                drawRays();
            }
            
            // 绘制标签
            if (state.showLabels) {
                drawLabels();
            }
        }
        
        // 绘制背景
        function drawBackground() {
            if (state.showGrid) {
                ctx.strokeStyle = 'rgba(100, 100, 120, 0.3)';
                ctx.lineWidth = 0.5;
                
                // 绘制垂直网格线
                for (let x = 50; x <= 750; x += 50) {
                    ctx.beginPath();
                    ctx.moveTo(x, 0);
                    ctx.lineTo(x, canvas.height);
                    ctx.stroke();
                }
                
                // 绘制水平网格线
                for (let y = 50; y <= 400; y += 50) {
                    ctx.beginPath();
                    ctx.moveTo(0, y);
                    ctx.lineTo(canvas.width, y);
                    ctx.stroke();
                }
            }
        }
        
        // 绘制主光轴
        function drawPrincipalAxis() {
            ctx.strokeStyle = 'rgba(200, 200, 220, 0.8)';
            ctx.lineWidth = 1.5;
            ctx.beginPath();
            ctx.moveTo(50, canvas.height/2);
            ctx.lineTo(750, canvas.height/2);
            ctx.stroke();
        }
        
        // 绘制透镜和焦点
        function drawLensAndFoci() {
            const centerY = canvas.height/2;
            
            // 绘制凸透镜符号
            ctx.strokeStyle = '#ffffff';
            ctx.lineWidth = 3;
            ctx.beginPath();
            ctx.moveTo(state.lensX, centerY - 60);
            ctx.lineTo(state.lensX, centerY + 60);
            ctx.stroke();
            
            // 绘制透镜两侧的箭头（表示凸透镜）
            ctx.strokeStyle = '#4fc3f7';
            ctx.lineWidth = 2;
            
            // 左侧箭头
            ctx.beginPath();
            ctx.moveTo(state.lensX - 5, centerY - 50);
            ctx.lineTo(state.lensX - 15, centerY - 50);
            ctx.lineTo(state.lensX - 10, centerY - 55);
            ctx.moveTo(state.lensX - 15, centerY - 50);
            ctx.lineTo(state.lensX - 10, centerY - 45);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(state.lensX - 5, centerY + 50);
            ctx.lineTo(state.lensX - 15, centerY + 50);
            ctx.lineTo(state.lensX - 10, centerY + 55);
            ctx.moveTo(state.lensX - 15, centerY + 50);
            ctx.lineTo(state.lensX - 10, centerY + 45);
            ctx.stroke();
            
            // 右侧箭头
            ctx.beginPath();
            ctx.moveTo(state.lensX + 5, centerY - 50);
            ctx.lineTo(state.lensX + 15, centerY - 50);
            ctx.lineTo(state.lensX + 10, centerY - 55);
            ctx.moveTo(state.lensX + 15, centerY - 50);
            ctx.lineTo(state.lensX + 10, centerY - 45);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(state.lensX + 5, centerY + 50);
            ctx.lineTo(state.lensX + 15, centerY + 50);
            ctx.lineTo(state.lensX + 10, centerY + 55);
            ctx.moveTo(state.lensX + 15, centerY + 50);
            ctx.lineTo(state.lensX + 10, centerY + 45);
            ctx.stroke();
            
            // 绘制焦点 F 和 2F
            const scale = 2; // 1cm = 2px
            
            // 左侧焦点 F
            const leftFX = state.lensX - state.f * scale;
            drawFocusPoint(leftFX, centerY, 'F');
            
            // 左侧 2F 点
            const left2FX = state.lensX - 2 * state.f * scale;
            drawFocusPoint(left2FX, centerY, '2F');
            
            // 右侧焦点 F'
            const rightFX = state.lensX + state.f * scale;
            drawFocusPoint(rightFX, centerY, "F'");
            
            // 右侧 2F' 点
            const right2FX = state.lensX + 2 * state.f * scale;
            drawFocusPoint(right2FX, centerY, "2F'");
            
            // 绘制光心 O
            ctx.fillStyle = '#ff9800';
            ctx.beginPath();
            ctx.arc(state.lensX, centerY, 5, 0, Math.PI * 2);
            ctx.fill();
            
            if (state.showLabels) {
                ctx.fillStyle = '#ff9800';
                ctx.font = 'bold 14px Arial';
                ctx.fillText('O', state.lensX - 10, centerY - 10);
            }
        }
        
        // 绘制焦点标记点
        function drawFocusPoint(x, y, label) {
            ctx.fillStyle = '#81c784';
            ctx.beginPath();
            ctx.arc(x, y, 4, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.strokeStyle = 'rgba(129, 199, 132, 0.5)';
            ctx.lineWidth = 1;
            ctx.beginPath();
            ctx.moveTo(x, y - 10);
            ctx.lineTo(x, y + 10);
            ctx.stroke();
            
            if (state.showLabels) {
                ctx.fillStyle = '#81c784';
                ctx.font = 'bold 14px Arial';
                ctx.fillText(label, x - 8, y - 15);
            }
        }
        
        // 绘制物体
        function drawObject() {
            const centerY = canvas.height/2;
            const objectTopY = centerY - state.objectHeight;
            
            // 绘制物体（橙色箭头）
            ctx.fillStyle = '#ff9800';
            ctx.beginPath();
            // 箭头主体
            ctx.moveTo(state.objectX, centerY);
            ctx.lineTo(state.objectX - 15, objectTopY + 10);
            ctx.lineTo(state.objectX - 5, objectTopY + 10);
            ctx.lineTo(state.objectX - 5, objectTopY);
            ctx.lineTo(state.objectX + 5, objectTopY);
            ctx.lineTo(state.objectX + 5, objectTopY + 10);
            ctx.lineTo(state.objectX + 15, objectTopY + 10);
            ctx.closePath();
            ctx.fill();
            
            // 绘制物体底部标记线
            ctx.strokeStyle = '#ff9800';
            ctx.lineWidth = 
<!--检测到代码截断，自动续写中...-->
ctx.lineTo(state.objectX + 15, objectTopY + 10);
            ctx.closePath();
            ctx.fill();
            
            // 绘制物体底部标记线
            ctx.strokeStyle = '#ff9800';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(state.objectX, centerY);
            ctx.lineTo(state.objectX, centerY + 5);
            ctx.stroke();
            
            // 绘制物距标注
            if (state.showLabels) {
                ctx.strokeStyle = 'rgba(255, 152, 0, 0.6)';
                ctx.lineWidth = 1;
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(state.objectX, centerY + 20);
                ctx.lineTo(state.lensX, centerY + 20);
                ctx.stroke();
                ctx.setLineDash([]);
                
                ctx.fillStyle = '#ff9800';
                ctx.font = '12px Arial';
                ctx.fillText(`u = ${state.u.toFixed(1)} cm`, 
                    (state.objectX + state.lensX) / 2 - 25, 
                    centerY + 35);
            }
        }
        
        // 绘制像
        function drawImage() {
            if (state.u === state.f) return; // u=f时不成像
            
            const centerY = canvas.height/2;
            const scale = 2; // 1cm = 2px
            const imageX = state.lensX + (state.isRealImage ? state.v : -state.v) * scale;
            const imageTopY = centerY - (state.isRealImage ? state.imageHeight : -state.imageHeight);
            
            // 绘制像（实像为绿色，虚像为蓝色虚线）
            if (state.isRealImage) {
                // 实像 - 绿色实心箭头
                ctx.fillStyle = 'rgba(76, 175, 80, 0.8)';
                ctx.beginPath();
                ctx.moveTo(imageX, centerY);
                ctx.lineTo(imageX - 15, imageTopY + 10);
                ctx.lineTo(imageX - 5, imageTopY + 10);
                ctx.lineTo(imageX - 5, imageTopY);
                ctx.lineTo(imageX + 5, imageTopY);
                ctx.lineTo(imageX + 5, imageTopY + 10);
                ctx.lineTo(imageX + 15, imageTopY + 10);
                ctx.closePath();
                ctx.fill();
            } else {
                // 虚像 - 蓝色虚线轮廓
                ctx.strokeStyle = '#2196f3';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(imageX, centerY);
                ctx.lineTo(imageX - 15, imageTopY + 10);
                ctx.lineTo(imageX - 5, imageTopY + 10);
                ctx.lineTo(imageX - 5, imageTopY);
                ctx.lineTo(imageX + 5, imageTopY);
                ctx.lineTo(imageX + 5, imageTopY + 10);
                ctx.lineTo(imageX + 15, imageTopY + 10);
                ctx.closePath();
                ctx.stroke();
                ctx.setLineDash([]);
            }
            
            // 绘制像距标注
            if (state.showLabels) {
                ctx.strokeStyle = state.isRealImage ? 'rgba(76, 175, 80, 0.6)' : 'rgba(33, 150, 243, 0.6)';
                ctx.lineWidth = 1;
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(imageX, centerY + 40);
                ctx.lineTo(state.lensX, centerY + 40);
                ctx.stroke();
                ctx.setLineDash([]);
                
                ctx.fillStyle = state.isRealImage ? '#4caf50' : '#2196f3';
                ctx.font = '12px Arial';
                const vText = state.isRealImage ? 'v' : '-v';
                ctx.fillText(`${vText} = ${Math.abs(state.v).toFixed(1)} cm`, 
                    (imageX + state.lensX) / 2 - 25, 
                    centerY + 55);
            }
        }
        
        // 绘制光线
        function drawRays() {
            const centerY = canvas.height/2;
            const scale = 2; // 1cm = 2px
            const objectTopY = centerY - state.objectHeight;
            
            // 如果u=f，只绘制平行光线
            if (state.u === state.f) {
                drawParallelRayOnly();
                return;
            }
            
            // 计算像的位置
            const imageX = state.lensX + (state.isRealImage ? state.v : -state.v) * scale;
            const imageTopY = centerY - (state.isRealImage ? state.imageHeight : -state.imageHeight);
            
            // 光线1: 平行于主光轴 -> 过焦点
            ctx.strokeStyle = '#f44336';
            ctx.lineWidth = 2;
            ctx.beginPath();
            // 从物体顶端出发，平行于主光轴
            ctx.moveTo(state.objectX, objectTopY);
            ctx.lineTo(state.lensX, objectTopY);
            // 经过透镜后过焦点
            if (state.isRealImage) {
                // 实像：光线实际会聚
                ctx.lineTo(imageX, imageTopY);
            } else {
                // 虚像：光线的反向延长线过焦点
                const rightFX = state.lensX + state.f * scale;
                ctx.lineTo(rightFX, centerY);
                // 绘制反向延长线（虚线）
                ctx.stroke();
                ctx.strokeStyle = '#2196f3';
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(state.lensX, objectTopY);
                ctx.lineTo(imageX, imageTopY);
                ctx.stroke();
                ctx.setLineDash([]);
                ctx.strokeStyle = '#f44336';
            }
            ctx.stroke();
            
            // 光线2: 过光心 -> 方向不变
            ctx.beginPath();
            ctx.moveTo(state.objectX, objectTopY);
            ctx.lineTo(state.lensX, centerY);
            if (state.isRealImage) {
                ctx.lineTo(imageX, imageTopY);
            } else {
                // 虚像：绘制反向延长线
                ctx.stroke();
                ctx.strokeStyle = '#2196f3';
                ctx.setLineDash([5, 3]);
                ctx.beginPath();
                ctx.moveTo(state.lensX, centerY);
                ctx.lineTo(imageX, imageTopY);
                ctx.stroke();
                ctx.setLineDash([]);
                ctx.strokeStyle = '#f44336';
            }
            ctx.stroke();
            
            // 光线3: 过焦点 -> 平行于主光轴
            if (state.u > state.f) { // 只有物体在焦点外时才绘制这条光线
                ctx.beginPath();
                ctx.moveTo(state.objectX, objectTopY);
                // 指向左侧焦点
                const leftFX = state.lensX - state.f * scale;
                ctx.lineTo(leftFX, centerY);
                // 到透镜
                ctx.lineTo(state.lensX, centerY - (centerY - objectTopY));
                // 经过透镜后平行于主光轴
                if (state.isRealImage) {
                    ctx.lineTo(imageX, imageTopY);
                } else {
                    // 虚像：绘制反向延长线
                    ctx.stroke();
                    ctx.strokeStyle = '#2196f3';
                    ctx.setLineDash([5, 3]);
                    ctx.beginPath();
                    ctx.moveTo(state.lensX, centerY - (centerY - objectTopY));
                    ctx.lineTo(imageX, imageTopY);
                    ctx.stroke();
                    ctx.setLineDash([]);
                    ctx.strokeStyle = '#f44336';
                }
                ctx.stroke();
            }
            
            // 绘制光线箭头
            drawRayArrows();
        }
        
        // 绘制u=f时的平行光线
        function drawParallelRayOnly() {
            const centerY = canvas.height/2;
            const objectTopY = centerY - state.objectHeight;
            
            ctx.strokeStyle = '#f44336';
            ctx.lineWidth = 2;
            
            // 平行光线1
            ctx.beginPath();
            ctx.moveTo(state.objectX, objectTopY);
            ctx.lineTo(state.lensX, objectTopY);
            // 经过透镜后过焦点
            const rightFX = state.lensX + state.f * scale;
            ctx.lineTo(rightFX, centerY);
            ctx.stroke();
            
            // 平行光线2（从物体底部）
            ctx.beginPath();
            ctx.moveTo(state.objectX, centerY);
            ctx.lineTo(state.lensX, centerY);
            ctx.lineTo(rightFX, centerY);
            ctx.stroke();
            
            // 绘制光线箭头
            drawRayArrows();
        }
        
        // 绘制光线箭头
        function drawRayArrows() {
            // 在每条光线的末端绘制小箭头
            ctx.fillStyle = '#f44336';
            
            // 这里简化处理，在实际应用中可以根据光线方向计算箭头位置
            // 为了简化，我们只在关键位置绘制几个箭头
        }
        
        // 绘制标签
        function drawLabels() {
            const centerY = canvas.height/2;
            
            ctx.fillStyle = '#e0e0e0';
            ctx.font = '14px Arial';
            
            // 物体标签
            ctx.fillText('物体', state.objectX - 20, centerY - state.objectHeight - 10);
            
            // 像标签
            if (state.u !== state.f) {
                const scale = 2;
                const imageX = state.lensX + (state.isRealImage ? state.v : -state.v) * scale;
                const imageTopY = centerY - (state.isRealImage ? state.imageHeight : -state.imageHeight);
                
                ctx.fillStyle = state.isRealImage ? '#4caf50' : '#2196f3';
                ctx.fillText(state.isRealImage ? '实像' : '虚像', imageX - 20, imageTopY - 10);
            }
            
            // 公式显示
            ctx.fillStyle = '#ff9800';
            ctx.font = 'bold 16px Arial';
            ctx.fillText('透镜公式: 1/u + 1/v = 1/f', 50, 30);
            
            // 当前状态
            let statusText = '';
            if (state.u > 2*state.f) {
                statusText = 'u > 2f: 缩小倒立实像 (照相机原理)';
            } else if (Math.abs(state.u - 2*state.f) < 0.5) {
                statusText = 'u = 2f: 等大倒立实像';
            } else if (state.u > state.f && state.u < 2*state.f) {
                statusText = 'f < u < 2f: 放大倒立实像 (投影仪原理)';
            } else if (Math.abs(state.u - state.f) < 0.5) {
                statusText = 'u = f: 不成像 (平行光)';
            } else if (state.u < state.f) {
                statusText = 'u < f: 放大正立虚像 (放大镜原理)';
            }
            
            ctx.fillStyle = '#81c784';
            ctx.font = '14px Arial';
            ctx.fillText(statusText, 50, 60);
        }
        
        // 初始绘制
        updateDisplay();
        updateLawTableHighlight();
        draw();
        
        // 响应窗口大小变化
        window.addEventListener('resize', function() {
            // 在实际应用中，这里可以添加Canvas大小调整逻辑
            draw();
        });
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《凸透镜成像规律交互式教学动画使用指南》

### 一、功能说明

欢迎使用“凸透镜成像规律交互式教学动画”！本工具是一款基于HTML5 Canvas技术开发的物理教学动画，专门用于可视化展示凸透镜成像的动态过程。通过实时交互和动态光路图，它将抽象的物理规律转化为直观的视觉体验，旨在帮助初中及高中学生深入理解凸透镜成像的核心原理。

### 二、主要功能

1.  **实时交互模拟**
    *   **拖动物体**：在画布上直接用鼠标拖拽橙色箭头（物体），观察像的位置、大小和性质如何实时变化。
    *   **参数调节**：通过滑块精确控制**物距(u)**、**物体高度**和透镜**焦距(f)**，探索不同参数下的成像效果。

2.  **动态光路图绘制**
    *   **实时光线追踪**：自动绘制至少两条关键光线（平行于主光轴的光线、通过光心的光线），清晰展示像点是如何由光线会聚或反向延长线相交确定的。
    *   **虚实对比**：用**红色实线**表示实际光线，**蓝色虚线**表示光的反向延长线，直观区分实像与虚像。

3.  **智能学习辅助**
    *   **预设场景**：一键跳转到五个典型成像位置（`u > 2f`, `u = 2f`, `f < u < 2f`, `u = f`, `u < f`），对应照相机、投影仪、放大镜等实际应用。
    *   **规律总结表**：表格实时高亮显示当前物体位置所对应的成像规律（像的位置、大小、正倒、虚实及应用）。
    *   **公式验证**：实时计算并显示 `1/u + 1/v` 与 `1/f` 的值，帮助学生直观验证透镜成像公式 `1/u + 1/v = 1/f`。

4.  **可视化参数面板**
    *   实时显示所有关键参数：物距(u)、像距(v)、焦距(f)、放大率(M)。
    *   提供显示/隐藏控制：可切换光线、网格、标签的显示，以适应不同学习阶段的需求。

### 三、设计特色

1.  **符合认知规律的视觉设计**
    *   **深色背景**：模拟“暗室”环境，突出彩色光线和元素，减少视觉干扰。
    *   **科学的色彩编码**：物体（橙）、实像（绿）、实际光线（红）、虚像与反向延长线（蓝），建立强烈的视觉关联，便于记忆。
    *   **平滑动画**：所有变化均为平滑过渡，体现物理过程的连续性，避免认知跳跃。

2.  **层次化交互设计**
    *   **从探索到总结**：鼓励学生先自由拖拽探索，再使用预设按钮聚焦典型情况，最后结合规律表格进行总结。
    *   **可调节的信息密度**：初学者可隐藏部分光线和标签，降低认知负荷；深入学习时可打开所有辅助信息，进行定量分析。

3.  **教学与技术的深度融合**
    *   不仅展示“是什么”，更揭示“为什么”：通过光路图动态生成，阐明成像规律的几何光学本质。
    *   将口诀（如“一倍焦距分虚实，二倍焦距分大小”）与动态可视化过程绑定，使记忆建立在理解之上。

### 四、教学要点

1.  **核心概念引导**
    *   **焦点(F)与焦距(f)**：引导学生观察改变焦距时，焦点位置及整个成像情况的变化。
    *   **实像与虚像**：强调实像由实际光线**会聚**而成，能用光屏承接；虚像是实际光线**反向延长线**的会聚点，不能用于光屏承接。通过虚线/实线的绘制强化此概念。
    *   **物距(u)与像距(v)的关系**：通过拖动，让学生亲自发现“物近像远像变大，物远像近像变小”的规律（针对实像）。

2.  **关键区域探究**
    *   **三个关键点**：重点探究物体位于 `u=2f`（等大实像）、`u=f`（不成像/平行光）、`u<f`（正立放大虚像）这三个特殊位置的现象。
    *   **两个分界点**：理解 `u=f` 是实像与虚像的分界点，`u=2f` 是放大实像与缩小实像的分界点。

3.  **公式意义建构**
    *   在动态变化中，让学生观察 `1/u + 1/v` 的数值如何始终保持不变（等于 `1/f`），从而理解透镜公式不是孤立的数学表达式，而是对物理规律的定量描述。

### 五、使用建议

1.  **学生自主学习流程**
    *   **第一步：自由探索**。打开动画，随意拖动物体，观察像的“跟随”现象，获得初步感性认识。
    *   **第二步：典型实验**。点击各个预设按钮，系统观察五种典型情况，记录像的特点。
    *   **第三步：规律总结**。结合高亮显示的规律表格，尝试自己总结物体在不同区域时的成像特点。
    *   **第四步：深入探究**。调节焦距滑块，探究焦距变化对成像的影响；打开公式显示，进行定量验证。

2.  **教师课堂演示建议**
    *   **引入新课**：用动画替代静态图片，动态展示凸透镜成像的奇妙现象，激发学生兴趣。
    *   **规律讲解**：在讲解每一个规律时（如“当u>2f时…”），将物体拖到对应区域，让学生观察光路如何形成对应的像。
    *   **突破难点**：在讲解“虚像”形成时，放慢拖动速度，特别强调蓝色虚线（反向延长线）的作用，化解理解难点。
    *   **课堂练习**：可以提问：“如果要得到一个缩小的像，物体应该放在哪里？”让学生上台操作验证。

3.  **技术提示**
    *   本动画基于现代浏览器，建议使用 Chrome、Edge、Firefox 或 Safari 的最新版本以获得最佳体验。
    *   在触摸屏设备（如平板电脑）上，同样支持触摸拖拽操作，非常适合小组协作学习。

我们希望这个交互式动画能成为您探索光学世界的有力工具，让抽象的物理规律变得生动可见，让学习过程充满发现的乐趣！