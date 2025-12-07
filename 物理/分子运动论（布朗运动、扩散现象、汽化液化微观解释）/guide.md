# 需求：分子运动论（布朗运动、扩散现象、汽化液化微观解释）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向初中或高中物理初学者，旨在将抽象的“分子运动论”核心概念可视化、动态化，帮助学生建立微观世界的物理图景。用户的核心需求是：
1.  **理解抽象概念**：将肉眼不可见的分子运动、布朗运动、扩散等现象，通过动画直观呈现，降低理解门槛。
2.  **建立微观模型**：清晰地展示分子间存在间隙、分子永不停息地做无规则运动、分子间存在相互作用力这三个基本观点。
3.  **连接宏观与微观**：能够将宏观现象（如墨水扩散、液体蒸发、气体液化）与微观的分子运动机制联系起来，完成从现象到本质的认知飞跃。
4.  **主动探索与验证**：提供交互控制，让学生能够通过改变参数（如温度、分子种类）来观察结果变化，从而加深对规律（如温度越高，分子运动越剧烈）的理解。

#### 教学设计思路
*   **核心概念**：围绕分子运动论的三个基本观点展开，并具体化为三个可视化场景：
    1.  **分子运动基本模型**：展示分子（小球）在固定空间内永不停息、无规则地运动，相互碰撞并与容器壁碰撞。
    2.  **布朗运动与扩散现象**：用较大的颗粒（布朗颗粒）在分子撞击下的无规则运动，模拟布朗运动；用两种不同颜色的分子群体相互混合的过程，模拟扩散。
    3.  **物态变化的微观解释**：重点展示“汽化”与“液化”。汽化时，部分动能大的分子克服分子间引力逸出液面；液化时，气体分子相互靠近，动能减小，在引力作用下聚集为液体。
*   **认知规律**：遵循“具体 → 抽象 → 应用”的路径。先呈现最基础的分子运动动画，建立基本模型；然后引入布朗运动和扩散这两个可观测的宏观现象，用已建立的模型进行解释；最后将模型应用于解释更复杂的相变过程（汽化/液化），完成知识迁移。
*   **交互设计**：
    *   **场景切换**：通过标签页或导航按钮，在“分子模型”、“布朗与扩散”、“汽化与液化”三个核心场景间清晰切换。
    *   **控制面板**：每个场景配备独立的控制面板，允许用户实时调整关键参数（如：温度滑块、分子数量、暂停/播放、重置）。
    *   **提示与标注**：鼠标悬停在关键元素（如分子、布朗颗粒、液面）上时，显示简要说明。在动画关键步骤（如分子逸出液面）时，辅以动态文字标注或高亮提示。
    *   **对比观察**：在“扩散”和“汽化液化”场景中，提供并排对比视图（如高温 vs 低温下的扩散速度，加热 vs 冷却下的相变），强化变量影响。
*   **视觉呈现**：
    *   **分子**：用简洁的、有轻微光晕效果的小球表示。不同物质（如空气分子、水分子、墨水分子）用颜色区分。
    *   **运动轨迹**：为布朗颗粒提供短暂的轨迹拖尾，以清晰展示其无规则路径。普通分子运动不显示轨迹，避免画面混乱。
    *   **容器与界面**：容器用简洁的线条表示，突出内部的动态内容。控制面板设计为半透明浮动样式，确保不遮挡主动画区。
    *   **动态箭头**：用动态变化的箭头长度表示分子动能大小或作用力大小，使“能量”和“力”可视化。

#### 配色方案选择
*   **主色调**：采用深蓝色（`#1a237e`）或深空蓝作为背景和标题色，营造科学、深邃、聚焦的微观世界氛围。
*   **分子颜色**：
    *   通用分子/空气分子：浅蓝色（`#81d4fa`）或白色，代表中性、基础。
    *   另一种物质分子（如墨水）：亮橙色（`#ff9800`）或绿色（`#4caf50`），与主色形成对比，便于在扩散实验中观察混合。
    *   布朗颗粒：使用深色（如`#37474f`）或红色（`#f44336`），使其在分子群中清晰可辨。
*   **高亮与提示色**：使用明黄色（`#ffeb3b`）或亮青色（`#00e5ff`）进行高亮、标注和显示重要箭头（如逸出分子的高动能）。
*   **控制面板UI**：浅灰色（`#f5f5f5`）背景，深灰色（`#424242`）文字和控件，确保清晰可读且不刺眼。
*   **整体原则**：保证高对比度以便观察，颜色种类不过多，保持界面干净、专业。

#### 交互功能列表
1.  **全局控制**：
    *   播放/暂停按钮：控制所有动画的进行与停止。
    *   重置按钮：将当前场景恢复到初始状态。
2.  **场景一：分子运动基本模型**
    *   温度调节滑块：实时改变所有分子的平均运动速率（动能）。
    *   分子密度调节滑块：增加或减少容器内分子的数量，直观感受“间隙”和“压强”变化。
    *   显示/隐藏分子间作用力箭头（示意性）：开关选项，展示当分子非常接近时出现的斥力或引力箭头。
3.  **场景二：布朗运动与扩散**
    *   **布朗运动子场景**：
        *   可拖放多个布朗颗粒到容器中任意位置。
        *   温度调节滑块：观察温度对布朗运动剧烈程度的影响。
        *   布朗颗粒大小选择器：对比不同大小颗粒的运动差异。
        *   轨迹显示开关：开启/关闭布朗颗粒的运动轨迹。
    *   **扩散现象子场景**：
        *   两种分子颜色选择器。
        *   温度调节滑块：对比高温与低温下的扩散速度。
        *   隔板移除按钮：点击后移除两种气体间的隔板，开始扩散过程。
4.  **场景三：汽化与液化**
    *   **汽化（蒸发）子场景**：
        *   加热/冷却按钮或滑块：向系统增加或减少能量。
        *   液面标识与动态分子：展示液面处，动能大的分子挣脱束缚逸出。
        *   逸出分子计数器：统计单位时间内逸出的分子数，关联蒸发速率。
    *   **液化子场景**：
        *   冷却滑块：降低系统温度。
        *   显示分子间引力范围（示意性光圈）：冷却时，光圈出现，分子进入范围后速度减慢并聚集。
        *   液滴形成可视化：气体分子逐渐聚集形成小液滴并下落。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>分子运动论教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1b2a 0%, #1a237e 100%);
            color: #e0e0e0;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(30, 30, 46, 0.8);
            border-radius: 16px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        header {
            background: linear-gradient(to right, #1a237e, #283593);
            padding: 24px 32px;
            text-align: center;
            border-bottom: 2px solid #00e5ff;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 8px;
            color: #ffffff;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .subtitle {
            font-size: 1.1rem;
            opacity: 0.9;
            color: #81d4fa;
        }
        
        .scene-tabs {
            display: flex;
            background-color: rgba(25, 25, 35, 0.9);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .tab {
            flex: 1;
            padding: 18px 20px;
            text-align: center;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            color: #b0b0b0;
            border-bottom: 4px solid transparent;
        }
        
        .tab:hover {
            background-color: rgba(66, 66, 66, 0.3);
            color: #ffffff;
        }
        
        .tab.active {
            color: #00e5ff;
            border-bottom: 4px solid #00e5ff;
            background-color: rgba(0, 229, 255, 0.05);
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            padding: 24px;
            gap: 24px;
        }
        
        @media (min-width: 900px) {
            .main-content {
                flex-direction: row;
            }
        }
        
        .animation-area {
            flex: 3;
            background-color: rgba(10, 15, 30, 0.9);
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            border: 1px solid rgba(255, 255, 255, 0.05);
            min-height: 500px;
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .control-panel {
            flex: 1;
            background-color: rgba(40, 40, 60, 0.8);
            border-radius: 12px;
            padding: 24px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            min-width: 280px;
        }
        
        .scene-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: #81d4fa;
            padding-bottom: 12px;
            border-bottom: 1px solid rgba(129, 212, 250, 0.3);
        }
        
        .scene-description {
            margin-bottom: 24px;
            font-size: 0.95rem;
            line-height: 1.7;
            color: #cccccc;
        }
        
        .control-group {
            margin-bottom: 24px;
        }
        
        .control-title {
            font-size: 1.1rem;
            margin-bottom: 12px;
            color: #ffeb3b;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .control-title i {
            font-size: 1.2rem;
        }
        
        .slider-container {
            margin-bottom: 16px;
        }
        
        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 6px;
            font-size: 0.9rem;
        }
        
        .slider-value {
            color: #00e5ff;
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
            background: #00e5ff;
            cursor: pointer;
            box-shadow: 0 0 8px rgba(0, 229, 255, 0.7);
        }
        
        .button-group {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 12px 18px;
            border: none;
            border-radius: 8px;
            background-color: #37474f;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        button.primary {
            background-color: #1a237e;
        }
        
        button.primary:hover {
            background-color: #283593;
        }
        
        button.secondary {
            background-color: #ff9800;
            color: #1a1a1a;
        }
        
        button.secondary:hover {
            background-color: #ffb74d;
        }
        
        .toggle-container {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
        }
        
        .toggle-label {
            margin-left: 10px;
            font-size: 0.95rem;
        }
        
        .toggle-switch {
            position: relative;
            display: inline-block;
            width: 50px;
            height: 24px;
        }
        
        .toggle-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .toggle-slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #37474f;
            transition: .4s;
            border-radius: 24px;
        }
        
        .toggle-slider:before {
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
        
        input:checked + .toggle-slider {
            background-color: #00e5ff;
        }
        
        input:checked + .toggle-slider:before {
            transform: translateX(26px);
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 20px;
            padding-top: 16px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.85rem;
        }
        
        .legend-color {
            width: 16px;
            height: 16px;
            border-radius: 50%;
        }
        
        .info-box {
            background-color: rgba(0, 229, 255, 0.1);
            border-left: 4px solid #00e5ff;
            padding: 12px 16px;
            margin-top: 20px;
            border-radius: 0 8px 8px 0;
            font-size: 0.9rem;
        }
        
        .hidden {
            display: none;
        }
        
        .stats {
            position: absolute;
            top: 16px;
            left: 16px;
            background-color: rgba(0, 0, 0, 0.6);
            padding: 10px 16px;
            border-radius: 8px;
            font-size: 0.9rem;
            color: #ffeb3b;
            z-index: 10;
            border: 1px solid rgba(255, 235, 59, 0.3);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
            color: #81d4fa;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>分子运动论教学动画</h1>
            <p class="subtitle">探索微观世界：布朗运动、扩散现象与物态变化的微观解释</p>
        </header>
        
        <div class="scene-tabs">
            <div class="tab active" data-scene="1">分子运动模型</div>
            <div class="tab" data-scene="2">布朗运动与扩散</div>
            <div class="tab" data-scene="3">汽化与液化</div>
        </div>
        
        <div class="main-content">
            <div class="animation-area">
                <div class="stats" id="stats">分子数: 50 | 温度: 25°C</div>
                <canvas id="animationCanvas"></canvas>
            </div>
            
            <div class="control-panel">
                <div id="scene1-controls">
                    <h2 class="scene-title">分子运动模型</h2>
                    <p class="scene-description">观察分子在容器内的无规则运动。分子间存在间隙，永不停息地运动，相互碰撞并与容器壁碰撞。</p>
                    
                    <div class="control-group">
                        <div class="control-title">温度控制</div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>温度</span>
                                <span class="slider-value" id="tempValue1">25°C</span>
                            </div>
                            <input type="range" id="temperature1" min="0" max="50" value="25" step="1">
                        </div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>分子密度</span>
                                <span class="slider-value" id="densityValue1">50</span>
                            </div>
                            <input type="range" id="density1" min="10" max="100" value="50" step="5">
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">显示选项</div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="showForces1">
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">显示分子间作用力</span>
                        </div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="showVelocity1">
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">显示速度箭头</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button class="primary" id="playPause1">暂停动画</button>
                            <button id="reset1">重置</button>
                        </div>
                    </div>
                    
                    <div class="info-box">
                        <strong>观察要点：</strong> 提高温度会使分子运动更剧烈；增加密度会使分子间隙变小，碰撞更频繁。
                    </div>
                </div>
                
                <div id="scene2-controls" class="hidden">
                    <h2 class="scene-title">布朗运动与扩散</h2>
                    <p class="scene-description">左侧：布朗颗粒在分子撞击下的无规则运动。右侧：两种不同颜色的分子相互混合的扩散现象。</p>
                    
                    <div class="control-group">
                        <div class="control-title">实验控制</div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>温度</span>
                                <span class="slider-value" id="tempValue2">25°C</span>
                            </div>
                            <input type="range" id="temperature2" min="0" max="50" value="25" step="1">
                        </div>
                        <div class="button-group">
                            <button class="secondary" id="addBrownian">添加布朗颗粒</button>
                            <button id="removeBrownian">移除颗粒</button>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">显示选项</div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="showTrajectory" checked>
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">显示布朗运动轨迹</span>
                        </div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="startDiffusion">
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">开始扩散实验</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button class="primary" id="playPause2">暂停动画</button>
                            <button id="reset2">重置</button>
                        </div>
                    </div>
                    
                    <div class="info-box">
                        <strong>观察要点：</strong> 布朗颗粒越小，运动越明显；温度越高，扩散速度越快。
                    </div>
                </div>
                
                <div id="scene3-controls" class="hidden">
                    <h2 class="scene-title">汽化与液化</h2>
                    <p class="scene-description">左侧：液体蒸发 - 动能大的分子克服分子间引力逸出液面。右侧：气体液化 - 冷却使分子动能减小，在引力作用下聚集为液体。</p>
                    
                    <div class="control-group">
                        <div class="control-title">能量控制</div>
                        <div class="slider-container">
                            <div class="slider-label">
                                <span>系统能量</span>
                                <span class="slider-value" id="energyValue">50%</span>
                            </div>
                            <input type="range" id="energy" min="0" max="100" value="50" step="1">
                        </div>
                        <div class="button-group">
                            <button class="secondary" id="heatBtn">加热</button>
                            <button class="secondary" id="coolBtn">冷却</button>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-title">显示选项</div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="showEvaporation">
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">高亮逸出分子</span>
                        </div>
                        <div class="toggle-container">
                            <label class="toggle-switch">
                                <input type="checkbox" id="showCondensation">
                                <span class="toggle-slider"></span>
                            </label>
                            <span class="toggle-label">显示液化过程</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="button-group">
                            <button class="primary" id="playPause3">暂停动画</button>
                            <button id="reset3">重置</button>
                        </div>
                    </div>
                    
                    <div class="info-box">
                        <strong>观察要点：</strong> 加热增加分子动能，促进蒸发；冷却减少分子动能，促进液化。
                    </div>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #81d4fa;"></div>
                        <span>空气/水分子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ff9800;"></div>
                        <span>另一种分子</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #f44336;"></div>
                        <span>布朗颗粒</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #00e5ff;"></div>
                        <span>高能分子</span>
                    </div>
                </div>
            </div>
        </div>
        
        <footer>
            <p>分子运动论教学动画 | 设计原理：分子永不停息地做无规则运动，分子间存在间隙，分子间存在相互作用力</p>
        </footer>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animationCanvas');
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
        
        // 场景管理
        let currentScene = 1;
        const tabs = document.querySelectorAll('.tab');
        const sceneControls = [
            document.getElementById('scene1-controls'),
            document.getElementById('scene2-controls'),
            document.getElementById('scene3-controls')
        ];
        
        // 切换场景
        tabs.forEach(tab => {
            tab.addEventListener('click', () => {
                const sceneNum = parseInt(tab.dataset.scene);
                switchScene(sceneNum);
            });
        });
        
        function switchScene(sceneNum) {
            currentScene = sceneNum;
            
            // 更新标签状态
            tabs.forEach(tab => {
                if (parseInt(tab.dataset.scene) === sceneNum) {
                    tab.classList.add('active');
                } else {
                    tab.classList.remove('active');
                }
            });
            
            // 更新控制面板
            sceneControls.forEach((control, index) => {
                if (index + 1 === sceneNum) {
                    control.classList.remove('hidden');
                } else {
                    control.classList.add('hidden');
                }
            });
            
            // 重置动画状态
            resetAllScenes();
            initScene(sceneNum);
        }
        
        // 全局动画状态
        let animationId = null;
        let isPlaying = true;
        
        // 场景1：分子运动模型
        let molecules1 = [];
        const moleculeCount1 = 50;
        let temperature1 = 25;
        let showForces1 = false;
        let showVelocity1 = false;
        
        // 场景2：布朗运动与扩散
        let molecules2a = []; // 左侧分子
        let molecules2b = []; // 右侧分子（不同颜色）
        let brownianParticles = [];
        let showTrajectory = true;
        let diffusionStarted = false;
        let temperature2 = 25;
        
        // 场景3：汽化与液化
        let liquidMolecules = [];
        let gasMolecules = [];
        let energyLevel = 50;
        let showEvaporation = true;
        let showCondensation = true;
        
        // 分子类
        class Molecule {
            constructor(x, y, radius, color, isBrownian = false) {
                this.x = x;
                this.y = y;
                this.radius = radius;
                this.color = color;
                this.isBrownian = isBrownian;
                
                // 布朗颗粒速度较慢
                const speedFactor = isBrownian ? 0.3 : 1;
                const baseSpeed = 1 + temperature1 / 50;
                
                this.vx = (Math.random() - 0.5) * baseSpeed * speedFactor;
                this.vy = (Math.random() - 0.5) * baseSpeed * speedFactor;
                
                // 布朗颗粒轨迹
                this.trail = [];
                this.maxTrailLength = 20;
            }
            
            update(containerWidth, containerHeight, temperature) {
                // 根据温度调整速度
                const speedMultiplier = 0.5 + temperature / 50;
                
                // 布朗颗粒受分子撞击，运动更随机
                if (this.isBrownian) {
                    this.vx += (Math.random() - 0.5) * 0.1;
                    this.vy += (Math.random() - 0.5) * 0.1;
                    
                    // 限制布朗颗粒速度
                    const maxSpeed = 1.5 * speedMultiplier;
                    const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                    if (speed > maxSpeed) {
                        this.vx = (this.vx / speed) * maxSpeed;
                        this.vy = (this.vy / speed) * maxSpeed;
                    }
                    
                    // 记录轨迹
                    this.trail.push({x: this.x, y: this.y});
                    if (this.trail.length > this.maxTrailLength) {
                        this.trail.shift();
                    }
                } else {
                    this.vx *= 0.99; // 轻微阻力
                    this.vy *= 0.99;
                }
                
                // 更新位置
                this.x += this.vx * speedMultiplier;
                this.y += this.vy * speedMultiplier;
                
                // 边界碰撞
                if (this.x - this.radius < 0) {
                    this.x = this.radius;
                    this.vx = Math.abs(this.vx) * 0.9;
                }
                if (this.x + this.radius > containerWidth) {
                    this.x = containerWidth - this.radius;
                    this.vx = -Math.abs(this.vx) * 0.9;
                }
                if (this.y - this.radius < 0) {
                    this.y = this.radius;
                    this.vy = Math.abs(this.vy) * 0.9;
                }
                if (this.y + this.radius > containerHeight) {
                    this.y = containerHeight - this.radius;
                    this.vy = -Math.abs(this.vy) * 0.9;
                }
            }
            
            draw(ctx) {
                // 绘制轨迹（仅布朗颗粒）
                if (this.isBrownian && showTrajectory && this.trail.length > 1) {
                    ctx.beginPath();
                    ctx.moveTo(this.trail[0].x, this.trail[0].y);
                    
                    for (let i = 1; i < this.trail.length; i++) {
                        const point = this.trail[i];
                        ctx.lineTo(point.x, point.y);
                    }
                    
                    ctx.strokeStyle = 'rgba(244, 67, 54, 0.3)';
                    ctx.lineWidth = 2;
                    ctx.stroke();
                }
                
                // 绘制分子
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                
                // 创建发光效果
                const gradient = ctx.createRadialGradient(
                    this.x, this.y, 0,
                    this.x, this.y, this.radius * 1.5
                );
                
                if (this.isBrownian) {
                    gradient.addColorStop(0, '#f44336');
                    gradient.addColorStop(0.7, '#d32f2f');
                    gradient.addColorStop(1, 'rgba(211, 47, 47, 0)');
                } else {
                    if (this.color === 'blue') {
                        gradient.addColorStop(0, '#81d4fa');
                        gradient.addColorStop(0.7, '#4fc3f7');
                        gradient.addColorStop(1, 'rgba(79, 195, 247, 0)');
                    } else {
                        gradient.addColorStop(0, '#ff9800');
                        gradient.addColorStop(0.7, '#ff8a00');
                        gradient.addColorStop(1, 'rgba(255, 138, 0, 0)');
                    }
                }
                
                ctx.fillStyle = gradient;
                ctx.fill();
                
                // 绘制高能分子边框
                if (!this.isBrownian) {
                    const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                    if (speed > 2) {
                        ctx.beginPath();
                        ctx.arc(this.x, this.y, this.radius + 2, 0, Math.PI * 2);
                        ctx.strokeStyle = '#00e5ff';
                        ctx.lineWidth = 1.5;
                        ctx.stroke();
                    }
                }
                
                // 绘制速度箭头
                if (showVelocity1 && currentScene === 1 && !this.isBrownian) {
                    const speed = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                    if (speed > 0.1) {
                        const arrowLength = speed * 10;
                        const angle = Math.atan2(this.vy, this.vx);
                        
                        ctx.beginPath();
                        ctx.moveTo(this.x, this.y);
                        ctx.lineTo(
                            this.x + Math.cos(angle) * arrowLength,
                            this.y + Math.sin(angle) * arrowLength
                        );
                        ctx.strokeStyle = '#ffeb3b';
                        ctx.lineWidth = 1.5;
                        ctx.stroke();
                        
                        // 绘制箭头头部
                        ctx.beginPath();
                        ctx.moveTo(
                            this.x + Math.cos(angle) * arrowLength,
                            this.y + Math.sin(angle) * arrowLength
                        );
                        ctx.lineTo(
                            this.x + Math.cos(angle - Math.PI/6) * arrowLength * 0.7,
                            this.y + Math.sin(angle - Math.PI/6) * arrowLength * 0.7
                        );
                        ctx.lineTo(
                            this.x + Math.cos(angle + Math.PI/6) * arrowLength * 0.7,
                            this.y + Math.sin(angle + Math.PI/6) * arrowLength * 0.7
                        );
                        ctx.closePath();
                        ctx.fillStyle = '#ffeb3b';
                        ctx.fill();
                    }
                }
            }
            
            // 检查与其他分子的碰撞
            checkCollision(other) {
                const dx = other.x - this.x;
                const dy = other.y - this.y;
                const distance = Math.sqrt(dx * dx + dy * dy);
                const minDistance = this.radius + other.radius;
                
                if (distance < minDistance && distance > 0) {
                    // 计算碰撞角度
                    const angle = Math.atan2(dy, dx);
                    
                    // 计算速度分量
                    const speed1 = Math.sqrt(this.vx * this.vx + this.vy * this.vy);
                    const speed2 = Math.sqrt(other.vx * other.vx + other.vy * other.vy);
                    
                    // 计算方向
                    const direction1 = Math.atan2(this.vy, this.vx);
                    const direction2 = Math.atan2(other.vy, other.vx);
                    
                    // 碰撞后的速度（简化模型）
                    const newSpeed1 = speed2 * 0.9;
                    const newSpeed2 = speed1 * 0.9;
                    
                    // 更新速度
                    this.vx = Math.cos(direction2) * newSpeed1;
                    this.vy = Math.sin(direction2) * newSpeed1;
                    other.vx = Math.cos(direction1) * newSpeed2;
                    other.vy = Math.sin(direction1) * newSpeed2;
                    
                    // 防止重叠
                    const overlap = minDistance - distance;
                    this.x -= Math.cos(angle) * overlap / 2;
                    this.y -= Math.sin(angle) * overlap / 2;
                    other.x += Math.cos(angle) * overlap / 2;
                    other.y += Math.sin(angle) * overlap / 2;
                    
                    return true;
                }
                return false;
            }
        }
        
        // 初始化场景
        function initScene(sceneNum) {
            const width = canvas.width;
            const height = canvas.height;
            
            if (sceneNum === 1) {
                // 场景1：分子运动模型
                molecules1 = [];
                const count = parseInt(document.getElementById('density1').value);
                
                for (let i = 0; i < count; i++) {
                    const radius = 6 + Math.random() * 4;
                    const x = radius + Math.random() * (width - radius * 2);
                    const y = radius + Math.random() * (height - radius * 2);
                    
                    molecules1.push(new Molecule(x, y, radius, 'blue'));
                }
                
                updateStats();
            } 
            else if (sceneNum === 2) {
                // 场景2：布朗运动与扩散
                molecules2a = [];
                molecules2b = [];
                brownianParticles = [];
                
                // 左侧分子（蓝色）
                for (let i = 0; i < 40; i++) {
                    const radius = 5 + Math.random() * 3;
                    const x = radius + Math.random() * (width/2 - radius * 2);
                    const y = radius + Math.random() * (height - radius * 2);
                    
                    molecules2a.push(new Molecule(x, y, radius, 'blue'));
                }
                
                // 右侧分子（橙色）
                for (let i = 0; i < 40; i++) {
                    const radius = 5 + Math.random() * 3;
                    const x = width/2 + radius + Math.random() * (width/2 - radius * 2);
                    const y = radius + Math.random() * (height - radius * 2);
                    
                    molecules2b.push(new Molecule(x, y, radius, 'orange'));
                }
                
                // 添加几个布朗颗粒
                for (let i = 0; i < 3; i++) {
                    const radius = 10 + Math.random() * 5;
                    const x = radius + Math.random() * (width/2 - radius * 2);
                    const y = radius + Math.random() * (height - radius * 2);
                    
                    brownianParticles.push(new Molecule(x, y, radius, 'red', true));
                }
            }
            else if (sceneNum === 3) {
                // 场景3：汽化与液化
                liquidMolecules = [];
                gasMolecules = [];
                
                // 创建液体分子（底部）
                const liquidHeight = height * 0.6;
                for (let i = 0; i < 60; i++) {
                    const radius = 5 + Math.random() * 3;
                    const x = radius + Math.random() * (width/2 - radius * 2);
                    const y = height - liquidHeight + radius + Math.random() * (liquidHeight - radius * 2);
                    
                    const molecule = new Molecule(x, y, radius, 'blue');
                    // 液体分子运动较慢
                    molecule.vx *= 0.5;
                    molecule.vy *= 0.5;
                    liquidMolecules.push(molecule);
                }
                
                // 创建气体分子（右侧）
                for (let i = 0; i < 30; i++) {
                    const radius = 4 + Math.random() * 2;
                    const x = width/2 + radius + Math.random() * (width/2 - radius * 2);
                    const y = radius + Math.random() * (height - radius * 2);
                    
                    gasMolecules.push(new Molecule(x, y, radius, 'blue'));
                }
            }
        }
        
        // 重置所有场景
        function resetAllScenes() {
            molecules1 = [];
            molecules2a = [];
            molecules2b = [];
            brownianParticles = [];
            liquidMolecules = [];
            gasMolecules = [];
        }
        
        // 更新统计信息
        function updateStats() {
            const stats = document.getElementById('stats');
            if (currentScene === 1) {
                stats.textContent = `分子数: ${molecules1.length} | 温度: ${temperature1}°C`;
            } else if (currentScene === 2) {
                stats.textContent = `布朗颗粒: ${brownianParticles.length} | 温度: ${temperature2}°C`;
            } else if (currentScene === 3) {
                const evaporationRate = gasMolecules.length;
                stats.textContent = `液体分子: ${liquidMolecules.length} | 气体分子: ${evaporationRate} | 能量: ${energyLevel}%`;
            }
        }
        
        // 绘制场景1
        function drawScene1() {
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制容器
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.strokeRect(10, 10, width - 20, height - 20);
            
            // 更新并绘制分子
            for (let i = 0; i < molecules1.length; i++) {
                molecules1[i].update(width - 20, height - 20, temperature1);
                molecules1[i].draw(ctx);
                
                // 检查碰撞
                for (let j = i + 1; j < molecules1.length; j++) {
                    molecules1[i].checkCollision(molecules1[j]);
                }
                
                // 绘制分子间作用力（示意）
                if (showForces1) {
                    for (let j = i + 1; j < molecules1.length; j++) {
                        const dx = molecules1[j].x - molecules1[i].x;
                        const dy = molecules1[j].y - molecules1[i].y;
                        const distance = Math.sqrt(dx * dx + dy * dy);
                        
                        if (distance < 80) {
                            const force = 80 - distance; // 距离越近，力越大
                            const angle = Math.atan2(dy, dx);
                            
                            // 绘制力箭头
                            const arrowX = molecules1[i].x + dx / 2;
                            const arrowY = molecules1[i].y + dy / 2;
                            const arrowLength = Math.min(force / 5, 15);
                            
                            ctx.beginPath();
                            ctx.moveTo(arrowX, arrowY);
                            ctx.lineTo(
                                arrowX - Math.cos(angle) * arrowLength,
                                arrowY - Math.sin(angle) * arrowLength
                            );
                            ctx.strokeStyle = distance < 40 ? '#ff5252' : '#4caf50';
                            ctx.lineWidth = 1.5;
                            ctx.stroke();
                            
                            // 绘制箭头头部
                            ctx.beginPath();
                            ctx.moveTo(
                                arrowX - Math.cos(angle) * arrow
<!--检测到代码截断，自动续写中...-->
```html
                                arrowX - Math.cos(angle) * arrowLength,
                                arrowY - Math.sin(angle) * arrowLength
                            );
                            ctx.lineTo(
                                arrowX - Math.cos(angle - Math.PI/6) * arrowLength * 0.7,
                                arrowY - Math.sin(angle - Math.PI/6) * arrowLength * 0.7
                            );
                            ctx.lineTo(
                                arrowX - Math.cos(angle + Math.PI/6) * arrowLength * 0.7,
                                arrowY - Math.sin(angle + Math.PI/6) * arrowLength * 0.7
                            );
                            ctx.closePath();
                            ctx.fillStyle = distance < 40 ? '#ff5252' : '#4caf50';
                            ctx.fill();
                        }
                    }
                }
            }
            
            // 绘制标题
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('分子运动基本模型', width / 2, 40);
            
            // 绘制说明
            ctx.font = '14px Arial';
            ctx.fillText('分子永不停息地做无规则运动，相互碰撞并与容器壁碰撞', width / 2, height - 30);
        }
        
        // 绘制场景2
        function drawScene2() {
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制分隔线
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(width / 2, 0);
            ctx.lineTo(width / 2, height);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制左侧容器（布朗运动）
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.strokeRect(10, 10, width / 2 - 20, height - 20);
            
            // 绘制右侧容器（扩散）
            ctx.strokeRect(width / 2 + 10, 10, width / 2 - 20, height - 20);
            
            // 更新并绘制左侧分子
            const allMolecules2 = [...molecules2a, ...molecules2b];
            for (let i = 0; i < allMolecules2.length; i++) {
                // 限制分子在各自区域内（除非扩散开始）
                const molecule = allMolecules2[i];
                const isLeftMolecule = molecules2a.includes(molecule);
                
                if (!diffusionStarted) {
                    if (isLeftMolecule && molecule.x > width / 2 - molecule.radius) {
                        molecule.x = width / 2 - molecule.radius;
                        molecule.vx = -Math.abs(molecule.vx);
                    } else if (!isLeftMolecule && molecule.x < width / 2 + molecule.radius) {
                        molecule.x = width / 2 + molecule.radius;
                        molecule.vx = Math.abs(molecule.vx);
                    }
                }
                
                molecule.update(width - 20, height - 20, temperature2);
                molecule.draw(ctx);
                
                // 检查碰撞
                for (let j = i + 1; j < allMolecules2.length; j++) {
                    molecule.checkCollision(allMolecules2[j]);
                }
            }
            
            // 更新并绘制布朗颗粒
            for (let i = 0; i < brownianParticles.length; i++) {
                const particle = brownianParticles[i];
                
                // 限制布朗颗粒在左侧区域
                if (particle.x > width / 2 - particle.radius) {
                    particle.x = width / 2 - particle.radius;
                    particle.vx = -Math.abs(particle.vx);
                }
                
                particle.update(width / 2 - 20, height - 20, temperature2);
                particle.draw(ctx);
                
                // 布朗颗粒与分子碰撞
                for (let j = 0; j < molecules2a.length; j++) {
                    particle.checkCollision(molecules2a[j]);
                }
            }
            
            // 绘制标题
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('布朗运动', width / 4, 40);
            ctx.fillText('扩散现象', width * 3 / 4, 40);
            
            // 绘制说明
            ctx.font = '14px Arial';
            ctx.fillText('左侧：布朗颗粒受分子撞击做无规则运动', width / 4, height - 40);
            ctx.fillText('右侧：两种分子相互混合', width * 3 / 4, height - 40);
            
            if (diffusionStarted) {
                ctx.fillStyle = '#00e5ff';
                ctx.fillText('扩散进行中...', width * 3 / 4, height - 20);
            } else {
                ctx.fillStyle = '#ff9800';
                ctx.fillText('点击"开始扩散实验"观察混合过程', width * 3 / 4, height - 20);
            }
        }
        
        // 绘制场景3
        function drawScene3() {
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制分隔线
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.lineWidth = 1;
            ctx.setLineDash([5, 5]);
            ctx.beginPath();
            ctx.moveTo(width / 2, 0);
            ctx.lineTo(width / 2, height);
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制左侧容器（汽化）
            ctx.strokeStyle = 'rgba(255, 255, 255, 0.2)';
            ctx.lineWidth = 2;
            ctx.strokeRect(10, 10, width / 2 - 20, height - 20);
            
            // 绘制右侧容器（液化）
            ctx.strokeRect(width / 2 + 10, 10, width / 2 - 20, height - 20);
            
            // 绘制左侧液面
            const liquidLevel = height * 0.4;
            ctx.fillStyle = 'rgba(129, 212, 250, 0.3)';
            ctx.fillRect(10, height - liquidLevel, width / 2 - 20, liquidLevel);
            
            // 绘制液面线
            ctx.strokeStyle = 'rgba(129, 212, 250, 0.6)';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(10, height - liquidLevel);
            ctx.lineTo(width / 2 - 10, height - liquidLevel);
            ctx.stroke();
            
            // 更新并绘制液体分子
            const evaporationEnergy = energyLevel / 100 * 3; // 能量影响蒸发
            
            for (let i = 0; i < liquidMolecules.length; i++) {
                const molecule = liquidMolecules[i];
                
                // 限制在左侧区域
                if (molecule.x > width / 2 - molecule.radius) {
                    molecule.x = width / 2 - molecule.radius;
                    molecule.vx = -Math.abs(molecule.vx);
                }
                
                // 模拟蒸发：表面分子可能逸出
                if (molecule.y < height - liquidLevel + 30 && Math.random() < 0.01 * evaporationEnergy) {
                    // 分子获得足够能量逸出
                    molecule.vy = -Math.abs(molecule.vy) * (2 + Math.random() * evaporationEnergy);
                    
                    if (showEvaporation) {
                        // 高亮逸出分子
                        ctx.beginPath();
                        ctx.arc(molecule.x, molecule.y, molecule.radius + 4, 0, Math.PI * 2);
                        ctx.strokeStyle = '#00e5ff';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                        
                        // 绘制能量箭头
                        ctx.beginPath();
                        ctx.moveTo(molecule.x, molecule.y);
                        ctx.lineTo(molecule.x, molecule.y - 30);
                        ctx.strokeStyle = '#ffeb3b';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                        
                        // 箭头头部
                        ctx.beginPath();
                        ctx.moveTo(molecule.x, molecule.y - 30);
                        ctx.lineTo(molecule.x - 5, molecule.y - 25);
                        ctx.lineTo(molecule.x + 5, molecule.y - 25);
                        ctx.closePath();
                        ctx.fillStyle = '#ffeb3b';
                        ctx.fill();
                    }
                }
                
                molecule.update(width / 2 - 20, height - 20, energyLevel / 2);
                molecule.draw(ctx);
                
                // 液体分子间碰撞
                for (let j = i + 1; j < liquidMolecules.length; j++) {
                    molecule.checkCollision(liquidMolecules[j]);
                }
            }
            
            // 更新并绘制气体分子
            for (let i = 0; i < gasMolecules.length; i++) {
                const molecule = gasMolecules[i];
                
                // 限制在右侧区域
                if (molecule.x < width / 2 + molecule.radius) {
                    molecule.x = width / 2 + molecule.radius;
                    molecule.vx = Math.abs(molecule.vx);
                }
                
                // 模拟液化：冷却时分子可能聚集
                const condensationFactor = (100 - energyLevel) / 100; // 能量越低，液化越容易
                
                if (condensationFactor > 0.5 && Math.random() < 0.005 * condensationFactor) {
                    // 分子速度减慢，模拟液化
                    molecule.vx *= 0.9;
                    molecule.vy *= 0.9;
                    
                    if (showCondensation) {
                        // 显示液化过程
                        ctx.beginPath();
                        ctx.arc(molecule.x, molecule.y, molecule.radius + 3, 0, Math.PI * 2);
                        ctx.strokeStyle = '#4caf50';
                        ctx.lineWidth = 1.5;
                        ctx.stroke();
                        
                        // 绘制引力范围
                        ctx.beginPath();
                        ctx.arc(molecule.x, molecule.y, 30, 0, Math.PI * 2);
                        ctx.strokeStyle = 'rgba(76, 175, 80, 0.3)';
                        ctx.lineWidth = 1;
                        ctx.stroke();
                    }
                }
                
                molecule.update(width - 20, height - 20, energyLevel / 2);
                molecule.draw(ctx);
                
                // 气体分子间碰撞
                for (let j = i + 1; j < gasMolecules.length; j++) {
                    molecule.checkCollision(gasMolecules[j]);
                }
            }
            
            // 绘制标题
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.font = 'bold 18px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('汽化（蒸发）', width / 4, 40);
            ctx.fillText('液化', width * 3 / 4, 40);
            
            // 绘制说明
            ctx.font = '14px Arial';
            ctx.fillText('加热增加分子动能，促进蒸发', width / 4, height - 40);
            ctx.fillText('冷却减少分子动能，促进液化', width * 3 / 4, height - 40);
            
            // 绘制能量指示器
            ctx.fillStyle = energyLevel > 50 ? '#ff9800' : '#81d4fa';
            ctx.fillText(`能量水平: ${energyLevel}%`, width / 4, height - 20);
            ctx.fillText(`能量水平: ${energyLevel}%`, width * 3 / 4, height - 20);
        }
        
        // 主动画循环
        function animate() {
            if (!isPlaying) return;
            
            if (currentScene === 1) {
                drawScene1();
            } else if (currentScene === 2) {
                drawScene2();
            } else if (currentScene === 3) {
                drawScene3();
            }
            
            updateStats();
            animationId = requestAnimationFrame(animate);
        }
        
        // 初始化事件监听器
        function initEventListeners() {
            // 场景1控制
            document.getElementById('temperature1').addEventListener('input', function() {
                temperature1 = parseInt(this.value);
                document.getElementById('tempValue1').textContent = temperature1 + '°C';
            });
            
            document.getElementById('density1').addEventListener('input', function() {
                const density = parseInt(this.value);
                document.getElementById('densityValue1').textContent = density;
                initScene(1);
            });
            
            document.getElementById('showForces1').addEventListener('change', function() {
                showForces1 = this.checked;
            });
            
            document.getElementById('showVelocity1').addEventListener('change', function() {
                showVelocity1 = this.checked;
            });
            
            document.getElementById('playPause1').addEventListener('click', function() {
                isPlaying = !isPlaying;
                this.textContent = isPlaying ? '暂停动画' : '播放动画';
                if (isPlaying) animate();
            });
            
            document.getElementById('reset1').addEventListener('click', function() {
                initScene(1);
            });
            
            // 场景2控制
            document.getElementById('temperature2').addEventListener('input', function() {
                temperature2 = parseInt(this.value);
                document.getElementById('tempValue2').textContent = temperature2 + '°C';
            });
            
            document.getElementById('addBrownian').addEventListener('click', function() {
                const width = canvas.width;
                const height = canvas.height;
                const radius = 10 + Math.random() * 5;
                const x = radius + Math.random() * (width/2 - radius * 2);
                const y = radius + Math.random() * (height - radius * 2);
                
                brownianParticles.push(new Molecule(x, y, radius, 'red', true));
            });
            
            document.getElementById('removeBrownian').addEventListener('click', function() {
                if (brownianParticles.length > 0) {
                    brownianParticles.pop();
                }
            });
            
            document.getElementById('showTrajectory').addEventListener('change', function() {
                showTrajectory = this.checked;
            });
            
            document.getElementById('startDiffusion').addEventListener('change', function() {
                diffusionStarted = this.checked;
            });
            
            document.getElementById('playPause2').addEventListener('click', function() {
                isPlaying = !isPlaying;
                this.textContent = isPlaying ? '暂停动画' : '播放动画';
                if (isPlaying) animate();
            });
            
            document.getElementById('reset2').addEventListener('click', function() {
                initScene(2);
            });
            
            // 场景3控制
            document.getElementById('energy').addEventListener('input', function() {
                energyLevel = parseInt(this.value);
                document.getElementById('energyValue').textContent = energyLevel + '%';
            });
            
            document.getElementById('heatBtn').addEventListener('click', function() {
                energyLevel = Math.min(100, energyLevel + 10);
                document.getElementById('energy').value = energyLevel;
                document.getElementById('energyValue').textContent = energyLevel + '%';
            });
            
            document.getElementById('coolBtn').addEventListener('click', function() {
                energyLevel = Math.max(0, energyLevel - 10);
                document.getElementById('energy').value = energyLevel;
                document.getElementById('energyValue').textContent = energyLevel + '%';
            });
            
            document.getElementById('showEvaporation').addEventListener('change', function() {
                showEvaporation = this.checked;
            });
            
            document.getElementById('showCondensation').addEventListener('change', function() {
                showCondensation = this.checked;
            });
            
            document.getElementById('playPause3').addEventListener('click', function() {
                isPlaying = !isPlaying;
                this.textContent = isPlaying ? '暂停动画' : '播放动画';
                if (isPlaying) animate();
            });
            
            document.getElementById('reset3').addEventListener('click', function() {
                initScene(3);
            });
            
            // 全局播放/暂停按钮同步
            const playPauseButtons = ['playPause1', 'playPause2', 'playPause3'];
            playPauseButtons.forEach(buttonId => {
                document.getElementById(buttonId).addEventListener('click', function() {
                    // 更新所有播放/暂停按钮的文本
                    playPauseButtons.forEach(otherButtonId => {
                        if (otherButtonId !== buttonId) {
                            document.getElementById(otherButtonId).textContent = 
                                isPlaying ? '暂停动画' : '播放动画';
                        }
                    });
                });
            });
        }
        
        // 初始化
        function init() {
            resizeCanvas();
            initScene(1);
            initEventListeners();
            animate();
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>
```

### 3. 过程输出

### 3. 使用指南

## 分子运动论交互式教学动画使用指南

欢迎使用“分子运动论”交互式教学动画！本动画旨在通过可视化、可交互的方式，帮助您深入理解分子运动论的核心概念。无论您是教师、学生还是对物理学感兴趣的探索者，本工具都将为您提供直观的学习体验。

---

### 一、功能说明

本动画包含三个核心教学场景，每个场景都配有独立的控制面板，让您能够通过调整参数来观察微观世界的变化：

1. **分子运动模型** - 展示分子在容器内的无规则运动，验证分子运动论的基本观点
2. **布朗运动与扩散** - 模拟布朗颗粒的运动和两种分子的扩散过程
3. **汽化与液化** - 揭示物态变化的微观机制

### 二、主要功能

#### 场景切换
- 点击顶部的标签页（“分子运动模型”、“布朗运动与扩散”、“汽化与液化”）可在三个场景间自由切换
- 每个场景都有独立的动画和控制选项

#### 通用控制功能
- **播放/暂停**：控制动画的运行与停止
- **重置**：将当前场景恢复到初始状态
- **温度调节**：通过滑块实时改变系统温度，观察分子运动速度的变化
- **统计信息**：左上角实时显示当前场景的关键数据

#### 场景特有功能

**场景1：分子运动模型**
- 分子密度调节：改变容器内分子数量，观察间隙和碰撞频率变化
- 显示分子间作用力：可视化分子接近时的相互作用
- 显示速度箭头：用箭头表示分子的运动方向和速度大小

**场景2：布朗运动与扩散**
- 添加/移除布朗颗粒：可动态增加或减少布朗颗粒
- 轨迹显示开关：观察布朗颗粒的无规则运动路径
- 扩散实验开关：控制两种不同颜色分子的混合过程

**场景3：汽化与液化**
- 能量控制滑块：调节系统能量水平
- 加热/冷却按钮：快速改变系统温度
- 高亮显示：特别标记从液体逸出的高能分子和液化过程

### 三、设计特色

#### 1. 科学的可视化设计
- **颜色编码系统**：
  - 浅蓝色：空气/水分子
  - 橙色：另一种物质分子（用于扩散实验）
  - 红色：布朗颗粒
  - 亮青色：高能分子（即将逸出液面）
- **动态效果**：
  - 分子带有光晕效果，增强立体感
  - 布朗颗粒显示运动轨迹
  - 高能分子有特殊边框标记

#### 2. 符合认知规律的教学流程
- 从简单到复杂：先建立基本分子模型，再解释宏观现象
- 对比观察：支持并排对比不同条件下的现象差异
- 即时反馈：所有参数调整都能立即看到效果

#### 3. 专业的交互设计
- 响应式布局：适应不同屏幕尺寸
- 直观的控制面板：参数调节与动画效果紧密关联
- 实时提示：每个场景都有“观察要点”提示框

### 四、教学要点

#### 核心概念验证
1. **分子永不停息地做无规则运动**
   - 观察场景1中分子的持续运动
   - 注意分子运动方向和大小的随机性

2. **分子间存在间隙**
   - 调节场景1的分子密度，观察间隙变化
   - 对比高密度和低密度下的分子分布

3. **分子间存在相互作用力**
   - 开启“显示分子间作用力”选项
   - 观察分子接近时作用力的变化（红色表示斥力，绿色表示引力）

#### 现象解释
1. **布朗运动**
   - 观察布朗颗粒在分子撞击下的“之”字形路径
   - 提高温度，观察运动加剧
   - 对比不同大小颗粒的运动差异

2. **扩散现象**
   - 启动扩散实验，观察两种分子逐渐混合
   - 对比高温和低温下的扩散速度
   - 思考：为什么扩散过程不可逆？

3. **物态变化的微观解释**
   - **汽化**：观察液面处动能大的分子如何克服引力逸出
   - **液化**：观察冷却时分子如何聚集形成液滴
   - 注意能量变化对相变过程的影响

### 五、使用建议

#### 对于教师
1. **课堂演示**
   - 使用投影仪全屏展示，配合讲解逐步演示
   - 重点演示温度变化对分子运动的影响
   - 使用“暂停”功能定格关键瞬间进行讲解

2. **探究式学习活动设计**
   - 提出问题：“温度从25°C升到50°C，分子运动速度变化多少？”
   - 让学生预测结果，然后通过动画验证
   - 设计对比实验：高温vs低温下的扩散速度

3. **概念强化**
   - 在讲解布朗运动时，强调“分子撞击”是根本原因
   - 在讲解相变时，突出“能量变化”的关键作用
   - 使用动画纠正常见误解（如“冷分子不动”）

#### 对于学生
1. **自主学习**
   - 按照“分子模型→布朗运动→物态变化”的顺序探索
   - 对每个控制选项都尝试调节，观察变化
   - 记录观察结果，与理论知识对照

2. **实验验证**
   - 假设：“分子越小，布朗运动越明显”
   - 验证：添加不同大小的布朗颗粒进行观察
   - 结论：通过动画数据支持或修正假设

3. **复习巩固**
   - 在考试前，通过动画快速回顾核心概念
   - 重点关注宏观现象与微观解释的联系
   - 利用交互功能加深对难点问题的理解

#### 技术提示
1. **最佳观看体验**
   - 使用Chrome、Firefox或Edge等现代浏览器
   - 确保屏幕分辨率不低于1366×768
   - 全屏模式下可获得最佳视觉效果

2. **性能优化**
   - 如果动画运行卡顿，可适当减少分子数量
   - 关闭不需要的可视化选项（如轨迹显示）
   - 暂停动画后再进行复杂的参数调整

3. **教学扩展**
   - 鼓励学生提出自己的实验方案
   - 将动画观察与真实实验相结合
   - 讨论动画的局限性（如简化模型vs真实情况）

---

### 探索开始！

现在，您已经掌握了本教学动画的所有功能。请点击不同的场景标签，大胆尝试各种控制选项，亲自探索分子世界的奥秘。记住：最好的学习方式就是动手尝试！

如果您在教学过程中有任何发现或建议，欢迎记录并与他人分享。祝您探索愉快！

**熊猫老师提示**：科学探索的乐趣在于发现规律的过程，而不仅仅是记住结论。尽情享受这个发现之旅吧！