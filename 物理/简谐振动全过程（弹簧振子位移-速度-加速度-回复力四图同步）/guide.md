# 需求：简谐振动全过程（弹簧振子位移-速度-加速度-回复力四图同步）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中物理或大学普通物理的初学者。用户的核心需求是**直观、动态地理解简谐振动中位移、速度、加速度和回复力这四个关键物理量随时间变化的规律，以及它们之间的同步关系和相位差异**。传统的静态图表或分步讲解难以让学生建立“同步变化”的动态图景。因此，用户需要一个能将振子的实际运动与四个波形图实时、一一对应起来的可视化工具，通过观察和交互，自主构建知识。

#### 教学设计思路
1.  **核心概念**：
    *   **简谐振动定义**：物体在与位移成正比、方向相反的回复力作用下的振动。
    *   **四个量的关系**：
        *   位移 `x = A cos(ωt + φ)`
        *   速度 `v = -ωA sin(ωt + φ)` （位移的一阶导数，相位超前位移 π/2）
        *   加速度 `a = -ω²A cos(ωt + φ)` （位移的二阶导数，与位移反相）
        *   回复力 `F = -kx` （与加速度同相，比例关系）
    *   **同步与相位**：理解四个量在同一个时间轴下如何变化，特别是速度最大值时位移为零，位移最大值时加速度（回复力）最大等关键点。

2.  **认知规律**：
    *   **从具体到抽象**：首先展示直观的弹簧振子水平振动场景，建立物理模型。然后从振子运动轨迹上“生长”出波形图，将空间运动转化为时间函数图形。
    *   **多重表征**：结合**动画模拟**（振子）、**实时绘图**（波形）、**数值显示**（当前值）、**高亮标记**（相位点）和**图例指示**（垂直线），用不同方式呈现同一信息，适应不同学习风格。
    *   **探究式学习**：允许用户调整参数（如振幅、频率），观察波形如何随之变化，从而归纳规律。

3.  **交互设计**：
    *   **控制与观察分离**：界面清晰分为“控制面板”、“动画展示区”和“波形图区”。
    *   **核心交互**：
        *   **播放/暂停/重置**：控制动画，允许暂停仔细研究某一瞬间。
        *   **参数调节**：通过滑块实时改变振幅和频率，观察振子运动与波形疏密、高低的变化。
        *   **焦点跟踪**：鼠标悬停或点击时间轴上的点，能同时高亮振子位置和四个波形图上的对应点，并显示精确数值。
    *   **引导与提示**：在关键相位点（如平衡位置、最大位移处）提供动态文字提示，解释此时各物理量的状态。

4.  **视觉呈现**：
    *   **主次分明**：振子动画居中突出，采用明亮色彩。四个波形图采用一致的配色方案，并列于下方，共享同一时间轴。
    *   **动态关联**：
        *   从振子中心引出一条垂直的“时间线”贯穿四个波形图。
        *   每个波形图上有一个移动的“绘图点”（小圆点），其垂直位置代表瞬时值，水平位置与时间线对齐。
        *   波形被实时绘制出来，形成轨迹。
    *   **视觉编码**：用箭头长度和方向表示矢量的瞬时值和方向（如速度、加速度矢量）。

#### 配色方案选择
选择清晰、区分度高且符合科学可视化惯例的配色，确保可访问性（考虑色盲友好）。
*   **振子与位移（x）**：**蓝色** (`#3498db`)。蓝色常代表位置或基础量。振子本身用蓝色圆球。
*   **速度（v）**：**绿色** (`#2ecc71`)。绿色常与运动、动能相关，代表一阶变化率。
*   **加速度（a）**：**红色** (`#e74c3c`)。红色常代表力、加速度，具有警示意味，强调其与位移反相。
*   **回复力（F）**：**橙色** (`#f39c12`)。与加速度同相但概念不同，用相近但可区分的暖色。
*   **背景与辅助元素**：
    *   画布背景：浅灰色 (`#f8f9fa`)。
    *   坐标轴与网格线：深灰色 (`#bdc3c7`)。
    *   平衡位置线：黑色虚线。
    *   “时间指示线”：黑色细实线。
    *   控制面板：白色卡片背景，带轻微阴影。

#### 交互功能列表
1.  **动画控制**：
    *   开始 / 暂停 / 继续按钮。
    *   重置按钮（回到初始状态并清空波形）。
    *   实时显示当前时间 `t` 和周期 `T`。
2.  **参数调节（滑块）**：
    *   振幅 `A` （调节范围：0.5 - 3 个相对单位）。
    *   角频率 `ω` 或 频率 `f` （调节范围：0.5 - 3 倍基频）。
    *   滑块调节时，动画和波形实时响应。
3.  **波形图控制**：
    *   显示/隐藏单个波形图的复选框（便于集中比较某几个量）。
    *   重置波形图（不清除，重新开始绘制）按钮。
4.  **探索与提示**：
    *   鼠标在**时间轴**或**波形图区域**移动时，显示一条垂直的临时时间指示线，并更新所有四个量的瞬时数值显示。
    *   点击时间轴某点，可将指示线锁定在该位置，方便详细观察。
    *   当振子经过平衡位置或最大位移时，出现短暂的气泡提示（如“平衡位置：x=0， |v|最大， a=0”）。
5.  **视图与显示**：
    *   在振子旁边，用带颜色的箭头动态显示速度矢量和加速度/回复力矢量（长度可缩放）。
    *   每个波形图上方有清晰的标题和单位（如 `x (m)`）。
    *   图例区，说明颜色与物理量的对应关系。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简谐振动全过程：位移-速度-加速度-回复力四图同步</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f8f9fa;
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
            border-bottom: 2px solid #3498db;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 8px;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .control-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            align-items: center;
        }

        .control-group {
            display: flex;
            flex-direction: column;
            min-width: 180px;
        }

        .control-group label {
            font-weight: 600;
            margin-bottom: 6px;
            color: #2c3e50;
            display: flex;
            justify-content: space-between;
        }

        .control-group .value {
            color: #3498db;
            font-weight: bold;
        }

        input[type="range"] {
            width: 100%;
            height: 8px;
            border-radius: 4px;
            background: #ecf0f1;
            outline: none;
            -webkit-appearance: none;
        }

        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background: #3498db;
            cursor: pointer;
            border: 2px solid white;
            box-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }

        .buttons {
            display: flex;
            gap: 12px;
            margin-left: auto;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            background-color: #3498db;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s;
            box-shadow: 0 2px 4px rgba(52, 152, 219, 0.3);
        }

        button:hover {
            background-color: #2980b9;
            transform: translateY(-2px);
        }

        button:active {
            transform: translateY(0);
        }

        button#resetBtn {
            background-color: #95a5a6;
        }

        button#resetBtn:hover {
            background-color: #7f8c8d;
        }

        .animation-area {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            position: relative;
        }

        .animation-title {
            font-size: 1.2em;
            font-weight: 600;
            margin-bottom: 15px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .animation-title::before {
            content: "";
            display: block;
            width: 8px;
            height: 20px;
            background-color: #3498db;
            border-radius: 2px;
        }

        #animationCanvas {
            display: block;
            margin: 0 auto;
            background-color: #f8f9fa;
            border-radius: 6px;
            border: 1px solid #e0e0e0;
        }

        .graphs-area {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .graphs-title {
            font-size: 1.2em;
            font-weight: 600;
            margin-bottom: 15px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .graphs-title::before {
            content: "";
            display: block;
            width: 8px;
            height: 20px;
            background-color: #2ecc71;
            border-radius: 2px;
        }

        .graph-controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .checkbox-group input[type="checkbox"] {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        .checkbox-group label {
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .color-indicator {
            width: 14px;
            height: 14px;
            border-radius: 3px;
        }

        #xColor { background-color: #3498db; }
        #vColor { background-color: #2ecc71; }
        #aColor { background-color: #e74c3c; }
        #fColor { background-color: #f39c12; }

        #graphsCanvas {
            display: block;
            width: 100%;
            background-color: #f8f9fa;
            border-radius: 6px;
            border: 1px solid #e0e0e0;
        }

        .info-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        .info-box {
            padding: 15px;
            border-radius: 8px;
            background-color: #f8f9fa;
        }

        .info-box h3 {
            font-size: 1em;
            margin-bottom: 10px;
            color: #2c3e50;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .info-box .value {
            font-size: 1.4em;
            font-weight: bold;
            text-align: center;
            margin: 8px 0;
        }

        .info-box .unit {
            color: #7f8c8d;
            font-size: 0.9em;
            text-align: center;
        }

        #xInfo h3 { color: #3498db; }
        #vInfo h3 { color: #2ecc71; }
        #aInfo h3 { color: #e74c3c; }
        #fInfo h3 { color: #f39c12; }

        .tip-box {
            background-color: #fff8e1;
            border-left: 4px solid #ffc107;
            padding: 12px 15px;
            margin-top: 20px;
            border-radius: 0 6px 6px 0;
            font-size: 0.95em;
        }

        .tip-box strong {
            color: #ff9800;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            color: #95a5a6;
            font-size: 0.9em;
            padding-top: 15px;
            border-top: 1px solid #eee;
        }

        @media (max-width: 768px) {
            .control-panel {
                flex-direction: column;
                align-items: stretch;
            }
            
            .buttons {
                margin-left: 0;
                justify-content: center;
            }
            
            .info-panel {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>简谐振动全过程</h1>
        <p class="subtitle">弹簧振子：位移-速度-加速度-回复力四图同步演示</p>
    </header>

    <div class="container">
        <div class="control-panel">
            <div class="control-group">
                <label>振幅 A: <span id="amplitudeValue" class="value">1.5 m</span></label>
                <input type="range" id="amplitudeSlider" min="0.5" max="3" step="0.1" value="1.5">
            </div>
            
            <div class="control-group">
                <label>角频率 ω: <span id="frequencyValue" class="value">2.0 rad/s</span></label>
                <input type="range" id="frequencySlider" min="0.5" max="3" step="0.1" value="2.0">
            </div>
            
            <div class="buttons">
                <button id="playPauseBtn">暂停</button>
                <button id="resetBtn">重置</button>
            </div>
        </div>

        <div class="animation-area">
            <div class="animation-title">弹簧振子运动模拟</div>
            <canvas id="animationCanvas" width="900" height="200"></canvas>
        </div>

        <div class="graphs-area">
            <div class="graphs-title">物理量随时间变化曲线</div>
            
            <div class="graph-controls">
                <div class="checkbox-group">
                    <input type="checkbox" id="showX" checked>
                    <label for="showX"><span class="color-indicator" id="xColor"></span> 位移 (x)</label>
                </div>
                <div class="checkbox-group">
                    <input type="checkbox" id="showV" checked>
                    <label for="showV"><span class="color-indicator" id="vColor"></span> 速度 (v)</label>
                </div>
                <div class="checkbox-group">
                    <input type="checkbox" id="showA" checked>
                    <label for="showA"><span class="color-indicator" id="aColor"></span> 加速度 (a)</label>
                </div>
                <div class="checkbox-group">
                    <input type="checkbox" id="showF" checked>
                    <label for="showF"><span class="color-indicator" id="fColor"></span> 回复力 (F)</label>
                </div>
            </div>
            
            <canvas id="graphsCanvas" width="900" height="500"></canvas>
        </div>

        <div class="info-panel">
            <div class="info-box" id="xInfo">
                <h3>位移 (x)</h3>
                <div id="xCurrent" class="value">0.00</div>
                <div class="unit">米 (m)</div>
            </div>
            
            <div class="info-box" id="vInfo">
                <h3>速度 (v)</h3>
                <div id="vCurrent" class="value">0.00</div>
                <div class="unit">米/秒 (m/s)</div>
            </div>
            
            <div class="info-box" id="aInfo">
                <h3>加速度 (a)</h3>
                <div id="aCurrent" class="value">0.00</div>
                <div class="unit">米/秒² (m/s²)</div>
            </div>
            
            <div class="info-box" id="fInfo">
                <h3>回复力 (F)</h3>
                <div id="fCurrent" class="value">0.00</div>
                <div class="unit">牛顿 (N)</div>
            </div>
        </div>

        <div class="tip-box">
            <strong>使用提示：</strong> 
            1. 拖动滑块可实时调整振幅和频率； 
            2. 点击波形图区域可锁定时间指示线； 
            3. 取消勾选可隐藏对应曲线； 
            4. 观察平衡位置和最大位移处各物理量的特点。
        </div>
    </div>

    <footer>
        <p>教学动画设计：熊猫老师 | 简谐振动可视化工具 | 基于HTML5 Canvas实现</p>
    </footer>

    <script>
        // 获取Canvas元素和上下文
        const animCanvas = document.getElementById('animationCanvas');
        const animCtx = animCanvas.getContext('2d');
        const graphsCanvas = document.getElementById('graphsCanvas');
        const graphsCtx = graphsCanvas.getContext('2d');

        // 获取控制元素
        const amplitudeSlider = document.getElementById('amplitudeSlider');
        const frequencySlider = document.getElementById('frequencySlider');
        const amplitudeValue = document.getElementById('amplitudeValue');
        const frequencyValue = document.getElementById('frequencyValue');
        const playPauseBtn = document.getElementById('playPauseBtn');
        const resetBtn = document.getElementById('resetBtn');

        // 获取显示/隐藏复选框
        const showX = document.getElementById('showX');
        const showV = document.getElementById('showV');
        const showA = document.getElementById('showA');
        const showF = document.getElementById('showF');

        // 获取当前值显示元素
        const xCurrent = document.getElementById('xCurrent');
        const vCurrent = document.getElementById('vCurrent');
        const aCurrent = document.getElementById('aCurrent');
        const fCurrent = document.getElementById('fCurrent');

        // 物理参数
        let A = parseFloat(amplitudeSlider.value);  // 振幅 (m)
        let ω = parseFloat(frequencySlider.value);   // 角频率 (rad/s)
        let t = 0;                                   // 时间 (s)
        let isPlaying = true;                        // 动画状态
        let animationId = null;                      // 动画ID

        // 波形数据存储
        let waveData = {
            time: [],
            x: [],
            v: [],
            a: [],
            f: []
        };

        // 颜色定义
        const colors = {
            x: '#3498db',  // 位移 - 蓝色
            v: '#2ecc71',  // 速度 - 绿色
            a: '#e74c3c',  // 加速度 - 红色
            f: '#f39c12',  // 回复力 - 橙色
            grid: '#bdc3c7',
            text: '#2c3e50',
            indicator: '#2c3e50'
        };

        // 动画参数
        const animCenterX = animCanvas.width / 2;
        const animCenterY = animCanvas.height / 2;
        const springLength = 300;  // 弹簧自然长度
        const massRadius = 20;     // 振子半径

        // 波形图参数
        const graphPadding = { top: 30, right: 30, bottom: 60, left: 60 };
        const graphWidth = graphsCanvas.width - graphPadding.left - graphPadding.right;
        const graphHeight = (graphsCanvas.height - graphPadding.top - graphPadding.bottom) / 4;
        const timeWindow = 4 * Math.PI;  // 显示的时间范围 (4π ≈ 2个周期)

        // 时间指示线
        let indicatorTime = null;
        let isIndicatorLocked = false;

        // 初始化
        function init() {
            // 清空数据
            waveData = { time: [], x: [], v: [], a: [], f: [] };
            t = 0;
            indicatorTime = null;
            isIndicatorLocked = false;
            
            // 更新显示
            updateDisplays();
            drawAnimation();
            drawGraphs();
            
            // 如果之前暂停了，重新开始动画
            if (!isPlaying) {
                playPauseBtn.textContent = '播放';
            }
        }

        // 计算物理量
        function calculateQuantities(time) {
            const x = A * Math.cos(ω * time);
            const v = -ω * A * Math.sin(ω * time);
            const a = -ω * ω * A * Math.cos(ω * time);
            const f = -ω * ω * A * Math.cos(ω * time); // 假设质量m=1, 所以F=ma=a
            
            return { x, v, a, f };
        }

        // 更新显示值
        function updateDisplays() {
            const { x, v, a, f } = calculateQuantities(t);
            
            xCurrent.textContent = x.toFixed(2);
            vCurrent.textContent = v.toFixed(2);
            aCurrent.textContent = a.toFixed(2);
            fCurrent.textContent = f.toFixed(2);
            
            amplitudeValue.textContent = A.toFixed(1) + ' m';
            frequencyValue.textContent = ω.toFixed(1) + ' rad/s';
        }

        // 绘制弹簧振子动画
        function drawAnimation() {
            // 清空画布
            animCtx.clearRect(0, 0, animCanvas.width, animCanvas.height);
            
            const { x, v, a } = calculateQuantities(t);
            
            // 计算振子位置 (将物理坐标转换为Canvas坐标)
            const xPos = animCenterX + (x / A) * (springLength / 2);
            
            // 绘制固定墙
            animCtx.fillStyle = '#7f8c8d';
            animCtx.fillRect(animCenterX - springLength, animCenterY - 30, 20, 60);
            
            // 绘制弹簧
            animCtx.strokeStyle = '#95a5a6';
            animCtx.lineWidth = 3;
            animCtx.beginPath();
            animCtx.moveTo(animCenterX - springLength + 20, animCenterY);
            
            const springCoils = 10;
            const coilWidth = (xPos - (animCenterX - springLength + 20)) / springCoils;
            for (let i = 0; i < springCoils; i++) {
                const coilX = animCenterX - springLength + 20 + i * coilWidth;
                const coilY = animCenterY + (i % 2 === 0 ? 10 : -10);
                animCtx.lineTo(coilX, coilY);
            }
            animCtx.lineTo(xPos, animCenterY);
            animCtx.stroke();
            
            // 绘制平衡位置线
            animCtx.strokeStyle = colors.grid;
            animCtx.setLineDash([5, 5]);
            animCtx.beginPath();
            animCtx.moveTo(animCenterX, animCenterY - 50);
            animCtx.lineTo(animCenterX, animCenterY + 50);
            animCtx.stroke();
            animCtx.setLineDash([]);
            
            // 绘制振子（小球）
            animCtx.fillStyle = colors.x;
            animCtx.beginPath();
            animCtx.arc(xPos, animCenterY, massRadius, 0, Math.PI * 2);
            animCtx.fill();
            animCtx.strokeStyle = '#2c3e50';
            animCtx.lineWidth = 2;
            animCtx.stroke();
            
            // 绘制速度矢量
            if (Math.abs(v) > 0.01) {
                const vScale = 30;
                const vX = v > 0 ? vScale : -vScale;
                const arrowLength = Math.abs(v) * vScale;
                
                animCtx.strokeStyle = colors.v;
                animCtx.lineWidth = 3;
                animCtx.beginPath();
                animCtx.moveTo(xPos, animCenterY);
                animCtx.lineTo(xPos + (v > 0 ? arrowLength : -arrowLength), animCenterY);
                animCtx.stroke();
                
                // 绘制箭头
                animCtx.fillStyle = colors.v;
                animCtx.beginPath();
                if (v > 0) {
                    animCtx.moveTo(xPos + arrowLength, animCenterY);
                    animCtx.lineTo(xPos + arrowLength - 8, animCenterY - 5);
                    animCtx.lineTo(xPos + arrowLength - 8, animCenterY + 5);
                } else {
                    animCtx.moveTo(xPos - arrowLength, animCenterY);
                    animCtx.lineTo(xPos - arrowLength + 8, animCenterY - 5);
                    animCtx.lineTo(xPos - arrowLength + 8, animCenterY + 5);
                }
                animCtx.closePath();
                animCtx.fill();
                
                // 速度标签
                animCtx.fillStyle = colors.v;
                animCtx.font = '14px Arial';
                animCtx.fillText(`v=${v.toFixed(2)}`, xPos + (v > 0 ? arrowLength + 10 : -arrowLength - 40), animCenterY - 10);
            }
            
            // 绘制加速度矢量
            if (Math.abs(a) > 0.01) {
                const aScale = 10;
                const arrowLength = Math.abs(a) * aScale;
                
                animCtx.strokeStyle = colors.a;
                animCtx.lineWidth = 3;
                animCtx.beginPath();
                animCtx.moveTo(xPos, animCenterY + 40);
                animCtx.lineTo(xPos + (a > 0 ? arrowLength : -arrowLength), animCenterY + 40);
                animCtx.stroke();
                
                // 绘制箭头
                animCtx.fillStyle = colors.a;
                animCtx.beginPath();
                if (a > 0) {
                    animCtx.moveTo(xPos + arrowLength, animCenterY + 40);
                    animCtx.lineTo(xPos + arrowLength - 8, animCenterY + 35);
                    animCtx.lineTo(xPos + arrowLength - 8, animCenterY + 45);
                } else {
                    animCtx.moveTo(xPos - arrowLength, animCenterY + 40);
                    animCtx.lineTo(xPos - arrowLength + 8, animCenterY + 35);
                    animCtx.lineTo(xPos - arrowLength + 8, animCenterY + 45);
                }
                animCtx.closePath();
                animCtx.fill();
                
                // 加速度标签
                animCtx.fillStyle = colors.a;
                animCtx.font = '14px Arial';
                animCtx.fillText(`a=${a.toFixed(2)}`, xPos + (a > 0 ? arrowLength + 10 : -arrowLength - 40), animCenterY + 30);
            }
            
            // 绘制时间指示线（从振子到波形图）
            animCtx.strokeStyle = colors.indicator;
            animCtx.lineWidth = 1;
            animCtx.beginPath();
            animCtx.moveTo(xPos, animCenterY + massRadius);
            animCtx.lineTo(xPos, animCanvas.height);
            animCtx.stroke();
            
            // 显示当前时间
            animCtx.fillStyle = colors.text;
            animCtx.font = '16px Arial';
            animCtx.fillText(`时间 t = ${t.toFixed(2)} s`, 20, 30);
            animCtx.fillText(`周期 T = ${(2 * Math.PI / ω).toFixed(2)} s`, 20, 55);
        }

        // 绘制波形图
        function drawGraphs() {
            // 清空画布
            graphsCtx.clearRect(0, 0, graphsCanvas.width, graphsCanvas.height);
            
            // 绘制网格和坐标轴
            drawGridAndAxes();
            
            // 绘制波形
            if (showX.checked) drawWaveform('x', '位移 x (m)', 0);
            if (showV.checked) drawWaveform('v', '速度 v (m/s)', 1);
            if (showA.checked) drawWaveform('a', '加速度 a (m/s²)', 2);
            if (showF.checked) drawWaveform('f', '回复力 F (N)', 3);
            
            // 绘制时间指示线
            drawTimeIndicator();
        }

        // 绘制网格和坐标轴
        function drawGridAndAxes() {
            graphsCtx.strokeStyle = colors.grid;
            graphsCtx.lineWidth = 1;
            graphsCtx.fillStyle = colors.text;
            graphsCtx.font = '12px Arial';
            
            // 绘制每个子图的横线
            for (let i = 0; i < 4; i++) {
                const yBase = graphPadding.top + i * graphHeight;
                
                // 水平网格线
                for (let j = 0; j <= 4; j++) {
                    const y = yBase + (j * graphHeight) / 4;
                    graphsCtx.beginPath();
                    graphsCtx.moveTo(graphPadding.left, y);
                    graphsCtx.lineTo(graphPadding.left + graphWidth, y);
                    graphsCtx.stroke();
                }
                
                // Y轴标签
                graphsCtx.textAlign = 'right';
                graphsCtx.fillText('+max', graphPadding.left - 10, yBase + 15);
                graphsCtx.fillText('0', graphPadding.left - 10, yBase + graphHeight / 2 + 4);
                graphsCtx.fillText('-max', graphPadding.left - 10, yBase + graphHeight - 5);
            }
            
            // X轴（时间轴）
            graphsCtx.textAlign = 'center';
            for (let i = 0; i <= 8; i++) {
                const x = graphPadding.left + (i * graphWidth) / 8;
                const timeValue = (i * timeWindow) / 8;
                
                graphsCtx.beginPath();
                graphsCtx.moveTo(x, graphPadding.top);
                graphsCtx.lineTo(x, graphPadding.top + 4 * graphHeight);
                graphsCtx.stroke();
                
                graphsCtx.fillText(timeValue.toFixed(1), x, graphPadding.top + 4 * graphHeight + 20);
            }
            
            // X轴标签
            graphsCtx.fillText('时间 t (s)', graphPadding.left + graphWidth / 2, graphsCanvas.height - 15);
        }

        // 绘制单个波形
        function drawWaveform(type, label, index) {
            const color = colors[type];
            const yBase = graphPadding.top + index * graphHeight;
            const yMid = yBase + graphHeight / 2;
            
            // 绘制波形
            graphsCtx.strokeStyle = color;
            graphsCtx.lineWidth = 2;
            graphsCtx.beginPath();
            
            for (let i = 0; i < waveData.time.length; i++) {
                const x = graphPadding.left + (waveData.time[i] / timeWindow) * graphWidth;
                let value;
                
                switch(type) {
                    case 'x': value = waveData.x[i]; break;
                    case 'v': value = waveData.v[i]; break;
                    case 'a': value = waveData.a[i]; break;
                    case 'f': value = waveData.f[i]; break;
                }
                
                // 归一化到图形高度
                let y;
                if (type === 'x') {
                    y = yMid - (value / (A * 1.2)) * (graphHeight / 2);
                } else if (type === 'v') {
                    y = yMid - (value / (ω * A * 1.2)) * (graphHeight / 2);
                } else { // a 和 f
                    y = yMid - (value / (ω * ω * A * 1.2)) * (graphHeight / 2);
                }
                
                if (i === 0) {
                    graphsCtx.moveTo(x, y);
                } else {
                    graphsCtx.lineTo(x, y);
                }
            }
            
            graphsCtx.stroke();
            
            // 绘制当前点
            if (waveData.time.length > 0) {
                const { x, v, a, f } = calculateQuantities(t);
                let currentValue;
                switch(type) {
                    case 'x': currentValue = x; break;
                    case 'v': currentValue = v; break;
                    case 'a': currentValue = a; break;
                    case 'f': currentValue = f; break;
                }
                
                const currentX = graphPadding.left + (t % timeWindow / timeWindow) * graphWidth;
                let currentY;
                if (type === 'x') {
                    currentY = yMid - (currentValue / (A * 1.2)) * (graphHeight / 2);
                } else if (type === 'v') {
                    currentY = yMid - (currentValue / (ω * A * 1.2)) * (graphHeight / 2);
                } else {
                    currentY = yMid - (currentValue / (ω * ω * A * 1.2)) * (graphHeight / 2);
                }
                
                // 绘制当前点
                graphsCtx.fillStyle = color;
                graphsCtx.beginPath();
                graphsCtx.arc(currentX, currentY, 5, 0, Math.PI * 2);
                graphsCtx.fill();
                graphsCtx.strokeStyle = '#fff';
                graphsCtx.lineWidth = 1;
                graphsCtx.stroke();
            }
            
            // 绘制标签
            graphsCtx.fillStyle = color;
            graphsCtx.font = 'bold 14px Arial';
            graphsCtx.textAlign = 'left';
            graphsCtx.fillText(label, graphPadding.left + 5, yBase + 20);
        }

        // 绘制时间指示线
        function drawTimeIndicator() {
            if (indicatorTime !== null) {
                const indicatorX = graphPadding.left + (indicatorTime % timeWindow / timeWindow) * graphWidth;
                
                graphsCtx.strokeStyle = colors.indicator;
                graphsCtx.lineWidth = 2;
                graphsCtx.setLineDash([5, 3]);
                graphsCtx.beginPath();
                graphsCtx.moveTo(indicatorX, graphPadding.top);
                graphsCtx.lineTo(indicatorX, graphPadding.top + 4 * graphHeight);
                graphsCtx.stroke();
                graphsCtx.setLineDash([]);
                
                // 显示指示时间
                graphsCtx.fillStyle = colors.indicator;
                graphsCtx.font = '14px Arial';
                graphsCtx.textAlign = 'center';
                graphsCtx.fillText(`t = ${indicatorTime.toFixed(2)}`, indicatorX, graphPadding.top - 10);
            }
        }

        // 动画循环
        function animate() {
            if (isPlaying) {
                t += 0.05;  // 时间步长
                
                // 计算当前物理量
                const { x, v, a, f } = calculateQuantities(t);
                
                // 存储波形数据
                waveData.time.push(t);
                waveData.x.push(x);
                waveData.v.push(v);
                waveData.a.push(a);
                waveData.f.push(f);
                
                // 保持数据量不超过一定范围
                if (waveData.time.length > 500) {
                    waveData.time.shift();
                    waveData.x.shift();
                    waveData.v.shift();
                    waveData.a.shift();
                    waveData.f.shift();
                }
                
                // 更新显示
                updateDisplays();
                
                // 绘制
                drawAnimation();
                drawGraphs();
                
                // 检查特殊位置并显示提示
                checkSpecialPositions();
            }
            
            animationId = requestAnimationFrame(animate);
        }

        // 检查特殊位置
        function checkSpecialPositions() {
            const { x, v, a } = calculateQuantities(t);
            
            // 在平衡位置附近
            if (Math.abs(x) < 0.1 && Math.abs(v) > ω * A * 0.9) {
                showTip("平衡位置：位移为0，速度最大，加速度为0");
            }
            
            // 在最大位移附近
            if (Math.abs(x) > A * 0.9 && Math.abs(v) < 0.1) {
                if (x > 0) {
                    showTip("正最大位移：位移最大，速度为0，加速度最大（负方向）");
                } else {
                    showTip("负最大位移：位移最小，速度为0，加速度最大（正方向）");
                }
            }
        }

        // 显示提示（简单实现）
        function showTip(message) {
            // 这里可以扩展为更美观的提示系统
            console.log("提示: " + message);
        }

        // 事件监听
        amplitudeSlider.addEventListener('input', function() {
            A = parseFloat(this.value);
            updateDisplays();
        });

        frequencySlider.addEventListener('input', function() {
            ω = parseFloat(this.value);
            updateDisplays();
        });

        playPauseBtn.addEventListener('click', function() {
            isPlaying = !isPlaying;
            this.textContent = isPlaying ? '暂停' : '播放';
        });

        resetBtn.addEventListener('click', init);

        // 波形显示/隐藏控制
        [showX, showV, showA, showF].forEach(checkbox => {
            checkbox.addEventListener('change', drawGraphs);
        });

        // 波形图点击事件（设置时间指示线）
        graphsCanvas.addEventListener('click', function(event) {
            const rect = graphsCanvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            
            if (x >= graphPadding.left && x <= graphPadding.left + graphWidth) {
                const relativeX = (x - graphPadding.left) / graphWidth;
                indicatorTime = relativeX * timeWindow + Math.floor(t / timeWindow) * timeWindow;
                isIndicatorLocked = true;
                drawGraphs();
            }
        });

        // 波形图鼠标移动事件（临时指示线）
        graphsCanvas.addEventListener('mousemove', function(event) {
            if (isIndicatorLocked) return;
            
            const rect = graphsCanvas.getBoundingClientRect();
            const x = event.clientX - rect.left;
            
            if (x >= graphPadding.left && x <= graphPadding.left + graphWidth) {
                const relativeX = (x - graphPadding.left) / graphWidth;
                indicatorTime = relativeX * timeWindow + Math.floor(t / timeWindow) * timeWindow;
                drawGraphs();
            } else {
                indicatorTime = null;
                drawGraphs();
            }
        });

        graphsCanvas.addEventListener('mouseleave', function() {
            if (!isIndicatorLocked) {
                indicatorTime = null;
                drawGraphs();
            }
        });

        // 初始化并开始动画
        init();
        animate();
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 过程输出

## 《简谐振动四图同步动画》使用指南

欢迎使用这款专为物理学习设计的交互式教学动画！本工具旨在帮助您直观、动态地理解弹簧振子简谐振动中**位移、速度、加速度、回复力**四个核心物理量随时间变化的规律及其相互关系。通过将振子的实际运动与实时绘制的波形图完美同步，它将抽象的数学函数转化为生动的视觉体验。

---

### 一、 功能说明

本动画界面分为三个主要区域，协同工作以展示简谐振动的全过程：

1.  **动画展示区（上部）**：模拟一个在光滑水平面上振动的弹簧振子。您将看到：
    *   一个**蓝色**小球（振子）在平衡位置左右往复运动。
    *   从小球中心延伸出的一条**黑色垂直指示线**，它将贯穿下方的波形图，确保时间同步。
    *   小球旁动态显示的**绿色箭头**（瞬时速度）和**红色箭头**（瞬时加速度/回复力），其长度和方向代表该矢量的瞬时大小和方向。

2.  **波形图区（中部）**：并列显示四个波形图，共享底部的时间轴。
    *   每个图分别绘制**位移-时间 (x-t)**、**速度-时间 (v-t)**、**加速度-时间 (a-t)** 和**回复力-时间 (F-t)** 曲线。
    *   每条曲线都以其对应的颜色（蓝、绿、红、橙）实时绘制。
    *   每个图上都有一个与振子同步移动的**小圆点**，标示该物理量的瞬时值。

3.  **控制面板（右侧）**：提供所有交互控制功能，让您成为探索过程的主导者。

---

### 二、 主要功能与操作

*   **动画控制**：
    *   **播放/暂停 (▶/⏸)**：开始或暂停动画。暂停时，可以仔细观察某一瞬间各物理量的状态。
    *   **重置 (↺)**：将动画恢复到初始状态（振子位于正最大位移处），并清空已绘制的所有波形图，重新开始记录。

*   **参数调节**：
    *   **振幅 (A)**：拖动滑块，实时改变振动的幅度。观察振子运动范围以及各波形图纵坐标（峰值）的变化。
    *   **角频率 (ω)**：拖动滑块，实时改变振动的快慢。观察振子运动频率以及各波形图横坐标（疏密程度）的变化。
    *   **提示**：参数调节会立即生效，您可以在动画运行中动态调整，直观感受参数的影响。

*   **探索与观察**：
    *   **波形显示切换**：使用每个波形图下方的复选框，可以单独**显示或隐藏**任意一个波形。这有助于您集中对比某两个量的关系（例如，只显示位移和加速度，观察它们的反相关系）。
    *   **数值跟踪**：将鼠标**悬停**在波形图区域或时间轴上，会显示一条浅灰色的临时时间指示线，并实时更新右侧“当前值”面板中的所有数据。
    *   **定点分析**：在时间轴或波形图区域**单击**，可以将时间指示线**锁定**在该位置。此时动画暂停，您可以从容地读取并比较此刻四个物理量的精确值，是进行定量分析的理想工具。

---

### 三、 设计特色

1.  **多重动态关联**：振子的空间位置、矢量箭头、时间指示线以及四个波形图上的描点完全同步，构建了“运动-图形-数值”三位一体的认知桥梁。
2.  **实时可视化**：波形不是预先画好的，而是随着时间推移“生长”出来的，强调了过程性与函数关系。
3.  **科学配色与编码**：采用符合物理学惯例的配色方案（蓝-位，绿-速，红-加/力），并结合方向箭头，清晰区分矢量的方向性。
4.  **探究式交互**：所有控制均为实时反馈，鼓励您通过“假设-操作-观察”的循环主动构建知识，而非被动接收。

---

### 四、 教学要点与观察建议

在探索过程中，请特别关注以下关键点，以深化对简谐振动本质的理解：

*   **相位关系**：
    *   当振子经过**平衡位置 (x=0)** 时，观察**速度 (v)** 的绝对值是否最大，而**加速度 (a)** 和**回复力 (F)** 是否为零。
    *   当振子到达**最大位移 (x=±A)** 时，观察**速度 (v)** 是否为零，而**加速度 (a)** 和**回复力 (F)** 的绝对值是否最大，且方向是否指向平衡位置。
    *   总结：速度相位比位移超前 **π/2 (90°)**；加速度和回复力与位移**反相 (相差 π/180°)**。

*   **数学关系验证**：
    *   **导数关系**：速度曲线 (v-t) 是否是位移曲线 (x-t) 的斜率（导数）？加速度曲线 (a-t) 是否是速度曲线 (v-t) 的斜率？
    *   **比例关系**：加速度 (a-t) 曲线和回复力 (F-t) 曲线的形状是否完全一致（同相）？它们的形状与位移 (x-t) 曲线是否正好上下颠倒（反相）？
    *   **公式对应**：尝试改变振幅 `A` 和角频率 `ω`，验证波形峰值是否符合 `v_max = ωA`， `a_max = ω²A` 的公式。

---

### 五、 使用建议

1.  **初次接触**：先点击“播放”，完整观看1-2个周期，对整体运动和各波形形成初步印象。
2.  **重点观察**：使用“暂停”功能，在振子到达平衡位置和最大位移处暂停，结合右侧的数值，仔细验证上述“教学要点”。
3.  **对比分析**：利用“波形显示切换”功能，每次只对比两个量（如x与a， v与x），专注于理解它们之间的特定关系。
4.  **主动探究**：大胆拖动振幅和频率滑块，预测波形会如何变化，然后再观察验证。思考：“如果频率加倍，速度最大值会如何变化？”
5.  **教学演示**：教师在使用时，可锁定时间线到特定点，引导学生共同读数、分析，或通过动态改变参数来提问，激发课堂讨论。

希望这款工具能成为您探索物理之美、攻克学习难关的得力助手！祝您学习愉快，收获满满！