# 需求：氯气与氢气爆炸（光照+微观链式反应）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画面向高中或大学低年级的化学学习者。用户的核心需求是：
1.  **理解宏观现象**：直观地看到氯气与氢气混合气体在光照下发生爆炸的宏观现象。
2.  **建立宏观-微观联系**：理解宏观爆炸现象背后的微观本质——光引发的自由基链式反应。
3.  **掌握反应机理**：清晰地掌握链引发、链增长、链终止三个关键步骤，理解“链式”的含义。
4.  **明确反应条件**：深刻理解“光照”作为反应启动条件的必要性，以及混合气体比例（爆炸极限）的概念。
5.  **克服认知难点**：传统教学难以动态展示瞬间的链式反应过程，本动画需将这一抽象、快速的过程可视化、慢放化、步骤化。

#### 教学设计思路（核心概念、认知规律、交互设计、视觉呈现）

*   **核心概念**：
    *   宏观：氯氢混合气、光照条件、爆炸现象。
    *   微观：光子能量、氯分子均裂（产生氯自由基）、链引发、链增长（自由基传递）、链终止。
    *   联系：一个光子引发一个氯分子均裂，产生两个自由基，进而引发成千上万个分子反应，释放大量热和光，导致气体体积急剧膨胀（爆炸）。

*   **认知规律**：
    *   **从宏观到微观**：先展示爆炸的震撼效果（吸引注意），再引导探究其内部机理。
    *   **分解复杂过程**：将瞬间完成的链式反应分解为可暂停、可观察的独立步骤。
    *   **可视化抽象粒子**：用不同颜色、形状的球体代表原子、分子和自由基，并用“闪烁”、“高亮”、“路径线”等视觉元素强调关键事件（如光子撞击、化学键断裂/形成）。
    *   **交互式控制**：允许用户控制反应进程（播放/暂停/步骤）、调节条件（如光照强度、气体比例），以观察不同变量下的结果，深化理解。

*   **交互设计**：
    *   **场景切换**：设计“宏观实验舱”和“微观反应视图”两个主场景，可一键切换。
    *   **控制面板**：提供反应启动（模拟光照）、暂停、步进（下一步）、重置按钮。
    *   **参数调节**：在宏观场景中，提供滑块调节氢气和氯气的初始比例，观察是否爆炸及爆炸强度。
    *   **信息提示**：鼠标悬停在粒子、按钮上时，显示名称和解释（如“Cl· 氯自由基”）。
    *   **步骤高亮**：在微观视图中，当前正在进行的反应步骤（如链引发）会有标题和边框高亮提示。

*   **视觉呈现**：
    *   **宏观场景**：
        *   一个透明的反应器（如集气瓶或石英管），内部有黄绿色（Cl₂）和浅灰色（H₂，视觉上可稍显透明）的混合气体。
        *   一束代表强光（如紫外光）的光柱从顶部射入。
        *   爆炸时，反应器内瞬间充满白光，伴随“膨胀”动画和模拟震动效果，随后显示产物HCl的“白雾”（可用半透明白色粒子流表示）。
    *   **微观场景**：
        *   深色背景，聚焦于一个区域内的粒子运动。
        *   **粒子设计**：
            *   氯原子（Cl）：绿色球体。
            *   氢原子（H）：浅灰色或白色小球体。
            *   氯分子（Cl₂）：两个绿色球体由一根“化学键”（粗实线或弹簧状连接）连接。
            *   氢分子（H₂）：两个浅灰色球体连接。
            *   氯化氢分子（HCl）：一个绿色球体和一个浅灰色球体连接。
            *   **自由基（关键！）**：在对应原子球体上加一个显著的“高亮外圈”或一个“小黑点”作为电子标记，例如氯自由基（Cl·）是带高亮外圈的绿色球体。
        *   **反应动画**：
            *   **链引发**：一个“光子”（闪烁的黄色光点）击中一个Cl₂，化学键剧烈振动后断裂，两个Cl·向两边飞开，带有动能效果。
            *   **链增长**：
                *   Cl· 高速撞向 H₂，H-H键断裂，形成 HCl 和 H·。
                *   H· 高速撞向 Cl₂，Cl-Cl键断裂，形成 HCl 和新的 Cl·。
                *   此过程循环，用“追踪线”或短暂高亮显示一个自由基的传递路径，清晰展示“链”的延伸。
            *   **链终止**：两个自由基（如 Cl· + Cl·，或 H· + Cl·，或 H· + H·）相遇结合成稳定分子，反应链中断。

#### 配色方案选择
*   **主色调**：深蓝或深灰色背景，营造科学、微观世界的氛围，同时能突出前景的彩色粒子。
*   **粒子色**：
    *   **氯 (Cl)**：**黄绿色** (#9ACD32 或 #ADFF2F)，贴近氯气的真实颜色，建立直观联系。
    *   **氢 (H)**：**浅灰色** (#D3D3D3) 或 **极浅的蓝色** (#E6F7FF)，表示无色。
    *   **氯化氢 (HCl)**：组合色，或采用**白色半透明**，以关联其遇水汽形成的白雾。
*   **高亮与特效色**：
    *   **光子/能量**：亮黄色 (#FFFF00) 或白色，带有光晕。
    *   **爆炸光效**：白色与橙色 (#FFA500) 渐变。
    *   **化学键**：淡灰色 (#AAAAAA) 实线或渐变线。
    *   **自由基高亮**：亮黄色 (#FFFF00) 或亮青色 (#00FFFF) 外圈。
    *   **交互元素（按钮）**：科技蓝 (#4A90E2) 为主，悬停时变为亮蓝 (#66B3FF)。

#### 交互功能列表
1.  **场景切换按钮**：在“宏观实验”与“微观视角”之间切换。
2.  **宏观场景控制**：
    *   **气体比例调节滑块**：两个滑块分别控制H₂和Cl₂的初始分子数比例（如1:1， 1:2， 2:1）。
    *   **“启动光照”按钮**：触发爆炸动画。
    *   **爆炸重置按钮**：清除爆炸效果，恢复混合气体状态。
3.  **微观场景控制**：
    *   **播放/暂停按钮**：开始或暂停链式反应动画。
    *   **步进（下一步）按钮**：手动逐步进行反应（链引发→步骤1→步骤2→链终止…）。
    *   **重置按钮**：清除所有反应粒子，恢复为初始的H₂和Cl₂分子混合状态。
    *   **反应步骤说明面板**：实时显示当前步骤的名称和化学方程式（如“链引发：Cl₂ → 2Cl·”）。
4.  **信息提示**：鼠标悬停在任何粒子或按钮上时，弹出文本框进行简要说明。
5.  **动画速度调节**（可选）：一个滑块，用于调节微观粒子运动的快慢。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>氯气与氢气爆炸 - 链式反应教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #0a1929 0%, #1a3a5f 100%);
            color: #e6f7ff;
            min-height: 100vh;
            padding: 20px;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4A90E2;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #9ACD32;
            text-shadow: 0 0 10px rgba(154, 205, 50, 0.3);
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #ADFF2F;
            opacity: 0.9;
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        .scene-selector {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 10px;
        }
        
        .scene-btn {
            padding: 12px 24px;
            background-color: #4A90E2;
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
        }
        
        .scene-btn:hover {
            background-color: #66B3FF;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 179, 255, 0.3);
        }
        
        .scene-btn.active {
            background-color: #ADFF2F;
            color: #0a1929;
            box-shadow: 0 0 15px rgba(173, 255, 47, 0.5);
        }
        
        .scene-container {
            background-color: rgba(10, 25, 41, 0.7);
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid #2a4a6f;
        }
        
        .scene-title {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #ADFF2F;
            text-align: center;
        }
        
        #macro-scene, #micro-scene {
            display: none;
            flex-direction: column;
            gap: 20px;
        }
        
        #macro-scene.active, #micro-scene.active {
            display: flex;
        }
        
        .canvas-container {
            position: relative;
            width: 100%;
            height: 400px;
            background-color: #0a1929;
            border-radius: 8px;
            overflow: hidden;
            border: 2px solid #2a4a6f;
        }
        
        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }
        
        .controls {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            align-items: center;
            padding: 15px;
            background-color: rgba(26, 58, 95, 0.5);
            border-radius: 8px;
        }
        
        .control-group {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
        }
        
        .control-label {
            font-size: 0.9rem;
            color: #9ACD32;
        }
        
        .slider-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        input[type="range"] {
            width: 150px;
            height: 6px;
            -webkit-appearance: none;
            background: #2a4a6f;
            border-radius: 3px;
            outline: none;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: #4A90E2;
            cursor: pointer;
            border: 2px solid #e6f7ff;
        }
        
        .slider-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: #ADFF2F;
        }
        
        .btn {
            padding: 10px 20px;
            background-color: #4A90E2;
            color: white;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            font-weight: bold;
        }
        
        .btn:hover {
            background-color: #66B3FF;
            transform: translateY(-2px);
        }
        
        .btn:active {
            transform: translateY(0);
        }
        
        .btn-primary {
            background-color: #ADFF2F;
            color: #0a1929;
        }
        
        .btn-primary:hover {
            background-color: #9ACD32;
        }
        
        .btn-danger {
            background-color: #ff4757;
        }
        
        .btn-danger:hover {
            background-color: #ff6b81;
        }
        
        .info-panel {
            background-color: rgba(26, 58, 95, 0.7);
            border-radius: 8px;
            padding: 15px;
            margin-top: 10px;
            border-left: 4px solid #4A90E2;
        }
        
        .info-title {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #ADFF2F;
        }
        
        .step-info {
            background-color: rgba(154, 205, 50, 0.1);
            border-radius: 6px;
            padding: 12px;
            margin-top: 10px;
            border: 1px solid rgba(154, 205, 50, 0.3);
        }
        
        .step-title {
            font-weight: bold;
            color: #9ACD32;
            margin-bottom: 5px;
        }
        
        .step-equation {
            font-family: 'Courier New', monospace;
            background-color: rgba(0, 0, 0, 0.3);
            padding: 5px 10px;
            border-radius: 4px;
            margin: 5px 0;
            color: #ADFF2F;
        }
        
        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 15px;
        }
        
        .legend-item {
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
        }
        
        .legend-label {
            font-size: 0.9rem;
        }
        
        .footer {
            text-align: center;
            margin-top: 30px;
            padding-top: 20px;
            border-top: 1px solid #2a4a6f;
            color: #9ACD32;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .scene-selector {
                flex-direction: column;
                align-items: center;
            }
            
            .controls {
                flex-direction: column;
                align-items: stretch;
            }
            
            .control-group {
                width: 100%;
            }
            
            input[type="range"] {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>氯气与氢气爆炸反应</h1>
            <p class="subtitle">光照条件下的链式反应微观机理</p>
        </header>
        
        <main class="main-content">
            <div class="scene-selector">
                <button id="macro-btn" class="scene-btn active">宏观实验</button>
                <button id="micro-btn" class="scene-btn">微观视角</button>
            </div>
            
            <!-- 宏观场景 -->
            <div id="macro-scene" class="scene-container active">
                <h2 class="scene-title">宏观实验：氯气与氢气混合光照爆炸</h2>
                
                <div class="canvas-container">
                    <canvas id="macro-canvas"></canvas>
                </div>
                
                <div class="controls">
                    <div class="control-group">
                        <div class="control-label">氢气比例 (H₂)</div>
                        <div class="slider-container">
                            <input type="range" id="h2-slider" min="1" max="10" value="5">
                            <span id="h2-value" class="slider-value">5</span>
                        </div>
                    </div>
                    
                    <div class="control-group">
                        <div class="control-label">氯气比例 (Cl₂)</div>
                        <div class="slider-container">
                            <input type="range" id="cl2-slider" min="1" max="10" value="5">
                            <span id="cl2-value" class="slider-value">5</span>
                        </div>
                    </div>
                    
                    <button id="light-btn" class="btn btn-primary">启动光照</button>
                    <button id="reset-macro-btn" class="btn">重置实验</button>
                </div>
                
                <div class="info-panel">
                    <div class="info-title">实验说明</div>
                    <p>调整氢气和氯气的比例，然后点击"启动光照"模拟紫外光照射。当混合气体比例在爆炸极限范围内时，会发生剧烈爆炸，生成氯化氢气体（遇水汽形成白雾）。</p>
                    <p>注意：实际实验中，氯气呈黄绿色，氢气无色，氯化氢遇水汽形成白雾。</p>
                </div>
            </div>
            
            <!-- 微观场景 -->
            <div id="micro-scene" class="scene-container">
                <h2 class="scene-title">微观视角：链式反应机理</h2>
                
                <div class="canvas-container">
                    <canvas id="micro-canvas"></canvas>
                </div>
                
                <div class="controls">
                    <button id="play-btn" class="btn">播放反应</button>
                    <button id="pause-btn" class="btn">暂停</button>
                    <button id="step-btn" class="btn">下一步</button>
                    <button id="reset-micro-btn" class="btn btn-danger">重置</button>
                    
                    <div class="control-group">
                        <div class="control-label">动画速度</div>
                        <div class="slider-container">
                            <input type="range" id="speed-slider" min="1" max="10" value="5">
                            <span id="speed-value" class="slider-value">5</span>
                        </div>
                    </div>
                </div>
                
                <div class="step-info">
                    <div class="step-title" id="step-title">准备开始</div>
                    <div class="step-equation" id="step-equation">H₂ + Cl₂ → 2HCl (光照)</div>
                    <p id="step-description">点击"播放反应"开始观察链式反应过程。</p>
                </div>
                
                <div class="legend">
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #9ACD32;"></div>
                        <div class="legend-label">氯原子 (Cl)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #D3D3D3;"></div>
                        <div class="legend-label">氢原子 (H)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #ADFF2F; border: 2px solid #FFFF00;"></div>
                        <div class="legend-label">氯自由基 (Cl·)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFFFFF; border: 2px solid #FFFF00;"></div>
                        <div class="legend-label">氢自由基 (H·)</div>
                    </div>
                    <div class="legend-item">
                        <div class="legend-color" style="background-color: #FFFF00;"></div>
                        <div class="legend-label">光子/能量</div>
                    </div>
                </div>
            </div>
        </main>
        
        <footer class="footer">
            <p>教学动画设计：氯气与氢气爆炸的链式反应机理 | 反应式：H₂ + Cl₂ → 2HCl (光照)</p>
            <p>提示：鼠标悬停在粒子或按钮上可查看详细信息</p>
        </footer>
    </div>

    <script>
        // 全局变量
        let currentScene = 'macro';
        let macroAnimationId = null;
        let microAnimationId = null;
        let isMicroPlaying = false;
        let microStep = 0;
        let animationSpeed = 1;
        
        // 场景切换
        document.getElementById('macro-btn').addEventListener('click', () => {
            switchScene('macro');
        });
        
        document.getElementById('micro-btn').addEventListener('click', () => {
            switchScene('micro');
        });
        
        function switchScene(scene) {
            currentScene = scene;
            
            // 更新按钮状态
            document.getElementById('macro-btn').classList.toggle('active', scene === 'macro');
            document.getElementById('micro-btn').classList.toggle('active', scene === 'micro');
            
            // 更新场景显示
            document.getElementById('macro-scene').classList.toggle('active', scene === 'macro');
            document.getElementById('micro-scene').classList.toggle('active', scene === 'micro');
            
            // 停止动画
            if (macroAnimationId) {
                cancelAnimationFrame(macroAnimationId);
                macroAnimationId = null;
            }
            
            if (microAnimationId) {
                cancelAnimationFrame(microAnimationId);
                microAnimationId = null;
            }
            
            // 启动新场景动画
            if (scene === 'macro') {
                initMacroScene();
                animateMacro();
            } else {
                initMicroScene();
                animateMicro();
            }
        }
        
        // ==================== 宏观场景 ====================
        const macroCanvas = document.getElementById('macro-canvas');
        const macroCtx = macroCanvas.getContext('2d');
        
        // 调整画布大小
        function resizeCanvas() {
            const container = macroCanvas.parentElement;
            macroCanvas.width = container.clientWidth;
            macroCanvas.height = container.clientHeight;
            
            const microCanvas = document.getElementById('micro-canvas');
            const microContainer = microCanvas.parentElement;
            microCanvas.width = microContainer.clientWidth;
            microCanvas.height = microContainer.clientHeight;
        }
        
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();
        
        // 宏观场景变量
        let macroState = 'ready'; // ready, exploding, aftermath
        let explosionProgress = 0;
        let explosionIntensity = 1;
        let h2Ratio = 5;
        let cl2Ratio = 5;
        let particles = [];
        let lightBeam = { y: -50, height: 0, active: false };
        let aftermathParticles = [];
        
        // 滑块事件
        document.getElementById('h2-slider').addEventListener('input', function() {
            h2Ratio = parseInt(this.value);
            document.getElementById('h2-value').textContent = h2Ratio;
            if (macroState === 'ready') {
                initMacroParticles();
            }
        });
        
        document.getElementById('cl2-slider').addEventListener('input', function() {
            cl2Ratio = parseInt(this.value);
            document.getElementById('cl2-value').textContent = cl2Ratio;
            if (macroState === 'ready') {
                initMacroParticles();
            }
        });
        
        document.getElementById('light-btn').addEventListener('click', startExplosion);
        document.getElementById('reset-macro-btn').addEventListener('click', resetMacro);
        
        // 初始化宏观场景
        function initMacroScene() {
            macroState = 'ready';
            explosionProgress = 0;
            lightBeam = { y: -50, height: 0, active: false };
            initMacroParticles();
            aftermathParticles = [];
        }
        
        // 初始化宏观粒子
        function initMacroParticles() {
            particles = [];
            const totalParticles = 80;
            const totalRatio = h2Ratio + cl2Ratio;
            
            for (let i = 0; i < totalParticles; i++) {
                // 根据比例决定粒子类型
                let type;
                if (i < totalParticles * (h2Ratio / totalRatio)) {
                    type = 'h2';
                } else {
                    type = 'cl2';
                }
                
                particles.push({
                    x: Math.random() * macroCanvas.width,
                    y: Math.random() * macroCanvas.height,
                    radius: type === 'h2' ? 4 : 6,
                    color: type === 'h2' ? 'rgba(211, 211, 211, 0.7)' : 'rgba(154, 205, 50, 0.8)',
                    type: type,
                    vx: (Math.random() - 0.5) * 0.5,
                    vy: (Math.random() - 0.5) * 0.5
                });
            }
        }
        
        // 开始爆炸
        function startExplosion() {
            if (macroState !== 'ready') return;
            
            // 计算爆炸强度（基于比例）
            const ratio = h2Ratio / cl2Ratio;
            explosionIntensity = Math.exp(-Math.pow(Math.log(ratio), 2)); // 在1:1时强度最大
            
            macroState = 'exploding';
            explosionProgress = 0;
            lightBeam.active = true;
            lightBeam.height = 0;
            
            // 更新按钮状态
            document.getElementById('light-btn').disabled = true;
            document.getElementById('light-btn').textContent = '爆炸中...';
        }
        
        // 重置宏观场景
        function resetMacro() {
            macroState = 'ready';
            explosionProgress = 0;
            lightBeam.active = false;
            lightBeam.height = 0;
            aftermathParticles = [];
            
            document.getElementById('light-btn').disabled = false;
            document.getElementById('light-btn').textContent = '启动光照';
            
            initMacroParticles();
        }
        
        // 绘制宏观场景
        function drawMacroScene() {
            // 清空画布
            macroCtx.clearRect(0, 0, macroCanvas.width, macroCanvas.height);
            
            // 绘制反应器
            macroCtx.strokeStyle = '#4A90E2';
            macroCtx.lineWidth = 3;
            macroCtx.strokeRect(50, 50, macroCanvas.width - 100, macroCanvas.height - 100);
            
            // 绘制光照光束
            if (lightBeam.active) {
                const gradient = macroCtx.createLinearGradient(
                    macroCanvas.width/2, lightBeam.y,
                    macroCanvas.width/2, lightBeam.y + lightBeam.height
                );
                gradient.addColorStop(0, 'rgba(255, 255, 200, 0.9)');
                gradient.addColorStop(1, 'rgba(255, 255, 100, 0.2)');
                
                macroCtx.fillStyle = gradient;
                macroCtx.fillRect(macroCanvas.width/2 - 30, lightBeam.y, 60, lightBeam.height);
            }
            
            // 绘制爆炸效果
            if (macroState === 'exploding') {
                const intensity = Math.sin(explosionProgress * Math.PI);
                const radius = intensity * 200 * explosionIntensity;
                
                // 爆炸光晕
                const gradient = macroCtx.createRadialGradient(
                    macroCanvas.width/2, macroCanvas.height/2, 0,
                    macroCanvas.width/2, macroCanvas.height/2, radius
                );
                gradient.addColorStop(0, 'rgba(255, 255, 255, 0.9)');
                gradient.addColorStop(0.5, 'rgba(255, 200, 100, 0.6)');
                gradient.addColorStop(1, 'rgba(255, 100, 0, 0)');
                
                macroCtx.fillStyle = gradient;
                macroCtx.fillRect(0, 0, macroCanvas.width, macroCanvas.height);
                
                // 震动效果
                const shake = intensity * 10;
                macroCtx.translate(Math.random() * shake - shake/2, Math.random() * shake - shake/2);
            }
            
            // 绘制粒子
            particles.forEach(particle => {
                macroCtx.beginPath();
                macroCtx.arc(particle.x, particle.y, particle.radius, 0, Math.PI * 2);
                macroCtx.fillStyle = particle.color;
                macroCtx.fill();
                
                // 更新位置
                if (macroState === 'ready') {
                    particle.x += particle.vx;
                    particle.y += particle.vy;
                    
                    // 边界反弹
                    if (particle.x < 60 || particle.x > macroCanvas.width - 60) particle.vx *= -1;
                    if (particle.y < 60 || particle.y > macroCanvas.height - 60) particle.vy *= -1;
                }
            });
            
            // 绘制爆炸后的白雾（HCl）
            if (macroState === 'aftermath') {
                aftermathParticles.forEach(particle => {
                    macroCtx.beginPath();
                    macroCtx.arc(particle.x, particle.y, particle.radius, 0, Math.PI * 2);
                    macroCtx.fillStyle = `rgba(255, 255, 255, ${particle.opacity})`;
                    macroCtx.fill();
                    
                    // 更新位置和透明度
                    particle.y += particle.vy;
                    particle.opacity *= 0.98;
                });
                
                // 移除消失的粒子
                aftermathParticles = aftermathParticles.filter(p => p.opacity > 0.05);
            }
            
            // 重置变换
            macroCtx.setTransform(1, 0, 0, 1, 0, 0);
            
            // 绘制场景标签
            macroCtx.fillStyle = '#ADFF2F';
            macroCtx.font = '16px Arial';
            macroCtx.fillText('反应器', 20, 30);
            
            if (macroState === 'ready') {
                macroCtx.fillStyle = '#9ACD32';
                macroCtx.fillText(`混合气体: H₂:Cl₂ = ${h2Ratio}:${cl2Ratio}`, macroCanvas.width/2 - 80, 30);
            }
        }
        
        // 更新宏观场景
        function updateMacroScene() {
            if (macroState === 'exploding') {
                explosionProgress += 0.02;
                
                // 更新光照光束
                if (lightBeam.height < macroCanvas.height) {
                    lightBeam.height += 10;
                }
                
                // 爆炸结束
                if (explosionProgress >= 1) {
                    macroState = 'aftermath';
                    
                    // 生成白雾粒子
                    for (let i = 0; i < 100; i++) {
                        aftermathParticles.push({
                            x: Math.random() * macroCanvas.width,
                            y: macroCanvas.height - 50,
                            radius: Math.random() * 8 + 2,
                            opacity: Math.random() * 0.5 + 0.3,
                            vy: -Math.random() * 0.5 - 0.2
                        });
                    }
                    
                    // 恢复按钮状态
                    setTimeout(() => {
                        document.getElementById('light-btn').disabled = false;
                        document.getElementById('light-btn').textContent = '启动光照';
                    }, 1000);
                }
            }
        }
        
        // 宏观动画循环
        function animateMacro() {
            updateMacroScene();
            drawMacroScene();
            macroAnimationId = requestAnimationFrame(animateMacro);
        }
        
        // ==================== 微观场景 ====================
        const microCanvas = document.getElementById('micro-canvas');
        const microCtx = microCanvas.getContext('2d');
        
        // 微观场景变量
        let microParticles = [];
        let chainReactionStep = 0; // 0: 准备, 1: 链引发, 2: 链增长1, 3: 链增长2, 4: 链终止
        let reactionProgress = 0;
        let photon = null;
        let freeRadicals = [];
        let reactionHistory = [];
        
        // 微观控制事件
        document.getElementById('play-btn').addEventListener('click', () => {
            isMicroPlaying = true;
            microStep = 0;
        });
        
        document.getElementById('pause-btn').addEventListener('click', () => {
            isMicroPlaying = false;
        });
        
        document.getElementById('step-btn').addEventListener('click', nextMicroStep);
        
        document.getElementById('reset-micro-btn').addEventListener('click', resetMicro);
        
        document.getElementById('speed-slider').addEventListener('input', function() {
            animationSpeed = parseInt(this.value) / 5;
            document.getElementById('speed-value').textContent = this.value;
        });
        
        // 初始化微观场景
        function initMicroScene() {
            microParticles = [];
            freeRadicals = [];
            reactionHistory = [];
            chainReactionStep = 0;
            reactionProgress = 0;
            photon = null;
            isMicroPlaying = false;
            microStep = 0;
            
            // 创建初始分子
            const centerX = microCanvas.width / 2;
            const centerY = microCanvas.height / 2;
            
            // 创建氯分子
            for (let i = 0; i < 4; i++) {
                const angle = (i / 4) * Math.PI * 2;
                const x = centerX + Math.cos(angle) * 120;
                const y = centerY + Math.sin(angle) * 120;
                
                microParticles.push({
                    type: 'Cl2',
                    x1: x - 15, y1: y,
                    x2: x + 15, y2: y,
                    color1: '#9ACD32',
                    color2: '#9ACD32',
                    bondStrength: 1,
                    isBondBreaking: false
                });
            }
            
            // 创建氢分子
            for (let i = 0; i < 4; i++) {
                const angle = (i / 4) * Math.PI * 2 + Math.PI/8;
                const x = centerX + Math.cos(angle) * 80;
                const y = centerY + Math.sin(angle) * 80;
                
                microParticles.push({
                    type: 'H2',
                    x1: x - 10, y1: y,
                    x2: x + 10, y2: y,
                    color1: '#D3D3D3',
                    color2: '#D3D3D3',
                    bondStrength: 1,
                    isBondBreaking: false
                });
            }
            
            updateStepInfo();
        }
        
        // 下一步
        function nextMicroStep() {
            if (!isMicroPlaying) {
                microStep++;
                if (microStep > 4) microStep = 0;
                
                chainReactionStep = microStep;
                reactionProgress = 0;
                
                // 执行步骤
                executeMicroStep();
            }
        }
        
        // 执行微观步骤
        function executeMicroStep() {
            switch (chainReactionStep) {
                case 1: // 链引发
                    photon = {
                        x: microCanvas.width / 2,
                        y: -20,
                        targetX: microCanvas.width / 2 + 120,
                        targetY: microCanvas.height / 2,
                        progress: 0
                    };
                    break;
                    
                case 2: // 链增长1: Cl· + H2 → HCl + H·
                    if (freeRadicals.length > 0) {
                        const clRadical = freeRadicals.find(r => r.type === 'Cl·');
                        if (clRadical) {
                            // 寻找一个H2分子
                            const h2Molecule = microParticles.find(p => p.type === 'H2' && !p.isBondBreaking);
                            if (h2Molecule) {
                                h2Molecule.isBondBreaking = true;
                                h2Molecule.breakingFor = 'Cl·';
                                h2Molecule.breakerX = clRadical.x;
                                h2Molecule.breakerY = clRadical.y;
                            }
                        }
                    }
                    break;
                    
                case 3: // 链增长2: H· + Cl2 → HCl + Cl·
                    const hRadical = freeRadicals.find(r => r.type === 'H·');
                    if (hRadical) {
                        // 寻找一个Cl2分子
                        const cl2Molecule = microParticles.find(p => p.type === 'Cl2' && !p.isBondBreaking);
                        if (cl2Molecule) {
                            cl2Molecule.isBondBreaking = true;
                            cl2Molecule.breakingFor = 'H·';
                            cl2Molecule.breakerX = hRadical.x;
                            cl2Molecule.breakerY = hRadical.y;
                        }
                    }
                    break;
                    
                case 4: // 链终止: Cl· + Cl· → Cl2
                    // 随机选择两个氯自由基结合
                    const clRadicals = freeRadicals.filter(r => r.type === 'Cl·');
                    if (clRadicals.length >= 2) {
                        clRadicals[0].combiningWith = clRadicals[1];
                        clRadicals[1].combiningWith = clRadicals[0];
                    }
                    break;
            }
            
            updateStepInfo();
        }
        
        // 更新步骤信息
        function updateStepInfo() {
            const stepTitle = document.getElementById('step-title');
            const stepEquation = document.getElementById('step-equation');
            const stepDescription = document.getElementById('step-description');
            
            switch (chainReactionStep) {
                case 0:
                    stepTitle.textContent = '准备开始';
                    stepEquation.textContent = 'H₂ + Cl₂ → 2HCl (光照)';
                    stepDescription.textContent = '初始状态：氢分子(H₂)和氯分子(Cl₂)混合。点击"播放反应"开始观察链式反应过程。';
                    break;
                    
                case 1:
                    stepTitle.textContent = '链引发 (光子激发)';
                    stepEquation.textContent = 'Cl₂ + hν → 2Cl·';
                    stepDescription.textContent = '光子(hν)携带能量撞击氯分子，使Cl-Cl键断裂，生成两个高活性的氯自由基(Cl·)。';
                    break;
                    
                case 2:
                    stepTitle.textContent = '链增长 (步骤1)';
                    stepEquation.textContent = 'Cl· + H₂ → HCl + H·';
                    stepDescription.textContent = '氯自由基(Cl·)攻击氢分子，夺取一个氢原子形成HCl，同时生成一个新的氢自由基(H·)。';
                    break;
                    
                case 3:
                    stepTitle.textContent = '链增长 (步骤2)';
                    stepEquation.textContent = 'H· + Cl₂ → HCl + Cl·';
                    stepDescription.textContent = '氢自由基(H·)攻击氯分子，夺取一个氯原子形成HCl，同时生成一个新的氯自由基(Cl·)。';
                    break;
                    
                case 4:
                    stepTitle.textContent = '链终止';
                    stepEquation.textContent = 'Cl· + Cl· → Cl₂ 或 H· + Cl· → HCl 或 H· + H· → H₂';
                    stepDescription.textContent = '两个自由基相遇结合成稳定分子，反应链终止。';
                    break;
            }
        }
        
        // 重置微观场景
        function resetMicro() {
            initMicroScene();
            isMicroPlaying = false;
        }
        
        // 绘制微观场景
        function drawMicroScene() {
            // 清空画布
            microCtx.clearRect(0, 0, microCanvas.width, microCanvas.height);
            
            // 绘制背景网格
            microCtx.strokeStyle = 'rgba(74, 144, 226, 0.1)';
            microCtx.lineWidth = 1;
            const gridSize = 40;
            
            for (let x = 0; x < microCanvas.width; x += gridSize) {
                microCtx.beginPath();
                microCtx.moveTo(x, 0);
                microCtx.lineTo(x, microCanvas.height);
                microCtx.stroke();
            }
            
            for (let y = 0; y < microCanvas.height; y += gridSize) {
                microCtx.beginPath();
                microCtx.moveTo(0, y);
                microCtx.lineTo(microCanvas.width, y);
                microCtx.stroke();
            }
            
            // 绘制光子
            if (photon) {
                microCtx.beginPath();
                microCtx.arc(photon.x, photon.y, 8, 0, Math.PI * 2);
                microCtx.fillStyle = '#FFFF00';
                microCtx.fill();
                
                // 光晕效果
                microCtx.beginPath();
                microCtx.arc(photon.x, photon.y, 15, 0, Math.PI * 2);
                const gradient = microCtx.createRadialGradient(
                    photon.x, photon.y, 8,
                    photon.x, photon.y, 15
                );
                gradient.addColorStop(0, 'rgba(255, 255, 0, 0.8)');
                gradient.addColorStop(1, 'rgba(255, 255, 0, 0)');
                microCtx.fillStyle = gradient;
                microCtx.fill();
            }
            
            // 绘制分子
            microParticles.forEach(particle => {
                // 绘制化学键
                microCtx.strokeStyle = particle.isBondBreaking ? 
                    `rgba(255, 100, 100, ${particle.bondStrength})` : 'rgba(170, 170, 170, 0.8)';
                microCtx.lineWidth = particle.isBondBreaking ? 4 : 3;
                microCtx.beginPath();
                microCtx.moveTo(particle.x1, particle.y1);
                microCtx.lineTo(particle.x2, particle.y2);
                microCtx.stroke();
                
                // 绘制原子1
                microCtx.beginPath();
                microCtx.arc(particle.x1, particle.y1, 12, 0, Math.PI * 2);
                microCtx.fillStyle = particle.color1;
                microCtx.fill();
                
                // 绘制原子2
                microCtx.beginPath();
                microCtx.arc(particle.x2, particle.y2, 12, 0, Math.PI * 2);
                microCtx.fillStyle = particle.color2;
                microCtx.fill();
                
                // 如果是自由基，绘制高亮外圈
                if (particle.color1.includes('radical')) {
                    microCtx.strokeStyle = '#FFFF00';
                    microCtx.lineWidth = 2;
                    microCtx.beginPath();
                    microCtx.arc(particle.x1, particle.y1, 15, 0, Math.P
<!--检测到代码截断，自动续写中...-->
I*2);
                    microCtx.stroke();
                }
                
                if (particle.color2.includes('radical')) {
                    microCtx.strokeStyle = '#FFFF00';
                    microCtx.lineWidth = 2;
                    microCtx.beginPath();
                    microCtx.arc(particle.x2, particle.y2, 15, 0, Math.PI*2);
                    microCtx.stroke();
                }
                
                // 绘制分子标签
                microCtx.fillStyle = '#ADFF2F';
                microCtx.font = '12px Arial';
                const labelX = (particle.x1 + particle.x2) / 2;
                const labelY = (particle.y1 + particle.y2) / 2;
                microCtx.fillText(particle.type, labelX - 10, labelY - 15);
            });
            
            // 绘制自由基
            freeRadicals.forEach(radical => {
                // 绘制自由基球体
                microCtx.beginPath();
                microCtx.arc(radical.x, radical.y, 10, 0, Math.PI * 2);
                microCtx.fillStyle = radical.type === 'Cl·' ? '#ADFF2F' : '#FFFFFF';
                microCtx.fill();
                
                // 绘制自由基高亮外圈
                microCtx.strokeStyle = '#FFFF00';
                microCtx.lineWidth = 3;
                microCtx.beginPath();
                microCtx.arc(radical.x, radical.y, 13, 0, Math.PI * 2);
                microCtx.stroke();
                
                // 绘制自由基标签
                microCtx.fillStyle = '#FFFF00';
                microCtx.font = 'bold 11px Arial';
                microCtx.fillText(radical.type, radical.x - 8, radical.y - 15);
                
                // 绘制自由基运动轨迹（如果正在移动）
                if (radical.targetX !== undefined) {
                    microCtx.strokeStyle = 'rgba(255, 255, 0, 0.5)';
                    microCtx.lineWidth = 2;
                    microCtx.setLineDash([5, 5]);
                    microCtx.beginPath();
                    microCtx.moveTo(radical.originX, radical.originY);
                    microCtx.lineTo(radical.targetX, radical.targetY);
                    microCtx.stroke();
                    microCtx.setLineDash([]);
                }
            });
            
            // 绘制反应历史（已生成的HCl分子）
            reactionHistory.forEach(hcl => {
                // 绘制HCl化学键
                microCtx.strokeStyle = 'rgba(255, 255, 255, 0.7)';
                microCtx.lineWidth = 2;
                microCtx.beginPath();
                microCtx.moveTo(hcl.x1, hcl.y1);
                microCtx.lineTo(hcl.x2, hcl.y2);
                microCtx.stroke();
                
                // 绘制Cl原子
                microCtx.beginPath();
                microCtx.arc(hcl.x1, hcl.y1, 10, 0, Math.PI * 2);
                microCtx.fillStyle = '#9ACD32';
                microCtx.fill();
                
                // 绘制H原子
                microCtx.beginPath();
                microCtx.arc(hcl.x2, hcl.y2, 8, 0, Math.PI * 2);
                microCtx.fillStyle = '#D3D3D3';
                microCtx.fill();
                
                // 绘制HCl标签
                microCtx.fillStyle = '#FFFFFF';
                microCtx.font = '12px Arial';
                microCtx.fillText('HCl', (hcl.x1 + hcl.x2) / 2 - 10, (hcl.y1 + hcl.y2) / 2 - 15);
            });
            
            // 绘制当前步骤高亮框
            if (chainReactionStep > 0) {
                microCtx.strokeStyle = '#ADFF2F';
                microCtx.lineWidth = 3;
                microCtx.setLineDash([10, 5]);
                microCtx.strokeRect(20, 20, microCanvas.width - 40, microCanvas.height - 40);
                microCtx.setLineDash([]);
                
                // 绘制步骤标题
                microCtx.fillStyle = '#ADFF2F';
                microCtx.font = 'bold 16px Arial';
                microCtx.fillText(`当前步骤: ${document.getElementById('step-title').textContent}`, 30, 40);
            }
        }
        
        // 更新微观场景
        function updateMicroScene() {
            if (!isMicroPlaying && microStep === 0) return;
            
            // 自动推进步骤
            if (isMicroPlaying) {
                reactionProgress += 0.02 * animationSpeed;
                
                if (reactionProgress >= 1) {
                    reactionProgress = 0;
                    microStep++;
                    if (microStep > 4) {
                        microStep = 0;
                        isMicroPlaying = false;
                    }
                    chainReactionStep = microStep;
                    executeMicroStep();
                }
            }
            
            // 更新光子位置
            if (photon) {
                photon.progress += 0.03 * animationSpeed;
                photon.x = photon.x + (photon.targetX - photon.x) * 0.1;
                photon.y = photon.y + (photon.targetY - photon.y) * 0.1;
                
                // 光子击中氯分子
                if (photon.progress >= 1) {
                    // 找到被击中的氯分子
                    const cl2Molecule = microParticles.find(p => p.type === 'Cl2');
                    if (cl2Molecule) {
                        cl2Molecule.isBondBreaking = true;
                        cl2Molecule.bondStrength = Math.max(0, cl2Molecule.bondStrength - 0.05 * animationSpeed);
                        
                        // 化学键完全断裂，生成自由基
                        if (cl2Molecule.bondStrength <= 0) {
                            // 移除分子
                            const index = microParticles.indexOf(cl2Molecule);
                            microParticles.splice(index, 1);
                            
                            // 创建两个氯自由基
                            freeRadicals.push({
                                type: 'Cl·',
                                x: cl2Molecule.x1,
                                y: cl2Molecule.y1,
                                originX: cl2Molecule.x1,
                                originY: cl2Molecule.y1,
                                targetX: cl2Molecule.x1 + 100,
                                targetY: cl2Molecule.y1 - 50
                            });
                            
                            freeRadicals.push({
                                type: 'Cl·',
                                x: cl2Molecule.x2,
                                y: cl2Molecule.y2,
                                originX: cl2Molecule.x2,
                                originY: cl2Molecule.y2,
                                targetX: cl2Molecule.x2 - 100,
                                targetY: cl2Molecule.y2 + 50
                            });
                            
                            photon = null;
                        }
                    }
                }
            }
            
            // 更新自由基位置
            freeRadicals.forEach(radical => {
                if (radical.targetX !== undefined) {
                    radical.x += (radical.targetX - radical.x) * 0.05 * animationSpeed;
                    radical.y += (radical.targetY - radical.y) * 0.05 * animationSpeed;
                    
                    // 如果自由基到达目标，清除目标
                    if (Math.abs(radical.x - radical.targetX) < 5 && Math.abs(radical.y - radical.targetY) < 5) {
                        radical.targetX = undefined;
                        radical.targetY = undefined;
                    }
                }
                
                // 更新结合过程
                if (radical.combiningWith) {
                    const target = radical.combiningWith;
                    radical.x += (target.x - radical.x) * 0.08 * animationSpeed;
                    radical.y += (target.y - radical.y) * 0.08 * animationSpeed;
                    
                    // 如果两个自由基足够接近，结合成分子
                    if (Math.abs(radical.x - target.x) < 15 && Math.abs(radical.y - target.y) < 15) {
                        // 移除自由基
                        const index1 = freeRadicals.indexOf(radical);
                        const index2 = freeRadicals.indexOf(target);
                        freeRadicals.splice(Math.max(index1, index2), 1);
                        freeRadicals.splice(Math.min(index1, index2), 1);
                        
                        // 创建新分子
                        if (radical.type === 'Cl·' && target.type === 'Cl·') {
                            microParticles.push({
                                type: 'Cl2',
                                x1: radical.x - 15,
                                y1: radical.y,
                                x2: target.x + 15,
                                y2: target.y,
                                color1: '#9ACD32',
                                color2: '#9ACD32',
                                bondStrength: 1,
                                isBondBreaking: false
                            });
                        }
                    }
                }
            });
            
            // 更新断裂中的化学键
            microParticles.forEach(particle => {
                if (particle.isBondBreaking) {
                    particle.bondStrength = Math.max(0, particle.bondStrength - 0.04 * animationSpeed);
                    
                    // 化学键完全断裂
                    if (particle.bondStrength <= 0) {
                        // 根据断裂类型处理
                        if (particle.breakingFor === 'Cl·') {
                            // Cl· + H2 → HCl + H·
                            const clRadical = freeRadicals.find(r => r.type === 'Cl·' && 
                                Math.abs(r.x - particle.breakerX) < 20 && 
                                Math.abs(r.y - particle.breakerY) < 20);
                            
                            if (clRadical) {
                                // 移除氯自由基
                                const radicalIndex = freeRadicals.indexOf(clRadical);
                                freeRadicals.splice(radicalIndex, 1);
                                
                                // 创建HCl分子
                                reactionHistory.push({
                                    x1: clRadical.x,
                                    y1: clRadical.y,
                                    x2: particle.x1,
                                    y2: particle.y1,
                                    type: 'HCl'
                                });
                                
                                // 创建氢自由基
                                freeRadicals.push({
                                    type: 'H·',
                                    x: particle.x2,
                                    y: particle.y2,
                                    originX: particle.x2,
                                    originY: particle.y2,
                                    targetX: particle.x2 + 80,
                                    targetY: particle.y2 + 80
                                });
                            }
                        } else if (particle.breakingFor === 'H·') {
                            // H· + Cl2 → HCl + Cl·
                            const hRadical = freeRadicals.find(r => r.type === 'H·' && 
                                Math.abs(r.x - particle.breakerX) < 20 && 
                                Math.abs(r.y - particle.breakerY) < 20);
                            
                            if (hRadical) {
                                // 移除氢自由基
                                const radicalIndex = freeRadicals.indexOf(hRadical);
                                freeRadicals.splice(radicalIndex, 1);
                                
                                // 创建HCl分子
                                reactionHistory.push({
                                    x1: particle.x1,
                                    y1: particle.y1,
                                    x2: hRadical.x,
                                    y2: hRadical.y,
                                    type: 'HCl'
                                });
                                
                                // 创建氯自由基
                                freeRadicals.push({
                                    type: 'Cl·',
                                    x: particle.x2,
                                    y: particle.y2,
                                    originX: particle.x2,
                                    originY: particle.y2,
                                    targetX: particle.x2 - 80,
                                    targetY: particle.y2 - 80
                                });
                            }
                        }
                        
                        // 移除断裂的分子
                        const particleIndex = microParticles.indexOf(particle);
                        microParticles.splice(particleIndex, 1);
                    }
                }
            });
        }
        
        // 微观动画循环
        function animateMicro() {
            updateMicroScene();
            drawMicroScene();
            microAnimationId = requestAnimationFrame(animateMicro);
        }
        
        // 初始化
        function init() {
            initMacroScene();
            initMicroScene();
            animateMacro();
            animateMicro();
            
            // 添加工具提示
            addTooltips();
        }
        
        // 添加工具提示
        function addTooltips() {
            // 为按钮添加简单提示
            const buttons = document.querySelectorAll('.btn, .scene-btn');
            buttons.forEach(btn => {
                btn.addEventListener('mouseenter', function() {
                    const originalTitle = this.getAttribute('data-original-title') || this.title;
                    if (originalTitle) {
                        // 可以在这里实现更复杂的工具提示
                        console.log(originalTitle);
                    }
                });
            });
            
            // 为滑块添加实时值显示
            const sliders = document.querySelectorAll('input[type="range"]');
            sliders.forEach(slider => {
                slider.addEventListener('input', function() {
                    const valueDisplay = this.nextElementSibling;
                    if (valueDisplay && valueDisplay.classList.contains('slider-value')) {
                        valueDisplay.textContent = this.value;
                    }
                });
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', init);
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 氯气与氢气爆炸反应交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过直观的视觉呈现和交互操作，帮助您深入理解氯气与氢气在光照条件下发生爆炸反应的宏观现象及其微观链式反应机理。无论您是教师、学生还是化学爱好者，都能通过本动画获得深刻的学习体验。

---

### 一、功能说明

本动画包含两个核心场景，分别从宏观和微观两个层面展示反应过程：

1. **宏观实验场景**：模拟实验室中氯气与氢气混合气体在光照下发生爆炸的实验现象。
2. **微观视角场景**：展示爆炸反应背后的微观链式反应机理，包括自由基的生成、传递和终止过程。

两个场景可随时切换，让您自由地在宏观现象与微观本质之间建立联系。

---

### 二、主要功能

#### 宏观实验场景功能：
- **比例调节**：通过滑块调整氢气(H₂)与氯气(Cl₂)的混合比例（1:1至10:10）
- **光照触发**：点击“启动光照”按钮模拟紫外光照射，触发爆炸反应
- **爆炸效果**：根据气体比例呈现不同强度的爆炸动画和震动效果
- **产物观察**：爆炸后观察氯化氢(HCl)白雾的生成与扩散
- **实验重置**：随时重置实验，重新调整参数进行探索

#### 微观视角场景功能：
- **反应控制**：通过“播放反应”、“暂停”、“下一步”按钮控制反应进程
- **步骤分解**：将链式反应分解为四个清晰步骤：
  1. 链引发（光子激发）
  2. 链增长第一步（Cl·攻击H₂）
  3. 链增长第二步（H·攻击Cl₂）
  4. 链终止（自由基结合）
- **速度调节**：通过滑块调整动画播放速度（1-10级）
- **信息提示**：实时显示当前步骤的化学方程式和反应机理说明
- **视觉追踪**：通过颜色编码和轨迹线追踪自由基的传递路径

---

### 三、设计特色

1. **科学的视觉编码系统**：
   - 氯原子/分子：黄绿色（#9ACD32），贴近真实氯气颜色
   - 氢原子/分子：浅灰色（#D3D3D3），表示无色气体
   - 自由基：在原子基础上添加亮黄色高亮外圈
   - 光子/能量：亮黄色光点带光晕效果
   - 化学键：灰色实线，断裂时变为红色并逐渐消失

2. **符合认知规律的教学设计**：
   - 从宏观现象入手，激发学习兴趣
   - 逐步分解复杂过程，降低认知负荷
   - 通过交互操作促进主动探索
   - 提供即时反馈，强化概念理解

3. **专业的交互体验**：
   - 流畅的动画过渡和物理模拟
   - 直观的控制面板和参数调节
   - 响应式设计，适配不同设备
   - 深色背景增强视觉对比度

---

### 四、教学要点

#### 核心概念强调：
1. **反应条件**：强调“光照”是启动反应的必要条件，提供足够能量使氯分子均裂
2. **自由基特性**：通过视觉设计突出自由基的高反应活性（高亮外圈）
3. **链式特征**：展示一个光子如何引发成千上万个分子反应，解释爆炸的剧烈性
4. **能量变化**：通过爆炸光效和粒子运动速度体现反应的能量释放

#### 关键反应步骤：
1. **链引发**：Cl₂ + hν → 2Cl·
   - 光子能量打断Cl-Cl键
   - 生成两个高活性氯自由基

2. **链增长**：
   - Cl· + H₂ → HCl + H·
   - H· + Cl₂ → HCl + Cl·
   - 循环往复，形成反应链

3. **链终止**：
   - Cl· + Cl· → Cl₂
   - H· + Cl· → HCl
   - H· + H· → H₂
   - 自由基消耗，反应停止

#### 安全与条件：
- 通过比例调节展示爆炸极限概念
- 强调实际实验的安全注意事项

---

### 五、使用建议

#### 对于教师：
1. **课堂演示**：
   - 先展示宏观爆炸现象，提出问题：“为什么光照会引发爆炸？”
   - 切换到微观视角，逐步讲解链式反应机理
   - 使用“下一步”功能分步讲解，配合板书或PPT

2. **探究式学习**：
   - 让学生自主探索不同气体比例对爆炸的影响
   - 提出问题：“为什么1:1比例时爆炸最剧烈？”
   - 引导学生观察自由基的“链式”传递过程

3. **概念巩固**：
   - 在讲解后让学生操作动画，复述反应步骤
   - 使用“暂停”功能在关键步骤提问
   - 对比链式反应与其他类型反应的区别

#### 对于学生：
1. **自主学习**：
   - 先观看完整反应过程，建立整体认识
   - 使用“下一步”功能仔细研究每个步骤
   - 调节动画速度，仔细观察自由基的运动

2. **概念理解**：
   - 关注自由基的“高亮外圈”视觉提示
   - 追踪一个自由基的完整“生命周期”
   - 理解“一个光子引发大量反应”的放大效应

3. **复习巩固**：
   - 在不看提示的情况下复述反应步骤
   - 解释为什么反应需要光照启动
   - 描述链终止的几种可能方式

#### 最佳实践流程：
1. **初次接触**：在宏观场景中，尝试不同比例，观察爆炸现象
2. **深入探究**：切换到微观场景，使用“播放反应”观看完整过程
3. **细节学习**：使用“下一步”功能，逐步研究每个反应步骤
4. **参数实验**：调节动画速度，仔细观察快速过程
5. **知识应用**：关闭提示，尝试解释观察到的现象
6. **拓展思考**：思考实际实验中的安全措施和条件控制

---

### 技术支持与反馈

本动画基于HTML5 Canvas技术开发，支持现代主流浏览器。如遇到显示或操作问题，请确保：
- 使用Chrome、Firefox、Edge等最新版本浏览器
- 启用JavaScript功能
- 在良好网络环境下加载

我们致力于持续改进教学工具的质量和效果。如果您有改进建议或发现任何问题，欢迎通过适当渠道反馈。您的意见将帮助我们创造更好的学习体验！

---

**祝您探索愉快，在化学的微观世界中收获知识与灵感！**

*“一个光子的能量，足以点燃链式反应的火焰；一次交互的探索，足以点亮科学思维的明灯。”*