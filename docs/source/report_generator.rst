report_generator.py
===================

소비 데이터를 기반으로 보고서를 생성하고 시각화하여 PDF 파일로 저장하는 기능을 제공합니다.

**Functions**

- :function:`generate_report`
- :function:`save_report_to_pdf`

generate_report(data, include_total=True, include_categories=True, include_monthly=True)
----------------------------------------------------------------------------------------
소비 데이터를 기반으로 보고서 생성.

**Parameters**:

- `data`: Pandas DataFrame 형태의 거래 데이터 
- `include_total`: 총 소비 큼액 포함 여부 (기본값: True) 
- `include_categories`: 카테고리별 소비 금액 포함 여부 (기본값: True) 
- `include_monthly`:  월별 소비 금액 포함 여부 (기본값: True) 


save_report_to_pdf(data, report_text, selected_graphs, show_report=True, 
                       font_color="black", pdf_path="results/report.pdf")
------------------
생성된 보고서와 선택된 그래프들을 PDF 파일로 저장합니다.

**Parameters**:

- `data`: Pandas DataFrame 형태의 거래 데이터
- `report_text`: `generate_report()` 함수로 생성된 보고서 텍스트
- `selected_graphs`:  PDF에 포함할 그래프 유형의 목록 ("pie", "line", "bar")
- `show_report`: PDF에 보고서 텍스트 포함 여부
- `font_color`: 보고서 텍스트 색
- `pdf_path`:PDF가 저장될 위치
