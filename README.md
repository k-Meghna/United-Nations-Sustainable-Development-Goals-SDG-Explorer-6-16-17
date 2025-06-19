# United-Nations-Sustainable-Development-Goals-SDG-Explorer-6, 16 & 17
DAEN-690-010_Team UN

---
Project Overview:
---
The United Nations Sustainable Development Goals (SDGs), established in 2015, form a comprehensive global framework aimed at addressing critical issues including health, water access, governance, infrastructure, justice, sustainability, and international cooperation. Among these, SDG-6 (Clean Water and Sanitation), SDG-16 (Peace, Justice, and Strong Institutions), and SDG-17 (Partnerships for the Goals) are particularly important due to their interconnected nature and global relevance. The UN maintains a vast and continuously growing dataset to monitor SDG progress, with over 2.7 million records as of 2023. While this data is publicly available in formats like CSV and JSON, its complexity, scale, and multidimensional structure make it challenging to interpret using traditional 2D visualizations. These conventional tools often fall short in representing dynamic relationships between countries, goals, indicators, and time periods—limiting the ability of stakeholders to coordinate efforts or act on insights effectively.
To address these challenges, this project proposes an alternative approach using 3D visualizations via GaiaViz. By transforming SDG data into interactive structures, users can explore donor-recipient interactions, track financial and policy connections, and observe indicator-level progress across geographies and timeframes. The goal is to make complex development data more accessible, interpretable, and actionable.

---
Project Goals:
---
The primary objective of this project is to enhance understanding and transparency around global SDG implementation. For Spring 2025, the focus was placed on the following indicators:

SDG-6:

6.3.1 – Wastewater treatment

6.3.2 – Ambient water quality

6.5.1 – Integrated water resources management

6.a.1 – Official Development Assistance (ODA) to water and sanitation

SDG-16:

16.1.1 – Intentional homicides

16.3.2 – Unsentenced detainees

16.5.1 – Bribery incidence

16.6.1 – Government expenditure as a proportion of the approved budget

SDG-17:

17.3.1 – Foreign direct investment, remittances, and ODA

Using open-access datasets from the UN SDG database, we developed a pipeline that preprocesses, filters, and transforms data for compatibility with the GaiaViz platform. This pipeline includes steps such as country name standardization, stakeholder role assignment (e.g., torchbearer or donor, beneficiary or recipient), geolocation mapping, and indicator value normalization. In the GaiaViz visualization, each country is represented as a rod (node), placed within year rings that depict temporal groupings. Attached to each node are colored petals, representing individual SDG indicators. Links connect countries or indicators, encoding relationships such as donor-recipient or torchbearer-beneficiary impact. Link thickness and direction reflect funding magnitude or policy relevance. The final visual output enables stakeholders to analyze and understand how different actors—countries, regions, and organizations—interact within the SDG ecosystem, contributing to more effective policymaking and international coordination. 

---
Initial Requirements: 
---
To run this project, you'll need to install the following dependencies: • Python 3.x • Pandas • Requests • Zipfile (Standard Python Library) • Jupyter Notebook (Optional, for interactive data exploration)

---
Notebooks:
---
Jupyter notebooks that handle data cleaning: Integrated_Datasets_Indicators.ipynb, processing, and export operations across various Sustainable Development Goals. The notebook SDG-6_Global.ipynb is dedicated to global-level processing of SDG-6 indicators, including steps such as normalization, geolocation mapping, and tag generation. For region-specific analysis, SDG-6_EU_US_china.ipynb processes SDG-6 data for the United States, European Union, and China by assigning roles, formatting the data for GaiaViz, and exporting node and tag files. The SDG-16_Global.ipynb notebook supports global analysis of SDG-16 indicators, applying similar transformations. Finally, SDG-6, 16, 17_Fullcode.ipynb is a consolidated notebook that integrates datasets for SDG-6, SDG-16, and SDG-17 into a single pipeline, producing unified visualizations for comprehensive analysis within the GaiaViz platform.

---
Datasets and Templates:
---
These files serve as both datasets and templates for structuring the visual output. Dataset_Sorted_by_Indicator.csv is the complete combined dataset for SDG-6 and SDG-16, preprocessed and organized by indicator. For global SDG-6 analysis, SDG_6_Indicators_Aligned.csv is used, while Combined_SDG6_Countries_Data_Corrected.csv includes region-specific data filtered for the US, EU, and China. The file SDG16_Dataset_With_Roles_Updated.csv contains the cleaned and role-assigned dataset for SDG-16 at the global level. The comprehensive dataset final_dataset_sdg61617_with_roles.csv merges SDG-6, SDG-16, and SDG-17 indicators, incorporating normalized values and assigned stakeholder roles. To support accurate and consistent visual formatting, Tag_Template_SDG-6.csv and Tag_Template_SDG-16.csv provide indicator-level tag configuration for SDG-6 and SDG-16 respectively. These templates define visual elements such as petal placement, color mapping, and tag types in the GaiaViz environment. The general-purpose templates np_tag-template.csv and np_node-template.csv define the required schema for tag and node files across all SDGs. Additionally, the colors.csv file maps each SDG indicator to a specific RGB color code, ensuring standardized, visually coherent representation across the entire visualization landscape.












