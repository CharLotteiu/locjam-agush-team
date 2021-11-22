# LocJam - Agush Team
## 项目信息

**Website:** https://sites.google.com/view/from-games-to-gamers/locjam

**Target Language:** Chinese

**Masterclass:**
- What is expected of a game localisation project
- how to carry out the project
- The use of CAT tools is encouraged but not compulsory

**Assessment:**
Translations will be assessed by audience feedback: the texts submitted will be made available for all interested users to test and judge using an assessment form covering different criteria.

**Results & Awards:**
Reported online on or around 11 December

## 项目交付
**Delivery Time:** until **1pm**(14:00 CET), Saturday November 27  
**Delivery Link:**
- adding a folder with your team's name; only one folder per team https://drive.google.com/drive/folders/1907E26k7NysNaMjdSudPwcmvRgWfQT6V
- send a .zip file with [WeTransfer](https://wetransfer.com/ "WeTransfer") at localisationdijon@gmail.com

**[Agush]_[Chinese].zip file:**
- the localized game project , which is the folder “Have I Seen You Somewhere Before” only
- PowerPoint comment
	- things you liked
	- things you didn’t like
	- the particular challenges you faced
	- how you dealt with those challenges
	- why did you translate this or that, that way
	- etc.

## 联系方式
- Email：localisationdijon@gmail.com
- Discord：https://discord.gg/M2SWnZH5tD
- Yizhen: yizhen.li33@mail.dcu.ie
- Yijie: wangyijieaudrey@gmail.com
- Ling: lingling.liu26@mail.dcu.ie
- Shan: shan.su3@mail.dcu.ie

## 协作工具
- 公邮：locjam.zh@gmail.com (locjam.zh1120)
- 翻译工具：Ren'py 软件内翻译工具
- GitHub: https://github.com/CharLotteiu/locjam-agush-team
- Google drive: https://drive.google.com/file/d/1t7uDlLUSuyIP8yNKIguEOZo8AhLmUCC6/view?usp=sharing

## 启动会议（11.21）
- 协作方式: GitHub
- 时间节点:
	- 中期会议 11.23 中午 12：30
- 小组分工:
	- Lars: Ling and Su
	- Michael: ezhen
	- Skylar: Audrey
- 翻译风格: 口语化，简单直白？
- 具体问题
	- xingjiang 是谁？
	- GitHub 仓库建设，使用指南
		- 教程网址 https://b23.tv/6kHWiZe
	- 人名翻译风格问题：简单直接一些？
	- 开场标题（一张图片）是否需要本地化
	- 换一个更适合的字体
		- 猫啃网 https://www.maoken.com/
	- 主人公有灵感来源 [Mads Mikkelsen](https://en.wikipedia.org/wiki/Mads_Mikkelsen)

## 中期会议（11.23 中午 12：30）
- 是否区分不同角色的语气词，如何区分
	- 要不要对不同的characters personalise一下表达风格，v.s. 全文统一（consistent + 方便省事，但可能有点僵？）
- 省略号使用习惯 …… ... ......
- Pull Request 与 Merge to Main 的形式与时间，Review 的形式与时间
	- 按照 Date 提交

## 项目文件分析
- common.py old->new,内容原封不动，可以写个脚本
- options.py 标题，左上角可以直接显示，暂时不用考虑编码问题
- screens.py 菜单栏，编码问题
- script.py 参考截止行数 2726

## 问题解决
### 菜单界面、游戏内选项、人物名称不显示
game/gui.rpy 文件中第 58、61、64 行代码所用字体 primer.ttf 或 poetsenone.ttf 不支持中文，需替换为支持中文的字体。  

```python 
## Fonts and Font Sizes ########################################################

## The font used for in-game text.（原为 primer.ttf）
define gui.text_font = "Deng.ttf"

## The font used for character names.（原为 primer.ttf）
define gui.name_text_font = "Deng.ttf"

## The font used for out-of-game text.（原为 poetsenone.ttf）
define gui.interface_text_font = "Deng.ttf" 
```
字体选择待确认，可选字体链接：https://www.maoken.com/freefonts/12727.html

## 参考材料
- RenPy中文论坛：https://www.renpy.cn/
