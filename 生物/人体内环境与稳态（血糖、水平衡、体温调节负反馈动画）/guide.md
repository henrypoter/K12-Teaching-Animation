# 需求：人体内环境与稳态（血糖、水平衡、体温调节负反馈动画）

### 1. 专业思考

### 1. 专业思考

#### 用户需求分析
本动画的目标用户是高中生物学或医学预科的学生。他们的核心需求是：
1.  **理解抽象概念**：将“负反馈调节”这一抽象生理学机制，通过动态、可视化的方式具象化，降低认知负荷。
2.  **建立系统关联**：理解血糖、水平衡、体温调节并非孤立过程，而是共享“传感器-控制中心-效应器”这一基本调节模式，共同维持内环境稳态。
3.  **掌握动态过程**：清晰看到稳态被打破（刺激）到恢复（响应）的完整因果链条和循环过程，而非记忆静态结论。
4.  **激发学习兴趣**：通过交互和生动的视觉表现，将枯燥的生理学知识转化为引人入胜的探索过程。

#### 教学设计思路
*   **核心概念**：围绕“**稳态**”与“**负反馈调节**”两个核心概念展开。动画将展示，当内环境参数（血糖浓度、体液渗透压、体温）偏离设定点（如血糖：~5.6 mmol/L）时，机体通过一系列检测、决策和执行步骤，产生对抗偏离方向的变化，最终使参数回归正常范围。
*   **认知规律**：
    *   **从具体到抽象，再归纳共性**：先分别、详细地演示三个具体调节实例（血糖、水、体温），让学生建立感性认识。然后通过对比和总结，抽象出通用的“负反馈调节模型”。
    *   **分步引导**：每个调节实例都分解为“稳态→偏离→检测→传递→决策→执行→恢复”的清晰步骤，并用高亮、箭头、文字标签同步提示。
    *   **主动建构**：通过交互（如拖动滑块改变初始值、点击触发调节步骤），让学生成为变化的“发起者”和过程的“推动者”，在操作中深化理解。
*   **交互设计**：
    *   **模块化导航**：顶部或侧边设有“血糖调节”、“水平衡调节”、“体温调节”、“模型总结”四个标签页，允许学生按需学习或对比。
    *   **参数控制台**：每个模块配备简易控制面板（如滑块、按钮），用于“设定”初始偏离状态（如“升高血糖”、“降低体温”）。
    *   **分步播放/连续播放**：提供“下一步”按钮供分步学习，也提供“播放/暂停”按钮观看连续动画。
    *   **动态图示与标签**：关键结构和物质（如胰岛、下丘脑、激素、感受器）在激活时高亮并显示名称和当前作用。
*   **视觉呈现**：
    *   **主体采用示意图风格**：人体或器官采用简洁、卡通化的矢量图形，突出功能而非解剖细节。例如，用一个大水箱代表体液，用火焰图标代表产热。
    *   **数据可视化**：在画面一侧动态绘制关键参数（血糖浓度、渗透压、体温）随时间变化的曲线图，直观展示“偏离-回归-稳定”的过程。
    *   **流程可视化**：使用彩色箭头（如红色代表“升高”信号，蓝色代表“降低”信号）和粒子流动效果（代表神经冲动、激素运输）来表现信息流和物质流。
    *   **对比色强调**：用对比色高亮当前正在活动的调节路径，非活动部分灰度化，减少视觉干扰。

#### 配色方案选择
*   **主色调**：采用温和、专业的科技蓝（`#4A90E2`）作为界面主色，象征理性、科学与人体系统的精密。
*   **辅助色与语义色**：
    *   **警报/升高**：暖色系。如橙色（`#FF9500`）代表血糖升高、体温升高；红色（`#FF3B30`）用于警告标识。
    *   **纠正/降低**：冷色系。如蓝色（`#007AFF`）代表胰岛素作用、体温散热；绿色（`#34C759`）代表恢复稳态、正常范围。
    *   **中性背景**：浅灰色（`#F5F5F7`）作为画布背景，深灰色（`#8E8E93`）用于注释文字和次要元素。
    *   **生物组织**：采用柔和的肉粉色（`#FFD6CC`）代表人体轮廓，用不同的柔和色区分主要器官（如肝脏用土黄色，胰腺用淡紫色）。
*   **原则**：保证色彩对比度满足可访问性标准，且配色有助于传达信息（如红/蓝直接对应升高/降低的生理变化），而非仅为装饰。

#### 交互功能列表
1.  **全局导航**：点击标签在“血糖”、“水平衡”、“体温”、“总结”四个模块间切换。
2.  **情景初始化**：
    *   **血糖模块**：滑块模拟“摄入葡萄糖”或“运动消耗”，设定初始血糖水平（高/低）。
    *   **水平衡模块**：按钮模拟“大量出汗”（失水）或“饮用盐水”（渗透压升高）。
    *   **体温模块**：滑块模拟“环境温度”变化或按钮模拟“剧烈运动”。
3.  **动画控制**：
    *   “**播放/暂停**”按钮：开始或暂停连续的调节动画。
    *   “**下一步**”按钮：手动控制，逐步展示调节过程的每一个关键阶段，并伴有文字解说。
    *   “**重置**”按钮：将动画恢复至初始稳态状态。
4.  **焦点提示**：鼠标悬停在关键器官、激素或流程箭头上时，显示更详细的名称和功能说明卡片。
5.  **动态图表**：实时绘制并高亮显示参数变化曲线，可点击曲线上的点查看对应时刻的生理状态说明。
6.  **模型总结页**：
    *   可拖动的通用“传感器”、“控制中心”、“效应器”组件图标。
    *   一个空的调节环路图，让学生将三个实例中的具体组件（如“下丘脑渗透压感受器”、“胰岛B细胞”、“汗腺”）拖拽到通用模型的对应位置，完成知识建构。
    *   “检查答案”按钮，提供反馈。

### 2. HTML_CODE

### 2. HTML_CODE

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>人体内环境与稳态调节动画</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
        }

        body {
            background-color: #F5F5F7;
            color: #333;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 2px solid #4A90E2;
        }

        .header h1 {
            color: #4A90E2;
            margin-bottom: 10px;
            font-size: 2.2em;
        }

        .header p {
            color: #8E8E93;
            font-size: 1.1em;
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.5;
        }

        .main-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .tabs {
            display: flex;
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .tab {
            flex: 1;
            padding: 18px 10px;
            text-align: center;
            background-color: #f8f9fa;
            border: none;
            font-size: 1.1em;
            font-weight: 600;
            color: #666;
            cursor: pointer;
            transition: all 0.3s ease;
            border-bottom: 3px solid transparent;
        }

        .tab:hover {
            background-color: #e9ecef;
        }

        .tab.active {
            background-color: white;
            color: #4A90E2;
            border-bottom: 3px solid #4A90E2;
        }

        .content-area {
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .animation-section {
            background-color: white;
            border-radius: 12px;
            padding: 25px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            display: flex;
            flex-direction: column;
            gap: 25px;
        }

        .animation-title {
            color: #4A90E2;
            font-size: 1.6em;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .animation-title .icon {
            width: 36px;
            height: 36px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
        }

        #glucose-title .icon { background-color: #FF9500; }
        #water-title .icon { background-color: #007AFF; }
        #temp-title .icon { background-color: #FF3B30; }
        #model-title .icon { background-color: #34C759; }

        .animation-container {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }

        .canvas-container {
            flex: 1;
            min-width: 300px;
            min-height: 400px;
            border-radius: 8px;
            overflow: hidden;
            background-color: #f8f9fa;
            position: relative;
        }

        canvas {
            display: block;
            width: 100%;
            height: 100%;
        }

        .controls-container {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .control-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
        }

        .control-panel h3 {
            color: #555;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .scenario-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 20px;
        }

        .scenario-btn {
            padding: 10px 15px;
            border: none;
            border-radius: 6px;
            background-color: #e9ecef;
            color: #555;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            min-width: 120px;
        }

        .scenario-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .glucose-btn.increase { background-color: #FF9500; color: white; }
        .glucose-btn.decrease { background-color: #007AFF; color: white; }
        .water-btn.lose { background-color: #FF9500; color: white; }
        .water-btn.salt { background-color: #FF3B30; color: white; }
        .temp-btn.hot { background-color: #FF3B30; color: white; }
        .temp-btn.cold { background-color: #007AFF; color: white; }
        .temp-btn.exercise { background-color: #FF9500; color: white; }

        .slider-container {
            margin-bottom: 20px;
        }

        .slider-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            color: #555;
        }

        .slider {
            width: 100%;
            height: 8px;
            -webkit-appearance: none;
            appearance: none;
            background: #ddd;
            border-radius: 4px;
            outline: none;
        }

        .slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            appearance: none;
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: #4A90E2;
            cursor: pointer;
            border: 3px solid white;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }

        .animation-controls {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .anim-btn {
            padding: 12px 20px;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }

        .anim-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .play-btn {
            background-color: #34C759;
            color: white;
        }

        .step-btn {
            background-color: #4A90E2;
            color: white;
        }

        .reset-btn {
            background-color: #8E8E93;
            color: white;
        }

        .chart-container {
            background-color: white;
            border-radius: 8px;
            padding: 15px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            height: 200px;
            margin-top: 10px;
        }

        .info-panel {
            background-color: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            margin-top: 10px;
        }

        .info-panel h3 {
            color: #555;
            margin-bottom: 15px;
            font-size: 1.2em;
        }

        .step-info {
            background-color: white;
            border-radius: 6px;
            padding: 15px;
            margin-bottom: 10px;
            border-left: 4px solid #4A90E2;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }

        .step-info.active {
            border-left-color: #34C759;
            background-color: #f0f9ff;
        }

        .step-info h4 {
            color: #4A90E2;
            margin-bottom: 8px;
            font-size: 1.1em;
        }

        .step-info p {
            color: #666;
            line-height: 1.5;
        }

        .model-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .model-canvas-container {
            height: 400px;
            border-radius: 8px;
            overflow: hidden;
            background-color: #f8f9fa;
            position: relative;
        }

        .model-controls {
            display: flex;
            justify-content: center;
            gap: 15px;
        }

        .model-btn {
            padding: 12px 25px;
            border: none;
            border-radius: 6px;
            background-color: #4A90E2;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.2s ease;
        }

        .model-btn:hover {
            background-color: #3a7bc8;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .model-btn.check {
            background-color: #34C759;
        }

        .hidden {
            display: none !important;
        }

        .feedback {
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
            text-align: center;
            font-weight: 600;
            display: none;
        }

        .feedback.correct {
            background-color: rgba(52, 199, 89, 0.1);
            color: #2a8c4a;
            border: 1px solid #34C759;
        }

        .feedback.incorrect {
            background-color: rgba(255, 59, 48, 0.1);
            color: #c62b2b;
            border: 1px solid #FF3B30;
        }

        @media (max-width: 768px) {
            .animation-container {
                flex-direction: column;
            }
            
            .canvas-container, .controls-container {
                min-width: 100%;
            }
            
            .tabs {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>人体内环境与稳态调节</h1>
        <p>探索人体如何通过负反馈机制维持血糖、水平衡和体温的稳定。交互式动画展示生理调节的精密过程。</p>
    </div>

    <div class="main-container">
        <div class="tabs">
            <button class="tab active" data-tab="glucose">血糖调节</button>
            <button class="tab" data-tab="water">水平衡调节</button>
            <button class="tab" data-tab="temperature">体温调节</button>
            <button class="tab" data-tab="model">模型总结</button>
        </div>

        <div class="content-area">
            <!-- 血糖调节模块 -->
            <div id="glucose-section" class="animation-section">
                <div class="animation-title" id="glucose-title">
                    <div class="icon">G</div>
                    <h2>血糖调节 (负反馈机制)</h2>
                </div>
                
                <div class="animation-container">
                    <div class="canvas-container">
                        <canvas id="glucose-canvas" width="800" height="500"></canvas>
                    </div>
                    
                    <div class="controls-container">
                        <div class="control-panel">
                            <h3>情景模拟</h3>
                            <div class="scenario-buttons">
                                <button class="scenario-btn glucose-btn increase" data-scenario="high-glucose">摄入葡萄糖 (血糖升高)</button>
                                <button class="scenario-btn glucose-btn decrease" data-scenario="low-glucose">运动消耗 (血糖降低)</button>
                            </div>
                            
                            <div class="slider-container">
                                <div class="slider-label">
                                    <span>初始血糖浓度</span>
                                    <span id="glucose-value">5.6 mmol/L (正常)</span>
                                </div>
                                <input type="range" min="2" max="10" step="0.1" value="5.6" class="slider" id="glucose-slider">
                            </div>
                            
                            <div class="animation-controls">
                                <button class="anim-btn play-btn" id="glucose-play">
                                    <span>▶</span> 播放动画
                                </button>
                                <button class="anim-btn step-btn" id="glucose-step">
                                    <span>→</span> 下一步
                                </button>
                                <button class="anim-btn reset-btn" id="glucose-reset">
                                    <span>↺</span> 重置
                                </button>
                            </div>
                        </div>
                        
                        <div class="chart-container">
                            <canvas id="glucose-chart" width="600" height="180"></canvas>
                        </div>
                        
                        <div class="info-panel">
                            <h3>调节步骤</h3>
                            <div class="step-info" id="glucose-step1">
                                <h4>1. 稳态被打破</h4>
                                <p>血糖浓度偏离正常范围 (3.9-6.1 mmol/L)。</p>
                            </div>
                            <div class="step-info" id="glucose-step2">
                                <h4>2. 检测与信号传递</h4>
                                <p>胰岛中的血糖感受器检测到变化，向胰岛B细胞(高血糖)或A细胞(低血糖)发送信号。</p>
                            </div>
                            <div class="step-info" id="glucose-step3">
                                <h4>3. 控制中心响应</h4>
                                <p>胰岛B细胞分泌胰岛素(降血糖)或A细胞分泌胰高血糖素(升血糖)。</p>
                            </div>
                            <div class="step-info" id="glucose-step4">
                                <h4>4. 效应器执行</h4>
                                <p>激素通过血液运输到肝脏、肌肉等靶器官，调节糖原合成/分解、葡萄糖利用。</p>
                            </div>
                            <div class="step-info" id="glucose-step5">
                                <h4>5. 恢复稳态</h4>
                                <p>血糖浓度回归正常范围，激素分泌减少，调节过程减弱。</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 水平衡调节模块 -->
            <div id="water-section" class="animation-section hidden">
                <div class="animation-title" id="water-title">
                    <div class="icon">W</div>
                    <h2>水平衡调节 (渗透压调节)</h2>
                </div>
                
                <div class="animation-container">
                    <div class="canvas-container">
                        <canvas id="water-canvas" width="800" height="500"></canvas>
                    </div>
                    
                    <div class="controls-container">
                        <div class="control-panel">
                            <h3>情景模拟</h3>
                            <div class="scenario-buttons">
                                <button class="scenario-btn water-btn lose" data-scenario="lose-water">大量出汗 (失水)</button>
                                <button class="scenario-btn water-btn salt" data-scenario="drink-salt">饮用盐水 (渗透压升高)</button>
                            </div>
                            
                            <div class="slider-container">
                                <div class="slider-label">
                                    <span>体液渗透压</span>
                                    <span id="osmolarity-value">300 mOsm/L (正常)</span>
                                </div>
                                <input type="range" min="280" max="320" step="1" value="300" class="slider" id="osmolarity-slider">
                            </div>
                            
                            <div class="animation-controls">
                                <button class="anim-btn play-btn" id="water-play">
                                    <span>▶</span> 播放动画
                                </button>
                                <button class="anim-btn step-btn" id="water-step">
                                    <span>→</span> 下一步
                                </button>
                                <button class="anim-btn reset-btn" id="water-reset">
                                    <span>↺</span> 重置
                                </button>
                            </div>
                        </div>
                        
                        <div class="chart-container">
                            <canvas id="water-chart" width="600" height="180"></canvas>
                        </div>
                        
                        <div class="info-panel">
                            <h3>调节步骤</h3>
                            <div class="step-info" id="water-step1">
                                <h4>1. 稳态被打破</h4>
                                <p>体液渗透压偏离正常范围，细胞脱水或水肿。</p>
                            </div>
                            <div class="step-info" id="water-step2">
                                <h4>2. 检测与信号传递</h4>
                                <p>下丘脑渗透压感受器检测到渗透压变化，发送信号至下丘脑合成抗利尿激素(ADH)。</p>
                            </div>
                            <div class="step-info" id="water-step3">
                                <h4>3. 控制中心响应</h4>
                                <p>下丘脑视上核和室旁核合成ADH，垂体后叶释放ADH入血。</p>
                            </div>
                            <div class="step-info" id="water-step4">
                                <h4>4. 效应器执行</h4>
                                <p>ADH作用于肾脏集合管，增加水通道蛋白，促进水重吸收；同时产生渴感，促进行为调节(饮水)。</p>
                            </div>
                            <div class="step-info" id="water-step5">
                                <h4>5. 恢复稳态</h4>
                                <p>体液渗透压恢复正常，ADH分泌减少，尿量恢复正常。</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 体温调节模块 -->
            <div id="temperature-section" class="animation-section hidden">
                <div class="animation-title" id="temp-title">
                    <div class="icon">T</div>
                    <h2>体温调节 (恒温机制)</h2>
                </div>
                
                <div class="animation-container">
                    <div class="canvas-container">
                        <canvas id="temp-canvas" width="800" height="500"></canvas>
                    </div>
                    
                    <div class="controls-container">
                        <div class="control-panel">
                            <h3>情景模拟</h3>
                            <div class="scenario-buttons">
                                <button class="scenario-btn temp-btn hot" data-scenario="hot-env">高温环境</button>
                                <button class="scenario-btn temp-btn cold" data-scenario="cold-env">低温环境</button>
                                <button class="scenario-btn temp-btn exercise" data-scenario="exercise">剧烈运动</button>
                            </div>
                            
                            <div class="slider-container">
                                <div class="slider-label">
                                    <span>核心体温</span>
                                    <span id="temperature-value">37.0°C (正常)</span>
                                </div>
                                <input type="range" min="35" max="39" step="0.1" value="37.0" class="slider" id="temperature-slider">
                            </div>
                            
                            <div class="animation-controls">
                                <button class="anim-btn play-btn" id="temp-play">
                                    <span>▶</span> 播放动画
                                </button>
                                <button class="anim-btn step-btn" id="temp-step">
                                    <span>→</span> 下一步
                                </button>
                                <button class="anim-btn reset-btn" id="temp-reset">
                                    <span>↺</span> 重置
                                </button>
                            </div>
                        </div>
                        
                        <div class="chart-container">
                            <canvas id="temp-chart" width="600" height="180"></canvas>
                        </div>
                        
                        <div class="info-panel">
                            <h3>调节步骤</h3>
                            <div class="step-info" id="temp-step1">
                                <h4>1. 稳态被打破</h4>
                                <p>核心体温偏离设定点(约37°C)，体温过高或过低。</p>
                            </div>
                            <div class="step-info" id="temp-step2">
                                <h4>2. 检测与信号传递</h4>
                                <p>皮肤温度感受器和下丘脑温度敏感神经元检测变化，发送信号至下丘脑体温调节中枢。</p>
                            </div>
                            <div class="step-info" id="temp-step3">
                                <h4>3. 控制中心响应</h4>
                                <p>下丘脑整合信息，发出神经信号调节产热和散热过程。</p>
                            </div>
                            <div class="step-info" id="temp-step4">
                                <h4>4. 效应器执行</h4>
                                <p>高温时：皮肤血管舒张、出汗增加；低温时：血管收缩、颤抖、代谢产热增加。</p>
                            </div>
                            <div class="step-info" id="temp-step5">
                                <h4>5. 恢复稳态</h4>
                                <p>体温回归正常范围，调节反应减弱，维持动态平衡。</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- 模型总结模块 -->
            <div id="model-section" class="animation-section hidden">
                <div class="animation-title" id="model-title">
                    <div class="icon">M</div>
                    <h2>负反馈调节通用模型</h2>
                </div>
                
                <div class="model-container">
                    <div class="model-canvas-container">
                        <canvas id="model-canvas" width="1000" height="400"></canvas>
                    </div>
                    
                    <div class="control-panel">
                        <h3>模型组件</h3>
                        <p>将下列组件拖拽到上方模型的正确位置，构建完整的负反馈调节环路。</p>
                        
                        <div class="scenario-buttons" style="margin-top: 15px;">
                            <button class="model-btn" id="model-reset">重置模型</button>
                            <button class="model-btn check" id="model-check">检查答案</button>
                        </div>
                        
                        <div class="feedback" id="model-feedback"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // 全局变量和状态管理
        const state = {
            currentTab: 'glucose',
            glucose: {
                value: 5.6,
                normalRange: { min: 3.9, max: 6.1 },
                step: 0,
                isPlaying: false,
                animationId: null,
                chartData: [],
                time: 0
            },
            water: {
                osmolarity: 300,
                normalRange: { min: 290, max: 310 },
                step: 0,
                isPlaying: false,
                animationId: null,
                chartData: [],
                time: 0
            },
            temperature: {
                value: 37.0,
                normalRange: { min: 36.5, max: 37.5 },
                step: 0,
                isPlaying: false,
                animationId: null,
                chartData: [],
                time: 0
            },
            model: {
                draggedComponent: null,
                components: [
                    { id: 'sensor', name: '传感器', x: 50, y: 150, width: 100, height: 60, color: '#4A90E2', correctX: 150, correctY: 100 },
                    { id: 'control', name: '控制中心', x: 50, y: 250, width: 100, height: 60, color: '#FF9500', correctX: 400, correctY: 100 },
                    { id: 'effector', name: '效应器', x: 50, y: 350, width: 100, height: 60, color: '#34C759', correctX: 650, correctY: 100 },
                    { id: 'parameter', name: '受控变量', x: 50, y: 50, width: 100, height: 60, color: '#8E8E93', correctX: 150, correctY: 250 }
                ],
                placed: {
                    sensor: false,
                    control: false,
                    effector: false,
                    parameter: false
                }
            }
        };

        // 初始化函数
        document.addEventListener('DOMContentLoaded', function() {
            // 标签切换
            document.querySelectorAll('.tab').forEach(tab => {
                tab.addEventListener('click', function() {
                    const tabId = this.getAttribute('data-tab');
                    switchTab(tabId);
                });
            });

            // 血糖模块事件
            document.getElementById('glucose-slider').addEventListener('input', function() {
                state.glucose.value = parseFloat(this.value);
                document.getElementById('glucose-value').textContent = 
                    `${state.glucose.value.toFixed(1)} mmol/L ${getStatusText(state.glucose.value, state.glucose.normalRange)}`;
                drawGlucoseCanvas();
            });

            document.querySelectorAll('.glucose-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const scenario = this.getAttribute('data-scenario');
                    if (scenario === 'high-glucose') {
                        state.glucose.value = 8.5;
                    } else {
                        state.glucose.value = 3.0;
                    }
                    document.getElementById('glucose-slider').value = state.glucose.value;
                    document.getElementById('glucose-value').textContent = 
                        `${state.glucose.value.toFixed(1)} mmol/L ${getStatusText(state.glucose.value, state.glucose.normalRange)}`;
                    drawGlucoseCanvas();
                });
            });

            document.getElementById('glucose-play').addEventListener('click', toggleGlucoseAnimation);
            document.getElementById('glucose-step').addEventListener('click', nextGlucoseStep);
            document.getElementById('glucose-reset').addEventListener('click', resetGlucose);

            // 水平衡模块事件
            document.getElementById('osmolarity-slider').addEventListener('input', function() {
                state.water.osmolarity = parseFloat(this.value);
                document.getElementById('osmolarity-value').textContent = 
                    `${state.water.osmolarity} mOsm/L ${getStatusText(state.water.osmolarity, state.water.normalRange)}`;
                drawWaterCanvas();
            });

            document.querySelectorAll('.water-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const scenario = this.getAttribute('data-scenario');
                    if (scenario === 'lose-water') {
                        state.water.osmolarity = 315;
                    } else {
                        state.water.osmolarity = 285;
                    }
                    document.getElementById('osmolarity-slider').value = state.water.osmolarity;
                    document.getElementById('osmolarity-value').textContent = 
                        `${state.water.osmolarity} mOsm/L ${getStatusText(state.water.osmolarity, state.water.normalRange)}`;
                    drawWaterCanvas();
                });
            });

            document.getElementById('water-play').addEventListener('click', toggleWaterAnimation);
            document.getElementById('water-step').addEventListener('click', nextWaterStep);
            document.getElementById('water-reset').addEventListener('click', resetWater);

            // 体温模块事件
            document.getElementById('temperature-slider').addEventListener('input', function() {
                state.temperature.value = parseFloat(this.value);
                document.getElementById('temperature-value').textContent = 
                    `${state.temperature.value.toFixed(1)}°C ${getStatusText(state.temperature.value, state.temperature.normalRange)}`;
                drawTempCanvas();
            });

            document.querySelectorAll('.temp-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const scenario = this.getAttribute('data-scenario');
                    if (scenario === 'hot-env') {
                        state.temperature.value = 38.5;
                    } else if (scenario === 'cold-env') {
                        state.temperature.value = 35.5;
                    } else {
                        state.temperature.value = 38.0;
                    }
                    document.getElementById('temperature-slider').value = state.temperature.value;
                    document.getElementById('temperature-value').textContent = 
                        `${state.temperature.value.toFixed(1)}°C ${getStatusText(state.temperature.value, state.temperature.normalRange)}`;
                    drawTempCanvas();
                });
            });

            document.getElementById('temp-play').addEventListener('click', toggleTempAnimation);
            document.getElementById('temp-step').addEventListener('click', nextTempStep);
            document.getElementById('temp-reset').addEventListener('click', resetTemp);

            // 模型模块事件
            document.getElementById('model-reset').addEventListener('click', resetModel);
            document.getElementById('model-check').addEventListener('click', checkModel);

            // 初始化画布
            initCanvases();
            drawGlucoseCanvas();
            drawWaterCanvas();
            drawTempCanvas();
            drawModelCanvas();
            initCharts();
        });

        // 工具函数
        function getStatusText(value, range) {
            if (value < range.min) return '(过低)';
            if (value > range.max) return '(过高)';
            return '(正常)';
        }

        function switchTab(tabId) {
            // 更新标签状态
            document.querySelectorAll('.tab').forEach(tab => {
                tab.classList.remove('active');
                if (tab.getAttribute('data-tab') === tabId) {
                    tab.classList.add('active');
                }
            });

            // 更新内容显示
            document.querySelectorAll('.animation-section').forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(`${tabId}-section`).classList.remove('hidden');

            // 停止所有动画
            stopAllAnimations();
            state.currentTab = tabId;
        }

        function stopAllAnimations() {
            if (state.glucose.animationId) {
                cancelAnimationFrame(state.glucose.animationId);
                state.glucose.isPlaying = false;
                state.glucose.animationId = null;
            }
            if (state.water.animationId) {
                cancelAnimationFrame(state.water.animationId);
                state.water.isPlaying = false;
                state.water.animationId = null;
            }
            if (state.temperature.animationId) {
                cancelAnimationFrame(state.temperature.animationId);
                state.temperature.isPlaying = false;
                state.temperature.animationId = null;
            }
        }

        // 血糖调节功能
        function toggleGlucoseAnimation() {
            if (state.glucose.isPlaying) {
                cancelAnimationFrame(state.glucose.animationId);
                state.glucose.isPlaying = false;
                document.getElementById('glucose-play').innerHTML = '<span>▶</span> 播放动画';
            } else {
                state.glucose.isPlaying = true;
                document.getElementById('glucose-play').innerHTML = '<span>⏸</span> 暂停动画';
                animateGlucose();
            }
        }

        function animateGlucose() {
            if (!state.glucose.isPlaying) return;

            // 模拟血糖回归正常的过程
            const target = 5.6;
            const diff = target - state.glucose.value;
            
            if (Math.abs(diff) > 0.05) {
                state.glucose.value += diff * 0.05;
                state.glucose.time += 0.1;
                
                // 更新滑块和显示
                document.getElementById('glucose-slider').value = state.glucose.value;
                document.getElementById('glucose-value').textContent = 
                    `${state.glucose.value.toFixed(1)} mmol/L ${getStatusText(state.glucose.value, state.glucose.normalRange)}`;
                
                // 更新图表数据
                state.glucose.chartData.push({
                    time: state.glucose.time,
                    value: state.glucose.value
                });
                if (state.glucose.chartData.length > 50) {
                    state.glucose.chartData.shift();
                }
                
                // 更新步骤显示
                updateGlucoseStep();
                drawGlucoseCanvas();
                updateGlucoseChart();
                
                state.glucose.animationId = requestAnimationFrame(animateGlucose);
            } else {
                state.glucose.isPlaying = false;
                document.getElementById('glucose-play').innerHTML = '<span>▶</span> 播放动画';
                state.glucose.step = 5;
                updateGlucoseStep();
            }
        }

        function nextGlucoseStep() {
            if (state.glucose.step < 5) {
                state.glucose.step++;
                updateGlucoseStep();
                
                // 模拟血糖变化
                if (state.glucose.step >= 2 && state.glucose.step <= 4) {
                    const target = 5.6;
                    const diff = target - state.glucose.value;
                    state.glucose.value += diff * 0.3;
                    state.glucose.time += 0.5;
                    
                    document.getElementById('glucose-slider').value = state.glucose.value;
                    document.getElementById('glucose-value').textContent = 
                        `${state.glucose.value.toFixed(1)} mmol/L ${getStatusText(state.glucose.value, state.glucose.normalRange)}`;
                    
                    state.glucose.chartData.push({
                        time: state.glucose.time,
                        value: state.glucose.value
                    });
                    if (state.glucose.chartData.length > 50) {
                        state.glucose.chartData.shift();
                    }
                    
                    updateGlucoseChart();
                }
                
                drawGlucoseCanvas();
            }
        }

        function updateGlucoseStep() {
            // 重置所有步骤
            for (let i = 1; i <= 5; i++) {
                document.getElementById(`glucose-step${i}`).classList.remove('active');
            }
            
            // 激活当前步骤
            if (state.glucose.step > 0 && state.glucose.step <= 5) {
                document.getElementById(`glucose-step${state.glucose.step}`).classList.add('active');
            }
        }

        function resetGlucose() {
            state.glucose.value = 5.6;
            state.glucose.step = 0;
            state.glucose.time = 0;
            state.glucose.chartData = [];
            
            document.getElementById('glucose-slider').value = state.glucose.value;
            document.getElementById('glucose-value').textContent = '5.6 mmol/L (正常)';
            
            if (state.glucose.isPlaying) {
                cancelAnimationFrame(state.glucose.animationId);
                state.glucose.isPlaying = false;
                document.getElementById('glucose-play').innerHTML = '<span>▶</span> 播放动画';
            }
            
            updateGlucoseStep();
            drawGlucoseCanvas();
            updateGlucoseChart();
        }

        // 水平衡调节功能 (类似血糖，略简)
        function toggleWaterAnimation() {
            if (state.water.isPlaying) {
                cancelAnimationFrame(state.water.animationId);
                state.water.isPlaying = false;
                document.getElementById('water-play').innerHTML = '<span>▶</span> 播放动画';
            } else {
                state.water.isPlaying = true;
                document.getElementById('water-play').innerHTML = '<span>⏸</span> 暂停动画';
                animateWater();
            }
        }

        function animateWater() {
            if (!state.water.isPlaying) return;

            const target = 300;
            const diff = target - state.water.osmolarity;
            
            if (Math.abs(diff) > 0
<!--检测到代码截断，自动续写中...-->
if (Math.abs(diff) > 0.5) {
                state.water.osmolarity += diff * 0.05;
                state.water.time += 0.1;
                
                document.getElementById('osmolarity-slider').value = state.water.osmolarity;
                document.getElementById('osmolarity-value').textContent = 
                    `${state.water.osmolarity} mOsm/L ${getStatusText(state.water.osmolarity, state.water.normalRange)}`;
                
                state.water.chartData.push({
                    time: state.water.time,
                    value: state.water.osmolarity
                });
                if (state.water.chartData.length > 50) {
                    state.water.chartData.shift();
                }
                
                updateWaterStep();
                drawWaterCanvas();
                updateWaterChart();
                
                state.water.animationId = requestAnimationFrame(animateWater);
            } else {
                state.water.isPlaying = false;
                document.getElementById('water-play').innerHTML = '<span>▶</span> 播放动画';
                state.water.step = 5;
                updateWaterStep();
            }
        }

        function nextWaterStep() {
            if (state.water.step < 5) {
                state.water.step++;
                updateWaterStep();
                
                if (state.water.step >= 2 && state.water.step <= 4) {
                    const target = 300;
                    const diff = target - state.water.osmolarity;
                    state.water.osmolarity += diff * 0.3;
                    state.water.time += 0.5;
                    
                    document.getElementById('osmolarity-slider').value = state.water.osmolarity;
                    document.getElementById('osmolarity-value').textContent = 
                        `${state.water.osmolarity} mOsm/L ${getStatusText(state.water.osmolarity, state.water.normalRange)}`;
                    
                    state.water.chartData.push({
                        time: state.water.time,
                        value: state.water.osmolarity
                    });
                    if (state.water.chartData.length > 50) {
                        state.water.chartData.shift();
                    }
                    
                    updateWaterChart();
                }
                
                drawWaterCanvas();
            }
        }

        function updateWaterStep() {
            for (let i = 1; i <= 5; i++) {
                document.getElementById(`water-step${i}`).classList.remove('active');
            }
            
            if (state.water.step > 0 && state.water.step <= 5) {
                document.getElementById(`water-step${state.water.step}`).classList.add('active');
            }
        }

        function resetWater() {
            state.water.osmolarity = 300;
            state.water.step = 0;
            state.water.time = 0;
            state.water.chartData = [];
            
            document.getElementById('osmolarity-slider').value = state.water.osmolarity;
            document.getElementById('osmolarity-value').textContent = '300 mOsm/L (正常)';
            
            if (state.water.isPlaying) {
                cancelAnimationFrame(state.water.animationId);
                state.water.isPlaying = false;
                document.getElementById('water-play').innerHTML = '<span>▶</span> 播放动画';
            }
            
            updateWaterStep();
            drawWaterCanvas();
            updateWaterChart();
        }

        // 体温调节功能
        function toggleTempAnimation() {
            if (state.temperature.isPlaying) {
                cancelAnimationFrame(state.temperature.animationId);
                state.temperature.isPlaying = false;
                document.getElementById('temp-play').innerHTML = '<span>▶</span> 播放动画';
            } else {
                state.temperature.isPlaying = true;
                document.getElementById('temp-play').innerHTML = '<span>⏸</span> 暂停动画';
                animateTemp();
            }
        }

        function animateTemp() {
            if (!state.temperature.isPlaying) return;

            const target = 37.0;
            const diff = target - state.temperature.value;
            
            if (Math.abs(diff) > 0.05) {
                state.temperature.value += diff * 0.05;
                state.temperature.time += 0.1;
                
                document.getElementById('temperature-slider').value = state.temperature.value;
                document.getElementById('temperature-value').textContent = 
                    `${state.temperature.value.toFixed(1)}°C ${getStatusText(state.temperature.value, state.temperature.normalRange)}`;
                
                state.temperature.chartData.push({
                    time: state.temperature.time,
                    value: state.temperature.value
                });
                if (state.temperature.chartData.length > 50) {
                    state.temperature.chartData.shift();
                }
                
                updateTempStep();
                drawTempCanvas();
                updateTempChart();
                
                state.temperature.animationId = requestAnimationFrame(animateTemp);
            } else {
                state.temperature.isPlaying = false;
                document.getElementById('temp-play').innerHTML = '<span>▶</span> 播放动画';
                state.temperature.step = 5;
                updateTempStep();
            }
        }

        function nextTempStep() {
            if (state.temperature.step < 5) {
                state.temperature.step++;
                updateTempStep();
                
                if (state.temperature.step >= 2 && state.temperature.step <= 4) {
                    const target = 37.0;
                    const diff = target - state.temperature.value;
                    state.temperature.value += diff * 0.3;
                    state.temperature.time += 0.5;
                    
                    document.getElementById('temperature-slider').value = state.temperature.value;
                    document.getElementById('temperature-value').textContent = 
                        `${state.temperature.value.toFixed(1)}°C ${getStatusText(state.temperature.value, state.temperature.normalRange)}`;
                    
                    state.temperature.chartData.push({
                        time: state.temperature.time,
                        value: state.temperature.value
                    });
                    if (state.temperature.chartData.length > 50) {
                        state.temperature.chartData.shift();
                    }
                    
                    updateTempChart();
                }
                
                drawTempCanvas();
            }
        }

        function updateTempStep() {
            for (let i = 1; i <= 5; i++) {
                document.getElementById(`temp-step${i}`).classList.remove('active');
            }
            
            if (state.temperature.step > 0 && state.temperature.step <= 5) {
                document.getElementById(`temp-step${state.temperature.step}`).classList.add('active');
            }
        }

        function resetTemp() {
            state.temperature.value = 37.0;
            state.temperature.step = 0;
            state.temperature.time = 0;
            state.temperature.chartData = [];
            
            document.getElementById('temperature-slider').value = state.temperature.value;
            document.getElementById('temperature-value').textContent = '37.0°C (正常)';
            
            if (state.temperature.isPlaying) {
                cancelAnimationFrame(state.temperature.animationId);
                state.temperature.isPlaying = false;
                document.getElementById('temp-play').innerHTML = '<span>▶</span> 播放动画';
            }
            
            updateTempStep();
            drawTempCanvas();
            updateTempChart();
        }

        // 模型总结功能
        function resetModel() {
            state.model.components.forEach(comp => {
                comp.x = 50;
                comp.y = 50 + (['sensor', 'control', 'effector', 'parameter'].indexOf(comp.id) * 100);
            });
            
            state.model.placed = {
                sensor: false,
                control: false,
                effector: false,
                parameter: false
            };
            
            const feedback = document.getElementById('model-feedback');
            feedback.style.display = 'none';
            feedback.className = 'feedback';
            
            drawModelCanvas();
        }

        function checkModel() {
            let correct = 0;
            let total = 0;
            
            state.model.components.forEach(comp => {
                const dx = Math.abs(comp.x - comp.correctX);
                const dy = Math.abs(comp.y - comp.correctY);
                
                if (dx < 60 && dy < 40) {
                    correct++;
                }
                total++;
            });
            
            const feedback = document.getElementById('model-feedback');
            feedback.style.display = 'block';
            
            if (correct === total) {
                feedback.textContent = '✓ 完美！所有组件都放置正确！你已掌握负反馈调节的基本模型。';
                feedback.className = 'feedback correct';
            } else {
                feedback.textContent = `放置了 ${correct}/${total} 个组件。请调整位置，使传感器、控制中心、效应器和受控变量形成完整的调节环路。`;
                feedback.className = 'feedback incorrect';
            }
        }

        // 画布绘制函数
        function initCanvases() {
            // 获取所有Canvas上下文
            window.canvasContexts = {
                glucose: document.getElementById('glucose-canvas').getContext('2d'),
                water: document.getElementById('water-canvas').getContext('2d'),
                temp: document.getElementById('temp-canvas').getContext('2d'),
                model: document.getElementById('model-canvas').getContext('2d'),
                glucoseChart: document.getElementById('glucose-chart').getContext('2d'),
                waterChart: document.getElementById('water-chart').getContext('2d'),
                tempChart: document.getElementById('temp-chart').getContext('2d')
            };
            
            // 设置模型画布的拖拽事件
            const modelCanvas = document.getElementById('model-canvas');
            modelCanvas.addEventListener('mousedown', handleModelMouseDown);
            modelCanvas.addEventListener('mousemove', handleModelMouseMove);
            modelCanvas.addEventListener('mouseup', handleModelMouseUp);
        }

        function drawGlucoseCanvas() {
            const ctx = window.canvasContexts.glucose;
            const canvas = document.getElementById('glucose-canvas');
            const width = canvas.width;
            const height = canvas.height;
            
            // 清空画布
            ctx.clearRect(0, 0, width, height);
            
            // 绘制背景
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, width, height);
            
            // 绘制人体轮廓
            ctx.fillStyle = '#FFD6CC';
            ctx.beginPath();
            ctx.ellipse(width/2, height/2, 150, 200, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#D4A5A5';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制胰腺
            const pancreasX = width/2 + 60;
            const pancreasY = height/2 - 30;
            ctx.fillStyle = '#E0B0FF';
            ctx.beginPath();
            ctx.ellipse(pancreasX, pancreasY, 25, 15, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#B57EDC';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制肝脏
            ctx.fillStyle = '#D2B48C';
            ctx.beginPath();
            ctx.ellipse(width/2 - 40, height/2 - 20, 40, 30, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#B8860B';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制血糖值指示器
            const glucoseLevel = (state.glucose.value - 2) / 8; // 归一化到0-1
            const indicatorHeight = 200;
            const indicatorY = height/2 + 100 - glucoseLevel * indicatorHeight;
            
            // 血糖计背景
            ctx.fillStyle = '#e9ecef';
            ctx.fillRect(width - 100, height/2 - 100, 60, indicatorHeight);
            
            // 正常范围
            const normalMinY = height/2 + 100 - ((state.glucose.normalRange.max - 2) / 8) * indicatorHeight;
            const normalMaxY = height/2 + 100 - ((state.glucose.normalRange.min - 2) / 8) * indicatorHeight;
            ctx.fillStyle = 'rgba(52, 199, 89, 0.3)';
            ctx.fillRect(width - 100, normalMinY, 60, normalMaxY - normalMinY);
            
            // 当前血糖水平
            ctx.fillStyle = state.glucose.value > state.glucose.normalRange.max ? '#FF9500' : 
                           state.glucose.value < state.glucose.normalRange.min ? '#007AFF' : '#34C759';
            ctx.beginPath();
            ctx.arc(width - 70, indicatorY, 15, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制激素流动效果
            if (state.glucose.step >= 2 && state.glucose.step <= 4) {
                const time = Date.now() / 1000;
                const pulse = Math.sin(time * 5) * 0.5 + 0.5;
                
                if (state.glucose.value > state.glucose.normalRange.max) {
                    // 胰岛素从胰腺流向肝脏
                    ctx.strokeStyle = '#007AFF';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(pancreasX - 20, pancreasY);
                    ctx.lineTo(width/2 - 40, height/2 - 20);
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 绘制胰岛素粒子
                    ctx.fillStyle = '#007AFF';
                    for (let i = 0; i < 5; i++) {
                        const progress = (time * 2 + i * 0.4) % 1;
                        const x = pancreasX - 20 + (width/2 - 40 - (pancreasX - 20)) * progress;
                        const y = pancreasY + (height/2 - 20 - pancreasY) * progress;
                        ctx.beginPath();
                        ctx.arc(x, y, 4 + pulse * 2, 0, Math.PI * 2);
                        ctx.fill();
                    }
                } else if (state.glucose.value < state.glucose.normalRange.min) {
                    // 胰高血糖素从胰腺流向肝脏
                    ctx.strokeStyle = '#FF9500';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(pancreasX - 20, pancreasY);
                    ctx.lineTo(width/2 - 40, height/2 - 20);
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 绘制胰高血糖素粒子
                    ctx.fillStyle = '#FF9500';
                    for (let i = 0; i < 5; i++) {
                        const progress = (time * 2 + i * 0.4) % 1;
                        const x = pancreasX - 20 + (width/2 - 40 - (pancreasX - 20)) * progress;
                        const y = pancreasY + (height/2 - 20 - pancreasY) * progress;
                        ctx.beginPath();
                        ctx.arc(x, y, 4 + pulse * 2, 0, Math.PI * 2);
                        ctx.fill();
                    }
                }
            }
            
            // 绘制标签
            ctx.fillStyle = '#333';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('人体', width/2, height/2 + 220);
            ctx.fillText('胰腺', pancreasX, pancreasY - 25);
            ctx.fillText('肝脏', width/2 - 40, height/2 - 60);
            ctx.fillText('血糖浓度', width - 70, height/2 - 120);
            
            ctx.font = '14px Arial';
            ctx.fillText(`${state.glucose.value.toFixed(1)} mmol/L`, width - 70, indicatorY - 20);
        }

        function drawWaterCanvas() {
            const ctx = window.canvasContexts.water;
            const canvas = document.getElementById('water-canvas');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, width, height);
            
            // 绘制人体轮廓
            ctx.fillStyle = '#FFD6CC';
            ctx.beginPath();
            ctx.ellipse(width/2, height/2, 150, 200, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#D4A5A5';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制下丘脑
            const hypothalamusX = width/2;
            const hypothalamusY = height/2 - 80;
            ctx.fillStyle = '#FFB6C1';
            ctx.beginPath();
            ctx.arc(hypothalamusX, hypothalamusY, 20, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#FF69B4';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制肾脏
            ctx.fillStyle = '#87CEEB';
            ctx.beginPath();
            ctx.ellipse(width/2 - 60, height/2 + 40, 25, 40, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.beginPath();
            ctx.ellipse(width/2 + 60, height/2 + 40, 25, 40, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#4682B4';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制体液水箱
            const tankX = width - 120;
            const tankY = height/2 - 50;
            const tankWidth = 80;
            const tankHeight = 150;
            
            // 水箱边框
            ctx.strokeStyle = '#666';
            ctx.lineWidth = 3;
            ctx.strokeRect(tankX, tankY, tankWidth, tankHeight);
            
            // 水位（根据渗透压计算）
            const waterLevel = 1 - (state.water.osmolarity - 280) / 40;
            const waterHeight = Math.max(10, Math.min(tankHeight - 10, waterLevel * (tankHeight - 20)));
            
            // 水体颜色（根据渗透压变化）
            const blueIntensity = Math.max(100, Math.min(255, 255 - (state.water.osmolarity - 280) * 4));
            ctx.fillStyle = `rgb(100, 150, ${blueIntensity})`;
            ctx.fillRect(tankX + 5, tankY + tankHeight - waterHeight - 5, tankWidth - 10, waterHeight);
            
            // 绘制ADH流动效果
            if (state.water.step >= 2 && state.water.step <= 4) {
                const time = Date.now() / 1000;
                const pulse = Math.sin(time * 5) * 0.5 + 0.5;
                
                if (state.water.osmolarity > state.water.normalRange.max) {
                    // ADH从下丘脑流向肾脏
                    ctx.strokeStyle = '#007AFF';
                    ctx.lineWidth = 3;
                    ctx.setLineDash([5, 5]);
                    ctx.beginPath();
                    ctx.moveTo(hypothalamusX, hypothalamusY + 20);
                    ctx.lineTo(width/2, height/2 + 40);
                    ctx.stroke();
                    ctx.setLineDash([]);
                    
                    // 绘制ADH粒子
                    ctx.fillStyle = '#007AFF';
                    for (let i = 0; i < 5; i++) {
                        const progress = (time * 2 + i * 0.4) % 1;
                        const x = hypothalamusX + (width/2 - hypothalamusX) * progress;
                        const y = hypothalamusY + 20 + (height/2 + 40 - (hypothalamusY + 20)) * progress;
                        ctx.beginPath();
                        ctx.arc(x, y, 4 + pulse * 2, 0, Math.PI * 2);
                        ctx.fill();
                    }
                }
            }
            
            // 绘制标签
            ctx.fillStyle = '#333';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('人体', width/2, height/2 + 220);
            ctx.fillText('下丘脑', hypothalamusX, hypothalamusY - 30);
            ctx.fillText('肾脏', width/2, height/2 + 100);
            ctx.fillText('体液', tankX + tankWidth/2, tankY - 20);
            ctx.fillText('渗透压', tankX + tankWidth/2, tankY + tankHeight + 30);
            
            ctx.font = '14px Arial';
            ctx.fillText(`${state.water.osmolarity} mOsm/L`, tankX + tankWidth/2, tankY + tankHeight + 50);
        }

        function drawTempCanvas() {
            const ctx = window.canvasContexts.temp;
            const canvas = document.getElementById('temp-canvas');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, width, height);
            
            // 绘制人体轮廓
            ctx.fillStyle = '#FFD6CC';
            ctx.beginPath();
            ctx.ellipse(width/2, height/2, 150, 200, 0, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#D4A5A5';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制下丘脑体温调节中枢
            const hypothalamusX = width/2;
            const hypothalamusY = height/2 - 80;
            ctx.fillStyle = '#FFB6C1';
            ctx.beginPath();
            ctx.arc(hypothalamusX, hypothalamusY, 20, 0, Math.PI * 2);
            ctx.fill();
            ctx.strokeStyle = '#FF69B4';
            ctx.lineWidth = 2;
            ctx.stroke();
            
            // 绘制温度计
            const thermometerX = width - 100;
            const thermometerY = height/2 - 80;
            
            // 温度计主体
            ctx.fillStyle = '#e9ecef';
            ctx.fillRect(thermometerX - 10, thermometerY, 20, 160);
            ctx.strokeStyle = '#666';
            ctx.lineWidth = 2;
            ctx.strokeRect(thermometerX - 10, thermometerY, 20, 160);
            
            // 温度刻度
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'right';
            for (let i = 35; i <= 39; i += 0.5) {
                const y = thermometerY + 160 - ((i - 35) / 4) * 160;
                ctx.beginPath();
                ctx.moveTo(thermometerX - 15, y);
                ctx.lineTo(thermometerX - 10, y);
                ctx.stroke();
                
                if (i % 1 === 0) {
                    ctx.fillText(`${i}°C`, thermometerX - 20, y + 4);
                }
            }
            
            // 温度指示
            const tempLevel = (state.temperature.value - 35) / 4;
            const indicatorY = thermometerY + 160 - tempLevel * 160;
            
            ctx.fillStyle = state.temperature.value > state.temperature.normalRange.max ? '#FF3B30' : 
                           state.temperature.value < state.temperature.normalRange.min ? '#007AFF' : '#34C759';
            ctx.beginPath();
            ctx.arc(thermometerX, indicatorY, 12, 0, Math.PI * 2);
            ctx.fill();
            
            // 绘制散热/产热效果
            if (state.temperature.step >= 2 && state.temperature.step <= 4) {
                const time = Date.now() / 1000;
                
                if (state.temperature.value > state.temperature.normalRange.max) {
                    // 散热：汗滴和血管扩张
                    ctx.fillStyle = '#007AFF';
                    for (let i = 0; i < 8; i++) {
                        const angle = (i / 8) * Math.PI * 2;
                        const radius = 180;
                        const x = width/2 + Math.cos(angle) * radius;
                        const y = height/2 + Math.sin(angle) * radius;
                        
                        // 汗滴
                        const dropProgress = (time * 3 + i * 0.5) % 1;
                        const dropY = y + dropProgress * 40;
                        
                        if (dropProgress < 0.7) {
                            ctx.beginPath();
                            ctx.ellipse(x, dropY, 3, 5, 0, 0, Math.PI * 2);
                            ctx.fill();
                        }
                    }
                } else if (state.temperature.value < state.temperature.normalRange.min) {
                    // 产热：颤抖和代谢增加
                    ctx.fillStyle = '#FF9500';
                    const shake = Math.sin(time * 10) * 3;
                    
                    // 颤抖效果
                    for (let i = 0; i < 4; i++) {
                        const angle = Math.PI/4 + (i / 4) * Math.PI/2;
                        const length = 80;
                        const startX = width/2 + Math.cos(angle) * 100;
                        const startY = height/2 + Math.sin(angle) * 100;
                        const endX = startX + Math.cos(angle) * length;
                        const endY = startY + Math.sin(angle) * length;
                        
                        ctx.beginPath();
                        ctx.moveTo(startX, startY);
                        for (let j = 0; j <= 10; j++) {
                            const progress = j / 10;
                            const x = startX + (endX - startX) * progress;
                            const y = startY + (endY - startY) * progress;
                            const offset = Math.sin(time * 20 + j) * 5;
                            ctx.lineTo(x + Math.cos(angle + Math.PI/2) * offset, 
                                      y + Math.sin(angle + Math.PI/2) * offset);
                        }
                        ctx.strokeStyle = '#FF9500';
                        ctx.lineWidth = 2;
                        ctx.stroke();
                    }
                }
            }
            
            // 绘制标签
            ctx.fillStyle = '#333';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('人体', width/2, height/2 + 220);
            ctx.fillText('下丘脑体温调节中枢', hypothalamusX, hypothalamusY - 30);
            ctx.fillText('核心体温', thermometerX, thermometerY - 20);
            
            ctx.font = '14px Arial';
            ctx.fillText(`${state.temperature.value.toFixed(1)}°C`, thermometerX, indicatorY - 20);
        }

        function drawModelCanvas() {
            const ctx = window.canvasContexts.model;
            const canvas = document.getElementById('model-canvas');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            ctx.fillStyle = '#f8f9fa';
            ctx.fillRect(0, 0, width, height);
            
            // 绘制负反馈环路背景
            ctx.strokeStyle = 'rgba(74, 144, 226, 0.3)';
            ctx.lineWidth = 4;
            ctx.setLineDash([10, 5]);
            
            // 主环路
            ctx.beginPath();
            ctx.moveTo(150, 100);  // 传感器
            ctx.lineTo(400, 100);  // 控制中心
            ctx.lineTo(650, 100);  // 效应器
            ctx.lineTo(650, 250);  // 向下
            ctx.lineTo(150, 250);  // 回到受控变量
            ctx.lineTo(150, 100);  // 闭合环路
            ctx.stroke();
            ctx.setLineDash([]);
            
            // 绘制箭头
            function drawArrow(x1, y1, x2, y2) {
                const headlen = 10;
                const dx = x2 - x1;
                const dy = y2 - y1;
                const angle = Math.atan2(dy, dx);
                
                ctx.beginPath();
                ctx.moveTo(x1, y1);
                ctx.lineTo(x2, y2);
                ctx.lineTo(x2 - headlen * Math.cos(angle - Math.PI/6), y2 - headlen * Math.sin(angle - Math.PI/6));
                ctx.moveTo(x2, y2);
                ctx.lineTo(x2 - headlen * Math.cos(angle + Math.PI/6), y2 - headlen * Math.sin(angle + Math.PI/6));
                ctx.stroke();
            }
            
            // 绘制组件放置区域
            ctx.strokeStyle = 'rgba(52, 199, 89, 0.5)';
            ctx.lineWidth = 2;
            ctx.setLineDash([5, 5]);
            
            // 传感器区域
            ctx.strokeRect(120, 70, 60, 60);
            ctx.fillStyle = 'rgba(52, 199, 89, 0.1)';
            ctx.fillRect(120, 70, 60, 60);
            
            // 控制中心区域
            ctx.strokeRect(370, 70, 60, 60);
            ctx.fillRect(370, 70, 60, 60);
            
            // 效应器区域
            ctx.strokeRect(620, 70, 60, 60);
            ctx.fillRect(620, 70, 60, 60);
            
            // 受控变量区域
            ctx.strokeRect(120, 220, 60, 60);
            ctx.fillRect(120, 220, 60, 60);
            
            ctx.setLineDash([]);
            
            // 绘制组件
            state.model.components.forEach(comp => {
                // 组件框
                ctx.fillStyle = comp.color;
                ctx.fillRect(comp.x, comp.y, comp.width, comp.height);
                
                ctx.strokeStyle = '#333';
                ctx.lineWidth = 2;
                ctx.strokeRect(comp.x, comp.y, comp.width, comp.height);
                
                // 组件文字
                ctx.fillStyle = '#333';
                ctx.font = 'bold 16px Arial';
                ctx.textAlign = 'center';
                ctx.textBaseline = 'middle';
                ctx.fillText(comp.name, comp.x + comp.width/2, comp.y + comp.height/2);
                
                // 如果是被拖拽的组件，添加阴影
                if (state.model.draggedComponent === comp.id) {
                    ctx.shadowColor = 'rgba(0, 0, 0, 0.3)';
                    ctx.shadowBlur = 10;
                    ctx.shadowOffsetX = 5;
                    ctx.shadowOffsetY = 5;
                    
                    // 重绘以应用阴影
                    ctx.fillRect(comp.x, comp.y, comp.width, comp.height);
                    ctx.strokeRect(comp.x, comp.y, comp.width, comp.height);
                    ctx.fillText(comp.name, comp.x + comp.width/2, comp.y + comp.height/2);
                    
                    ctx.shadowColor = 'transparent';
                    ctx.shadowBlur = 0;
                    ctx.shadowOffsetX = 0;
                    ctx.shadowOffsetY = 0;
                }
            });
            
            // 绘制标签
            ctx.fillStyle = '#666';
            ctx.font = '14px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('将左侧组件拖拽到正确位置', width/2, 30);
            ctx.fillText('构建负反馈调节通用模型', width/2, 50);
            
            // 绘制示例标签
            ctx.fillStyle = '#4A90E2';
            ctx.font = 'bold 14px Arial';
            ctx.fillText('示例：血糖调节', width/2, 350);
            
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'left';
            ctx.fillText('• 传感器：胰岛血糖感受器', 50, 380);
            ctx.fillText('• 控制中心：胰岛B细胞/A细胞', 50, 400);
            ctx.fillText('• 效应器：肝脏、肌肉等靶器官', 50, 420);
            ctx.fillText('• 受控变量：血糖浓度', 50, 440);
        }

        // 模型拖拽功能
        function handleModelMouseDown(e) {
            const rect = e.target.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 检查点击了哪个组件
            for (const comp of state.model.components) {
                if (x >= comp.x && x <= comp.x + comp.width &&
                    y >= comp.y && y <= comp.y + comp.height) {
                    state.model.draggedComponent = comp.id;
                    drawModelCanvas();
                    break;
                }
            }
        }

        function handleModelMouseMove(e) {
            if (!state.model.draggedComponent) return;
            
            const rect = e.target.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            // 更新被拖拽组件的位置
            const comp = state.model.components.find(c => c.id === state.model.draggedComponent);
            if (comp) {
                comp.x = x - comp.width/2;
                comp.y = y - comp.height/2;
                drawModelCanvas();
            }
        }

        function handleModelMouseUp() {
            state.model.draggedComponent = null;
            drawModelCanvas();
        }

        // 图表功能
        function initCharts() {
            // 初始化图表数据
            state.glucose.chartData = [{time: 0, value: state.glucose.value}];
            state.water.chartData = [{time: 0, value: state.water.osmolarity}];
            state.temperature.chartData = [{time: 0, value: state.temperature.value}];
            
            updateGlucoseChart();
            updateWaterChart();
            updateTempChart();
        }

        function updateGlucoseChart() {
            const ctx = window.canvasContexts.glucoseChart;
            const canvas = document.getElementById('glucose-chart');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            
            if (state.glucose.chartData.length < 2) return;
            
            // 绘制坐标轴
            ctx.strokeStyle = '#ccc';
            ctx.lineWidth = 1;
            
            // Y轴
            ctx.beginPath();
            ctx.moveTo(40, 20);
            ctx.lineTo(40, height - 20);
            ctx.stroke();
            
            // X轴
            ctx.beginPath();
            ctx.moveTo(40, height - 20);
            ctx.lineTo(width - 20, height - 20);
            ctx.stroke();
            
            // 绘制正常范围区域
            const yMin = 2;
            const yMax = 10;
            const normalMinY = height - 20 - ((state.glucose.normalRange.min - yMin) / (yMax - yMin)) * (height - 40);
            const normalMaxY = height - 20 - ((state.glucose.normalRange.max - yMin) / (yMax - yMin)) * (height - 40);
            
            ctx.fillStyle = 'rgba(52, 199, 89, 0.1)';
            ctx.fillRect(40, normalMaxY, width - 60, normalMinY - normalMaxY);
            
            // 绘制曲线
            ctx.beginPath();
            ctx.strokeStyle = '#4A90E2';
            ctx.lineWidth = 3;
            
            const maxTime = Math
<!--检测到代码截断，自动续写中...-->
const maxTime = Math.max(...state.glucose.chartData.map(d => d.time));
            
            for (let i = 0; i < state.glucose.chartData.length; i++) {
                const data = state.glucose.chartData[i];
                const x = 40 + (data.time / maxTime) * (width - 60);
                const y = height - 20 - ((data.value - yMin) / (yMax - yMin)) * (height - 40);
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
            }
            ctx.stroke();
            
            // 绘制当前点
            if (state.glucose.chartData.length > 0) {
                const lastData = state.glucose.chartData[state.glucose.chartData.length - 1];
                const x = 40 + (lastData.time / maxTime) * (width - 60);
                const y = height - 20 - ((lastData.value - yMin) / (yMax - yMin)) * (height - 40);
                
                ctx.fillStyle = state.glucose.value > state.glucose.normalRange.max ? '#FF9500' : 
                               state.glucose.value < state.glucose.normalRange.min ? '#007AFF' : '#34C759';
                ctx.beginPath();
                ctx.arc(x, y, 6, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制标签
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('时间 →', width/2, height - 5);
            
            ctx.textAlign = 'right';
            ctx.fillText('血糖浓度 (mmol/L)', 35, 15);
            
            // 绘制刻度
            ctx.fillStyle = '#999';
            ctx.font = '10px Arial';
            ctx.textAlign = 'right';
            
            // Y轴刻度
            for (let value = 3; value <= 9; value += 2) {
                const y = height - 20 - ((value - yMin) / (yMax - yMin)) * (height - 40);
                ctx.beginPath();
                ctx.moveTo(35, y);
                ctx.lineTo(40, y);
                ctx.stroke();
                ctx.fillText(value.toString(), 33, y + 3);
            }
        }

        function updateWaterChart() {
            const ctx = window.canvasContexts.waterChart;
            const canvas = document.getElementById('water-chart');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            
            if (state.water.chartData.length < 2) return;
            
            // 绘制坐标轴
            ctx.strokeStyle = '#ccc';
            ctx.lineWidth = 1;
            
            ctx.beginPath();
            ctx.moveTo(40, 20);
            ctx.lineTo(40, height - 20);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(40, height - 20);
            ctx.lineTo(width - 20, height - 20);
            ctx.stroke();
            
            // 绘制正常范围区域
            const yMin = 280;
            const yMax = 320;
            const normalMinY = height - 20 - ((state.water.normalRange.min - yMin) / (yMax - yMin)) * (height - 40);
            const normalMaxY = height - 20 - ((state.water.normalRange.max - yMin) / (yMax - yMin)) * (height - 40);
            
            ctx.fillStyle = 'rgba(52, 199, 89, 0.1)';
            ctx.fillRect(40, normalMaxY, width - 60, normalMinY - normalMaxY);
            
            // 绘制曲线
            ctx.beginPath();
            ctx.strokeStyle = '#007AFF';
            ctx.lineWidth = 3;
            
            const maxTime = Math.max(...state.water.chartData.map(d => d.time));
            
            for (let i = 0; i < state.water.chartData.length; i++) {
                const data = state.water.chartData[i];
                const x = 40 + (data.time / maxTime) * (width - 60);
                const y = height - 20 - ((data.value - yMin) / (yMax - yMin)) * (height - 40);
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
            }
            ctx.stroke();
            
            // 绘制当前点
            if (state.water.chartData.length > 0) {
                const lastData = state.water.chartData[state.water.chartData.length - 1];
                const x = 40 + (lastData.time / maxTime) * (width - 60);
                const y = height - 20 - ((lastData.value - yMin) / (yMax - yMin)) * (height - 40);
                
                ctx.fillStyle = state.water.osmolarity > state.water.normalRange.max ? '#FF9500' : 
                               state.water.osmolarity < state.water.normalRange.min ? '#007AFF' : '#34C759';
                ctx.beginPath();
                ctx.arc(x, y, 6, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制标签
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('时间 →', width/2, height - 5);
            
            ctx.textAlign = 'right';
            ctx.fillText('渗透压 (mOsm/L)', 35, 15);
            
            // 绘制刻度
            ctx.fillStyle = '#999';
            ctx.font = '10px Arial';
            ctx.textAlign = 'right';
            
            for (let value = 285; value <= 315; value += 10) {
                const y = height - 20 - ((value - yMin) / (yMax - yMin)) * (height - 40);
                ctx.beginPath();
                ctx.moveTo(35, y);
                ctx.lineTo(40, y);
                ctx.stroke();
                ctx.fillText(value.toString(), 33, y + 3);
            }
        }

        function updateTempChart() {
            const ctx = window.canvasContexts.tempChart;
            const canvas = document.getElementById('temp-chart');
            const width = canvas.width;
            const height = canvas.height;
            
            ctx.clearRect(0, 0, width, height);
            
            if (state.temperature.chartData.length < 2) return;
            
            // 绘制坐标轴
            ctx.strokeStyle = '#ccc';
            ctx.lineWidth = 1;
            
            ctx.beginPath();
            ctx.moveTo(40, 20);
            ctx.lineTo(40, height - 20);
            ctx.stroke();
            
            ctx.beginPath();
            ctx.moveTo(40, height - 20);
            ctx.lineTo(width - 20, height - 20);
            ctx.stroke();
            
            // 绘制正常范围区域
            const yMin = 35;
            const yMax = 39;
            const normalMinY = height - 20 - ((state.temperature.normalRange.min - yMin) / (yMax - yMin)) * (height - 40);
            const normalMaxY = height - 20 - ((state.temperature.normalRange.max - yMin) / (yMax - yMin)) * (height - 40);
            
            ctx.fillStyle = 'rgba(52, 199, 89, 0.1)';
            ctx.fillRect(40, normalMaxY, width - 60, normalMinY - normalMaxY);
            
            // 绘制曲线
            ctx.beginPath();
            ctx.strokeStyle = '#FF3B30';
            ctx.lineWidth = 3;
            
            const maxTime = Math.max(...state.temperature.chartData.map(d => d.time));
            
            for (let i = 0; i < state.temperature.chartData.length; i++) {
                const data = state.temperature.chartData[i];
                const x = 40 + (data.time / maxTime) * (width - 60);
                const y = height - 20 - ((data.value - yMin) / (yMax - yMin)) * (height - 40);
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
            }
            ctx.stroke();
            
            // 绘制当前点
            if (state.temperature.chartData.length > 0) {
                const lastData = state.temperature.chartData[state.temperature.chartData.length - 1];
                const x = 40 + (lastData.time / maxTime) * (width - 60);
                const y = height - 20 - ((lastData.value - yMin) / (yMax - yMin)) * (height - 40);
                
                ctx.fillStyle = state.temperature.value > state.temperature.normalRange.max ? '#FF3B30' : 
                               state.temperature.value < state.temperature.normalRange.min ? '#007AFF' : '#34C759';
                ctx.beginPath();
                ctx.arc(x, y, 6, 0, Math.PI * 2);
                ctx.fill();
            }
            
            // 绘制标签
            ctx.fillStyle = '#666';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText('时间 →', width/2, height - 5);
            
            ctx.textAlign = 'right';
            ctx.fillText('体温 (°C)', 35, 15);
            
            // 绘制刻度
            ctx.fillStyle = '#999';
            ctx.font = '10px Arial';
            ctx.textAlign = 'right';
            
            for (let value = 36; value <= 38; value += 0.5) {
                if (value % 1 === 0) {
                    const y = height - 20 - ((value - yMin) / (yMax - yMin)) * (height - 40);
                    ctx.beginPath();
                    ctx.moveTo(35, y);
                    ctx.lineTo(40, y);
                    ctx.stroke();
                    ctx.fillText(value.toString(), 33, y + 3);
                }
            }
        }
    </script>
</body>
</html>

### 3. 过程输出

### 3. 使用指南

## 人体内环境与稳态调节交互式教学动画使用指南

欢迎使用本交互式教学动画！本工具旨在通过动态可视化方式，帮助您深入理解人体维持血糖、水平衡和体温稳态的精密负反馈调节机制。以下是详细的使用说明，助您获得最佳学习体验。

---

### 一、 功能说明

本动画是一个基于HTML5 Canvas开发的交互式学习工具，包含四个核心模块：
1.  **血糖调节**：模拟血糖升高或降低后，胰岛素与胰高血糖素的调节过程。
2.  **水平衡调节**：模拟体液渗透压变化后，抗利尿激素（ADH）的调节与渴觉产生。
3.  **体温调节**：模拟高温或低温环境下，机体的散热与产热调节机制。
4.  **模型总结**：通过拖拽互动，构建负反馈调节的通用模型，实现知识迁移与升华。

每个模块均包含**情景模拟、动画演示、动态图表和分步解说**，形成一个完整的学习闭环。

---

### 二、 主要功能与操作

#### 1. 模块导航
- **顶部标签页**：点击“血糖调节”、“水平衡调节”、“体温调节”、“模型总结”四个标签，可在不同主题间自由切换。
- **设计意图**：支持对比学习，帮助您发现不同生理调节背后的共同模式。

#### 2. 情景模拟（以血糖模块为例）
- **预设情景按钮**：点击“摄入葡萄糖”或“运动消耗”按钮，快速设定一个偏离稳态的初始状态。
- **精细调节滑块**：拖动滑块，可任意设定血糖浓度、渗透压或体温的初始值，观察不同偏离程度下的调节过程。
- **实时状态显示**：数值旁会动态显示“（正常）”、“（过高）”或“（过低）”的提示。

#### 3. 动画控制
- **播放/暂停（▶/⏸）**：观看从稳态打破到完全恢复的连续动画过程。
- **下一步（→）**：手动控制，分步学习调节机制的每一个关键环节（稳态打破→检测→控制→执行→恢复），适合初次学习。
- **重置（↺）**：将动画恢复至初始的稳态状态，以便重新开始或尝试不同参数。

#### 4. 信息呈现
- **主动画区**：采用示意图风格，突出关键器官（胰腺、下丘脑、肝脏等）、物质流动（激素、神经信号）和参数指示器。
- **动态图表区**：实时绘制关键生理参数随时间变化的曲线，直观展示其“偏离→回归→稳定”的动态过程。
- **分步解说区**：与动画步骤同步高亮显示当前阶段的文字说明，帮助您将视觉信息与概念理解相结合。

#### 5. 知识建构（模型总结页）
- **拖拽互动**：将左侧的通用组件（传感器、控制中心、效应器、受控变量）拖拽到右侧环路的正确位置。
- **检查答案**：系统会反馈您的完成情况，帮助您巩固对负反馈调节通用模型的理解。
- **示例参考**：页面下方提供了血糖调节的具体实例，辅助您完成抽象模型的构建。

---

### 三、 设计特色

1.  **符合认知规律**：采用“具体实例→抽象模型”的递进式设计，先建立感性认识，再归纳共性规律。
2.  **双重学习路径**：支持“连续播放”整体把握流程，也支持“分步学习”深入理解细节，满足不同学习风格。
3.  **语义化视觉编码**：
    - **颜色**：暖色（橙、红）代表“升高/警报”，冷色（蓝）代表“降低/纠正”，绿色代表“正常/恢复”。
    - **动态元素**：闪烁的高亮、流动的粒子、抖动的线条，用于强调正在活跃的调节路径。
4.  **数据可视化整合**：将难以直接观察的生理参数变化，转化为直观的实时曲线图，实现“可视化”与“量化”结合。

---

### 四、 教学要点与学习目标

通过本动画，您将能够：
1.  **描述具体过程**：清晰阐述血糖、水平衡、体温调节中，从刺激到反应的完整因果链条。
2.  **识别核心组件**：准确指出每个调节实例中的“传感器”、“控制中心”和“效应器”。
3.  **理解负反馈本质**：解释为什么这些调节机制被称为“负反馈”，以及其对于维持“稳态”的核心价值。
4.  **建立通用模型**：将三个具体实例中的组件，映射到“受控变量→传感器→控制中心→效应器→受控变量”的通用负反馈环路模型中，实现知识的迁移与应用。

---

### 五、 使用建议

1.  **初次学习者**：
    - 建议按顺序（血糖→水平衡→体温）学习各个模块。
    - 每个模块先使用“下一步”功能进行分步学习，理解每一步的生理意义后，再使用“播放”功能观看连续过程。
    - 积极操作“情景模拟”滑块，观察不同程度偏离下的调节差异。

2.  **复习与巩固者**：
    - 直接使用“播放”功能快速回顾整体流程。
    - 挑战“模型总结”页面的拖拽任务，检验自己能否将具体知识抽象为通用模型。
    - 尝试对比三个模块的异同，思考“为什么下丘脑在多个调节中扮演核心角色？”等问题。

3.  **教师与教学组织者**：
    - 可作为课堂演示工具，直观展示抽象的生理过程。
    - 可布置探究任务：“如果胰岛素失效（模拟糖尿病），曲线图会如何变化？”引导学生思考。
    - 利用“模型总结”页面作为课堂互动环节，让学生上台完成组件拖拽。

**祝您探索愉快！希望这个动画能帮助您揭开人体精密调节系统的奥秘，感受生命维持稳态的智慧与魅力。**