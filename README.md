# fuzzy_wash_machine
以洗衣機為對象，設計一套模糊系統。
目的是在衣物投入後自動判斷各項參數並依此生成洗衣時長、水量、洗衣
劑用量、水溫，並依此自動洗衣達到智慧生活的目的，只需設定一個布料
敏感度參數即可不需要再設定其他的人工參數。
# 模糊系統介紹 
模糊系統的理論基礎是模糊子集(fuzzy subset)的概念，由美國自動控制專
家 Zadeh 於 1965 年提出，此後模糊系統理論得到發展。模糊系統(fuzzy 
system)，是一種將輸入、輸出和狀態變量透過歸屬函數( Membership 
function )、模糊、解模糊定義在模糊集上的系統。模糊系統從宏觀出發，
抓住了人腦思維的模糊性特點，在描述高階知識與行為方面發揮很好的效
用，可以模仿人的綜合推斷來處理常規數學方法難以解決的模糊信息處理
問題。

# Input Setting
將衣物髒污程度(cloth_dirtiness)、衣物多寡(cloth_mass)、布料敏感程度
(cloth_sensitivity)依照程度分成3類，水質軟硬(water_hardness)分成兩類。 
Fuzzy set of cloth_dirtiness: 依照程度分類 
Small(小髒) 0~50 
Medium(普通髒) 25~75 
Large(大髒) 50~100 
Fuzzy set of cloth_mass : 依照公斤( kg )分類 
Light(輕) 0~5 
Medium(普通) 2~8 
Leavy(重) 5~10 
Fuzzy set of cloth_sensitivity : 依照程度分類 
NotSensitive (布料不敏感) 0~50 
LessSensitive (布料稍微敏感) 25~75 
MoreSensitive (布料敏感) 50~100 
Fuzzy set of water_hardness : 依照程度分類 
Water_hardness_Soft (水質軟) 0~70 
Water_hardness_Hard (水質硬) 30~100
# Output Setting
將洗衣時間(wash_time) 分成五類、水量(water_amount)、洗衣劑用量
(detergent_amount)、水溫(water_temperature)依照程度分成3類。 
Fuzzy set of wash_time : 依照時間長短(分鐘 m)分類 
VeryShort (時間非常短) 10~25 
Short (時間短) 15~35 
Medium (時間正常) 25~45 
Long (時間長) 35~55 
VeryLong (時間非常長) 50~70 
Fuzzy set of water_amount : 依照公升( L )分類 
Low (水量少) 20~60 
Medium (水量中等) 50~90 
High (水量大) 80~120 
Fuzzy set of detergent : 依照程度分類 
Low (洗衣精少) 0~50 
Medium (洗衣精中等) 25~75 
High (洗衣精多) 50~100 
Fuzzy set of water temperature : 依照水溫( C )分類 
Low (涼水) 10~30 
Medium (溫水) 20~50 
High (熱水) 40~65
# UI DEMO
![Image]()
