# UniVision - 初期规划第二版 - 已完成初始(基础功能搭建)
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
