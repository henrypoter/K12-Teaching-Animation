# 需求：钠与水反应（剧烈+放出氢气+微观：2Na + 2H₂O → 2NaOH + H₂↑）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的主要用户是初中或高中化学初学者。他们的核心需求是：
1.  **理解宏观现象**：直观地看到钠与水反应的剧烈现象（浮、熔、游、响、红），并理解这些现象背后的原因。
2.  **建立微观联系**：将宏观现象与看不见的微观化学反应（原子、分子、离子）和化学方程式联系起来，这是化学学习的核心难点。
3.  **掌握核心知识**：明确反应物、生成物、反应条件，并能正确书写和配平化学方程式。
4.  **激发学习兴趣**：通过生动、直观、可交互的动画，打破对化学反应的抽象和枯燥印象，提升学习动机。

#### 教学设计思路
动画将遵循“宏观现象 → 微观解释 → 符号表达”的认知规律，层层递进。

*   **核心概念**：
    *   **宏观**：钠的物理性质（银白色、密度比水小、熔点低）、反应现象（浮、熔、游、响、生成碱性物质使酚酞变红）。
    *   **微观**：钠原子（Na）失去电子成为钠离子（Na⁺），水分子（H₂O）中的氢原子获得电子结合成氢气分子（H₂），同时生成氢氧根离子（OH⁻）。
    *   **符号**：化学方程式 `2Na + 2H₂O → 2NaOH + H₂↑` 及其配平意义。

*   **认知规律与流程设计**：
    1.  **情境导入**：展示实验装置（烧杯、水、酚酞），吸引注意力。
    2.  **现象观察**：播放钠与水反应的宏观动画，突出所有关键现象，并允许用户控制播放速度或重复观看。
    3.  **现象分析**：通过交互式标签或点击，逐一解释每个现象（如“浮”是因为密度小，“熔”是因为反应放热且钠熔点低）。
    4.  **微观探秘**：镜头拉入微观世界，动态展示反应物分子/原子如何断裂旧键、形成新键，生成新分子/离子的全过程。这是动画的核心价值所在。
    5.  **符号总结**：将微观粒子变化与化学方程式对应起来，动态生成方程式，并解释“2”的配平原因（电荷、原子守恒）。
    6.  **整合回顾**：提供一个可交互的总结图，将宏观、微观、符号三者并列，让用户点击触发不同层面的演示。

*   **交互设计**：
    *   **控制台**：提供“播放/暂停/重置”按钮，让用户掌控学习节奏。
    *   **步骤选择**：通过标签页或进度条，允许用户直接跳转到“宏观现象”、“微观过程”或“化学方程式”任一环节。
    *   **点击探索**：在宏观画面中，点击“钠块”、“气泡”、“红色区域”等，弹出文字解释。在微观画面中，点击原子或化学键，高亮显示并说明其变化。
    *   **拖拽配对**：在总结环节，可将“宏观现象”、“微观粒子”、“化学式”进行拖拽配对，以巩固理解。

*   **视觉呈现**：
    *   **风格**：采用简洁、扁平化或轻度拟物化的卡通风格，确保科学性的同时不失亲和力。
    *   **宏观场景**：烧杯、水、钠块、气泡、飞溅效果等要生动形象。
    *   **微观场景**：原子（Na、H、O）用不同颜色和大小的球体表示，化学键用弹簧或棍棒表示，断裂和形成过程要有清晰的动态效果。电子转移可用光点或流动轨迹表示。
    *   **信息分层**：通过放大、聚焦、淡出背景等方式，引导用户视线，避免信息过载。

#### 配色方案选择
*   **主色调**：采用科技蓝（`#3498db`）作为背景或主界面色，传达科学和理性的感觉。
*   **关键元素色**：
    *   水：半透明的浅蓝色（`#87CEEB`）。
    *   钠块：具有金属光泽的银灰色（线性渐变，`#E0E0E0` 到 `#B0B0B0`）。
    *   氢气气泡：无色（用轮廓线表示）或极浅的灰色。
    *   酚酞变红：醒目的粉红色（`#FF6B8B`）。
*   **微观原子色**：
    *   钠原子（Na）：保持银灰色（`#C0C0C0`），与宏观对应。
    *   氢原子（H）：浅灰色（`#D3D3D3`）或白色。
    *   氧原子（O）：红色（`#E74C3C`），这是化学中常见的约定色。
    *   电子/化学键：亮黄色（`#F1C40F`）或亮蓝色，用于高亮动态过程。
*   **界面/文字**：深灰色（`#2C3E50`）用于主要文字，白色用于对比。

#### 交互功能列表
1.  **主控制台**：播放、暂停、重置动画。
2.  **场景切换器**：在“宏观实验”、“微观反应”、“方程式”三个主要场景间切换。
3.  **宏观现象交互**：
    *   点击钠块：显示其物理性质（密度、熔点）。
    *   点击气泡：显示“氢气”。
    *   点击红色区域：显示“生成NaOH，溶液呈碱性”。
    *   悬停提示：对“浮、熔、游、响”进行文字提示。
4.  **微观过程交互**：
    *   播放/暂停粒子动画。
    *   点击特定原子或键：高亮并显示其名称及在反应中的变化（如“Na → Na⁺ + e⁻”）。
    *   分步演示按钮：将反应分解为“钠原子失去电子”、“水分子解离”、“氢离子得电子生成氢气”、“钠离子与氢氧根离子结合”等步骤。
5.  **化学方程式模块**：
    *   动态生成：伴随微观动画，粒子逐步“飞入”组成方程式。
    *   配平说明：点击方程式系数“2”，显示配平原因（原子数守恒）。
6.  **知识挑战/回顾游戏**（可选进阶）：
    *   拖拽题：将现象描述、粒子图片、化学式术语拖到正确分类（宏观/微观/符号）下。
    *   排序题：将反应过程的微观步骤图片进行正确排序。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>钠与水反应教学动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a2980, #26d0ce);
            color: #2C3E50;
            min-height: 100vh;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            overflow: hidden;
            padding: 25px;
            margin-bottom: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 3px solid #3498db;
        }

        h1 {
            color: #2C3E50;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #3498db;
            font-size: 1.2rem;
            font-weight: normal;
        }

        .scene-selector {
            display: flex;
            justify-content: center;
            margin-bottom: 25px;
            background: #f8f9fa;
            border-radius: 12px;
            padding: 8px;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.1);
        }

        .scene-btn {
            padding: 12px 25px;
            margin: 0 5px;
            border: none;
            border-radius: 8px;
            background: #ecf0f1;
            color: #2C3E50;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            flex: 1;
            max-width: 200px;
        }

        .scene-btn:hover {
            background: #d5dbdb;
            transform: translateY(-2px);
        }

        .scene-btn.active {
            background: #3498db;
            color: white;
            box-shadow: 0 4px 8px rgba(52, 152, 219, 0.3);
        }

        .animation-container {
            position: relative;
            width: 100%;
            height: 500px;
            background: linear-gradient(to bottom, #e3f2fd, #f3e5f5);
            border-radius: 15px;
            overflow: hidden;
            margin-bottom: 25px;
            border: 3px solid #3498db;
        }

        #animation-canvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .controls {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 25px;
        }

        .control-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 8px;
            background: #2ecc71;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-width: 120px;
        }

        .control-btn:hover {
            background: #27ae60;
            transform: translateY(-2px);
        }

        .control-btn.reset {
            background: #e74c3c;
        }

        .control-btn.reset:hover {
            background: #c0392b;
        }

        .control-btn:disabled {
            background: #95a5a6;
            cursor: not-allowed;
            transform: none;
        }

        .info-panel {
            background: #f8f9fa;
            border-radius: 15px;
            padding: 20px;
            margin-top: 20px;
            border-left: 5px solid #3498db;
        }

        .info-title {
            color: #2C3E50;
            font-size: 1.4rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .info-content {
            line-height: 1.6;
            color: #34495e;
        }

        .equation {
            text-align: center;
            font-size: 2rem;
            margin: 20px 0;
            padding: 15px;
            background: #e8f4fc;
            border-radius: 10px;
            border: 2px dashed #3498db;
        }

        .equation span {
            padding: 5px 10px;
            margin: 0 5px;
            border-radius: 5px;
        }

        .highlight {
            background-color: #fff3cd;
            color: #856404;
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: bold;
        }

        .micro-hint {
            position: absolute;
            top: 15px;
            right: 15px;
            background: rgba(255, 255, 255, 0.9);
            padding: 10px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.1);
            border-left: 4px solid #9b59b6;
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
            gap: 8px;
        }

        .legend-color {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            border: 2px solid rgba(0,0,0,0.1);
        }

        .phenomenon-tag {
            position: absolute;
            background: rgba(52, 152, 219, 0.9);
            color: white;
            padding: 8px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.3s ease;
            z-index: 10;
        }

        .phenomenon-tag:hover {
            background: rgba(41, 128, 185, 0.95);
            transform: scale(1.05);
        }

        .tooltip {
            position: absolute;
            background: rgba(0, 0, 0, 0.85);
            color: white;
            padding: 12px 15px;
            border-radius: 8px;
            font-size: 0.9rem;
            max-width: 250px;
            z-index: 100;
            pointer-events: none;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .tooltip.show {
            opacity: 1;
        }

        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .animation-container {
                height: 400px;
            }
            
            .controls {
                flex-wrap: wrap;
            }
            
            .scene-selector {
                flex-direction: column;
                align-items: center;
            }
            
            .scene-btn {
                width: 100%;
                margin-bottom: 5px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>钠与水反应教学动画</h1>
            <p class="subtitle">宏观现象 · 微观过程 · 化学方程式</p>
        </header>

        <div class="scene-selector">
            <button class="scene-btn active" data-scene="macro">宏观现象</button>
            <button class="scene-btn" data-scene="micro">微观过程</button>
            <button class="scene-btn" data-scene="equation">化学方程式</button>
        </div>

        <div class="animation-container">
            <canvas id="animation-canvas"></canvas>
            <div class="micro-hint" style="display: none;">
                💡 点击原子或化学键查看详细信息
            </div>
        </div>

        <div class="controls">
            <button class="control-btn" id="play-btn">
                <span>▶</span> 播放
            </button>
            <button class="control-btn" id="pause-btn" disabled>
                <span>⏸</span> 暂停
            </button>
            <button class="control-btn reset" id="reset-btn">
                <span>↺</span> 重置
            </button>
        </div>

        <div class="equation">
            <span style="color: #C0C0C0; background: #f0f0f0;">2Na</span> + 
            <span style="color: #3498db; background: #e8f4fc;">2H₂O</span> → 
            <span style="color: #2ecc71; background: #eafaf1;">2NaOH</span> + 
            <span style="color: #9b59b6; background: #f5eef8;">H₂↑</span>
        </div>

        <div class="info-panel">
            <h3 class="info-title">📚 当前知识点</h3>
            <div class="info-content" id="info-text">
                点击上方按钮选择不同场景，然后点击播放按钮开始动画。在微观场景中，您可以点击原子或化学键查看详细信息。
            </div>
        </div>

        <div class="legend">
            <div class="legend-item">
                <div class="legend-color" style="background: #C0C0C0;"></div>
                <span>钠原子 (Na)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background: #D3D3D3;"></div>
                <span>氢原子 (H)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background: #E74C3C;"></div>
                <span>氧原子 (O)</span>
            </div>
            <div class="legend-item">
                <div class="legend-color" style="background: #F1C40F; border: 2px solid #d4ac0d;"></div>
                <span>电子/化学键</span>
            </div>
        </div>
    </div>

    <script>
        // 获取Canvas和上下文
        const canvas = document.getElementById('animation-canvas');
        const ctx = canvas.getContext('2d');
        
        // 设置Canvas尺寸
        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }
        
        resizeCanvas();
        window.addEventListener('resize', resizeCanvas);
        
        // 动画状态
        let currentScene = 'macro'; // macro, micro, equation
        let animationPlaying = false;
        let animationTime = 0;
        let animationSpeed = 1;
        
        // 场景按钮事件
        document.querySelectorAll('.scene-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                document.querySelectorAll('.scene-btn').forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                currentScene = btn.dataset.scene;
                animationTime = 0;
                
                // 显示/隐藏微观提示
                document.querySelector('.micro-hint').style.display = 
                    currentScene === 'micro' ? 'block' : 'none';
                
                updateInfoText();
                draw();
            });
        });
        
        // 控制按钮事件
        const playBtn = document.getElementById('play-btn');
        const pauseBtn = document.getElementById('pause-btn');
        const resetBtn = document.getElementById('reset-btn');
        
        playBtn.addEventListener('click', () => {
            animationPlaying = true;
            playBtn.disabled = true;
            pauseBtn.disabled = false;
            animate();
        });
        
        pauseBtn.addEventListener('click', () => {
            animationPlaying = false;
            playBtn.disabled = false;
            pauseBtn.disabled = true;
        });
        
        resetBtn.addEventListener('click', () => {
            animationTime = 0;
            animationPlaying = false;
            playBtn.disabled = false;
            pauseBtn.disabled = true;
            draw();
        });
        
        // 工具提示
        const tooltip = document.createElement('div');
        tooltip.className = 'tooltip';
        document.querySelector('.animation-container').appendChild(tooltip);
        
        // 更新信息文本
        function updateInfoText() {
            const infoText = document.getElementById('info-text');
            
            switch(currentScene) {
                case 'macro':
                    infoText.innerHTML = `
                        <p><span class="highlight">钠与水反应宏观现象</span>：</p>
                        <ul>
                            <li><strong>浮</strong>：钠密度（0.97g/cm³）比水小，浮在水面</li>
                            <li><strong>熔</strong>：反应放热，钠熔点低（97.8℃），熔化成小球</li>
                            <li><strong>游</strong>：生成氢气推动钠球快速游动</li>
                            <li><strong>响</strong>：氢气燃烧或轻微爆炸发出响声</li>
                            <li><strong>红</strong>：生成NaOH使酚酞变红，溶液呈碱性</li>
                        </ul>
                    `;
                    break;
                    
                case 'micro':
                    infoText.innerHTML = `
                        <p><span class="highlight">钠与水反应微观过程</span>：</p>
                        <ul>
                            <li><strong>电子转移</strong>：钠原子失去电子 → 钠离子（Na⁺）</li>
                            <li><strong>水分子解离</strong>：水分子中氢-氧键断裂</li>
                            <li><strong>氢气生成</strong>：氢离子获得电子 → 氢气分子（H₂）</li>
                            <li><strong>离子结合</strong>：钠离子与氢氧根离子结合 → 氢氧化钠（NaOH）</li>
                            <li>总反应：2Na + 2H₂O → 2NaOH + H₂↑</li>
                        </ul>
                    `;
                    break;
                    
                case 'equation':
                    infoText.innerHTML = `
                        <p><span class="highlight">化学方程式解析</span>：</p>
                        <ul>
                            <li><strong>反应物</strong>：钠（Na） + 水（H₂O）</li>
                            <li><strong>生成物</strong>：氢氧化钠（NaOH） + 氢气（H₂）</li>
                            <li><strong>反应条件</strong>：常温，水为液态</li>
                            <li><strong>配平原理</strong>：</li>
                            <ul>
                                <li>原子守恒：左右两边Na、H、O原子数相等</li>
                                <li>电荷守恒：反应前后总电荷为零</li>
                                <li>需要2个Na原子与2个水分子反应</li>
                            </ul>
                            <li><strong>↑符号</strong>：表示氢气是气体，从溶液中逸出</li>
                        </ul>
                    `;
                    break;
            }
        }
        
        // 初始化信息文本
        updateInfoText();
        
        // 动画主循环
        function animate() {
            if (!animationPlaying) return;
            
            animationTime += 0.016 * animationSpeed; // 约60fps
            
            // 限制动画时间
            const maxTime = currentScene === 'macro' ? 8 : 
                           currentScene === 'micro' ? 12 : 6;
            
            if (animationTime > maxTime) {
                animationPlaying = false;
                playBtn.disabled = false;
                pauseBtn.disabled = true;
                animationTime = maxTime;
            }
            
            draw();
            requestAnimationFrame(animate);
        }
        
        // 绘制函数
        function draw() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            switch(currentScene) {
                case 'macro':
                    drawMacroScene();
                    break;
                case 'micro':
                    drawMicroScene();
                    break;
                case 'equation':
                    drawEquationScene();
                    break;
            }
        }
        
        // 绘制宏观场景
        function drawMacroScene() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制烧杯
            ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
            ctx.strokeStyle = '#95a5a6';
            ctx.lineWidth = 3;
            
            // 烧杯底部
            ctx.beginPath();
            ctx.ellipse(centerX, centerY + 150, 180, 30, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.stroke();
            
            // 烧杯侧面
            ctx.beginPath();
            ctx.moveTo(centerX - 150, centerY + 120);
            ctx.lineTo(centerX - 120, centerY - 100);
            ctx.lineTo(centerX + 120, centerY - 100);
            ctx.lineTo(centerX + 150, centerY + 120);
            ctx.closePath();
            ctx.fill();
            ctx.stroke();
            
            // 绘制水
            const waterLevel = centerY + 50;
            ctx.fillStyle = 'rgba(135, 206, 235, 0.6)';
            ctx.beginPath();
            ctx.moveTo(centerX - 120, waterLevel);
            ctx.lineTo(centerX + 120, waterLevel);
            ctx.lineTo(centerX + 150, centerY + 120);
            ctx.lineTo(centerX - 150, centerY + 120);
            ctx.closePath();
            ctx.fill();
            
            // 绘制钠球
            const sodiumSize = 30 + 5 * Math.sin(animationTime * 2);
            const sodiumX = centerX + 80 * Math.sin(animationTime * 1.5);
            const sodiumY = waterLevel - sodiumSize - 10;
            
            // 钠球光泽效果
            const sodiumGradient = ctx.createRadialGradient(
                sodiumX - 10, sodiumY - 10, 0,
                sodiumX, sodiumY, sodiumSize
            );
            sodiumGradient.addColorStop(0, '#F0F0F0');
            sodiumGradient.addColorStop(0.7, '#C0C0C0');
            sodiumGradient.addColorStop(1, '#A0A0A0');
            
            ctx.fillStyle = sodiumGradient;
            ctx.beginPath();
            ctx.arc(sodiumX, sodiumY, sodiumSize, 0, Math.PI * 2);
            ctx.fill();
            
            ctx.strokeStyle = '#A0A0A0';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制气泡（氢气）
            if (animationTime > 1) {
                const bubbleCount = Math.min(20, Math.floor((animationTime - 1) * 10));
                
                for (let i = 0; i < bubbleCount; i++) {
                    const bubbleSize = 5 + Math.random() * 8;
                    const bubbleX = sodiumX + (Math.random() - 0.5) * 40;
                    const bubbleY = waterLevel - (animationTime - 1 + Math.random() * 0.5) * 80 * i / bubbleCount;
                    
                    if (bubbleY > waterLevel - 10) continue;
                    
                    ctx.strokeStyle = 'rgba(52, 152, 219, 0.7)';
                    ctx.lineWidth = 1.5;
                    ctx.beginPath();
                    ctx.arc(bubbleX, bubbleY, bubbleSize, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 气泡高光
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.beginPath();
                    ctx.arc(bubbleX - bubbleSize/3, bubbleY - bubbleSize/3, bubbleSize/4, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制酚酞变红效果
            if (animationTime > 2) {
                const redIntensity = Math.min(1, (animationTime - 2) / 2);
                ctx.fillStyle = `rgba(255, 107, 139, ${0.3 * redIntensity})`;
                ctx.beginPath();
                ctx.moveTo(centerX - 120, waterLevel);
                ctx.lineTo(centerX + 120, waterLevel);
                ctx.lineTo(centerX + 150, centerY + 120);
                ctx.lineTo(centerX - 150, centerY + 120);
                ctx.closePath();
                ctx.fill();
            }
            
            // 绘制火花效果（反应剧烈）
            if (animationTime > 0.5 && animationTime < 3) {
                const sparkCount = 5;
                for (let i = 0; i < sparkCount; i++) {
                    const angle = Math.random() * Math.PI * 2;
                    const distance = 40 + Math.random() * 30;
                    const sparkX = sodiumX + Math.cos(angle) * distance;
                    const sparkY = sodiumY + Math.sin(angle) * distance;
                    
                    ctx.fillStyle = '#F1C40F';
                    ctx.beginPath();
                    ctx.arc(sparkX, sparkY, 2 + Math.random() * 3, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制现象标签
            if (animationTime > 0.5) {
                drawPhenomenonTag(centerX - 100, waterLevel - 80, "浮", "钠密度比水小");
                drawPhenomenonTag(sodiumX + 50, sodiumY, "熔", "反应放热，钠熔点低");
                drawPhenomenonTag(sodiumX, sodiumY - 50, "游", "氢气推动钠球运动");
                
                if (animationTime > 1.5) {
                    drawPhenomenonTag(centerX, centerY - 120, "响", "氢气燃烧或轻微爆炸");
                }
                
                if (animationTime > 2.5) {
                    drawPhenomenonTag(centerX + 100, waterLevel - 40, "红", "生成NaOH，溶液呈碱性");
                }
            }
        }
        
        // 绘制现象标签
        function drawPhenomenonTag(x, y, text, tooltipText) {
            ctx.fillStyle = 'rgba(52, 152, 219, 0.9)';
            ctx.beginPath();
            ctx.roundRect(x - 25, y - 15, 50, 30, 15);
            ctx.fill();
            
            ctx.fillStyle = 'white';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(text, x, y);
            
            // 检测鼠标悬停
            const mouseX = mousePos.x * canvas.width / canvas.offsetWidth;
            const mouseY = mousePos.y * canvas.height / canvas.offsetHeight;
            
            if (mouseX > x - 25 && mouseX < x + 25 && 
                mouseY > y - 15 && mouseY < y + 15) {
                tooltip.textContent = tooltipText;
                tooltip.style.left = (mouseX + 15) + 'px';
                tooltip.style.top = (mouseY + 15) + 'px';
                tooltip.classList.add('show');
            }
        }
        
        // 绘制微观场景
        function drawMicroScene() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制背景网格
            ctx.strokeStyle = 'rgba(200, 200, 200, 0.2)';
            ctx.lineWidth = 1;
            const gridSize = 40;
            
            for (let x = 0; x < canvas.width; x += gridSize) {
                ctx.beginPath();
                ctx.moveTo(x, 0);
                ctx.lineTo(x, canvas.height);
                ctx.stroke();
            }
            
            for (let y = 0; y < canvas.height; y += gridSize) {
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(canvas.width, y);
                ctx.stroke();
            }
            
            // 计算动画阶段
            const stageTime = animationTime / 3; // 每个阶段3秒
            const stage = Math.floor(stageTime);
            const stageProgress = stageTime - stage;
            
            // 绘制钠原子
            const sodiumCount = 2;
            const sodiumRadius = 25;
            
            for (let i = 0; i < sodiumCount; i++) {
                let sodiumX, sodiumY;
                
                if (stage === 0) {
                    // 初始位置
                    sodiumX = centerX - 150 + i * 60;
                    sodiumY = centerY;
                } else if (stage === 1) {
                    // 失去电子，向右移动
                    sodiumX = centerX - 100 + i * 60 + stageProgress * 50;
                    sodiumY = centerY;
                } else {
                    // 成为钠离子
                    sodiumX = centerX + 50 + i * 60;
                    sodiumY = centerY + 50;
                }
                
                // 绘制钠原子
                const sodiumGradient = ctx.createRadialGradient(
                    sodiumX - 8, sodiumY - 8, 0,
                    sodiumX, sodiumY, sodiumRadius
                );
                sodiumGradient.addColorStop(0, '#F0F0F0');
                sodiumGradient.addColorStop(0.7, '#C0C0C0');
                sodiumGradient.addColorStop(1, '#A0A0A0');
                
                ctx.fillStyle = sodiumGradient;
                ctx.beginPath();
                ctx.arc(sodiumX, sodiumY, sodiumRadius, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = '#2C3E50';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('Na', sodiumX, sodiumY);
                
                // 绘制电子（第一阶段）
                if (stage === 0 || (stage === 1 && stageProgress < 0.5)) {
                    const electronAngle = animationTime * 3 + i * Math.PI;
                    const electronRadius = sodiumRadius + 15;
                    const electronX = sodiumX + Math.cos(electronAngle) * electronRadius;
                    const electronY = sodiumY + Math.sin(electronAngle) * electronRadius;
                    
                    ctx.fillStyle = '#F1C40F';
                    ctx.beginPath();
                    ctx.arc(electronX, electronY, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    // 电子轨道
                    ctx.strokeStyle = 'rgba(241, 196, 15, 0.3)';
                    ctx.lineWidth = 1;
                    ctx.beginPath();
                    ctx.arc(sodiumX, sodiumY, electronRadius, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // 电子标签
                    ctx.fillStyle = '#F1C40F';
                    ctx.font = '12px Arial';
                    ctx.fillText('e⁻', electronX, electronY - 15);
                }
                
                // 绘制钠离子（第三阶段后）
                if (stage >= 2) {
                    ctx.fillStyle = '#3498db';
                    ctx.font = 'bold 16px Arial';
                    ctx.fillText('Na⁺', sodiumX, sodiumY + sodiumRadius + 20);
                }
            }
            
            // 绘制水分子
            const waterCount = 2;
            
            for (let i = 0; i < waterCount; i++) {
                let waterX, waterY;
                
                if (stage === 0) {
                    waterX = centerX + 100 + i * 80;
                    waterY = centerY - 30;
                } else if (stage === 1) {
                    waterX = centerX + 80 + i * 80;
                    waterY = centerY - 30 + stageProgress * 30;
                } else {
                    waterX = centerX + 100 + i * 80;
                    waterY = centerY + 30;
                }
                
                // 氧原子（红色）
                ctx.fillStyle = '#E74C3C';
                ctx.beginPath();
                ctx.arc(waterX, waterY, 20, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 18px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText('O', waterX, waterY);
                
                // 氢原子（灰色）
                const h1X = waterX - 35;
                const h1Y = waterY - 20;
                const h2X = waterX + 35;
                const h2Y = waterY - 20;
                
                ctx.fillStyle = '#D3D3D3';
                ctx.beginPath();
                ctx.arc(h1X, h1Y, 15, 0, Math.PI * 2);
                ctx.fill();
                ctx.beginPath();
                ctx.arc(h2X, h2Y, 15, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = '#2C3E50';
                ctx.fillText('H', h1X, h1Y);
                ctx.fillText('H', h2X, h2Y);
                
                // 化学键
                ctx.strokeStyle = '#F1C40F';
                ctx.lineWidth = 3;
                
                // O-H键
                ctx.beginPath();
                ctx.moveTo(waterX, waterY);
                ctx.lineTo(h1X, h1Y);
                ctx.stroke();
                
                ctx.beginPath();
                ctx.moveTo(waterX, waterY);
                ctx.lineTo(h2X, h2Y);
                ctx.stroke();
                
                // 断裂动画（第二阶段）
                if (stage === 1 && stageProgress > 0.3) {
                    const breakProgress = (stageProgress - 0.3) / 0.7;
                    
                    // 绘制断裂效果
                    ctx.strokeStyle = '#E74C3C';
                    ctx.lineWidth = 2;
                    ctx.setLineDash([5, 5]);
                    
                    ctx.beginPath();
                    ctx.moveTo(waterX, waterY);
                    ctx.lineTo(h1X + breakProgress * 20, h1Y - breakProgress * 20);
                    ctx.stroke();
                    
                    ctx.beginPath();
                    ctx.moveTo(waterX, waterY);
                    ctx.lineTo(h2X - breakProgress * 20, h2Y - breakProgress * 20);
                    ctx.stroke();
                    
                    ctx.setLineDash([]);
                    
                    // 绘制氢离子
                    if (stageProgress > 0.5) {
                        const ionProgress = (stageProgress - 0.5) / 0.5;
                        const h1FinalX = centerX - 50;
                        const h1FinalY = centerY - 50;
                        
                        ctx.fillStyle = '#9b59b6';
                        ctx.beginPath();
                        ctx.arc(
                            h1X + (h1FinalX - h1X) * ionProgress,
                            h1Y + (h1FinalY - h1Y) * ionProgress,
                            15, 0, Math.PI * 2
                        );
                        ctx.fill();
                        
                        ctx.fillStyle = 'white';
                        ctx.font = 'bold 16px Arial';
                        ctx.fillText('H⁺', 
                            h1X + (h1FinalX - h1X) * ionProgress,
                            h1Y + (h1FinalY - h1Y) * ionProgress
                        );
                    }
                }
            }
            
            // 绘制氢气分子（第三阶段）
            if (stage >= 2) {
                const h2X = centerX - 50;
                const h2Y = centerY - 50;
                const h2Progress = stage === 2 ? stageProgress : 1;
                
                // 两个氢原子
                ctx.fillStyle = '#9b59b6';
                ctx.beginPath();
                ctx.arc(h2X - 12, h2Y, 15, 0, Math.PI * 2);
                ctx.fill();
                ctx.beginPath();
                ctx.arc(h2X + 12, h2Y, 15, 0, Math.PI * 2);
                ctx.fill();
                
                // 化学键
                ctx.strokeStyle = '#F1C40F';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.moveTo(h2X - 12, h2Y);
                ctx.lineTo(h2X + 12, h2Y);
                ctx.stroke();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 16px Arial';
                ctx.fillText('H', h2X - 12, h2Y);
                ctx.fillText('H', h2X + 12, h2Y);
                
                // 氢气标签
                ctx.fillStyle = '#9b59b6';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('H₂', h2X, h2Y + 40);
                
                // 气泡上升效果
                if (h2Progress > 0.5) {
                    const bubbleY = h2Y - (h2Progress - 0.5) * 100;
                    ctx.strokeStyle = 'rgba(155, 89, 182, 0.7)';
                    ctx.lineWidth = 2;
                    ctx.beginPath();
                    ctx.arc(h2X, bubbleY, 20, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    ctx.fillStyle = 'rgba(255, 255, 255, 0.8)';
                    ctx.beginPath();
                    ctx.arc(h2X - 7, bubbleY - 7, 5, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 绘制氢氧根离子（第三阶段）
            if (stage >= 2) {
                const ohX = centerX + 150;
                const ohY = centerY + 50;
                
                // 氧原子
                ctx.fillStyle = '#E74C3C';
                ctx.beginPath();
                ctx.arc(ohX, ohY, 20, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('O', ohX, ohY);
                
                // 氢原子
                ctx.fillStyle = '#D3D3D3';
                ctx.beginPath();
                ctx.arc(ohX + 30, ohY, 15, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = '#2C3E50';
                ctx.fillText('H', ohX + 30, ohY);
                
                // 化学键
                ctx.strokeStyle = '#F1C40F';
                ctx.lineWidth = 3;
                ctx.beginPath();
                ctx.moveTo(ohX, ohY);
                ctx.lineTo(ohX + 30, ohY);
                ctx.stroke();
                
                // 氢氧根标签
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('OH
<!--检测到代码截断，自动续写中...-->
⁻', ohX + 15, ohY + 40);
            }
            
            // 绘制氢氧化钠（最终阶段）
            if (stage >= 3) {
                const naohX = centerX;
                const naohY = centerY + 150;
                
                // 绘制连接线
                ctx.strokeStyle = 'rgba(46, 204, 113, 0.5)';
                ctx.lineWidth = 2;
                ctx.setLineDash([5, 5]);
                
                // 从钠离子到NaOH
                ctx.beginPath();
                ctx.moveTo(centerX + 50, centerY + 75);
                ctx.lineTo(naohX - 40, naohY - 20);
                ctx.stroke();
                
                // 从氢氧根到NaOH
                ctx.beginPath();
                ctx.moveTo(centerX + 150, centerY + 70);
                ctx.lineTo(naohX + 40, naohY - 20);
                ctx.stroke();
                
                ctx.setLineDash([]);
                
                // 绘制NaOH分子
                // Na⁺
                ctx.fillStyle = '#C0C0C0';
                ctx.beginPath();
                ctx.arc(naohX - 30, naohY, 20, 0, Math.PI * 2);
                ctx.fill();
                ctx.fillStyle = '#2C3E50';
                ctx.font = 'bold 18px Arial';
                ctx.fillText('Na⁺', naohX - 30, naohY);
                
                // OH⁻
                ctx.fillStyle = '#E74C3C';
                ctx.beginPath();
                ctx.arc(naohX + 20, naohY - 15, 18, 0, Math.PI * 2);
                ctx.fill();
                ctx.fillStyle = 'white';
                ctx.fillText('O', naohX + 20, naohY - 15);
                
                ctx.fillStyle = '#D3D3D3';
                ctx.beginPath();
                ctx.arc(naohX + 45, naohY - 15, 14, 0, Math.PI * 2);
                ctx.fill();
                ctx.fillStyle = '#2C3E50';
                ctx.fillText('H', naohX + 45, naohY - 15);
                
                // 化学键
                ctx.strokeStyle = '#F1C40F';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.moveTo(naohX + 20, naohY - 15);
                ctx.lineTo(naohX + 45, naohY - 15);
                ctx.stroke();
                
                // NaOH标签
                ctx.fillStyle = '#2ecc71';
                ctx.font = 'bold 22px Arial';
                ctx.fillText('NaOH', naohX, naohY + 40);
            }
            
            // 绘制阶段标题
            const stageTitles = [
                "1. 钠原子准备失去电子",
                "2. 水分子解离，氢离子生成",
                "3. 氢气生成，钠离子与氢氧根结合",
                "4. 形成氢氧化钠"
            ];
            
            if (stage < stageTitles.length) {
                ctx.fillStyle = '#2C3E50';
                ctx.font = 'bold 20px Arial';
                ctx.textAlign = 'center';
                ctx.fillText(stageTitles[stage], centerX, 40);
                
                // 进度条
                ctx.fillStyle = '#ecf0f1';
                ctx.fillRect(centerX - 100, 60, 200, 10);
                ctx.fillStyle = '#3498db';
                ctx.fillRect(centerX - 100, 60, 200 * stageProgress, 10);
            }
        }
        
        // 绘制方程式场景
        function drawEquationScene() {
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 绘制背景
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制大标题
            ctx.fillStyle = '#2C3E50';
            ctx.font = 'bold 36px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('钠与水反应化学方程式', centerX, 80);
            
            // 计算动画进度
            const totalDuration = 6;
            const segmentDuration = totalDuration / 8;
            const segment = Math.floor(animationTime / segmentDuration);
            const segmentProgress = (animationTime % segmentDuration) / segmentDuration;
            
            // 绘制方程式各部分
            const eqX = centerX;
            const eqY = centerY;
            const spacing = 80;
            
            // 2Na
            if (segment >= 0) {
                const alpha = segment === 0 ? segmentProgress : 1;
                drawEquationPart(eqX - spacing * 3, eqY, '2Na', '#C0C0C0', alpha);
                
                if (segment === 0) {
                    drawFloatingAtoms(eqX - spacing * 3, eqY, 'Na', 2, segmentProgress);
                }
            }
            
            // + 号
            if (segment >= 1) {
                const alpha = segment === 1 ? segmentProgress : 1;
                ctx.fillStyle = `rgba(52, 73, 94, ${alpha})`;
                ctx.font = 'bold 40px Arial';
                ctx.fillText('+', eqX - spacing * 1.5, eqY);
            }
            
            // 2H₂O
            if (segment >= 2) {
                const alpha = segment === 2 ? segmentProgress : 1;
                drawEquationPart(eqX, eqY, '2H₂O', '#3498db', alpha);
                
                if (segment === 2) {
                    drawFloatingAtoms(eqX, eqY, 'H₂O', 2, segmentProgress);
                }
            }
            
            // → 号
            if (segment >= 3) {
                const alpha = segment === 3 ? segmentProgress : 1;
                ctx.fillStyle = `rgba(231, 76, 60, ${alpha})`;
                ctx.font = 'bold 40px Arial';
                ctx.fillText('→', eqX + spacing * 1.5, eqY);
            }
            
            // 2NaOH
            if (segment >= 4) {
                const alpha = segment === 4 ? segmentProgress : 1;
                drawEquationPart(eqX + spacing * 3, eqY - 50, '2NaOH', '#2ecc71', alpha);
                
                if (segment === 4) {
                    drawFloatingAtoms(eqX + spacing * 3, eqY - 50, 'NaOH', 2, segmentProgress);
                }
            }
            
            // + 号
            if (segment >= 5) {
                const alpha = segment === 5 ? segmentProgress : 1;
                ctx.fillStyle = `rgba(52, 73, 94, ${alpha})`;
                ctx.font = 'bold 40px Arial';
                ctx.fillText('+', eqX + spacing * 4.5, eqY - 50);
            }
            
            // H₂↑
            if (segment >= 6) {
                const alpha = segment === 6 ? segmentProgress : 1;
                drawEquationPart(eqX + spacing * 6, eqY - 50, 'H₂↑', '#9b59b6', alpha);
                
                if (segment === 6) {
                    // 绘制上升气泡
                    const bubbleY = eqY - 50 - segmentProgress * 100;
                    ctx.strokeStyle = `rgba(155, 89, 182, ${0.7 * alpha})`;
                    ctx.lineWidth = 3;
                    ctx.beginPath();
                    ctx.arc(eqX + spacing * 6, bubbleY, 25, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    ctx.fillStyle = `rgba(255, 255, 255, ${0.8 * alpha})`;
                    ctx.beginPath();
                    ctx.arc(eqX + spacing * 6 - 8, bubbleY - 8, 8, 0, Math.PI * 2);
                    ctx.fill();
                }
            }
            
            // 配平解释
            if (segment >= 7) {
                ctx.fillStyle = '#2C3E50';
                ctx.font = '20px Arial';
                ctx.textAlign = 'center';
                
                const explanations = [
                    "配平原理：原子守恒",
                    "左边：2Na, 4H, 2O",
                    "右边：2Na, 4H, 2O",
                    "电荷守恒：反应前后总电荷为0"
                ];
                
                explanations.forEach((text, index) => {
                    const y = eqY + 100 + index * 30;
                    const alpha = segment === 7 ? Math.min(1, segmentProgress * 4 - index * 0.5) : 1;
                    
                    if (alpha > 0) {
                        ctx.globalAlpha = alpha;
                        ctx.fillText(text, centerX, y);
                        ctx.globalAlpha = 1;
                    }
                });
            }
            
            // 绘制进度指示器
            ctx.fillStyle = '#ecf0f1';
            ctx.fillRect(centerX - 150, canvas.height - 40, 300, 10);
            ctx.fillStyle = '#3498db';
            ctx.fillRect(centerX - 150, canvas.height - 40, 300 * (animationTime / totalDuration), 10);
        }
        
        // 绘制方程式部分
        function drawEquationPart(x, y, text, color, alpha) {
            ctx.save();
            ctx.globalAlpha = alpha;
            
            // 背景框
            ctx.fillStyle = color + '20'; // 添加透明度
            ctx.beginPath();
            ctx.roundRect(x - 60, y - 40, 120, 80, 15);
            ctx.fill();
            
            // 边框
            ctx.strokeStyle = color;
            ctx.lineWidth = 3;
            ctx.stroke();
            
            // 文字
            ctx.fillStyle = color;
            ctx.font = 'bold 32px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(text, x, y);
            
            // 下标处理
            if (text.includes('₂')) {
                const parts = text.split('₂');
                if (parts.length > 1) {
                    ctx.font = 'bold 20px Arial';
                    ctx.fillText('₂', x + 20, y + 10);
                }
            }
            
            ctx.restore();
        }
        
        // 绘制浮动原子
        function drawFloatingAtoms(x, y, type, count, progress) {
            for (let i = 0; i < count; i++) {
                const angle = (i * Math.PI * 2 / count) + progress * Math.PI * 2;
                const radius = 30 + Math.sin(animationTime * 3 + i) * 10;
                const atomX = x + Math.cos(angle) * radius;
                const atomY = y + Math.sin(angle) * radius;
                
                let color, symbol;
                
                switch(type) {
                    case 'Na':
                        color = '#C0C0C0';
                        symbol = 'Na';
                        break;
                    case 'H₂O':
                        color = i === 0 ? '#3498db' : '#2980b9';
                        symbol = i === 0 ? 'H₂O' : 'H₂O';
                        break;
                    case 'NaOH':
                        color = '#2ecc71';
                        symbol = 'NaOH';
                        break;
                }
                
                ctx.fillStyle = color;
                ctx.beginPath();
                ctx.arc(atomX, atomY, 20, 0, Math.PI * 2);
                ctx.fill();
                
                ctx.fillStyle = 'white';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(symbol, atomX, atomY);
            }
        }
        
        // 鼠标位置跟踪
        const mousePos = { x: 0, y: 0 };
        
        canvas.addEventListener('mousemove', (e) => {
            const rect = canvas.getBoundingClientRect();
            mousePos.x = e.clientX - rect.left;
            mousePos.y = e.clientY - rect.top;
            
            // 隐藏工具提示
            tooltip.classList.remove('show');
        });
        
        canvas.addEventListener('mouseleave', () => {
            tooltip.classList.remove('show');
        });
        
        // 点击交互（微观场景）
        canvas.addEventListener('click', (e) => {
            if (currentScene !== 'micro') return;
            
            const rect = canvas.getBoundingClientRect();
            const x = (e.clientX - rect.left) * canvas.width / canvas.offsetWidth;
            const y = (e.clientY - rect.top) * canvas.height / canvas.offsetHeight;
            
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            
            // 检查是否点击了钠原子
            const sodiumRadius = 25;
            const sodiumX1 = centerX - 100;
            const sodiumX2 = centerX - 40;
            const sodiumY = centerY;
            
            if (Math.sqrt((x - sodiumX1)**2 + (y - sodiumY)**2) < sodiumRadius ||
                Math.sqrt((x - sodiumX2)**2 + (y - sodiumY)**2) < sodiumRadius) {
                showTooltip(x, y, "钠原子 (Na)\n金属原子，最外层有1个电子\n易失去电子形成Na⁺");
                return;
            }
            
            // 检查是否点击了水分子
            const waterX1 = centerX + 100;
            const waterX2 = centerX + 180;
            const waterY = centerY - 30;
            
            if (Math.sqrt((x - waterX1)**2 + (y - waterY)**2) < 30 ||
                Math.sqrt((x - waterX2)**2 + (y - waterY)**2) < 30) {
                showTooltip(x, y, "水分子 (H₂O)\n由2个H原子和1个O原子组成\nO-H键为极性共价键");
                return;
            }
            
            // 检查是否点击了氢气
            const h2X = centerX - 50;
            const h2Y = centerY - 50;
            
            if (Math.sqrt((x - h2X)**2 + (y - h2Y)**2) < 30) {
                showTooltip(x, y, "氢气分子 (H₂)\n由2个H原子通过共价键结合\n密度小，易燃");
                return;
            }
        });
        
        // 显示工具提示
        function showTooltip(x, y, text) {
            tooltip.textContent = text;
            tooltip.style.left = (x + 15) + 'px';
            tooltip.style.top = (y + 15) + 'px';
            tooltip.classList.add('show');
        }
        
        // 初始绘制
        draw();
        
        // 添加圆角矩形支持
        if (!ctx.roundRect) {
            ctx.roundRect = function(x, y, width, height, radius) {
                if (width < 2 * radius) radius = width / 2;
                if (height < 2 * radius) radius = height / 2;
                
                this.beginPath();
                this.moveTo(x + radius, y);
                this.arcTo(x + width, y, x + width, y + height, radius);
                this.arcTo(x + width, y + height, x, y + height, radius);
                this.arcTo(x, y + height, x, y, radius);
                this.arcTo(x, y, x + width, y, radius);
                this.closePath();
                return this;
            };
        }
    </script>
</body>
</html>

### 3. 过程输出

### 3. 过程输出

## 《钠与水反应交互式教学动画》使用指南

欢迎使用“钠与水反应”交互式教学动画！本动画由专业教育技术团队开发，旨在通过直观、生动的可视化方式，帮助您深入理解这一经典化学反应的宏观现象、微观本质和符号表达。无论您是学生、教师还是化学爱好者，本工具都将为您提供全新的学习体验。

---

### 一、功能说明

本动画是一个基于HTML5 Canvas技术开发的交互式教学工具，完全在浏览器中运行，无需安装任何插件。它通过三个精心设计的场景，完整呈现了钠与水反应的化学知识体系：

1. **宏观现象场景**：生动展示钠与水反应的完整实验过程
2. **微观过程场景**：深入揭示原子、分子层面的反应机理
3. **化学方程式场景**：系统解析反应方程式的配平原理

### 二、主要功能

#### 1. 场景切换功能
- **宏观现象**：点击左上角“宏观现象”按钮，进入实验观察模式
- **微观过程**：点击“微观过程”按钮，进入原子分子层面的动态演示
- **化学方程式**：点击“化学方程式”按钮，学习方程式的配平与书写

#### 2. 动画控制功能
- **播放/暂停**：控制动画的播放进度，便于重点观察
- **重置**：一键回到初始状态，可重复观看
- **进度条**：直观显示当前动画的播放进度

#### 3. 交互探索功能
- **点击标签**：在宏观场景中，点击“浮、熔、游、响、红”等标签，查看详细解释
- **微观点击**：在微观场景中，点击任意原子或分子，查看其化学性质和变化过程
- **悬停提示**：鼠标悬停在特定元素上，显示相关知识点

#### 4. 知识整合功能
- **实时信息面板**：右侧信息区随场景变化，显示对应的核心知识点
- **化学方程式高亮**：动态展示方程式的配平过程
- **颜色编码系统**：统一的颜色标识帮助记忆不同元素

### 三、设计特色

#### 1. 科学准确性
- 所有原子颜色遵循国际化学教育惯例（Na：银灰，H：浅灰，O：红色）
- 反应现象严格依据实验事实（浮、熔、游、响、红）
- 微观过程符合化学键理论（电子转移、键的断裂与形成）

#### 2. 认知层次性
- **现象层**：先观察宏观现象，建立感性认识
- **本质层**：再探究微观机理，理解反应本质
- **符号层**：最后学习化学方程式，掌握符号表达

#### 3. 交互友好性
- 界面简洁直观，操作逻辑清晰
- 响应式设计，适配不同屏幕尺寸
- 动画速度适中，兼顾观察与思考

#### 4. 教学专业性
- 遵循“宏观-微观-符号”三重表征教学理论
- 突出化学核心概念（电子转移、离子形成、质量守恒）
- 提供完整的教学支持材料

### 四、教学要点

#### 针对学生：
1. **预习阶段**：先观看宏观现象，了解反应的基本特征
2. **学习阶段**：结合微观动画，理解反应的本质过程
3. **复习阶段**：通过方程式解析，巩固符号表达能力
4. **探究阶段**：利用交互功能，自主探索感兴趣的知识点

#### 针对教师：
1. **课堂演示**：可作为多媒体课件，生动展示反应过程
2. **概念讲解**：利用微观动画解释抽象概念（如电子转移）
3. **难点突破**：通过分步演示，帮助学生理解配平原理
4. **探究引导**：鼓励学生提出假设，通过动画验证

#### 核心知识点分布：
- **宏观场景**：密度比较、放热反应、气体生成、指示剂变色
- **微观场景**：金属活动性、电子得失、共价键断裂、离子形成
- **方程式场景**：质量守恒、电荷守恒、状态符号、配平技巧

### 五、使用建议

#### 1. 自主学习路径建议
```
第一次使用：宏观现象（完整观看） → 微观过程（分步观察） → 化学方程式（理解配平）
深入探究：微观过程（点击交互） → 宏观现象（关联分析） → 尝试书写方程式
复习巩固：直接进入薄弱环节，利用控制功能重点学习
```

#### 2. 课堂教学应用建议
- **引入新课**：播放宏观现象，激发学生兴趣
- **讲解原理**：切换到微观场景，分步讲解反应机理
- **总结提升**：展示方程式，引导学生总结规律
- **课堂练习**：隐藏部分信息，让学生补充完整

#### 3. 最佳实践提示
- **控制节奏**：适当使用暂停功能，给学生思考时间
- **引导观察**：提示学生注意颜色变化、粒子运动等细节
- **联系实际**：结合生活中的类似现象（如钠的保存、氢气的应用）
- **鼓励提问**：利用动画的可重复性，验证学生的猜想

#### 4. 技术使用提示
- **浏览器**：建议使用Chrome、Edge等现代浏览器
- **屏幕尺寸**：在投影仪上使用时，可调整浏览器缩放比例
- **网络环境**：本动画为单文件，下载后可在离线环境下使用
- **保存分享**：可将HTML文件保存到本地，方便随时使用

---

### 六、教育价值

本动画不仅是一个演示工具，更是一个**探究平台**。它能够：

1. **化抽象为具体**：将看不见的微观过程可视化
2. **建立知识联系**：打通宏观、微观、符号三个层面的关联
3. **培养科学思维**：通过观察、分析、推理，提升科学素养
4. **激发学习兴趣**：生动的动画和交互设计让学习变得有趣

我们相信，通过合理使用本教学动画，您将能够：
- ✅ 深刻理解钠与水反应的本质
- ✅ 掌握化学方程式的配平方法
- ✅ 建立化学学习的思维框架
- ✅ 享受探索化学世界的乐趣

**开始您的化学探索之旅吧！点击播放按钮，让我们一起揭开钠与水反应的神秘面纱！**

---
*开发团队：教育技术专家与创意程序员联合制作*
*版本：1.0 | 最后更新：2024年*
*如有教学建议或技术问题，欢迎反馈*