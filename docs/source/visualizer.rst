visualizer.py
===================

사용자 지출 내역을 분석하고, 시각화를 위해 여러 그래프 생성

**Functions**

- :function:`load_data`
- :function:`draw_pie_chart`
- :function:`draw_line_chart`
- :function:`draw_bar_chart`


load_data(file_path)
--------------------
데이터를 불러와서 DataFrame으로 생성

**Parameters**:

- `file_path `: 거래 데이터가 포함된 CSV 파일 경로

**Returns**: 불러온 데이터 프레임


draw_pie_chart(data, ax=None)
-----------------------------
카테고리별 소비 금액의 비율을 나타내는 파이 차트 생성


**Parameters**:

- `data `: Pandas DataFrame 형태의 거래 데이터
- `ax `: 차트를 그릴 matplotlib 축 객체


draw_line_chart(data, ax=None)
------------------------------
날짜별 소비 추이를 나타내는 라인 차트 생성

**Parameters**:

- `data `: Pandas DataFrame 형태의 거래 데이터
- `ax `: 차트를 그릴 matplotlib 축 객체


draw_bar_chart(data, ax=None)
------------------------------
월별 소비 금액을 카테고리별로 나타내는 바 차트 생성

**Parameters**:

- `data `: Pandas DataFrame 형태의 거래 데이터
- `ax `: 차트를 그릴 matplotlib 축 객체