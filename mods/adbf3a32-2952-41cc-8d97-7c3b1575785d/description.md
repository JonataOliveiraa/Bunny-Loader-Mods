# ModDifficulty

给 Terraria 添加**自定义世界难度**。原版只有 普通 / 专家 / 大师 / 旅行 四档，这个 mod 让你在世界创建菜单里多出新的难度选项。

## 内容

- **难度系统**：注册新的难度，分配在原版 4 档之后的 ID
- **世界创建菜单**：新难度按钮出现在难度选择栏里，带图标、预览图和颜色
- **世界选择菜单**：世界列表里显示自定义难度的名称与颜色
- **兼容层**：hook `Main.Difficulty` 和 `Main.GameMode`，让游戏把自定义难度当成指定的原版难度运行
  （比如「专家级掉落 + 大师级数值」）

## 附带示例

`ExampleDifficulty`：紫色难度，按大师难度运行，显示名为 "Example"。

## 怎么加自己的难度

```js
import { ModDifficulty } from './DifficultySystem/ModDifficulty.js';

export class MyDifficulty extends ModDifficulty {
    constructor() {
        super();
        this.Texture = 'Textures/MyDifficulty';   // 放到 content/Textures/
    }
    get DisplayName() { return '我的难度'; }
    get Description() { return '说明文字'; }
    get VanillaEquivalent() { return 1; }         // 1=专家 2=大师 3=旅行 0=普通
    GetDifficultyLevel() { return 4; }            // 数值强度
    GetColor() { return Color.new(255, 100, 100); }
}
```

然后注册：

```js
ModDifficulty.register(MyDifficulty);
```

## 纹理

放进 `content/Textures/`，三张：

- `名称.png` —— 难度图标
- `名称_Preview.png` —— 创建菜单里的预览图
- `名称_Bunny.png` —— 可选

## 说明

- 自定义难度存在世界的 `GameMode` 字段里，超出原版 4 档的数值即为 mod 难度；
- 需要新建世界时才能选，已有世界改不了；
- 从 TL Pro 版移植。

## 作者

GST378（[YouTube](https://youtube.com/@gst_378)）
