<p align="center">
  <a href="https://github.com/backtomyJune/Dual_porosity-with-hydro-mechanical-chemical-/">中文</a>
  ｜
  <a href="https://github.com/backtomyJune/Dual_porosity-with-hydro-mechanical-chemical-/blob/main/README_en.md">English</a>
</p>

# DP-HMC 多物理场耦合：膨润土基防渗材料服役性能预测求解器平台
## 项目概述
本项目旨在开发一个基于 双孔隙模型 (Dual-Porosity, DP) 并耦合 水力-力学-化学 (Hydro-Mechanical-Chemical, HMC) 过程的数值模拟求解器平台

- 核心目标是攻克膨润土基防渗材料在复杂多物理场耦合服役环境下性能劣化机制不清晰与长期寿命预测不准的关键行业难题
- 求解器能够模拟流体渗流、溶质运移、力学变形及其相互耦合作用
- 因基金资助要求，项目只开源部分代码供参考学习
  
若本项目对您有帮助 :thumbsup: ，请右上角点个Star :star: 支持一下！！谢谢！！

## 当前研究进展
目前，本项目已完成模拟器中核心模块的开发：
### :white_check_mark: 已实现的功能：
### 1.对流-弥散模型求解器 (ADE Solver)
用于模拟在单一孔隙介质中的溶质迁移过程
### 2.双孔隙/两域模型求解器 (DP Solver)
针对膨润土基防渗材料具有显著宏观-微观孔隙特征的介质，实现了动水区与不动水区之间的质量交换，更准确地刻画了溶质运移的非Fick扩散与时间滞后效应。
### 3.COMSOL二次开发参数化建模
Python语言基于开源库mph：https://mph.readthedocs.io/en/1.2/ 的COMSOL模型二次开发，已完成随机二维多孔介质模型构建
### 4.集成机器学习模型预测服役寿命：极端梯度增强（Extreme Graddient Boosting，XGBoost）
在XGB集成机器学习模型的基础上考虑时间序列分析膨润土基防渗材料在DP+HMC多物理场耦合作用下的服役寿命影响分析

## :children_crossing: 进行中的工作
### 1.DP+HMC全耦合框架扩展
在现有溶质迁移（化学场，C）模块的基础上，正在集成水力场 (H) （如流体流动）和力学场 (M) （如应力、形变）的控制方程。
目标是最终实现真正意义上的水-力-化全耦合求解，以模拟膨润土基防渗材料在实际工程中受到侵蚀的复杂过程。
### 2.拓展二次开发模型内容
计划做用户交互UI界面和程序开发
### 3.拓展其他集成深度学习模型和机器学习模型
计划拓展的模型有：
轻量级梯度提升机（Light Gradient Boosting Machine，LightGBM）、自适应增强（Adaptive Boosting，AdaBoost）、随机森林（Random forest，RF）

## 技术栈
仿真软件：COMSOL6.2
开发工具: Python 3.9（scikit-learn、numpy、pandas、Matplotlib等），PyCharm2024

## 未来方向
- 完成HMC全耦合求解器的开发与验证。
- 引入机器学习方法（如物理信息神经网络PINNs、代理模型），用于加速计算、参数反演和不确定性量化。
- 针对特定工程场景（如垃圾填埋场近场环境）开发高级案例和寿命预测工具链。
- 开发UI交互程序

## 联系我
- 如果您有任何问题或合作意向，请通过以下方式联系：
- 邮箱：2311110061@nbu.edu.cn / 289176263@qq.com

## 致谢
- 感谢导师的国家自然科学基金（批准号42477151；42107174）、中国博士后科学基金（批准号2023M743058）、浙江省自然科学基金重点项目（LZ25E080009）、浙江省博士后科学基金（批准号ZJ2023111）对本研究的资助。
- 感谢宁波中淳高科股份有限公司提供的试验场地
