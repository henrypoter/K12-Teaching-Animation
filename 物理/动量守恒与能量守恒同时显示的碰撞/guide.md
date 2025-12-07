# 需求：动量守恒与能量守恒同时显示的碰撞

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中或大学低年级的物理学习者。他们已具备基本的力学知识（如速度、质量、动量、动能），但可能对两个守恒定律在碰撞过程中的动态关系、区别与联系感到抽象和困惑。
2.  **核心需求**：
    *   **直观理解**：希望看到动量守恒和能量守恒这两个抽象定律如何“同时”在碰撞中体现，而不仅仅是记住公式。
    *   **对比与联系**：需要清晰地区分“动量”和“能量”这两个概念，理解动量是矢量（有方向），能量是标量（无方向），以及它们在碰撞前后的变化（或不变）规律。
    *   **探究与验证**：希望通过调整参数（如质量、初速度、恢复系数）来观察两个守恒定律如何被满足或如何变化，从而加深理解。
    *   **问题诊断**：常见误区是混淆两个守恒定律的适用条件，动画应能清晰展示弹性碰撞、非弹性碰撞和完全非弹性碰撞下，两个定律的不同表现。

#### 教学设计思路
1.  **核心概念**：
    *   **动量守恒**：系统不受外力或合外力为零时，系统总动量（`p = m * v`，矢量）保持不变。重点展示碰撞前后，两个物体动量的矢量和（通过矢量箭头叠加）不变。
    *   **能量守恒（特指机械能）**：仅在弹性碰撞中，系统总动能（`Ek = 1/2 * m * v^2`，标量）保持不变。在非弹性碰撞中，部分动能转化为内能等其他形式，总动能减少。
    *   **关键对比**：动量是**矢量守恒**，关注方向；动能是**标量（可能不）守恒**，只关注大小。碰撞的“弹性”程度（恢复系数）决定了动能是否守恒。

2.  **认知规律**：
    *   **从具体到抽象**：先展示小球碰撞的直观物理现象，再同步呈现数据和图表，将感性认识与理性公式联系起来。
    *   **双重编码**：结合视觉动画（小球运动、箭头、条形图）和语言/数字信息（公式、数值、标签），强化记忆与理解。
    *   **对比突出**：将动量与能量的可视化元素（如箭头 vs. 条形图，矢量加法 vs. 标量加法）并置对比，突出其根本差异。
    *   **即时反馈**：用户每次调整参数后，动画立即运行，并实时更新所有数据和图表，让用户直接看到因果关系。

3.  **交互设计**：
    *   **“沙盒”式探索**：提供一个可自由调控的模拟环境，鼓励用户通过“假设-实验-观察”的循环进行主动学习。
    *   **分层控制**：提供预设场景（如经典弹性碰撞、质量悬殊碰撞、完全非弹性碰撞）供初学者快速观察，同时提供完整参数面板供深入探究。
    *   **焦点引导**：通过高亮、动画过渡和同步强调，在碰撞关键时刻引导用户注意力到关键数据的变化上。

4.  **视觉呈现**：
    *   **主舞台**：一个光滑的水平轨道，两个球体在其上进行一维碰撞，确保场景简洁，排除重力干扰。
    *   **双重可视化面板**：
        *   **动量面板**：用有颜色、带长度的箭头表示每个球的动量矢量。用“矢量加法”动画展示碰撞前后两个箭头的合矢量（如平移至共起点）保持不变。
        *   **能量面板**：用条形图表示每个球的动能，以及系统的总动能。用不同颜色或纹理区分“动能”和“内能等其他形式能量”（在非弹性碰撞时出现）。
    *   **实时数据仪表盘**：清晰显示碰撞前后各球的速度、动量、动能以及系统的总动量、总动能数值。
    *   **轨迹与历史**：可选显示动量矢量或能量柱状图随时间变化的轻量化历史轨迹，帮助理解动态过程。

#### 配色方案选择
*   **主色调与对象**：
    *   **球A**：采用冷色调，如 `#3498db`（蓝色），代表清晰、理性。
    *   **球B**：采用暖色调，如 `#e74c3c`（红色），代表活跃、明显。
    *   配色与对应的动量箭头、动能条形图颜色保持一致，建立强烈的视觉关联。
*   **背景与界面**：
    *   主背景：`#f8f9fa`（浅灰白），确保内容突出，减少视觉疲劳。
    *   轨道/界面控件：`#2c3e50`（深蓝灰），稳重、专业。
*   **数据与高亮**：
    *   总动量/合矢量：`#16a085`（青色），象征守恒、稳定。
    *   总动能条形图：`#f39c12`（橙色），醒目，用于强调变化或守恒。
    *   损失的能量（内能）：`#95a5a6`（灰色），表示“转化”或“耗散”。
    *   重要数值/碰撞瞬间高亮：使用柔和的高光或脉冲动画，如淡黄色背景。

#### 交互功能列表
1.  **模拟控制**：
    *   【开始/暂停/重置】按钮：控制动画播放。
    *   【单步前进】按钮：用于精细观察碰撞瞬间。
2.  **场景预设**（一键设置）：
    *   弹性碰撞（等质量，等速反向）
    *   弹性碰撞（大质量撞小质量）
    *   完全非弹性碰撞（碰后粘连）
    *   非弹性碰撞（一般情况）
3.  **参数调节面板**（滑块或输入框）：
    *   球A质量 `mA`、球B质量 `mB`
    *   球A初速度 `vA`、球B初速度 `vB`
    *   **恢复系数 `e`** (0 到 1)：核心参数，控制碰撞的弹性程度（`e=1`为弹性，`e=0`为完全非弹性）。
4.  **可视化显示开关**：
    *   显示/隐藏动量矢量箭头。
    *   显示/隐藏动量矢量合成图示。
    *   显示/隐藏动能条形图。
    *   显示/隐藏总能量损失（内能）条形。
    *   显示/隐藏实时数据面板。
5.  **数据与图表**：
    *   实时数值显示（速度、动量、动能、总和）。
    *   碰撞前后关键数据对比表格。
    *   （可选）动量与动能随时间变化的微型折线图。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>动量守恒与能量守恒碰撞模拟</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f8f9fa;
            color: #2c3e50;
            line-height: 1.6;
            padding: 20px;
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #3498db;
        }

        h1 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 2.2rem;
        }

        .subtitle {
            color: #7f8c8d;
            font-size: 1.1rem;
        }

        .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
        }

        .main-content {
            flex: 3;
            min-width: 300px;
        }

        .control-panel {
            flex: 1;
            min-width: 280px;
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
        }

        .simulation-area {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
            margin-bottom: 20px;
            position: relative;
        }

        .visualization-area {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .section-title {
            color: #2c3e50;
            font-size: 1.3rem;
            margin-bottom: 15px;
            padding-bottom: 8px;
            border-bottom: 2px solid #ecf0f1;
            display: flex;
            align-items: center;
        }

        .section-title i {
            margin-right: 8px;
            font-size: 1.2rem;
        }

        .canvas-container {
            position: relative;
            width: 100%;
            height: 200px;
            background-color: #f8f9fa;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #e0e0e0;
        }

        #simulationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .viz-canvas-container {
            height: 180px;
            background-color: #f8f9fa;
            border-radius: 8px;
            overflow: hidden;
            border: 1px solid #e0e0e0;
            position: relative;
        }

        #momentumCanvas, #energyCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .viz-label {
            display: flex;
            justify-content: space-between;
            margin-top: 8px;
            font-size: 0.9rem;
        }

        .control-group {
            margin-bottom: 25px;
        }

        .control-title {
            font-weight: 600;
            margin-bottom: 12px;
            color: #2c3e50;
            display: flex;
            align-items: center;
        }

        .control-title i {
            margin-right: 8px;
            color: #3498db;
        }

        .slider-container {
            margin-bottom: 15px;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }

        .slider-label span:first-child {
            font-weight: 500;
        }

        .slider-label span:last-child {
            color: #3498db;
            font-weight: 600;
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

        .preset-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            margin-bottom: 20px;
        }

        .preset-btn {
            padding: 10px;
            background-color: #ecf0f1;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.2s;
            text-align: center;
        }

        .preset-btn:hover {
            background-color: #d5dbdb;
            transform: translateY(-2px);
        }

        .preset-btn.active {
            background-color: #3498db;
            color: white;
        }

        .control-buttons {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }

        .control-btn {
            flex: 1;
            padding: 12px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .control-btn i {
            font-size: 1.1rem;
        }

        #startBtn {
            background-color: #2ecc71;
            color: white;
        }

        #startBtn:hover {
            background-color: #27ae60;
        }

        #pauseBtn {
            background-color: #f39c12;
            color: white;
        }

        #pauseBtn:hover {
            background-color: #d68910;
        }

        #resetBtn {
            background-color: #e74c3c;
            color: white;
        }

        #resetBtn:hover {
            background-color: #c0392b;
        }

        #stepBtn {
            background-color: #9b59b6;
            color: white;
        }

        #stepBtn:hover {
            background-color: #8e44ad;
        }

        .toggle-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        .toggle-btn {
            padding: 8px 12px;
            background-color: #ecf0f1;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.2s;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .toggle-btn.active {
            background-color: #3498db;
            color: white;
        }

        .data-panel {
            background-color: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            border: 1px solid #e0e0e0;
            margin-top: 20px;
        }

        .data-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .data-card {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            border-left: 4px solid #3498db;
        }

        .data-card h3 {
            font-size: 1rem;
            margin-bottom: 10px;
            color: #2c3e50;
        }

        .data-row {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding-bottom: 5px;
            border-bottom: 1px dashed #e0e0e0;
        }

        .data-row:last-child {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }

        .data-label {
            font-weight: 500;
        }

        .data-value {
            font-weight: 600;
            color: #2c3e50;
        }

        .momentum-value {
            color: #16a085;
        }

        .energy-value {
            color: #f39c12;
        }

        .ball-a-color {
            color: #3498db;
            font-weight: 600;
        }

        .ball-b-color {
            color: #e74c3c;
            font-weight: 600;
        }

        .total-color {
            color: #2c3e50;
            font-weight: 600;
        }

        .collision-status {
            position: absolute;
            top: 20px;
            right: 20px;
            background-color: rgba(52, 152, 219, 0.1);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            color: #3498db;
            border: 1px solid rgba(52, 152, 219, 0.3);
        }

        .legend {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 10px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 5px;
            font-size: 0.9rem;
        }

        .legend-color {
            width: 15px;
            height: 15px;
            border-radius: 3px;
        }

        footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #ecf0f1;
            color: #7f8c8d;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            
            .control-buttons {
                flex-wrap: wrap;
            }
            
            .preset-buttons {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <h1><i class="fas fa-atom"></i> 动量守恒与能量守恒碰撞模拟</h1>
        <p class="subtitle">直观展示碰撞过程中动量与能量的动态变化关系</p>
    </header>

    <div class="container">
        <div class="main-content">
            <div class="simulation-area">
                <div class="section-title">
                    <i class="fas fa-basketball-ball"></i> 碰撞模拟
                </div>
                <div class="canvas-container">
                    <canvas id="simulationCanvas"></canvas>
                    <div class="collision-status" id="collisionStatus">准备中...</div>
                </div>
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #3498db;"></div>
                        <span>球A (质量: <span id="massAValue">2.0</span> kg)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #e74c3c;"></div>
                        <span>球B (质量: <span id="massBValue">1.0</span> kg)</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #16a085;"></div>
                        <span>总动量 (守恒)</span>
                    </div>
                </div>
            </div>

            <div class="visualization-area">
                <div class="viz-section">
                    <div class="section-title">
                        <i class="fas fa-arrows-alt-h"></i> 动量变化 (矢量)
                    </div>
                    <div class="viz-canvas-container">
                        <canvas id="momentumCanvas"></canvas>
                    </div>
                    <div class="viz-label">
                        <span>碰撞前</span>
                        <span>碰撞后</span>
                    </div>
                </div>

                <div class="viz-section">
                    <div class="section-title">
                        <i class="fas fa-chart-bar"></i> 能量变化 (标量)
                    </div>
                    <div class="viz-canvas-container">
                        <canvas id="energyCanvas"></canvas>
                    </div>
                    <div class="viz-label">
                        <span>碰撞前</span>
                        <span>碰撞后</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="control-panel">
            <div class="section-title">
                <i class="fas fa-sliders-h"></i> 控制面板
            </div>

            <div class="control-group">
                <div class="control-title">
                    <i class="fas fa-cogs"></i> 模拟控制
                </div>
                <div class="control-buttons">
                    <button class="control-btn" id="startBtn">
                        <i class="fas fa-play"></i> 开始
                    </button>
                    <button class="control-btn" id="pauseBtn">
                        <i class="fas fa-pause"></i> 暂停
                    </button>
                    <button class="control-btn" id="resetBtn">
                        <i class="fas fa-redo"></i> 重置
                    </button>
                    <button class="control-btn" id="stepBtn">
                        <i class="fas fa-step-forward"></i> 单步
                    </button>
                </div>
            </div>

            <div class="control-group">
                <div class="control-title">
                    <i class="fas fa-vial"></i> 预设场景
                </div>
                <div class="preset-buttons">
                    <button class="preset-btn" id="preset1">弹性碰撞 (等质量)</button>
                    <button class="preset-btn" id="preset2">弹性碰撞 (质量悬殊)</button>
                    <button class="preset-btn" id="preset3">完全非弹性碰撞</button>
                    <button class="preset-btn" id="preset4">一般非弹性碰撞</button>
                </div>
            </div>

            <div class="control-group">
                <div class="control-title">
                    <i class="fas fa-tachometer-alt"></i> 参数调节
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>球A质量 (kg)</span>
                        <span id="massAValueDisplay">2.0</span>
                    </div>
                    <input type="range" id="massASlider" min="0.5" max="5" step="0.1" value="2.0">
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>球B质量 (kg)</span>
                        <span id="massBValueDisplay">1.0</span>
                    </div>
                    <input type="range" id="massBSlider" min="0.5" max="5" step="0.1" value="1.0">
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>球A初速度 (m/s)</span>
                        <span id="velocityAValueDisplay">2.0</span>
                    </div>
                    <input type="range" id="velocityASlider" min="-5" max="5" step="0.1" value="2.0">
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>球B初速度 (m/s)</span>
                        <span id="velocityBValueDisplay">-1.0</span>
                    </div>
                    <input type="range" id="velocityBSlider" min="-5" max="5" step="0.1" value="-1.0">
                </div>
                <div class="slider-container">
                    <div class="slider-label">
                        <span>恢复系数 (e)</span>
                        <span id="coefficientValueDisplay">1.0</span>
                    </div>
                    <input type="range" id="coefficientSlider" min="0" max="1" step="0.1" value="1.0">
                    <div style="font-size: 0.85rem; color: #7f8c8d; margin-top: 5px;">
                        e=1: 完全弹性 | e=0: 完全非弹性
                    </div>
                </div>
            </div>

            <div class="control-group">
                <div class="control-title">
                    <i class="fas fa-eye"></i> 显示选项
                </div>
                <div class="toggle-group">
                    <button class="toggle-btn active" id="toggleMomentum">
                        <i class="fas fa-arrows-alt-h"></i> 动量箭头
                    </button>
                    <button class="toggle-btn active" id="toggleEnergy">
                        <i class="fas fa-chart-bar"></i> 能量柱图
                    </button>
                    <button class="toggle-btn active" id="toggleVectorSum">
                        <i class="fas fa-plus-circle"></i> 矢量合成
                    </button>
                </div>
            </div>
        </div>
    </div>

    <div class="data-panel">
        <div class="section-title">
            <i class="fas fa-calculator"></i> 实时数据
        </div>
        <div class="data-grid">
            <div class="data-card">
                <h3>碰撞前状态</h3>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A速度:</span>
                    <span class="data-value" id="preVA">2.00 m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A动量:</span>
                    <span class="data-value" id="prePA">4.00 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A动能:</span>
                    <span class="data-value" id="preEA">4.00 J</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B速度:</span>
                    <span class="data-value" id="preVB">-1.00 m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B动量:</span>
                    <span class="data-value" id="prePB">-1.00 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B动能:</span>
                    <span class="data-value" id="preEB">0.50 J</span>
                </div>
            </div>

            <div class="data-card">
                <h3>碰撞后状态</h3>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A速度:</span>
                    <span class="data-value" id="postVA">0.67 m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A动量:</span>
                    <span class="data-value" id="postPA">1.33 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-a-color">球A动能:</span>
                    <span class="data-value" id="postEA">0.44 J</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B速度:</span>
                    <span class="data-value" id="postVB">2.33 m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B动量:</span>
                    <span class="data-value" id="postPB">2.33 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label ball-b-color">球B动能:</span>
                    <span class="data-value" id="postEB">2.72 J</span>
                </div>
            </div>

            <div class="data-card">
                <h3>守恒定律验证</h3>
                <div class="data-row">
                    <span class="data-label total-color">总动量 (前):</span>
                    <span class="data-value momentum-value" id="preTotalP">3.00 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label total-color">总动量 (后):</span>
                    <span class="data-value momentum-value" id="postTotalP">3.00 kg·m/s</span>
                </div>
                <div class="data-row">
                    <span class="data-label total-color">动量守恒:</span>
                    <span class="data-value momentum-value" id="momentumConserved">是 ✓</span>
                </div>
                <div class="data-row">
                    <span class="data-label total-color">总动能 (前):</span>
                    <span class="data-value energy-value" id="preTotalE">4.50 J</span>
                </div>
                <div class="data-row">
                    <span class="data-label total-color">总动能 (后):</span>
                    <span class="data-value energy-value" id="postTotalE">3.17 J</span>
                </div>
                <div class="data-row">
                    <span class="data-label total-color">动能守恒:</span>
                    <span class="data-value energy-value" id="energyConserved">否 (e=1.0时守恒)</span>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <p>教学动画设计：动量守恒与能量守恒碰撞模拟 | 使用HTML5 Canvas实现 | 适用于高中及大学物理教学</p>
        <p>提示：调整参数观察动量(矢量)守恒与能量(标量)变化的关系，注意弹性碰撞(e=1)与非弹性碰撞(e&lt;1)的区别</p>
    </footer>

    <script>
        // 物理模拟参数
        let simulation = {
            running: false,
            time: 0,
            dt: 0.016, // 约60fps
            collisionOccurred: false,
            collisionTime: 0,
            showMomentum: true,
            showEnergy: true,
            showVectorSum: true
        };

        // 球体参数
        let ballA = {
            x: 150,
            y: 100,
            radius: 25,
            mass: 2.0,
            velocity: 2.0,
            color: "#3498db",
            name: "球A"
        };

        let ballB = {
            x: 450,
            y: 100,
            radius: 20,
            mass: 1.0,
            velocity: -1.0,
            color: "#e74c3c",
            name: "球B"
        };

        // 恢复系数 (e=1: 完全弹性, e=0: 完全非弹性)
        let restitution = 1.0;

        // 碰撞前后的状态（用于可视化）
        let preCollisionState = {
            vA: ballA.velocity,
            vB: ballB.velocity,
            pA: ballA.mass * ballA.velocity,
            pB: ballB.mass * ballB.velocity,
            eA: 0.5 * ballA.mass * ballA.velocity * ballA.velocity,
            eB: 0.5 * ballB.mass * ballB.velocity * ballB.velocity
        };

        let postCollisionState = {
            vA: 0,
            vB: 0,
            pA: 0,
            pB: 0,
            eA: 0,
            eB: 0
        };

        // 计算碰撞后的速度（一维碰撞公式）
        function calculatePostCollision() {
            const mA = ballA.mass;
            const mB = ballB.mass;
            const uA = ballA.velocity;
            const uB = ballB.velocity;
            const e = restitution;
            
            // 一维碰撞公式
            const vA = ((mA - e * mB) * uA + (1 + e) * mB * uB) / (mA + mB);
            const vB = ((mB - e * mA) * uB + (1 + e) * mA * uA) / (mA + mB);
            
            // 更新碰撞后状态
            postCollisionState.vA = vA;
            postCollisionState.vB = vB;
            postCollisionState.pA = mA * vA;
            postCollisionState.pB = mB * vB;
            postCollisionState.eA = 0.5 * mA * vA * vA;
            postCollisionState.eB = 0.5 * mB * vB * vB;
            
            // 更新数据面板
            updateDataPanel();
            
            return { vA, vB };
        }

        // 更新数据面板
        function updateDataPanel() {
            // 更新碰撞前数据
            document.getElementById('preVA').textContent = ballA.velocity.toFixed(2) + " m/s";
            document.getElementById('prePA').textContent = (ballA.mass * ballA.velocity).toFixed(2) + " kg·m/s";
            document.getElementById('preEA').textContent = (0.5 * ballA.mass * ballA.velocity * ballA.velocity).toFixed(2) + " J";
            
            document.getElementById('preVB').textContent = ballB.velocity.toFixed(2) + " m/s";
            document.getElementById('prePB').textContent = (ballB.mass * ballB.velocity).toFixed(2) + " kg·m/s";
            document.getElementById('preEB').textContent = (0.5 * ballB.mass * ballB.velocity * ballB.velocity).toFixed(2) + " J";
            
            // 更新碰撞后数据
            document.getElementById('postVA').textContent = postCollisionState.vA.toFixed(2) + " m/s";
            document.getElementById('postPA').textContent = postCollisionState.pA.toFixed(2) + " kg·m/s";
            document.getElementById('postEA').textContent = postCollisionState.eA.toFixed(2) + " J";
            
            document.getElementById('postVB').textContent = postCollisionState.vB.toFixed(2) + " m/s";
            document.getElementById('postPB').textContent = postCollisionState.pB.toFixed(2) + " kg·m/s";
            document.getElementById('postEB').textContent = postCollisionState.eB.toFixed(2) + " J";
            
            // 计算总量
            const preTotalP = (ballA.mass * ballA.velocity + ballB.mass * ballB.velocity).toFixed(2);
            const postTotalP = (postCollisionState.pA + postCollisionState.pB).toFixed(2);
            
            const preTotalE = (0.5 * ballA.mass * ballA.velocity * ballA.velocity + 
                              0.5 * ballB.mass * ballB.velocity * ballB.velocity).toFixed(2);
            const postTotalE = (postCollisionState.eA + postCollisionState.eB).toFixed(2);
            
            // 更新守恒验证
            document.getElementById('preTotalP').textContent = preTotalP + " kg·m/s";
            document.getElementById('postTotalP').textContent = postTotalP + " kg·m/s";
            
            const momentumConserved = Math.abs(parseFloat(preTotalP) - parseFloat(postTotalP)) < 0.01;
            document.getElementById('momentumConserved').textContent = momentumConserved ? "是 ✓" : "否 ✗";
            document.getElementById('momentumConserved').style.color = momentumConserved ? "#16a085" : "#e74c3c";
            
            document.getElementById('preTotalE').textContent = preTotalE + " J";
            document.getElementById('postTotalE').textContent = postTotalE + " J";
            
            const energyConserved = Math.abs(parseFloat(preTotalE) - parseFloat(postTotalE)) < 0.01;
            document.getElementById('energyConserved').textContent = 
                energyConserved ? "是 ✓ (e=1.0)" : `否 (e=${restitution.toFixed(1)})`;
            document.getElementById('energyConserved').style.color = energyConserved ? "#16a085" : "#f39c12";
            
            // 更新状态显示
            const statusElement = document.getElementById('collisionStatus');
            if (simulation.collisionOccurred) {
                statusElement.textContent = `碰撞完成 (e=${restitution.toFixed(1)})`;
                statusElement.style.backgroundColor = restitution === 1 ? 
                    'rgba(46, 204, 113, 0.1)' : 'rgba(243, 156, 18, 0.1)';
                statusElement.style.color = restitution === 1 ? '#2ecc71' : '#f39c12';
                statusElement.style.borderColor = restitution === 1 ? 
                    'rgba(46, 204, 113, 0.3)' : 'rgba(243, 156, 18, 0.3)';
            } else if (simulation.running) {
                statusElement.textContent = '模拟运行中...';
                statusElement.style.backgroundColor = 'rgba(52, 152, 219, 0.1)';
                statusElement.style.color = '#3498db';
                statusElement.style.borderColor = 'rgba(52, 152, 219, 0.3)';
            } else {
                statusElement.textContent = '准备中...';
                statusElement.style.backgroundColor = 'rgba(52, 152, 219, 0.1)';
                statusElement.style.color = '#3498db';
                statusElement.style.borderColor = 'rgba(52, 152, 219, 0.3)';
            }
        }

        // 获取Canvas上下文
        const simCanvas = document.getElementById('simulationCanvas');
        const momentumCanvas = document.getElementById('momentumCanvas');
        const energyCanvas = document.getElementById('energyCanvas');
        
        const simCtx = simCanvas.getContext('2d');
        const momentumCtx = momentumCanvas.getContext('2d');
        const energyCtx = energyCanvas.getContext('2d');

        // 设置Canvas尺寸
        function resizeCanvases() {
            const simContainer = document.querySelector('.canvas-container');
            const vizContainer = document.querySelector('.viz-canvas-container');
            
            simCanvas.width = simContainer.clientWidth;
            simCanvas.height = simContainer.clientHeight;
            
            momentumCanvas.width = vizContainer.clientWidth;
            momentumCanvas.height = vizContainer.clientHeight;
            
            energyCanvas.width = vizContainer.clientWidth;
            energyCanvas.height = vizContainer.clientHeight;
            
            // 更新球的位置（基于新尺寸）
            ballA.x = simCanvas.width * 0.25;
            ballB.x = simCanvas.width * 0.75;
            ballA.y = simCanvas.height / 2;
            ballB.y = simCanvas.height / 2;
            
            // 根据质量设置半径
            ballA.radius = 15 + ballA.mass * 5;
            ballB.radius = 15 + ballB.mass * 5;
        }

        // 绘制模拟场景
        function drawSimulation() {
            // 清除画布
            simCtx.clearRect(0, 0, simCanvas.width, simCanvas.height);
            
            // 绘制轨道
            simCtx.beginPath();
            simCtx.moveTo(50, ballA.y);
            simCtx.lineTo(simCanvas.width - 50, ballA.y);
            simCtx.strokeStyle = '#2c3e50';
            simCtx.lineWidth = 2;
            simCtx.stroke();
            
            // 绘制轨道端点
            simCtx.fillStyle = '#2c3e50';
            simCtx.beginPath();
            simCtx.arc(50, ballA.y, 5, 0, Math.PI * 2);
            simCtx.fill();
            
            simCtx.beginPath();
            simCtx.arc(simCanvas.width - 50, ballA.y, 5, 0, Math.PI * 2);
            simCtx.fill();
            
            // 绘制球A
            simCtx.beginPath();
            simCtx.arc(ballA.x, ballA.y, ballA.radius, 0, Math.PI * 2);
            simCtx.fillStyle = ballA.color;
            simCtx.fill();
            simCtx.strokeStyle = '#2c3e50';
            simCtx.lineWidth = 2;
            simCtx.stroke();
            
            // 绘制球A标签
            simCtx.fillStyle = 'white';
            simCtx.font = 'bold 14px Arial';
            simCtx.textAlign = 'center';
            simCtx.textBaseline = 'middle';
            simCtx.fillText('A', ballA.x, ballA.y);
            
            // 绘制球B
            simCtx.beginPath();
            simCtx.arc(ballB.x, ballB.y, ballB.radius, 0, Math.PI * 2);
            simCtx.fillStyle = ballB.color;
            simCtx.fill();
            simCtx.strokeStyle = '#2c3e50';
            simCtx.lineWidth = 2;
            simCtx.stroke();
            
            // 绘制球B标签
            simCtx.fillStyle = 'white';
            simCtx.font = 'bold 14px Arial';
            simCtx.textAlign = 'center';
            simCtx.textBaseline = 'middle';
            simCtx.fillText('B', ballB.x, ballB.y);
            
            // 绘制速度箭头
            if (simulation.showMomentum) {
                drawVelocityArrow(ballA, ballA.velocity, simCtx);
                drawVelocityArrow(ballB, ballB.velocity, simCtx);
            }
            
            // 绘制碰撞检测区域（调试用）
            // const distance = Math.abs(ballA.x - ballB.x);
            // const minDistance = ballA.radius + ballB.radius;
            // if (distance < minDistance + 10) {
            //     simCtx.strokeStyle = 'rgba(231, 76, 60, 0.5)';
            //     simCtx.lineWidth = 1;
            //     simCtx.setLineDash([5, 5]);
            //     simCtx.beginPath
<!--检测到代码截断，自动续写中...-->
            //     simCtx.arc(ballA.x, ballA.y, ballA.radius + ballB.radius, 0, Math.PI * 2);
            //     simCtx.stroke();
            //     simCtx.setLineDash([]);
            // }
        }

        // 绘制速度箭头
        function drawVelocityArrow(ball, velocity, ctx) {
            const arrowLength = Math.abs(velocity) * 15;
            const direction = velocity > 0 ? 1 : -1;
            
            ctx.save();
            ctx.translate(ball.x, ball.y);
            
            // 绘制箭头线
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(direction * arrowLength, 0);
            ctx.strokeStyle = ball.color;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(direction * arrowLength, 0);
            ctx.lineTo(direction * (arrowLength - 10), -6);
            ctx.lineTo(direction * (arrowLength - 10), 6);
            ctx.closePath();
            ctx.fillStyle = ball.color;
            ctx.fill();
            
            // 绘制速度标签
            ctx.fillStyle = ball.color;
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = direction > 0 ? 'left' : 'right';
            ctx.textBaseline = 'bottom';
            ctx.fillText(`${velocity.toFixed(1)} m/s`, direction * (arrowLength + 10), -5);
            
            ctx.restore();
        }

        // 绘制动量可视化
        function drawMomentumVisualization() {
            // 清除画布
            momentumCtx.clearRect(0, 0, momentumCanvas.width, momentumCanvas.height);
            
            const centerY = momentumCanvas.height / 2;
            const preX = momentumCanvas.width * 0.25;
            const postX = momentumCanvas.width * 0.75;
            const scale = 15; // 动量缩放因子
            
            // 绘制标题
            momentumCtx.fillStyle = '#2c3e50';
            momentumCtx.font = 'bold 14px Arial';
            momentumCtx.textAlign = 'center';
            momentumCtx.fillText('动量 (矢量)', momentumCanvas.width / 2, 20);
            
            // 绘制碰撞前动量
            drawMomentumArrow(preX, centerY, preCollisionState.pA, ballA.color, '前', momentumCtx, scale);
            drawMomentumArrow(preX, centerY, preCollisionState.pB, ballB.color, '前', momentumCtx, scale);
            
            // 绘制碰撞后动量
            drawMomentumArrow(postX, centerY, postCollisionState.pA, ballA.color, '后', momentumCtx, scale);
            drawMomentumArrow(postX, centerY, postCollisionState.pB, ballB.color, '后', momentumCtx, scale);
            
            // 绘制矢量合成（如果启用）
            if (simulation.showVectorSum) {
                // 碰撞前总动量
                const preTotalP = preCollisionState.pA + preCollisionState.pB;
                drawVectorSum(preX, centerY + 70, preCollisionState.pA, preCollisionState.pB, 
                             ballA.color, ballB.color, preTotalP, momentumCtx, scale, '碰撞前总动量');
                
                // 碰撞后总动量
                const postTotalP = postCollisionState.pA + postCollisionState.pB;
                drawVectorSum(postX, centerY + 70, postCollisionState.pA, postCollisionState.pB, 
                             ballA.color, ballB.color, postTotalP, momentumCtx, scale, '碰撞后总动量');
            }
        }

        // 绘制动量箭头
        function drawMomentumArrow(x, y, momentum, color, label, ctx, scale) {
            const arrowLength = momentum * scale;
            
            ctx.save();
            ctx.translate(x, y);
            
            // 绘制基线
            ctx.beginPath();
            ctx.moveTo(-80, 0);
            ctx.lineTo(80, 0);
            ctx.strokeStyle = '#ddd';
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制零点
            ctx.beginPath();
            ctx.arc(0, 0, 3, 0, Math.PI * 2);
            ctx.fillStyle = '#7f8c8d';
            ctx.fill();
            
            // 绘制箭头
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(arrowLength, 0);
            ctx.strokeStyle = color;
            ctx.lineWidth = 4;
            ctx.stroke();
            
            // 绘制箭头头部
            if (Math.abs(arrowLength) > 5) {
                const direction = arrowLength > 0 ? 1 : -1;
                ctx.beginPath();
                ctx.moveTo(arrowLength, 0);
                ctx.lineTo(arrowLength - direction * 8, -6);
                ctx.lineTo(arrowLength - direction * 8, 6);
                ctx.closePath();
                ctx.fillStyle = color;
                ctx.fill();
            }
            
            // 绘制标签
            ctx.fillStyle = color;
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = arrowLength >= 0 ? 'left' : 'right';
            ctx.textBaseline = 'top';
            const offset = arrowLength >= 0 ? 5 : -5;
            ctx.fillText(`${momentum.toFixed(2)}`, arrowLength + offset, 5);
            
            // 绘制"碰撞前/后"标签
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(label === '前' ? '碰撞前' : '碰撞后', 0, -10);
            
            ctx.restore();
        }

        // 绘制矢量合成
        function drawVectorSum(x, y, pA, pB, colorA, colorB, totalP, ctx, scale, label) {
            ctx.save();
            ctx.translate(x, y);
            
            // 绘制说明文字
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '11px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(label, 0, -25);
            
            // 绘制矢量A
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(pA * scale, 0);
            ctx.strokeStyle = colorA;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制矢量B（从A的终点开始）
            ctx.beginPath();
            ctx.moveTo(pA * scale, 0);
            ctx.lineTo(pA * scale + pB * scale, 0);
            ctx.strokeStyle = colorB;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 绘制合矢量（从起点到终点）
            ctx.beginPath();
            ctx.moveTo(0, 0);
            ctx.lineTo(totalP * scale, 0);
            ctx.strokeStyle = '#16a085';
            ctx.lineWidth = 4;
            ctx.setLineDash([5, 3]);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制合矢量箭头
            if (Math.abs(totalP * scale) > 5) {
                const direction = totalP > 0 ? 1 : -1;
                ctx.beginPath();
                ctx.moveTo(totalP * scale, 0);
                ctx.lineTo(totalP * scale - direction * 8, -6);
                ctx.lineTo(totalP * scale - direction * 8, 6);
                ctx.closePath();
                ctx.fillStyle = '#16a085';
                ctx.fill();
            }
            
            // 绘制合矢量标签
            ctx.fillStyle = '#16a085';
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = totalP >= 0 ? 'left' : 'right';
            ctx.textBaseline = 'top';
            const offset = totalP >= 0 ? 5 : -5;
            ctx.fillText(`${totalP.toFixed(2)}`, totalP * scale + offset, 5);
            
            // 绘制起点和终点标记
            ctx.fillStyle = '#7f8c8d';
            ctx.beginPath();
            ctx.arc(0, 0, 3, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.beginPath();
            ctx.arc(totalP * scale, 0, 3, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.restore();
        }

        // 绘制能量可视化
        function drawEnergyVisualization() {
            // 清除画布
            energyCtx.clearRect(0, 0, energyCanvas.width, energyCanvas.height);
            
            const centerY = energyCanvas.height / 2;
            const preX = energyCanvas.width * 0.25;
            const postX = energyCanvas.width * 0.75;
            const maxEnergy = Math.max(
                preCollisionState.eA + preCollisionState.eB,
                postCollisionState.eA + postCollisionState.eB,
                1 // 最小值，避免除零
            );
            const scale = (energyCanvas.height * 0.6) / maxEnergy;
            
            // 绘制标题
            energyCtx.fillStyle = '#2c3e50';
            energyCtx.font = 'bold 14px Arial';
            energyCtx.textAlign = 'center';
            energyCtx.fillText('动能 (标量)', energyCanvas.width / 2, 20);
            
            // 绘制碰撞前能量
            drawEnergyBars(preX, centerY, preCollisionState.eA, preCollisionState.eB, 
                          ballA.color, ballB.color, scale, energyCtx, '碰撞前');
            
            // 绘制碰撞后能量
            drawEnergyBars(postX, centerY, postCollisionState.eA, postCollisionState.eB, 
                          ballA.color, ballB.color, scale, energyCtx, '碰撞后');
            
            // 绘制能量损失（如果是非弹性碰撞）
            if (restitution < 1) {
                const preTotalE = preCollisionState.eA + preCollisionState.eB;
                const postTotalE = postCollisionState.eA + postCollisionState.eB;
                const energyLoss = preTotalE - postTotalE;
                
                if (energyLoss > 0.01) {
                    drawEnergyLoss(postX, centerY, postTotalE, energyLoss, scale, energyCtx);
                }
            }
        }

        // 绘制能量柱状图
        function drawEnergyBars(x, y, eA, eB, colorA, colorB, scale, ctx, label) {
            const barWidth = 30;
            const gap = 15;
            
            ctx.save();
            ctx.translate(x, y);
            
            // 绘制基线
            ctx.beginPath();
            ctx.moveTo(-barWidth - gap, 0);
            ctx.lineTo(barWidth + gap, 0);
            ctx.strokeStyle = '#ddd';
            ctx.lineWidth = 1;
            ctx.stroke();
            
            // 绘制球A能量柱
            const barHeightA = eA * scale;
            ctx.fillStyle = colorA;
            ctx.fillRect(-barWidth - gap/2, -barHeightA, barWidth, barHeightA);
            
            // 绘制球A能量值
            ctx.fillStyle = colorA;
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(eA.toFixed(2), -barWidth - gap/2 + barWidth/2, -barHeightA - 5);
            
            // 绘制球B能量柱
            const barHeightB = eB * scale;
            ctx.fillStyle = colorB;
            ctx.fillRect(gap/2, -barHeightB, barWidth, barHeightB);
            
            // 绘制球B能量值
            ctx.fillStyle = colorB;
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(eB.toFixed(2), gap/2 + barWidth/2, -barHeightB - 5);
            
            // 绘制总能量线
            const totalHeight = (eA + eB) * scale;
            ctx.beginPath();
            ctx.moveTo(-barWidth - gap/2, -totalHeight);
            ctx.lineTo(gap/2 + barWidth, -totalHeight);
            ctx.strokeStyle = '#f39c12';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制总能量标签
            ctx.fillStyle = '#f39c12';
            ctx.font = 'bold 12px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(`总: ${(eA + eB).toFixed(2)}`, 0, -totalHeight - 8);
            
            // 绘制"碰撞前/后"标签
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'top';
            ctx.fillText(label, 0, 10);
            
            ctx.restore();
        }

        // 绘制能量损失
        function drawEnergyLoss(x, y, postTotalE, energyLoss, scale, ctx) {
            ctx.save();
            ctx.translate(x, y);
            
            const barWidth = 30;
            const gap = 15;
            const postHeight = postTotalE * scale;
            const lossHeight = energyLoss * scale;
            
            // 绘制损失的能量柱（灰色）
            ctx.fillStyle = '#95a5a6';
            ctx.fillRect(gap/2 + barWidth + 20, -postHeight - lossHeight, barWidth, lossHeight);
            
            // 绘制损失标签
            ctx.fillStyle = '#95a5a6';
            ctx.font = 'bold 11px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'bottom';
            ctx.fillText(`损失: ${energyLoss.toFixed(2)}`, gap/2 + barWidth + 20 + barWidth/2, -postHeight - lossHeight - 5);
            
            // 绘制箭头表示能量转化
            ctx.beginPath();
            ctx.moveTo(gap/2 + barWidth + 5, -postHeight - lossHeight/2);
            ctx.lineTo(gap/2 + barWidth + 19, -postHeight - lossHeight/2);
            ctx.strokeStyle = '#95a5a6';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制箭头头部
            ctx.beginPath();
            ctx.moveTo(gap/2 + barWidth + 19, -postHeight - lossHeight/2);
            ctx.lineTo(gap/2 + barWidth + 14, -postHeight - lossHeight/2 - 4);
            ctx.lineTo(gap/2 + barWidth + 14, -postHeight - lossHeight/2 + 4);
            ctx.closePath();
            ctx.fillStyle = '#95a5a6';
            ctx.fill();
            
            // 绘制"内能"标签
            ctx.fillStyle = '#7f8c8d';
            ctx.font = '10px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'top';
            ctx.fillText('转化为内能', gap/2 + barWidth + 20 + barWidth/2, 10);
            
            ctx.restore();
        }

        // 更新模拟
        function updateSimulation() {
            if (!simulation.running) return;
            
            // 更新时间
            simulation.time += simulation.dt;
            
            // 更新球的位置
            ballA.x += ballA.velocity * simulation.dt * 50; // 乘以50让运动更明显
            ballB.x += ballB.velocity * simulation.dt * 50;
            
            // 边界检测
            const minX = 50 + ballA.radius;
            const maxX = simCanvas.width - 50 - ballB.radius;
            
            if (ballA.x < minX) {
                ballA.x = minX;
                ballA.velocity = Math.abs(ballA.velocity); // 反弹
            }
            
            if (ballB.x > maxX) {
                ballB.x = maxX;
                ballB.velocity = -Math.abs(ballB.velocity); // 反弹
            }
            
            // 碰撞检测
            const distance = Math.abs(ballA.x - ballB.x);
            const minDistance = ballA.radius + ballB.radius;
            
            if (distance < minDistance && !simulation.collisionOccurred) {
                simulation.collisionOccurred = true;
                simulation.collisionTime = simulation.time;
                
                // 计算碰撞后的速度
                const { vA, vB } = calculatePostCollision();
                
                // 应用碰撞后的速度
                ballA.velocity = vA;
                ballB.velocity = vB;
                
                // 防止球重叠
                if (ballA.x < ballB.x) {
                    ballA.x = ballB.x - minDistance;
                } else {
                    ballB.x = ballA.x - minDistance;
                }
            }
            
            // 绘制所有内容
            drawSimulation();
            drawMomentumVisualization();
            drawEnergyVisualization();
            
            // 继续动画循环
            requestAnimationFrame(updateSimulation);
        }

        // 重置模拟
        function resetSimulation() {
            simulation.running = false;
            simulation.time = 0;
            simulation.collisionOccurred = false;
            
            // 重置球的位置
            ballA.x = simCanvas.width * 0.25;
            ballB.x = simCanvas.width * 0.75;
            ballA.y = simCanvas.height / 2;
            ballB.y = simCanvas.height / 2;
            
            // 更新碰撞前状态
            preCollisionState.vA = ballA.velocity;
            preCollisionState.vB = ballB.velocity;
            preCollisionState.pA = ballA.mass * ballA.velocity;
            preCollisionState.pB = ballB.mass * ballB.velocity;
            preCollisionState.eA = 0.5 * ballA.mass * ballA.velocity * ballA.velocity;
            preCollisionState.eB = 0.5 * ballB.mass * ballB.velocity * ballB.velocity;
            
            // 重新计算碰撞后状态
            calculatePostCollision();
            
            // 重新绘制
            drawSimulation();
            drawMomentumVisualization();
            drawEnergyVisualization();
            updateDataPanel();
        }

        // 单步前进
        function stepSimulation() {
            if (simulation.running) return;
            
            simulation.time += simulation.dt;
            
            // 更新球的位置
            ballA.x += ballA.velocity * simulation.dt * 50;
            ballB.x += ballB.velocity * simulation.dt * 50;
            
            // 边界检测
            const minX = 50 + ballA.radius;
            const maxX = simCanvas.width - 50 - ballB.radius;
            
            if (ballA.x < minX) {
                ballA.x = minX;
                ballA.velocity = Math.abs(ballA.velocity);
            }
            
            if (ballB.x > maxX) {
                ballB.x = maxX;
                ballB.velocity = -Math.abs(ballB.velocity);
            }
            
            // 碰撞检测
            const distance = Math.abs(ballA.x - ballB.x);
            const minDistance = ballA.radius + ballB.radius;
            
            if (distance < minDistance && !simulation.collisionOccurred) {
                simulation.collisionOccurred = true;
                
                // 计算碰撞后的速度
                const { vA, vB } = calculatePostCollision();
                
                // 应用碰撞后的速度
                ballA.velocity = vA;
                ballB.velocity = vB;
                
                // 防止球重叠
                if (ballA.x < ballB.x) {
                    ballA.x = ballB.x - minDistance;
                } else {
                    ballB.x = ballA.x - minDistance;
                }
            }
            
            // 绘制所有内容
            drawSimulation();
            drawMomentumVisualization();
            drawEnergyVisualization();
            updateDataPanel();
        }

        // 初始化事件监听器
        function initEventListeners() {
            // 控制按钮
            document.getElementById('startBtn').addEventListener('click', () => {
                simulation.running = true;
                updateSimulation();
            });
            
            document.getElementById('pauseBtn').addEventListener('click', () => {
                simulation.running = false;
            });
            
            document.getElementById('resetBtn').addEventListener('click', resetSimulation);
            
            document.getElementById('stepBtn').addEventListener('click', stepSimulation);
            
            // 预设场景
            document.getElementById('preset1').addEventListener('click', () => {
                // 弹性碰撞 (等质量)
                ballA.mass = 2.0;
                ballB.mass = 2.0;
                ballA.velocity = 3.0;
                ballB.velocity = -1.0;
                restitution = 1.0;
                updateSlidersFromState();
                resetSimulation();
                setActivePreset('preset1');
            });
            
            document.getElementById('preset2').addEventListener('click', () => {
                // 弹性碰撞 (质量悬殊)
                ballA.mass = 5.0;
                ballB.mass = 1.0;
                ballA.velocity = 2.0;
                ballB.velocity = 0.0;
                restitution = 1.0;
                updateSlidersFromState();
                resetSimulation();
                setActivePreset('preset2');
            });
            
            document.getElementById('preset3').addEventListener('click', () => {
                // 完全非弹性碰撞
                ballA.mass = 2.0;
                ballB.mass = 1.0;
                ballA.velocity = 3.0;
                ballB.velocity = -1.0;
                restitution = 0.0;
                updateSlidersFromState();
                resetSimulation();
                setActivePreset('preset3');
            });
            
            document.getElementById('preset4').addEventListener('click', () => {
                // 一般非弹性碰撞
                ballA.mass = 2.0;
                ballB.mass = 1.5;
                ballA.velocity = 2.5;
                ballB.velocity = -1.5;
                restitution = 0.5;
                updateSlidersFromState();
                resetSimulation();
                setActivePreset('preset4');
            });
            
            // 滑块控制
            document.getElementById('massASlider').addEventListener('input', (e) => {
                ballA.mass = parseFloat(e.target.value);
                document.getElementById('massAValueDisplay').textContent = ballA.mass.toFixed(1);
                document.getElementById('massAValue').textContent = ballA.mass.toFixed(1);
                calculatePostCollision();
                resetSimulation();
                clearActivePreset();
            });
            
            document.getElementById('massBSlider').addEventListener('input', (e) => {
                ballB.mass = parseFloat(e.target.value);
                document.getElementById('massBValueDisplay').textContent = ballB.mass.toFixed(1);
                document.getElementById('massBValue').textContent = ballB.mass.toFixed(1);
                calculatePostCollision();
                resetSimulation();
                clearActivePreset();
            });
            
            document.getElementById('velocityASlider').addEventListener('input', (e) => {
                ballA.velocity = parseFloat(e.target.value);
                document.getElementById('velocityAValueDisplay').textContent = ballA.velocity.toFixed(1);
                calculatePostCollision();
                resetSimulation();
                clearActivePreset();
            });
            
            document.getElementById('velocityBSlider').addEventListener('input', (e) => {
                ballB.velocity = parseFloat(e.target.value);
                document.getElementById('velocityBValueDisplay').textContent = ballB.velocity.toFixed(1);
                calculatePostCollision();
                resetSimulation();
                clearActivePreset();
            });
            
            document.getElementById('coefficientSlider').addEventListener('input', (e) => {
                restitution = parseFloat(e.target.value);
                document.getElementById('coefficientValueDisplay').textContent = restitution.toFixed(1);
                calculatePostCollision();
                resetSimulation();
                clearActivePreset();
            });
            
            // 显示选项切换
            document.getElementById('toggleMomentum').addEventListener('click', function() {
                simulation.showMomentum = !simulation.showMomentum;
                this.classList.toggle('active');
                drawSimulation();
            });
            
            document.getElementById('toggleEnergy').addEventListener('click', function() {
                simulation.showEnergy = !simulation.showEnergy;
                this.classList.toggle('active');
                drawEnergyVisualization();
            });
            
            document.getElementById('toggleVectorSum').addEventListener('click', function() {
                simulation.showVectorSum = !simulation.showVectorSum;
                this.classList.toggle('active');
                drawMomentumVisualization();
            });
            
            // 窗口大小调整
            window.addEventListener('resize', () => {
                resizeCanvases();
                resetSimulation();
            });
        }

        // 更新滑块状态
        function updateSlidersFromState() {
            document.getElementById('massASlider').value = ballA.mass;
            document.getElementById('massBSlider').value = ballB.mass;
            document.getElementById('velocityASlider').value = ballA.velocity;
            document.getElementById('velocityBSlider').value = ballB.velocity;
            document.getElementById('coefficientSlider').value = restitution;
            
            document.getElementById('massAValueDisplay').textContent = ballA.mass.toFixed(1);
            document.getElementById('massBValueDisplay').textContent = ballB.mass.toFixed(1);
            document.getElementById('velocityAValueDisplay').textContent = ballA.velocity.toFixed(1);
            document.getElementById('velocityBValueDisplay').textContent = ballB.velocity.toFixed(1);
            document.getElementById('coefficientValueDisplay').textContent = restitution.toFixed(1);
            
            document.getElementById('massAValue').textContent = ballA.mass.toFixed(1);
            document.getElementById('massBValue').textContent = ballB.mass.toFixed(1);
        }

        // 设置活动预设
        function setActivePreset(presetId) {
            const presetButtons = document.querySelectorAll('.preset-btn');
            presetButtons.forEach(btn => {
                btn.classList.remove('active');
            });
            document.getElementById(presetId).classList.add('active');
        }

        // 清除活动预设
        function clearActivePreset() {
            const presetButtons = document.querySelectorAll('.preset-btn');
            presetButtons.forEach(btn => {
                btn.classList.remove('active');
            });
        }

        // 初始化
        function init() {
            resizeCanvases();
            calculatePostCollision();
            initEventListeners();
            resetSimulation();
            setActivePreset('preset1'); // 默认选择第一个预设
        }

        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>


### 3. 过程输出

### 3. 使用指南

## 《动量守恒与能量守恒碰撞模拟》交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观、动态的可视化方式，帮助您深入理解碰撞过程中的动量守恒与能量守恒定律。无论您是学生、教师还是物理爱好者，都能通过亲手操作和观察，获得对这两个核心物理概念的深刻洞察。

---

### 一、 功能说明

本动画模拟了两个球体在一维光滑轨道上的碰撞过程，并**同步、实时**地展示了动量与能量的变化。它不仅仅是一个简单的动画，更是一个集成了物理引擎、数据可视化与交互控制的**教学实验沙盒**。

**核心目标**：让抽象的物理定律（动量守恒、能量守恒）变得**可见、可操作、可验证**。

---

### 二、 主要功能模块

1.  **碰撞模拟区（主舞台）**
    *   **直观动画**：观看蓝色球A与红色球B在轨道上的运动与碰撞。
    *   **实时矢量箭头**：附着在球体上的箭头直观显示其速度（动量）的大小与方向。
    *   **状态指示器**：实时显示当前模拟状态（运行中、碰撞完成、恢复系数e值）。

2.  **双重可视化面板**
    *   **动量变化（矢量）面板**：
        *   用箭头长度精确表示动量大小，方向表示动量方向。
        *   **关键特色**：展示碰撞前后动量矢量的**合成过程**，并用青色虚线箭头清晰标出**总动量矢量**，直观验证动量守恒（总矢量不变）。
    *   **能量变化（标量）面板**：
        *   用柱状图高度表示每个球的动能大小。
        *   **关键特色**：在非弹性碰撞时，会用灰色柱体显示**损失的能量**（转化为内能的部分），并标注“转化为内能”，清晰解释动能不守恒的原因。

3.  **控制面板**
    *   **模拟控制**：开始、暂停、重置、单步前进按钮，让您能精细控制模拟进程。
    *   **预设场景**：一键切换四种典型碰撞，快速观察不同条件下的物理现象。
    *   **参数调节**：通过滑块自由调节两球的质量、初速度以及**恢复系数 `e`**。
    *   **显示选项**：可单独开关“动量箭头”、“能量柱图”和“矢量合成”的显示，便于聚焦分析。

4.  **实时数据面板**
    *   以表格形式精确列出碰撞前后每个球的速度、动量、动能。
    *   **守恒定律验证区**：自动计算并对比系统总动量与总动能，明确给出“是/否”守恒的判断，并关联恢复系数 `e` 的值。

---

### 三、 设计特色与教学价值

1.  **对比式可视化**：
    *   **动量 vs. 能量**：左边面板用**箭头**（矢量）展示动量，右边面板用**柱图**（标量）展示能量，从视觉形式上就强调了二者的根本区别。
    *   **守恒 vs. 不守恒**：总动量箭头（青色）在碰撞前后保持**不变**；总动能柱顶线（橙色）在 `e<1` 时**降低**，其差值被明确标识为“损失”。这种并置对比极具冲击力。

2.  **核心参数 `e`（恢复系数）的突出作用**：
    *   将抽象的“弹性/非弹性”概念量化为一个从0到1可调的参数。
    *   调节 `e` 时，您可以立刻观察到能量损失柱的出现/消失，以及数据面板中“动能守恒”结论的变化。这直接揭示了 `e=1` 是动能守恒的充要条件。

3.  **“矢量合成”动画**：
    *   这是理解动量守恒（矢量守恒）的**关键**。动画将两个球的动量箭头首尾相接进行合成，清晰展示了无论碰撞如何激烈，那个从起点指向终点的**合矢量（总动量）始终不变**。

4.  **探究式学习环境**：
    *   从“预设场景”的观察到“自由调节”的探究，符合认知规律。
    *   **鼓励“假设-实验-观察”**：例如，“如果把大球的质量调得非常大，小球会怎样？”——立即调整参数，观察动画和数据验证你的猜想。

---

### 四、 教学要点与建议流程

**给学习者的建议：**

1.  **初次接触**：点击四个**预设场景**按钮，先“看”不同碰撞的现象，注意观察球的速度变化、动量箭头和能量柱的变化。
2.  **理解守恒**：
    *   运行“弹性碰撞（等质量）”预设。聚焦**动量面板**，观察青色总动量箭头在碰撞前后是否变化。
    *   运行“完全非弹性碰撞”预设。聚焦**能量面板**，观察灰色“损失能量”柱的出现，并查看数据面板中动能是否守恒。
3.  **深入探究**：
    *   使用滑块，将恢复系数 `e` 从1慢慢调到0。观察能量损失如何从无到有，逐渐增加，**建立 `e` 与能量损失的直接关联**。
    *   尝试制造一个“质量悬殊”的碰撞（如 `mA=5, mB=1`），预测并验证小球的速度变化。
    *   尝试让两个球同向运动 (`vB` 为正值但小于 `vA`)，观察追尾碰撞的结果。
4.  **挑战思考**：
    *   在完全非弹性碰撞 (`e=0`) 中，碰撞后两球粘连共速。此时，系统的总动量是否守恒？总动能是否守恒？为什么？
    *   能否通过调节参数，让碰撞后大球静止，小球以很快的速度弹出？（提示：参考牛顿摆现象）

**给教师的建议：**

1.  **课堂演示**：可用于引入概念、对比不同碰撞类型、验证守恒定律。利用“单步”功能分解碰撞瞬间。
2.  **设置探究任务**：向学生提出具体问题（如上述“挑战思考”），让他们利用动画自主寻找答案，并报告观察到的数据和现象。
3.  **联系公式**：在学生观察后，引导他们将可视化结果（箭头长度、柱图高度）与动量公式 `p=mv`、动能公式 `Ek=1/2 mv²` 以及碰撞速度公式联系起来。
4.  **误区澄清**：特别利用本工具强调“动量是矢量，守恒与方向有关”；“能量是标量，是否守恒取决于碰撞是否弹性（e值）”。

---

### 五、 使用建议

*   **循序渐进**：建议按照“观察预设 → 验证守恒 → 自由探索”的顺序使用。
*   **善用重置**：每次更改参数后，点击**重置**按钮，让小球回到起始位置，以便清晰观察完整过程。
*   **关注联动**：注意调节一个参数（如质量）时，不仅动画会变，下方的所有数据和图表都会**即时更新**，请养成综合观察的习惯。
*   **结合思考**：在操作间隙，不妨暂停一下，先预测结果，再运行模拟验证。这是将被动观看转化为主动学习的关键。

希望这个交互式动画能成为您探索物理世界的有力工具，让动量与能量守恒定律从课本上的公式，变为您脑海中生动而深刻的图景！祝您探索愉快！