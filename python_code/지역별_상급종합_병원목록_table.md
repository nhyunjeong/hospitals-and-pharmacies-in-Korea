```python
# 지역별 상급종합 병원목록
import pandas as pd 

hospital = pd.read_csv("c:\\data\\병원정보서비스216.csv",encoding = "ANSI")
hospital2 = hospital[['시도코드명','종별코드명','요양기관명']][hospital['종별코드명'] =='상급종합'].sort_values('시도코드명',ascending =True)
hospital2.to_csv("c:\\data\\지역별 상급종합병원 목록.csv",encoding ='ansi')```