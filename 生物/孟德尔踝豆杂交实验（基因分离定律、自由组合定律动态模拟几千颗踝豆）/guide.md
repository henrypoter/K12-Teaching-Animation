# 需求：孟德尔踝豆杂交实验（基因分离定律、自由组合定律动态模拟几千颗踝豆）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
1.  **目标用户**：主要为高中生物学学生，也可能包括对遗传学感兴趣的初学者。
2.  **核心需求**：用户需要直观、动态地理解孟德尔豌豆杂交实验中两个核心定律——基因分离定律和自由组合定律。静态的棋盘格（Punnett Square）和文字描述难以展现“概率”和“大样本统计”的本质。
3.  **深层需求**：
    *   **化抽象为具体**：将“基因”、“等位基因”、“配子”、“随机结合”等抽象概念可视化。
    *   **理解统计本质**：通过模拟大量“豌豆”（如几千颗）的杂交结果，让学生亲眼看到理论比例（如3:1， 9:3:3:1）是如何从随机事件中涌现出来的，从而理解概率与统计规律的关系。
    *   **自主探索**：允许用户调整实验参数（如亲本基因型、模拟数量），进行探究式学习，验证和巩固知识。
    *   **降低认知负荷**：通过清晰的视觉编码和分步引导，将复杂的实验过程分解，便于学生跟随。

#### 教学设计思路
1.  **核心概念**：
    *   **基因分离定律**：一对等位基因在形成配子时彼此分离。
    *   **自由组合定律**：不同对等位基因在形成配子时自由组合。
    *   **基因型与表现型**。
    *   **配子形成与随机受精**。

2.  **认知规律与流程设计**：
    *   **从简到繁**：先模拟单因子杂交（基因分离定律），再模拟双因子杂交（自由组合定律）。
    *   **从微观到宏观**：
        *   **步骤1（微观过程）**：动态展示亲本产生配子的过程（等位基因分离/自由组合动画）。
        *   **步骤2（结合过程）**：动态模拟配子随机结合形成合子（可用两个“配子池”随机配对的效果）。
        *   **步骤3（宏观结果）**：统计并可视化生成的大量“豌豆”的表现型，以柱状图或饼图展示比例，并与理论值对比。
    *   **从观察到验证**：提供“加速模拟”、“重置”、“修改参数”功能，鼓励学生进行多次实验，观察结果的波动与收敛。

3.  **交互设计**：
    *   **模式选择器**：在“分离定律”和“自由组合定律”模式间切换。
    *   **实验控制面板**：
        *   选择/输入亲本基因型（如YYRR, yyrr）。
        *   设置每轮模拟生成的“豌豆”数量（如100， 1000， 5000颗）。
        *   控制按钮：“单步演示”、“播放/暂停”、“重置”。
    *   **可视化区域分层**：
        *   **上层：亲本与配子形成动画区**。用卡通化的豌豆植株或豆荚代表亲本，从中“飞出”带有字母（Y， y， R， r）的圆形配子。
        *   **中层：随机结合过程区**。两个配子池（雌雄配子）中的配子随机配对，形成合子并显示其基因型。
        *   **下层：结果统计与展示区**：
            *   **实时计数器**：显示各表现型（如黄色圆粒、黄色皱粒等）的当前数量。
            *   **动态柱状图/饼图**：随模拟进行实时更新，直观展示比例。
            *   **理论比例对照表**：始终显示经典理论比例（如9:3:3:1），用于对比。

4.  **视觉呈现**：
    *   **角色化**：将豌豆表现型（黄色/绿色， 圆粒/皱粒）设计成可爱、辨识度高的卡通图标，增加趣味性。
    *   **基因可视化**：用不同颜色和字母的“卡片”或“珠子”代表等位基因（如黄色Y， 绿色y； 圆形R， 皱形r），附着在“豌豆”或“配子”上。
    *   **动画设计**：
        *   配子形成时，等位基因“分离”或“组合”的动画要清晰、舒缓。
        *   配子结合时，采用随机碰撞、连线配对等效果，强调随机性。
        *   结果“豌豆”像雨点一样落下，堆积成柱状图，或落入对应的分类篮筐中，富有动感和成就感。
    *   **信息层次**：通过颜色深浅、区域划分和动画焦点，引导用户视线，确保在动态过程中不丢失核心信息。

#### 配色方案选择
*   **主色调**：采用**清新、自然、护眼**的配色，符合生命科学主题。
    *   背景：浅米白或极浅的豆沙绿 (#f5f5f5 或 #f0f7e6)。
    *   主要区域：使用柔和的卡片式设计，带有轻微阴影。
*   **表现型编码色**（关键，需高区分度且符合常识）：
    *   **黄色豌豆**：明黄色 (#FFD700 或 #FFEB3B)。
    *   **绿色豌豆**：叶绿色 (#4CAF50 或 #8BC34A)。
    *   （为简化，圆粒和皱粒用形状区分，可辅以轻微高光/纹理差异）。
*   **基因/等位基因编码色**：
    *   **显性等位基因（Y， R）**：较深、饱和的颜色（深蓝 #2196F3 代表Y， 深橙 #FF9800 代表R）。
    *   **隐性等位基因（y， r）**：与对应显性基因同色系但更浅、更灰的颜色（浅蓝 #BBDEFB 代表y， 浅橙 #FFE0B2 代表r）。这有助于建立视觉关联。
*   **数据可视化色**：柱状图颜色直接采用对应表现型的颜色，保持一致性。
*   **交互元素色**：按钮使用友好的蓝色 (#2196F3) 或绿色 (#4CAF50)，悬停时有反馈。

#### 交互功能列表
1.  **实验模式切换**：单因子杂交（分离定律） / 双因子杂交（自由组合定律）切换按钮。
2.  **亲本配置**：
    *   下拉菜单或点击选择预设亲本组合（如纯种黄色圆粒 x 绿色皱粒）。
    *   高级模式：允许用户自定义亲本基因型（通过点击等位基因选择）。
3.  **模拟规模设置**：滑块或输入框，用于设置生成子代豌豆的数量（范围建议：100 - 10000）。
4.  **模拟控制按钮**：
    *   **单步演示**：一次只完成一个配子结合，用于细致观察。
    *   **播放/暂停**：开始或暂停连续模拟。
    *   **加速**：在播放模式下加快动画速度，快速看到统计结果。
    *   **重置**：清空所有结果，回到初始状态。
5.  **过程可视化控制**：可勾选“隐藏配子动画”以在重复实验时直接跳至结果，提升效率。
6.  **结果展示面板**：
    *   实时更新的数字计数器（各表现型计数及总计）。
    *   动态柱状图（或饼图），随模拟进行而增长。
    *   理论比例标签（始终显示）。
    *   **比例对比**：可选项，计算实际比例与理论比例的差值或百分比误差。
7.  **信息提示**：鼠标悬停在关键元素（如基因符号、豌豆、图表）上时，显示简要说明。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>孟德尔豌豆杂交实验动态模拟</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #f0f7e6;
            color: #333;
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4CAF50;
        }

        h1 {
            color: #2E7D32;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #666;
            font-size: 1.1em;
        }

        .container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .control-panel {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .control-group {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        h2, h3 {
            color: #2196F3;
            margin-bottom: 5px;
        }

        label {
            font-weight: 600;
            color: #555;
        }

        select, input[type="range"], button {
            padding: 10px 15px;
            border-radius: 8px;
            border: 2px solid #ddd;
            font-size: 16px;
            transition: all 0.3s;
        }

        select:focus, input[type="range"]:focus {
            outline: none;
            border-color: #2196F3;
        }

        button {
            background-color: #2196F3;
            color: white;
            border: none;
            cursor: pointer;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        button:hover {
            background-color: #1976D2;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(33, 150, 243, 0.3);
        }

        button:active {
            transform: translateY(0);
        }

        button.secondary {
            background-color: #4CAF50;
        }

        button.secondary:hover {
            background-color: #388E3C;
            box-shadow: 0 4px 8px rgba(76, 175, 80, 0.3);
        }

        button.reset {
            background-color: #f44336;
        }

        button.reset:hover {
            background-color: #d32f2f;
            box-shadow: 0 4px 8px rgba(244, 67, 54, 0.3);
        }

        .button-group {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .simulation-area {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .animation-container {
            background-color: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            position: relative;
            height: 500px;
            overflow: hidden;
        }

        #animationCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }

        .results-panel {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .stat-box {
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            color: white;
            font-weight: bold;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            min-height: 100px;
        }

        .stat-value {
            font-size: 2.5em;
            margin: 10px 0;
        }

        .stat-label {
            font-size: 1.1em;
            opacity: 0.9;
        }

        .chart-container {
            margin-top: 30px;
            height: 250px;
            position: relative;
        }

        .chart-bar {
            position: absolute;
            bottom: 0;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            width: 80px;
            border-radius: 8px 8px 0 0;
            transition: height 0.5s ease;
            color: white;
            font-weight: bold;
            padding: 10px 0;
        }

        .theory-label {
            position: absolute;
            top: -25px;
            font-size: 0.9em;
            color: #666;
            font-weight: bold;
        }

        .info-panel {
            background-color: #E3F2FD;
            border-radius: 12px;
            padding: 20px;
            margin-top: 20px;
            border-left: 5px solid #2196F3;
        }

        .info-panel h3 {
            color: #1565C0;
            margin-bottom: 10px;
        }

        .legend {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
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
            border-radius: 4px;
        }

        .gene-legend {
            display: flex;
            gap: 20px;
            margin-top: 15px;
            flex-wrap: wrap;
        }

        .gene-item {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        .gene-symbol {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #ddd;
            color: #777;
            font-size: 0.9em;
        }

        .speed-control {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .speed-value {
            min-width: 40px;
            text-align: center;
            font-weight: bold;
            color: #2196F3;
        }

        @media (max-width: 768px) {
            .control-panel {
                grid-template-columns: 1fr;
            }
            
            .animation-container {
                height: 400px;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>孟德尔豌豆杂交实验动态模拟</h1>
        <p class="subtitle">基因分离定律与自由组合定律可视化演示</p>
    </header>

    <div class="container">
        <div class="control-panel">
            <div class="control-group">
                <h3>实验模式</h3>
                <select id="experimentMode">
                    <option value="single">单因子杂交（基因分离定律）</option>
                    <option value="double" selected>双因子杂交（自由组合定律）</option>
                </select>
                
                <label for="peaCount">模拟豌豆数量: <span id="peaCountValue">1000</span></label>
                <input type="range" id="peaCount" min="100" max="10000" step="100" value="1000">
                
                <div class="speed-control">
                    <label for="speed">模拟速度:</label>
                    <input type="range" id="speed" min="1" max="10" value="5">
                    <span class="speed-value" id="speedValue">5</span>
                </div>
            </div>
            
            <div class="control-group">
                <h3>亲本基因型</h3>
                <div>
                    <label>亲本 P1 (母本):</label>
                    <select id="parent1">
                        <option value="YYRR" selected>YYRR (黄色圆粒)</option>
                        <option value="YYRr">YYRr (黄色圆粒)</option>
                        <option value="YYrr">YYrr (黄色皱粒)</option>
                        <option value="YyRR">YyRR (黄色圆粒)</option>
                        <option value="YyRr">YyRr (黄色圆粒)</option>
                        <option value="Yyrr">Yyrr (黄色皱粒)</option>
                        <option value="yyRR">yyRR (绿色圆粒)</option>
                        <option value="yyRr">yyRr (绿色圆粒)</option>
                        <option value="yyrr">yyrr (绿色皱粒)</option>
                    </select>
                </div>
                
                <div>
                    <label>亲本 P2 (父本):</label>
                    <select id="parent2">
                        <option value="YYRR">YYRR (黄色圆粒)</option>
                        <option value="YYRr">YYRr (黄色圆粒)</option>
                        <option value="YYrr">YYrr (黄色皱粒)</option>
                        <option value="YyRR">YyRR (黄色圆粒)</option>
                        <option value="YyRr">YyRr (黄色圆粒)</option>
                        <option value="Yyrr">Yyrr (黄色皱粒)</option>
                        <option value="yyRR">yyRR (绿色圆粒)</option>
                        <option value="yyRr">yyRr (绿色圆粒)</option>
                        <option value="yyrr" selected>yyrr (绿色皱粒)</option>
                    </select>
                </div>
            </div>
            
            <div class="control-group">
                <h3>实验控制</h3>
                <div class="button-group">
                    <button id="startBtn">
                        <span>▶ 开始模拟</span>
                    </button>
                    <button id="stepBtn" class="secondary">
                        <span>⏭ 单步演示</span>
                    </button>
                    <button id="pauseBtn" class="secondary">
                        <span>⏸ 暂停</span>
                    </button>
                    <button id="resetBtn" class="reset">
                        <span>↺ 重置</span>
                    </button>
                </div>
                
                <div>
                    <label>
                        <input type="checkbox" id="showAnimation" checked>
                        显示配子动画
                    </label>
                </div>
            </div>
        </div>
        
        <div class="simulation-area">
            <div class="animation-container">
                <canvas id="animationCanvas"></canvas>
            </div>
            
            <div class="results-panel">
                <h2>实验结果统计</h2>
                <div class="stats-container" id="statsContainer">
                    <!-- 动态生成统计框 -->
                </div>
                
                <div class="chart-container" id="chartContainer">
                    <!-- 动态生成柱状图 -->
                </div>
                
                <div class="info-panel">
                    <h3>理论比例参考</h3>
                    <div id="theoryInfo">
                        <!-- 动态生成理论比例信息 -->
                    </div>
                    
                    <div class="legend">
                        <h4>表现型图例</h4>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FFD700;"></div>
                            <span>黄色圆粒</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #FFEB3B;"></div>
                            <span>黄色皱粒</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #4CAF50;"></div>
                            <span>绿色圆粒</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color" style="background-color: #8BC34A;"></div>
                            <span>绿色皱粒</span>
                        </div>
                    </div>
                    
                    <div class="gene-legend">
                        <h4>基因图例</h4>
                        <div class="gene-item">
                            <div class="gene-symbol" style="background-color: #2196F3;">Y</div>
                            <span>显性黄色基因</span>
                        </div>
                        <div class="gene-item">
                            <div class="gene-symbol" style="background-color: #BBDEFB;">y</div>
                            <span>隐性绿色基因</span>
                        </div>
                        <div class="gene-item">
                            <div class="gene-symbol" style="background-color: #FF9800;">R</div>
                            <span>显性圆粒基因</span>
                        </div>
                        <div class="gene-item">
                            <div class="gene-symbol" style="background-color: #FFE0B2;">r</div>
                            <span>隐性皱粒基因</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <footer>
        <p>孟德尔豌豆杂交实验动态模拟 | 遗传学教学工具 | 基于HTML5 Canvas实现</p>
        <p>提示：调整亲本基因型和模拟数量，观察不同杂交组合的结果！</p>
    </footer>

    <script>
        // 全局变量
        let canvas, ctx;
        let animationId = null;
        let isAnimating = false;
        let isPaused = false;
        let currentStep = 0;
        let totalPeas = 1000;
        let simulationSpeed = 5;
        let showAnimation = true;
        
        // 实验数据
        let experimentMode = 'double'; // 'single' 或 'double'
        let parent1 = 'YYRR';
        let parent2 = 'yyrr';
        
        // 统计结果
        let results = {
            yellowRound: 0,
            yellowWrinkled: 0,
            greenRound: 0,
            greenWrinkled: 0
        };
        
        // 颜色定义
        const colors = {
            yellowRound: '#FFD700',
            yellowWrinkled: '#FFEB3B',
            greenRound: '#4CAF50',
            greenWrinkled: '#8BC34A',
            geneY: '#2196F3',
            geney: '#BBDEFB',
            geneR: '#FF9800',
            gener: '#FFE0B2',
            background: '#f0f7e6',
            panel: '#FFFFFF'
        };
        
        // 豌豆对象
        class Pea {
            constructor(x, y, genotype, phenotype) {
                this.x = x;
                this.y = y;
                this.genotype = genotype; // 如 "YyRr"
                this.phenotype = phenotype; // "yellowRound", "yellowWrinkled", "greenRound", "greenWrinkled"
                this.radius = 15;
                this.vx = (Math.random() - 0.5) * 4;
                this.vy = Math.random() * 3 + 2;
                this.rotation = 0;
                this.rotationSpeed = (Math.random() - 0.5) * 0.1;
                this.life = 1;
            }
            
            update() {
                this.x += this.vx;
                this.y += this.vy;
                this.rotation += this.rotationSpeed;
                
                // 边界反弹
                if (this.x < this.radius || this.x > canvas.width - this.radius) {
                    this.vx *= -0.8;
                }
                
                if (this.y > canvas.height - this.radius) {
                    this.vy *= -0.7;
                    this.y = canvas.height - this.radius;
                }
                
                // 重力
                this.vy += 0.1;
                
                // 生命衰减
                this.life -= 0.005;
            }
            
            draw() {
                ctx.save();
                ctx.translate(this.x, this.y);
                ctx.rotate(this.rotation);
                
                // 绘制豌豆主体
                ctx.fillStyle = this.getColor();
                ctx.beginPath();
                ctx.ellipse(0, 0, this.radius, this.radius * 0.8, 0, 0, Math.PI * 2);
                ctx.fill();
                
                // 绘制豌豆纹理
                ctx.strokeStyle = 'rgba(0, 0, 0, 0.1)';
                ctx.lineWidth = 1;
                ctx.beginPath();
                ctx.arc(0, 0, this.radius * 0.7, 0, Math.PI * 2);
                ctx.stroke();
                
                // 如果是皱粒，添加纹理
                if (this.phenotype.includes('Wrinkled')) {
                    ctx.strokeStyle = 'rgba(0, 0, 0, 0.2)';
                    ctx.lineWidth = 1.5;
                    for (let i = 0; i < 5; i++) {
                        ctx.beginPath();
                        ctx.arc(0, 0, this.radius * 0.6, i * 0.4, i * 0.4 + 0.2);
                        ctx.stroke();
                    }
                }
                
                // 绘制基因符号
                ctx.fillStyle = 'white';
                ctx.font = 'bold 10px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                if (experimentMode === 'single') {
                    // 单因子只显示Y/y
                    const gene = this.genotype.charAt(0);
                    ctx.fillStyle = gene === 'Y' ? colors.geneY : colors.geney;
                    ctx.fillText(gene, 0, 0);
                } else {
                    // 双因子显示YR/yr
                    ctx.font = 'bold 8px Arial';
                    ctx.fillStyle = this.genotype.includes('Y') ? colors.geneY : colors.geney;
                    ctx.fillText(this.genotype.charAt(0), -5, -5);
                    ctx.fillText(this.genotype.charAt(1), 5, -5);
                    ctx.fillStyle = this.genotype.includes('R') ? colors.geneR : colors.gener;
                    ctx.fillText(this.genotype.charAt(2), -5, 5);
                    ctx.fillText(this.genotype.charAt(3), 5, 5);
                }
                
                ctx.restore();
            }
            
            getColor() {
                switch(this.phenotype) {
                    case 'yellowRound': return colors.yellowRound;
                    case 'yellowWrinkled': return colors.yellowWrinkled;
                    case 'greenRound': return colors.greenRound;
                    case 'greenWrinkled': return colors.greenWrinkled;
                    default: return '#CCCCCC';
                }
            }
            
            isAlive() {
                return this.life > 0;
            }
        }
        
        // 配子对象
        class Gamete {
            constructor(x, y, alleles) {
                this.x = x;
                this.y = y;
                this.alleles = alleles; // 如 "YR", "Yr", "yR", "yr"
                this.radius = 12;
                this.targetX = x;
                this.targetY = y;
                this.speed = 2;
                this.active = false;
            }
            
            update() {
                if (this.active) {
                    const dx = this.targetX - this.x;
                    const dy = this.targetY - this.y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    if (distance > 1) {
                        this.x += (dx / distance) * this.speed;
                        this.y += (dy / distance) * this.speed;
                    }
                }
            }
            
            draw() {
                ctx.save();
                ctx.translate(this.x, this.y);
                
                // 绘制配子圆形
                ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                ctx.strokeStyle = '#2196F3';
                ctx.lineWidth = 2;
                ctx.beginPath();
                ctx.arc(0, 0, this.radius, 0, Math.PI * 2);
                ctx.fill();
                ctx.stroke();
                
                // 绘制等位基因符号
                ctx.fillStyle = '#333';
                ctx.font = 'bold 12px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                
                if (experimentMode === 'single') {
                    const allele = this.alleles.charAt(0);
                    ctx.fillStyle = allele === 'Y' ? colors.geneY : colors.geney;
                    ctx.fillText(allele, 0, 0);
                } else {
                    ctx.font = 'bold 10px Arial';
                    const allele1 = this.alleles.charAt(0);
                    const allele2 = this.alleles.charAt(1);
                    ctx.fillStyle = allele1 === 'Y' ? colors.geneY : colors.geney;
                    ctx.fillText(allele1, -6, 0);
                    ctx.fillStyle = allele2 === 'R' ? colors.geneR : colors.gener;
                    ctx.fillText(allele2, 6, 0);
                }
                
                ctx.restore();
            }
            
            moveTo(x, y) {
                this.targetX = x;
                this.targetY = y;
                this.active = true;
            }
        }
        
        // 豌豆数组
        let peas = [];
        let gametes1 = []; // 母本配子
        let gametes2 = []; // 父本配子
        let activeGametes = [];
        
        // 初始化Canvas
        function initCanvas() {
            canvas = document.getElementById('animationCanvas');
            ctx = canvas.getContext('2d');
            
            // 设置Canvas尺寸
            const container = canvas.parentElement;
            canvas.width = container.clientWidth;
            canvas.height = container.clientHeight;
            
            // 监听窗口大小变化
            window.addEventListener('resize', () => {
                canvas.width = container.clientWidth;
                canvas.height = container.clientHeight;
                drawStaticElements();
            });
            
            drawStaticElements();
        }
        
        // 绘制静态元素
        function drawStaticElements() {
            ctx.fillStyle = colors.background;
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // 绘制标题
            ctx.fillStyle = '#2E7D32';
            ctx.font = 'bold 20px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('孟德尔豌豆杂交实验模拟', canvas.width / 2, 30);
            
            // 绘制亲本区域
            const parentAreaHeight = 100;
            
            // 母本区域
            ctx.fillStyle = 'rgba(33, 150, 243, 0.1)';
            ctx.fillRect(50, 60, canvas.width / 2 - 70, parentAreaHeight);
            ctx.strokeStyle = '#2196F3';
            ctx.lineWidth = 2;
            ctx.strokeRect(50, 60, canvas.width / 2 - 70, parentAreaHeight);
            
            ctx.fillStyle = '#2196F3';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('母本 P1', 50 + (canvas.width / 2 - 70) / 2, 85);
            ctx.font = '14px Arial';
            ctx.fillText(parent1, 50 + (canvas.width / 2 - 70) / 2, 110);
            
            // 父本区域
            ctx.fillStyle = 'rgba(76, 175, 80, 0.1)';
            ctx.fillRect(canvas.width / 2 + 20, 60, canvas.width / 2 - 70, parentAreaHeight);
            ctx.strokeStyle = '#4CAF50';
            ctx.lineWidth = 2;
            ctx.strokeRect(canvas.width / 2 + 20, 60, canvas.width / 2 - 70, parentAreaHeight);
            
            ctx.fillStyle = '#4CAF50';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('父本 P2', canvas.width / 2 + 20 + (canvas.width / 2 - 70) / 2, 85);
            ctx.font = '14px Arial';
            ctx.fillText(parent2, canvas.width / 2 + 20 + (canvas.width / 2 - 70) / 2, 110);
            
            // 绘制配子结合区域
            ctx.fillStyle = 'rgba(255, 193, 7, 0.1)';
            ctx.fillRect(canvas.width / 2 - 100, 180, 200, 80);
            ctx.strokeStyle = '#FF9800';
            ctx.lineWidth = 2;
            ctx.strokeRect(canvas.width / 2 - 100, 180, 200, 80);
            
            ctx.fillStyle = '#FF9800';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('配子随机结合区', canvas.width / 2, 210);
            
            // 绘制结果区域
            ctx.fillStyle = 'rgba(156, 39, 176, 0.1)';
            ctx.fillRect(50, 280, canvas.width - 100, canvas.height - 320);
            ctx.strokeStyle = '#9C27B0';
            ctx.lineWidth = 2;
            ctx.strokeRect(50, 280, canvas.width - 100, canvas.height - 320);
            
            ctx.fillStyle = '#9C27B0';
            ctx.font = '16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('子代豌豆结果区', canvas.width / 2, 310);
        }
        
        // 生成配子
        function generateGametes() {
            gametes1 = [];
            gametes2 = [];
            
            // 解析亲本基因型
            const p1Genes = parent1.toUpperCase();
            const p2Genes = parent2.toUpperCase();
            
            // 生成母本配子
            if (experimentMode === 'single') {
                // 单因子杂交
                const alleles1 = p1Genes.substring(0, 2); // 只取第一对基因
                for (let i = 0; i < alleles1.length; i++) {
                    gametes1.push(new Gamete(
                        50 + (canvas.width / 2 - 70) / 2,
                        130,
                        alleles1[i]
                    ));
                }
                
                const alleles2 = p2Genes.substring(0, 2);
                for (let i = 0; i < alleles2.length; i++) {
                    gametes2.push(new Gamete(
                        canvas.width / 2 + 20 + (canvas.width / 2 - 70) / 2,
                        130,
                        alleles2[i]
                    ));
                }
            } else {
                // 双因子杂交
                const p1Alleles = [
                    p1Genes[0] + p1Genes[2], // YR
                    p1Genes[0] + p1Genes[3], // Yr
                    p1Genes[1] + p1Genes[2], // yR
                    p1Genes[1] + p1Genes[3]  // yr
                ];
                
                const p2Alleles = [
                    p2Genes[0] + p2Genes[2], // YR
                    p2Genes[0] + p2Genes[3], // Yr
                    p2Genes[1] + p2Genes[2], // yR
                    p2Genes[1] + p2Genes[3]  // yr
                ];
                
                // 去除重复的配子类型
                const uniqueP1Alleles = [...new Set(p1Alleles)];
                const uniqueP2Alleles = [...new Set(p2Alleles)];
                
                // 创建配子对象
                uniqueP1Alleles.forEach((alleles, index) => {
                    gametes1.push(new Gamete(
                        50 + (canvas.width / 2 - 70) / 2,
                        100 + index * 25,
                        alleles
                    ));
                });
                
                uniqueP2Alleles.forEach((alleles, index) => {
                    gametes2.push(new Gamete(
                        canvas.width / 2 + 20 + (canvas.width / 2 - 70) / 2,
                        100 + index * 25,
                        alleles
                    ));
                });
            }
        }
        
        // 执行一次杂交
        function performCross() {
            if (currentStep >= totalPeas) {
                stopAnimation();
                return;
            }
            
            // 选择随机配子
            const randomGamete1 = gametes1[Math.floor(Math.random() * gametes1.length)];
            const randomGamete2 = gametes2[Math.floor(Math.random() * gametes2.length)];
            
            // 复制配子用于动画
            const gamete1Copy = new Gamete(randomGamete1.x, randomGamete1.y, randomGamete1.alleles);
            const gamete2Copy = new Gamete(randomGamete2.x, randomGamete2.y, randomGamete2.alleles);
            
            // 设置配子移动目标
            const meetingX = canvas.width / 2;
            const meetingY = 220;
            
            gamete1Copy.moveTo(meetingX - 20, meetingY);
            gamete2Copy.moveTo(meetingX + 20, meetingY);
            
            activeGametes.push(gamete1Copy, gamete2Copy);
            
            // 延迟生成豌豆，等待配子动画
            setTimeout(() => {
                // 结合配子生成基因型
                let genotype;
                if (experimentMode === 'single') {
                    genotype = gamete1Copy.alleles + gamete2Copy.alleles;
                } else {
                    genotype = 
                        gamete1Copy.alleles[0] + gamete2Copy.alleles[0] + 
                        gamete1Copy.alleles[1] + gamete2Copy.alleles[1];
                }
                
                // 确定表现型
                const phenotype = determinePhenotype(genotype);
                
                // 更新统计
                updateResults(phenotype);
                
                // 创建豌豆
                const peaX = meetingX;
                const peaY = meetingY + 30;
                const newPea = new Pea(peaX, peaY, genotype, phenotype);
                
                // 给豌豆一个向上的初速度
                newPea.vy = -5;
                newPea.vx = (Math.random() - 0.5) * 6;
                
                peas.push(newPea);
                
                // 从活动配子中移除
                const index1 = activeGametes.indexOf(gamete1Copy);
                const index2 = activeGametes.indexOf(gamete2Copy);
                if (index1 > -1) activeGametes.splice(index1, 1);
                if (index2 > -1) activeGametes.splice(index2, 1);
                
                currentStep++;
                updateStatsDisplay();
                
                // 如果动画进行中且未暂停，继续下一步
                if (isAnimating && !isPaused && currentStep < totalPeas) {
                    setTimeout(performCross, 1000 / simulationSpeed);
                }
            }, showAnimation ? 800 : 100);
        }
        
        // 根据基因型确定表现型
        function determinePhenotype(genotype) {
            if (experimentMode === 'single') {
                // 单因子：只考虑颜色
                return genotype.includes('Y') ? 'yellowRound' : 'greenRound';
            } else {
                // 双因子：考虑颜色和形状
                const hasY = genotype.includes('Y');
                const hasR = genotype.includes('R');
                
                if (hasY && hasR) return 'yellowRound';
                if (hasY && !hasR) return 'yellowWrinkled';
                if (!hasY && hasR) return 'greenRound';
                return 'greenWrinkled';
            }
        }
        
        // 更新统计结果
        function updateResults(phenotype) {
            switch(phenotype) {
                case 'yellowRound':
                    results.yellowRound++;
                    break;
                case 'yellowWrinkled':
                    results.yellowWrinkled++;
                    break;
                case 'greenRound':
                    results.greenRound++;
                    break;
                case 'greenWrinkled':
                    results.greenWrinkled++;
                    break;
            }
        }
        
        // 更新统计显示
        function updateStatsDisplay() {
            const statsContainer = document.getElementById('statsContainer');
            const total = currentStep;
            
            // 清空容器
            statsContainer.innerHTML = '';
            
            // 根据实验模式显示不同的统计
            if (experimentMode === 'single') {
                // 单因子：黄色 vs 绿色
                const yellowCount = results.yellowRound;
                const greenCount = results.greenRound;
                
                const yellowPercent = total > 0 ? ((yellowCount / total) * 100).toFixed(1) : 0;
                const greenPercent = total > 0 ? ((greenCount / total) * 100).toFixed(1) : 0;
                
                statsContainer.innerHTML = `
                    <div class="stat-box" style="background-color: ${colors.yellowRound}">
                        <div class="stat-label">黄色豌豆</div>
                        <div class="stat-value">${yellowCount}</div>
                        <div>${yellowPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: ${colors.greenRound}">
                        <div class="stat-label">绿色豌豆</div>
                        <div class="stat-value">${greenCount}</div>
                        <div>${greenPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: #9C27B0">
                        <div class="stat-label">总计</div>
                        <div class="stat-value">${total}</div>
                        <div>100%</div>
                    </div>
                `;
            } else {
                // 双因子：四种表现型
                const yellowRoundCount = results.yellowRound;
                const yellowWrinkledCount = results.yellowWrinkled;
                const greenRoundCount = results.greenRound;
                const greenWrinkledCount = results.greenWrinkled;
                
                const yrPercent = total > 0 ? ((yellowRoundCount / total) * 100).toFixed(1) : 0;
                const ywPercent = total > 0 ? ((yellowWrinkledCount / total) * 100).toFixed(1) : 0;
                const grPercent = total > 0 ? ((greenRoundCount / total) * 100).toFixed(1) : 0;
                const gwPercent = total > 0 ? ((greenWrinkledCount / total) * 100).toFixed(1) : 0;
                
                statsContainer.innerHTML = `
                    <div class="stat-box" style="background-color: ${colors
<!--检测到代码截断，自动续写中...-->
yellowRound}">
                        <div class="stat-label">黄色圆粒</div>
                        <div class="stat-value">${yellowRoundCount}</div>
                        <div>${yrPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: ${colors.yellowWrinkled}">
                        <div class="stat-label">黄色皱粒</div>
                        <div class="stat-value">${yellowWrinkledCount}</div>
                        <div>${ywPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: ${colors.greenRound}">
                        <div class="stat-label">绿色圆粒</div>
                        <div class="stat-value">${greenRoundCount}</div>
                        <div>${grPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: ${colors.greenWrinkled}">
                        <div class="stat-label">绿色皱粒</div>
                        <div class="stat-value">${greenWrinkledCount}</div>
                        <div>${gwPercent}%</div>
                    </div>
                    <div class="stat-box" style="background-color: #9C27B0">
                        <div class="stat-label">总计</div>
                        <div class="stat-value">${total}</div>
                        <div>100%</div>
                    </div>
                `;
            }
            
            // 更新图表
            updateChart();
            
            // 更新理论比例信息
            updateTheoryInfo();
        }
        
        // 更新图表
        function updateChart() {
            const chartContainer = document.getElementById('chartContainer');
            const total = currentStep;
            
            if (total === 0) {
                chartContainer.innerHTML = '<p style="text-align: center; color: #666; margin-top: 50px;">模拟开始后，图表将在此显示</p>';
                return;
            }
            
            // 计算高度比例
            let maxCount = 0;
            let categories = [];
            let counts = [];
            let colorList = [];
            
            if (experimentMode === 'single') {
                categories = ['黄色豌豆', '绿色豌豆'];
                counts = [results.yellowRound, results.greenRound];
                colorList = [colors.yellowRound, colors.greenRound];
            } else {
                categories = ['黄色圆粒', '黄色皱粒', '绿色圆粒', '绿色皱粒'];
                counts = [results.yellowRound, results.yellowWrinkled, results.greenRound, results.greenWrinkled];
                colorList = [colors.yellowRound, colors.yellowWrinkled, colors.greenRound, colors.greenWrinkled];
            }
            
            maxCount = Math.max(...counts);
            const chartHeight = 200;
            
            // 生成图表HTML
            let chartHTML = '<div style="position: relative; height: 100%;">';
            
            categories.forEach((category, index) => {
                const count = counts[index];
                const percent = total > 0 ? ((count / total) * 100).toFixed(1) : 0;
                const height = maxCount > 0 ? (count / maxCount) * chartHeight : 0;
                const left = 50 + (index * 120); // 条形图位置
                
                chartHTML += `
                    <div class="chart-bar" style="left: ${left}px; height: ${height}px; background-color: ${colorList[index]}">
                        <div style="margin-bottom: 5px;">${count}</div>
                        <div>${percent}%</div>
                    </div>
                    <div class="theory-label" style="left: ${left}px;">${category}</div>
                `;
            });
            
            chartHTML += '</div>';
            chartContainer.innerHTML = chartHTML;
        }
        
        // 更新理论比例信息
        function updateTheoryInfo() {
            const theoryInfo = document.getElementById('theoryInfo');
            let theoryHTML = '';
            
            if (experimentMode === 'single') {
                // 单因子杂交理论比例
                const p1 = parent1.toUpperCase();
                const p2 = parent2.toUpperCase();
                
                // 判断杂交类型
                const isHeterozygous = (p1[0] !== p1[1]) || (p2[0] !== p2[1]);
                const hasDominant = p1.includes('Y') || p2.includes('Y');
                const hasRecessive = p1.includes('y') || p2.includes('y');
                
                if (isHeterozygous && hasDominant && hasRecessive) {
                    // 杂合子杂交：3:1
                    theoryHTML = '<p>理论比例：黄色 : 绿色 = 3 : 1</p>';
                } else if (!p1.includes('y') && !p2.includes('y')) {
                    // 纯合显性：全部黄色
                    theoryHTML = '<p>理论比例：全部为黄色豌豆</p>';
                } else if (!p1.includes('Y') && !p2.includes('Y')) {
                    // 纯合隐性：全部绿色
                    theoryHTML = '<p>理论比例：全部为绿色豌豆</p>';
                } else {
                    theoryHTML = '<p>理论比例：黄色 : 绿色 = 1 : 1 (测交比例)</p>';
                }
            } else {
                // 双因子杂交理论比例
                const p1 = parent1.toUpperCase();
                const p2 = parent2.toUpperCase();
                
                // 判断是否为经典双杂合子杂交
                const isClassicCross = 
                    (p1 === 'YYRR' || p1 === 'YYRr' || p1 === 'YyRR' || p1 === 'YyRr') &&
                    (p2 === 'yyrr') ||
                    (p1 === 'yyrr') &&
                    (p2 === 'YYRR' || p2 === 'YYRr' || p2 === 'YyRR' || p2 === 'YyRr');
                
                if (isClassicCross) {
                    theoryHTML = `
                        <p>理论比例（孟德尔经典实验）：</p>
                        <p>黄色圆粒 : 黄色皱粒 : 绿色圆粒 : 绿色皱粒 = 9 : 3 : 3 : 1</p>
                    `;
                } else {
                    theoryHTML = '<p>根据所选亲本基因型，理论比例会有所不同。请参考遗传学教材中的棋盘格分析法。</p>';
                }
            }
            
            // 添加当前比例
            const total = currentStep;
            if (total > 0) {
                if (experimentMode === 'single') {
                    const yellowCount = results.yellowRound;
                    const greenCount = results.greenRound;
                    theoryHTML += `<p>当前比例：黄色 : 绿色 = ${yellowCount} : ${greenCount}</p>`;
                } else {
                    theoryHTML += `
                        <p>当前比例：黄圆:黄皱:绿圆:绿皱 = 
                        ${results.yellowRound}:${results.yellowWrinkled}:${results.greenRound}:${results.greenWrinkled}</p>
                    `;
                }
            }
            
            theoryInfo.innerHTML = theoryHTML;
        }
        
        // 动画循环
        function animate() {
            // 清除画布
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // 绘制静态元素
            drawStaticElements();
            
            // 更新和绘制配子
            activeGametes.forEach(gamete => {
                gamete.update();
                gamete.draw();
            });
            
            // 更新和绘制豌豆
            for (let i = peas.length - 1; i >= 0; i--) {
                peas[i].update();
                peas[i].draw();
                
                // 移除消失的豌豆
                if (!peas[i].isAlive()) {
                    peas.splice(i, 1);
                }
            }
            
            // 绘制配子池中的配子
            gametes1.forEach(gamete => gamete.draw());
            gametes2.forEach(gamete => gamete.draw());
            
            // 绘制进度
            ctx.fillStyle = '#333';
            ctx.font = '16px Arial';
            ctx.textAlign = 'left';
            ctx.fillText(`进度: ${currentStep}/${totalPeas} (${((currentStep/totalPeas)*100).toFixed(1)}%)`, 20, canvas.height - 20);
            
            // 继续动画循环
            if (isAnimating && !isPaused) {
                animationId = requestAnimationFrame(animate);
            }
        }
        
        // 开始动画
        function startAnimation() {
            if (isAnimating) return;
            
            isAnimating = true;
            isPaused = false;
            
            // 生成配子
            generateGametes();
            
            // 开始动画循环
            animate();
            
            // 开始杂交过程
            performCross();
            
            // 更新按钮状态
            document.getElementById('startBtn').disabled = true;
            document.getElementById('pauseBtn').disabled = false;
        }
        
        // 单步演示
        function stepAnimation() {
            if (!isAnimating) {
                // 如果未开始，先初始化
                generateGametes();
                isAnimating = true;
                animate();
            }
            
            if (currentStep < totalPeas) {
                performCross();
            }
        }
        
        // 暂停动画
        function pauseAnimation() {
            isPaused = !isPaused;
            
            if (isPaused) {
                document.getElementById('pauseBtn').innerHTML = '<span>▶ 继续</span>';
            } else {
                document.getElementById('pauseBtn').innerHTML = '<span>⏸ 暂停</span>';
                animate();
                
                // 如果还有豌豆要生成，继续杂交过程
                if (currentStep < totalPeas) {
                    setTimeout(performCross, 1000 / simulationSpeed);
                }
            }
        }
        
        // 停止动画
        function stopAnimation() {
            isAnimating = false;
            isPaused = false;
            
            if (animationId) {
                cancelAnimationFrame(animationId);
                animationId = null;
            }
            
            // 更新按钮状态
            document.getElementById('startBtn').disabled = false;
            document.getElementById('pauseBtn').disabled = true;
            document.getElementById('pauseBtn').innerHTML = '<span>⏸ 暂停</span>';
        }
        
        // 重置实验
        function resetExperiment() {
            stopAnimation();
            
            // 重置变量
            currentStep = 0;
            results = {
                yellowRound: 0,
                yellowWrinkled: 0,
                greenRound: 0,
                greenWrinkled: 0
            };
            
            peas = [];
            gametes1 = [];
            gametes2 = [];
            activeGametes = [];
            
            // 更新显示
            updateStatsDisplay();
            drawStaticElements();
        }
        
        // 初始化事件监听
        function initEventListeners() {
            // 实验模式切换
            document.getElementById('experimentMode').addEventListener('change', function() {
                experimentMode = this.value;
                resetExperiment();
            });
            
            // 豌豆数量滑块
            const peaCountSlider = document.getElementById('peaCount');
            const peaCountValue = document.getElementById('peaCountValue');
            
            peaCountSlider.addEventListener('input', function() {
                totalPeas = parseInt(this.value);
                peaCountValue.textContent = totalPeas.toLocaleString();
            });
            
            // 速度滑块
            const speedSlider = document.getElementById('speed');
            const speedValue = document.getElementById('speedValue');
            
            speedSlider.addEventListener('input', function() {
                simulationSpeed = parseInt(this.value);
                speedValue.textContent = simulationSpeed;
            });
            
            // 亲本选择
            document.getElementById('parent1').addEventListener('change', function() {
                parent1 = this.value;
                resetExperiment();
            });
            
            document.getElementById('parent2').addEventListener('change', function() {
                parent2 = this.value;
                resetExperiment();
            });
            
            // 动画显示控制
            document.getElementById('showAnimation').addEventListener('change', function() {
                showAnimation = this.checked;
            });
            
            // 按钮事件
            document.getElementById('startBtn').addEventListener('click', startAnimation);
            document.getElementById('stepBtn').addEventListener('click', stepAnimation);
            document.getElementById('pauseBtn').addEventListener('click', pauseAnimation);
            document.getElementById('resetBtn').addEventListener('click', resetExperiment);
            
            // 初始禁用暂停按钮
            document.getElementById('pauseBtn').disabled = true;
        }
        
        // 页面加载完成后初始化
        window.addEventListener('load', function() {
            initCanvas();
            initEventListeners();
            updateStatsDisplay();
            updateTheoryInfo();
        });
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 孟德尔豌豆杂交实验交互式教学动画使用指南

欢迎使用这款精心设计的孟德尔豌豆杂交实验动态模拟工具！本指南将帮助您充分利用这一教学资源，深入理解遗传学的核心定律。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas技术的交互式模拟程序，旨在将孟德尔经典豌豆杂交实验（基因分离定律与自由组合定律）从抽象的理论和静态的棋盘格，转化为**动态、可视、可交互**的学习体验。它允许您模拟数千颗豌豆的杂交过程，直观地观察遗传规律如何从随机事件中涌现。

### 二、 主要功能

1.  **实验模式切换**
    *   **单因子杂交模式**：专注于一对等位基因（如颜色Y/y），演示基因分离定律。
    *   **双因子杂交模式**：同时研究两对等位基因（颜色Y/y和形状R/r），演示自由组合定律。这是默认的经典实验模式。

2.  **实验参数自定义**
    *   **亲本基因型选择**：可从下拉菜单中为母本(P1)和父本(P2)选择不同的基因型组合，从纯合到杂合，探索不同杂交组合的结果。
    *   **模拟规模控制**：通过滑块设置每轮实验生成的子代豌豆数量（100至10,000颗），体验“大数定律”——数量越大，结果越接近理论比例。
    *   **模拟速度调节**：控制动画播放速度，便于细致观察或快速获得统计结果。

3.  **模拟过程控制**
    *   **开始模拟**：启动完整的动态杂交过程，包括配子形成、随机结合和子代生成。
    *   **单步演示**：一次只生成一颗子代豌豆，适合逐步讲解和观察细节。
    *   **暂停/继续**：随时暂停动画，观察某一瞬间的状态，然后继续。
    *   **重置**：清空所有结果，恢复到初始状态，以便开始新的实验。

4.  **可视化呈现**
    *   **动态动画区**：在画布上实时展示亲本、配子（带有基因符号）、配子随机结合以及子代豌豆“生长”的全过程。
    *   **实时统计面板**：以彩色统计框和百分比数字，即时更新各表现型的数量与比例。
    *   **动态柱状图**：随着模拟进行，柱状图同步增长，直观对比不同表现型的数量差异。
    *   **理论比例参考**：面板始终显示当前实验组合对应的理论预期比例，方便与实际结果对比。

### 三、 设计特色

1.  **符合认知规律**：遵循“从微观过程（配子形成）到宏观结果（性状统计）”的认知路径，将复杂过程分解。
2.  **双重编码学习**：
    *   **视觉编码**：用特定颜色（黄/绿）和形状（圆滑/皱褶纹理）直观表示豌豆的表现型；用不同颜色（深蓝/浅蓝，深橙/浅橙）区分显隐性等位基因。
    *   **符号编码**：保留经典的基因符号（Y, y, R, r），建立与教材知识的直接联系。
3.  **探究式学习环境**：通过允许用户自由改变亲本基因型和实验规模，变“验证结论”为“发现规律”，鼓励猜想与验证。
4.  **游戏化与美感**：豌豆和配子的物理运动（弹跳、下落）增加了趣味性；清新护眼的配色和流畅的动画提供了愉悦的学习体验。

### 四、 教学要点

本工具可用于演示和探究以下核心概念：

1.  **基因分离定律**（单因子模式）：
    *   展示一对等位基因在形成配子时如何分离。
    *   观察杂合子自交（如 Yy × Yy）如何产生接近 3:1 的子代表现型比例。
    *   进行测交实验（如 Yy × yy），验证 1:1 的比例。

2.  **自由组合定律**（双因子模式）：
    *   展示两对等位基因如何独立分配和自由组合形成配子（YR, Yr, yR, yr）。
    *   经典双杂合子杂交（YyRr × YyRr）是重点，动态积累大量数据后，引导学生发现 **9:3:3:1** 的比例是如何出现的。
    *   理解“随机受精”是产生特定比例的关键。

3.  **基因型与表现型的关系**：
    *   通过观察相同表现型（如黄色圆粒）可能对应不同基因型（YYRR, YYRr, YyRR, YyRr），深化对这两个概念区别的理解。

4.  **概率与统计**：
    *   通过调整模拟数量（如从100颗到5000颗），让学生直观感受：**样本量越小，实际比例波动越大；样本量越大，实际比例越稳定地趋近理论概率**。这是理解遗传学统计本质的绝佳方式。

### 五、 使用建议

1.  **课堂教学演示**：
    *   **引入环节**：用“单步演示”模式，慢速展示一对配子从亲本产生、结合到形成一颗豌豆的全过程，讲解基本概念。
    *   **核心讲解环节**：切换到“双因子模式”，使用经典亲本（YYRR × yyrr 或 YyRr × YyRr），以中等速度（约500-1000颗）运行模拟。引导学生观察配子类型和子代豌豆的积累。
    *   **总结环节**：暂停模拟，将实时统计结果与理论比例对比，展开讨论。

2.  **学生自主探究**：
    *   **布置探究任务**：例如：“如果亲本改为 YYrr × yyRR，预测并验证子代的表现型比例。”
    *   **鼓励记录数据**：让学生在不同参数下运行多次实验，记录数据，计算比例，并撰写简短的实验报告。
    *   **挑战问题**：“如何设计实验来验证某个黄色圆粒豌豆的基因型？”让学生利用工具模拟测交实验。

3.  **效率与观察平衡**：
    *   初次学习时，**开启“显示配子动画”**，观察完整过程。
    *   进行重复实验或验证时，可以**关闭动画**，并调高速度，以快速获得统计结果。

4.  **结合传统教学**：
    *   本工具是强大的补充，而非替代。建议与绘制**棋盘格（Punnett Square）** 结合使用。动画展示了“过程”和“统计”，棋盘格则清晰地列出了“所有可能的基因型及其概率”。

希望这款交互式动画能成为您探索遗传学奥秘的得力助手，让孟德尔的经典实验在数字时代焕发新的活力，激发学生们对生命科学的好奇与热爱！