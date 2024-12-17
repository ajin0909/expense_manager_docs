Usage 
=====

Installation
------------

To use expense_manager_library, first install it using pip:

.. code-block:: console

    (.venv) $ pip install expense_manager_library


Library usage example
---------------------
.. code-block:: python

    import pandas as pd
    from expense_manager_library.data_cleaner import categorize_transactions
    from expense_manager_library.visualizer import load_data
    from expense_manager_library.report_generator import generate_report, save_report_to_pdf

    # 파일 경로 설정
    file_path = "examples/example_data.csv"  # 실제 사용자의 csv 파일 경로로 변경하세요!

    # 데이터 카테고리 분류
    categorize_transactions(file_path)  

    # 카테고리 분류된 데이터 로드
    categorized_data = load_data("results/classified_data.csv")  

    # 보고서 생성
    report_text = generate_report(
        categorized_data,
        include_total=True,
        include_categories=True,
        include_monthly=True
    )
    print(report_text)  

    # PDF로 저장
    save_report_to_pdf(
        categorized_data,
        report_text,
        selected_graphs=["pie", "line", "bar"],  
        show_report=True, 
        font_color="black",
        pdf_path="results/example_report.pdf"
    )

    print("PDF 파일이 저장되었습니다: results/example_report.pdf")
