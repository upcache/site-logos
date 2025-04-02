# 网站LOGO收集
本项目用于收集储存要加速的网站LOGO。任意用户都可提交您的网站或其他网站的LOGO图片，可以是jpg、png、svg、ico等格式。  
每个logo文件夹除了需要存放一些logo文件以外，还需要存放package.json，用于描述logo所在网站的信息。  

## 1.整体目录结构
目录结构如下：  
src   
└── [domain]  
    ├── [date]  
    │   ├── logo1.png  
    │   └── logo2.png  
    └── package.json   
其中，“[domain]”为域名或别名，“[date]”为年月日日期，例如：  
src  
└── cloud.baidu.com  
    ├── 20250331  
    │   ├── favicon.ico  
    │   ├── logo-full.png  
    │   └── logo-og.png  
    └── package.json  
   
## 2.Logo存放路径
存放路径格式为：/src/:domain/:date/:path
 - “:domain”为网站域名，如果前缀为www，则可省略；如果前缀为www，同时后缀为com，则前后两者都可省略；如果网站很出名，则可只写主体标识。例如：“github”、“cloud.baidu.com”。
 - “:date”为年月日日期，例如：20250331。
 - “:path”为文件路径，基本上不需要子目录。

## 3.Logo命名规则
Logo文件一般有favicon、logo、apply touch icon等形式以及其颜色、样式、倍率等变化。  
命名格式一般为“{name}(-{width}x{height}){.ext}”或者“{name}(@{rate}){.ext}”  
以下为具体说明，其中中小括号代表可省略，大括号代表必须。
 - favicon文件名格式为 “favicon(-size){.ext}”，例如：favicon-48.png
 - logo文件按内容大致可分为logo、logo-full、logo-text、logo-op等四类
 - (1) logo 表示正方形核心图像，命名为“logo(-{width}x{height}){.ext}”或者“logo(@{rate}){.ext}”，例如：logo-128x128.png、logo@2x.png。
 - (2) logo-text 表示只包含网站名称的logo图片，命名为“logo-text(-{width}x{height}){.ext}”或者“logo-text(@{rate}){.ext}”，例如：logo-text-260x128.png、logo-text@2x.png。
 - (3) logo-full 表示核心logo加上网站名称的合成图，命名为“logo-full(-{width}x{height}){.ext}”或者“logo-full(@{rate}){.ext}”，例如：logo-full-320x128.png、logo-full@2x.png。
 - (4) logo-op 表示网站首页OG标签(开放图像协议)对应的logo图，一般有尺寸标准，命名为“logo-og(-{width}x{height}){.ext}”或者“logo-og(@{rate}){.ext}”。
 - apply touch icon 为苹果相关应用下的展示图标，命名为“apple-touch-icon(-{width}x{height}){.ext}”，例如：apple-touch-icon-114x114.png。
 - 其他logo图片等，命名为“{name}(-{width}x{height}){.ext}”或者“{name}(@{rate}){.ext}”，例如：safari-pinned-tab.svg、apple-touch-icon-precomposed.png。
 
## 4.属性描述
使用logo文件夹下的package.json来描述该logo和所属网站的基本信息。结构与npm包描述文件package.json类似，但只包含以下字段信息：
 - name - 域名或别名，必填
 - title - 网站标题，可为空
 - description - 网站描述，可为空
 - version - logo最新版本，必填
 - homepage - 网站主页，必填
 - keywords - 关键字，数组，可为空

可参考本项目根目录下的package.sample.json文件。

## 5.支持网站域名 
为了使添加的logo有较高的质量和较长的活跃度，我们限制了域名类型。目前暂时仅限.com、.net、.org、.cn、.com.cn、.dev等域名类型的网站加入。比较出名的网站，或者有特别需要的网站，可申请加入。
