Updates On request designing : 
Daily/7-Day DSP and Driver Performance Analysis Curve:

Goal: Automate and generate performance analysis curves for each DSP and driver.
Action: Begin with Unimap and Shenghu to check if a similar tool is already in development.
Approach: If they aren't working on this, start developing the performance analysis tool by gathering all available DSP and driver data for daily/7-day performance.
Integration: Investigate Unimap’s underlying data and logic structure for potential collaboration.


# UniVision - 初期规划第二版 - 已完成初始(基础功能搭建)
---

# Driver Efficiency Analysis 司机效率分析

This project aims to analyze and visualize driver efficiency using data from multiple Excel files. The primary focus is on tracking and displaying trends in completion rates and other key metrics for specific drivers over time. The visualization includes line charts, bar charts, and pie charts, allowing for comprehensive insights into driver performance.

本项目旨在利用多个Excel文件中的数据分析和可视化司机效率。主要关注点是跟踪和显示特定司机的完成率及其他关键指标随时间的趋势变化。可视化内容包括折线图、柱状图和饼图，提供对司机表现的全面洞察。(之后会逐步加入对于DSP以及各个站点的综合分析,但会依据公司职员层级设置不同观测权限,保证公司数据安全).

## Project Overview 项目概述

The project processes data from Excel files containing driver performance metrics. The primary data points include `Completion Rate`, `Last Update`, and various status codes. The visualizations are interactive, allowing users to navigate between different charts using buttons.

本项目处理包含司机表现指标的Excel文件中的数据。主要数据点包括`完成率`、`最后更新时间`以及各种状态代码。可视化内容具有交互性，用户可以通过按钮在不同图表之间切换。

## Features 功能

1. **Completion Rate Trend Line Chart 完成率趋势折线图**:
   - Displays the trend of completion rates for a specific driver over time.
   - Data is consolidated from multiple files to show changes in performance.

   显示特定司机随时间变化的完成率趋势。数据来自多个文件，展示表现的变化。

2. **Completion Rate Bar Chart 完成率柱状图**:
   - Shows the completion rates for all drivers, highlighting those below a specific threshold with a different color.

   显示所有司机的完成率，并以不同颜色突出显示低于特定阈值的司机。

3. **Driver Status Distribution Pie Chart 司机状态分布饼图**:
   - Illustrates the distribution of various statuses for a specific driver, providing insight into the nature of tasks handled.

   展示特定司机的各种状态分布，提供处理任务性质的见解。

## Data Analysis and Visualization 数据分析与可视化

### Key Data Points 关键数据点
- **Completion Rate 完成率**: Percentage indicating the completion of assigned tasks. 表示分配任务完成情况的百分比。
- **Last Update 最后更新时间**: The date and time of the last recorded update for a driver. 司机的最后一次记录更新时间。(这里需要更准确的批次当天发货日期信息, 需要更加精准的数据 -⚠️ **Database 读取权限(无须写入)**
- **Status Codes 状态代码**: Various codes representing different states or actions in the delivery process (e.g., `200`, `202`, `211`, etc.). 表示配送过程中不同状态或操作的各种代码（如`200`、`202`、`211`等）。

### Analytical Focus 分析重点
1. **Trend Analysis 趋势分析**:
   - Observing how completion rates change over time for specific drivers.
   - Understanding factors contributing to changes in performance.

   观察特定司机的完成率随时间的变化。理解导致表现变化的因素。

2. **Performance Comparison 表现比较**:
   - Comparing completion rates across drivers to identify top performers and areas needing improvement.

   比较不同司机的完成率，识别表现优异者和需要改进的领域。(获取整体数据后加入整体对于城市间DSP的整体分析✅)

3. **Status Analysis 状态分析**:
   - Analyzing the distribution of various status codes to understand the common issues or states in the delivery process.

   分析各种状态代码的分布，了解配送过程中的常见问题或状态。

## Challenges and Solutions 挑战与解决方案

### Challenges 挑战
1. **Data Cleaning and Integration 数据清理与整合**:
   - Handling missing values and ensuring consistency across multiple data sources.
   - Merging data from different Excel sheets with potentially varying formats.

   处理缺失值并确保多个数据源之间的一致性。合并格式可能不同的Excel工作表中的数据。

2. **Visualization Accuracy 可视化准确性**:
   - Ensuring that charts accurately reflect data trends, especially when handling date-time data and percentages.

   确保图表准确反映数据趋势，特别是在处理日期时间数据和百分比时。

3. **Interactive Display 交互显示**:
   - Implementing an intuitive way for users to switch between different visualizations.

   实现一种直观的方式，供用户在不同的可视化之间切换。

### Solutions 解决方案
1. **Data Cleaning 数据清理**:
   - Implemented functions to clean and standardize completion rate data.
   - Used `pandas` to handle missing values and format inconsistencies.

   实施了清理和标准化完成率数据的函数。使用`pandas`处理缺失值和格式不一致问题。

2. **Accurate Plotting 准确绘图**:
   - Utilized `matplotlib` to plot data accurately, handling date-time conversions and percentage calculations.

   使用`matplotlib`准确绘制数据，处理日期时间转换和百分比计算。

3. **Interactive Controls 交互控制**:
   - Added buttons for navigating between charts, enhancing the user experience with interactive elements.

   添加了在图表之间导航的按钮，通过交互元素增强用户体验。

## How to Run 如何运行

1. **Dependencies 依赖**:
   - Python packages: `pandas`, `matplotlib`
   - Ensure the required packages are installed in your environment.

   确保在您的环境中安装所需的软件包。

2. **Execution 执行**:
   - Run the main script (`main.py`) to start the visualization interface.
   - Use the buttons to navigate between different charts.

   运行主脚本（`main.py`）启动可视化界面。使用按钮在不同图表之间导航。

3. **Data Files 数据文件**:
   - Place the relevant Excel files in the specified directory.
   - Update the file paths in the script if necessary.

   将相关的Excel文件放在指定目录中。如有必要，更新脚本中的文件路径。

## Future Improvements 未来改进

- **Additional Metrics 额外指标**: Incorporate more metrics for a comprehensive analysis of driver performance. 纳入更多指标以全面分析司机表现。
- **Enhanced Interactivity 增强交互性**: Add more interactive features, such as zooming and filtering data. 添加更多交互功能，如缩放和过滤数据。
- **Automated Updates 自动更新**: Set up a system for automatic updates and data processing as new data becomes available. 建立一个系统，以便在新数据可用时进行自动更新和数据处理。

## Contribution 贡献

Contributions are welcome! Please fork the repository and submit a pull request with your changes. For major changes, please open an issue first to discuss what you would like to change.

欢迎贡献！请fork此仓库并提交您的更改的pull request。如有重大更改，请先打开issue讨论您想要更改的内容。
请联系:xiyue1832@gmail.com




------------------------------------------------------------------
### Local Python Setup Decision 本地Python环境选择

In the initial stages of the project, the decision was made to utilize a local Python setup rather than relying solely on web-based solutions such as Jupyter Notebook. This choice was driven by several key considerations:

在项目的初期阶段，决定使用本地Python环境，而不是仅依赖于网络端解决方案，如Jupyter Notebook。这个选择基于以下几个关键考虑因素：

#### 1. Scalability and Integration with National Sites 扩展性与全国站点的集成

The project aims to eventually integrate with various sites across the United States. To achieve seamless integration and to provide a unified interface for data processing and analysis, a local Python setup offers greater flexibility and control. This setup allows for the development of APIs and microservices, facilitating smooth data exchange and processing between different sites and the central system.

该项目旨在最终与美国各地的不同站点进行集成。为了实现无缝集成，并为数据处理和分析提供统一的接口，本地Python环境提供了更大的灵活性和控制力。这种设置允许开发API和微服务，从而在不同站点与中央系统之间实现平稳的数据交换和处理。

#### 2. Performance and Customization 性能与定制化

Running Python scripts locally provides better performance, especially when dealing with large datasets and complex computations. Local setups allow for fine-tuned optimization and customization of the environment, including the use of specific Python packages and libraries tailored to the project's needs. This level of customization is often limited in web-based environments, where resource allocation and environment configurations are shared and less flexible.

在本地运行Python脚本可以提供更好的性能，尤其是在处理大数据集和复杂计算时。本地设置允许对环境进行精细优化和定制，包括使用针对项目需求的特定Python包和库。这种级别的定制在基于网络的环境中通常是有限的，资源分配和环境配置是共享的且较少灵活性。

#### 3. Data Security and Privacy 数据安全与隐私

Using a local environment enhances data security and privacy, as sensitive data does not need to be transmitted over the internet. This is particularly important when handling confidential information or when there are strict data governance policies in place. A local setup ensures that data processing and storage remain within a secure and controlled environment.

使用本地环境可以增强数据安全和隐私，因为敏感数据不需要通过互联网传输(这点很重要)。这在处理机密信息或有严格的数据治理政策时尤为重要。本地设置确保数据处理和存储保持在安全且受控的环境中。


总之，选择使用本地Python环境而不是基于网络的Jupyter Notebook设置，主要是由于对可扩展性、性能、安全性和灵活性的需求。这种设置使项目能够在受控环境中开发，为未来与全国站点的集成提供了坚实的基础，并确保了强大的安全数据处理能力。





--------------------------------------------------------------------------------08/06/2024
项目规划：UniVision 货运数据可视化项目
前期准备 (4周)
目标：了解技术栈，准备与公司API融洽的技术项目规划。

技术栈学习与熟悉（2周）：
学习和熟悉项目所需的技术栈，如前端框架（React.js 或 Vue.js）、后端框架（Node.js 或 Django）等。
理解快递物流实时数据接口和历史数据接口的使用方法。
需求分析与项目规划（2周）：
分析业务需求，明确项目目标和功能模块。
制定详细的项目计划，包括时间安排、任务分配、风险评估等。
准备技术文档和API文档，确保团队对技术要求和实现方案有清晰的理解。

**项目开发阶段 (6周)
**目标：完成平台后端数据API和数据搭建，初步实现数据可视化功能。

后端开发（4周）：

搭建后端框架，设计数据库结构。
实现实时数据API，处理快递物流实时司机配送地图轨迹查询的具体应用场景。
实现历史数据API，用于分析和展示过去的快递数据。
编写单元测试和集成测试，确保API的稳定性和可靠性。
前端开发（2周）：

设计并实现UI界面，包含图表、地图、仪表盘等可视化组件。
集成实时数据API，实现快递运输情况的实时展示。
集成历史数据API，展示过去一段时间的快递数据。
实现基本的交互功能，如筛选、排序、数据导出等。
项目整合与优化 (4周)
目标：进一步完善和优化项目，集成PowerBI，实现高级数据分析和展示。

功能完善（2周）：

优化前端UI和交互体验，提升用户友好度。
增加高级功能，如自定义报表、数据对比分析等。
修复开发过程中发现的bug，提升系统稳定性。
技术集成（2周）：
学习和了解PowerBI的功能和使用方法。
尝试将PowerBI集成到项目中，实现高级数据分析和展示。
编写文档和使用指南，帮助团队成员和用户更好地使用系统。
