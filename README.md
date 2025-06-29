这是一个配色方案生成工具。可以根据用户提供的原色生成一套符合莫兰迪配色规律的配色方案，从而提升高端感。

## 用法

1. 输入命令
```bash
moranti #FF6900 -o design.html
```
输出两段html标签
第一段是色彩的示例，色值仅用于参考，实际要根据原色值按照配色规则生成
```html
<div class="color-group" style=" display: flex;flex-direction: column;gap: 8px;">
	<div class="color-card" style="background: #f8f9fa;border-radius: 8px;padding: 12px;">
		<div class="color-title" style="font-weight: 600;margin-bottom: 8px;font-size: 16px;">小米-莫兰迪色系</div>
		
		<div class="color-swatch" style="background:#F3E0D1;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #4a4a4a;margin: 4px 0;">
			#F3E0D1
		</div>
		<div class="color-swatch" style="background:#E2C9BD;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #4a4a4a;margin: 4px 0;">
			#E2C9BD
		</div>
		<div class="color-swatch" style="background:#C2D8E4;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #4a4a4a;margin: 4px 0;">
			#C2D8E4
		</div>
		<div class="color-swatch" style="background:#B8C9B0;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #4a4a4a;margin: 4px 0;">
			#B8C9B0
		</div>
		<div class="color-swatch" style="background:#E5DED7;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #4a4a4a;margin: 4px 0;">
			#E5DED7
		</div>
		<div class="color-scene">适用：商务演示/产品画册</div>
	</div>
	<div class="color-card" style="background: #f8f9fa;border-radius: 8px;padding: 12px;">
		<div class="color-title" style="font-weight: 600;margin-bottom: 8px;font-size: 16px;">小米Logo辅助色</div>
		<div class="color-swatch" style="background:#898989;height: 40px;border-radius: 4px;display: flex;align-items: center;justify-content: center;font-size: 12px;color: #ffffff;margin: 4px 0;">
			#898989
		</div>
	</div>
</div>

```
第二段是实际应用的示例，色值仅用于参考，实际要根据原色值按照配色规则生成
```html
<!-- 应用预览 -->
<div style="background:#F8F5F0; padding:30px; border-radius:12px; margin-top:30px; max-width:1000px; margin:30px auto;">
  <h2 style="color:#4A4A4A; border-bottom:1px solid #E3B08C; padding-bottom:10px;">莫兰迪配色应用示例</h2>
  <div style="display:flex; gap:20px; margin-top:20px;">
    <div style="background:#E3B08C; padding:20px; border-radius:8px; flex:2;">
      <h3 style="color:#4A4A4A;">主色区域</h3>
      <p style="color:#4A4A4A;">基于#FF6900生成的莫兰迪陶橙作为主色，温暖而不刺眼</p>
      <button style="background:#8AA2A9; border:none; padding:10px 20px; border-radius:4px; margin-top:15px; color:#F5F5F5;">雾灰蓝按钮</button>
    </div>
    <div style="background:white; padding:20px; border-radius:8px; flex:1; border:1px solid #8AA2A9;">
      <h3 style="color:#4A4A4A;">辅助信息</h3>
      <p style="color:#4A4A4A;">使用雾灰蓝作为边框的辅助内容区</p>
    </div>
  </div>
</div>
```

## 配色规则

以下是将三个表格整合后的**莫兰迪配色核心规则总表**，按四大角色分类展示明度、饱和度、对比度等完整规范：

### 莫兰迪配色规则总表
| **角色**   | **明度范围 (L*)**          | **饱和度范围** | **对比度要求**                 | **视觉感受** | **适用场景**    | **示例颜色**                   | **色差要求 (ΔE)** |
| ---------- | -------------------------- | -------------- | ------------------------------ | ------------ | --------------- | ------------------------------ | ----------------- |
| **背景色** | 75%-85%                    | 20%-30%        | 与主色：ΔL=10-20 (2.0:1-3.0:1) | 轻盈、通透   | 大面积墙面/基底 | `#F5F3EF`（奶油白）            | ≤15               |
| **主色**   | 65%-75%                    | 30%-40%        | 与点缀：ΔL=10-15 (3.0:1-4.0:1) | 沉稳、柔和   | 主家具/功能主体 | `#A8C7E0`（雾灰蓝）            | 20-30             |
| **点缀色** | 55%-65%                    | 40%-50%        | 与背景：ΔL≥25 (≥4.5:1)         | 聚焦、层次感 | 小物件/强调元素 | `#D4A596`（陶土粉）            | ≥35               |
| **文本色** | 深：20%-40%<br>浅：80%-95% | 0%-20%         | 与背景：ΔL≥35 (≥4.5:1)         | 清晰、无干扰 | 信息传达        | 深：`#4A4A4A`<br>浅：`#F5F5F5` | -                 |

---

### 整合说明与关键规则
1. **明度阶梯系统**  
   ```mermaid
   graph LR
     A[背景 80%] --> B[主色 70%] 
     B --> C[点缀 60%] 
     C --> D[深文本 30%]
   ```
   - 严格保持：背景 > 主色 > 点缀 > 深文本
   - 明度差ΔL控制：10-20（相邻角色间）

2. **饱和度负相关原则**  
   | 角色变化  | 明度降低幅度 | 饱和度增加幅度 |
   | --------- | ------------ | -------------- |
   | 背景→主色 | -10%         | +10%           |
   | 主色→点缀 | -10%         | +10%           |
   ```数学
   饱和度补偿公式：  
   S_new = S_prev + (ΔL/10) × 0.1
   ```

3. **对比度黄金三角**  
   ```mermaid
   flowchart TD
     A[背景-主色] -- 2.0:1~3.0:1 --> B[主色-点缀]
     B -- 3.0:1~4.0:1 --> C[点缀-背景]
     C -- ≥4.5:1 --> D[文本-背景]
   ```

4. **色相协调守则**
   - 背景：中性色（40°-80°暖灰/200°-240°冷灰）
   - 主色：自然意象色（20°-30°陶橙/100°-140°灰绿）
   - 点缀：主色互补±30°（如橙主色配蓝点缀）
   - 文本：无彩色或同色系微饱和（ΔH≤5°）

---

### 跨角色验证指标
| **交互对**  | **合格标准**    | **检测工具**          |
| ----------- | --------------- | --------------------- |
| 背景-主色   | ΔL=10-20, ΔE≤15 | Adobe Color 对比分析  |
| 主色-点缀色 | ΔL=10-15, ΔE≥20 | WebAIM对比度检测器    |
| 背景-文本   | 对比度≥4.5:1    | WCAG Contrast Checker |
| 整体配色    | 色彩重心Y≥0.7   | Pantone色彩平衡仪     |


### 违规修正速查表
| **问题现象**     | **根本原因**     | **修正方案**             |
| ---------------- | ---------------- | ------------------------ |
| 主色淹没在背景中 | 背景-主色ΔL<10   | 主色明度-5%，饱和度+8%   |
| 点缀色突兀       | 主色-点缀ΔE>40   | 点缀添加15%背景色调和    |
| 文本阅读吃力     | 文本-背景ΔL<35   | 文本改用#333或#EEE       |
| 色彩沉闷缺乏层次 | 全角色饱和度<25% | 点缀饱和度+15%，主色+10% |

此整合表涵盖了莫兰迪配色的核心维度，可作为设计实施的标准化指南。