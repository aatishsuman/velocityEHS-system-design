# velocityEHS-system-design
Partial POC of the system design question of the velocityEHS interview.

## Directions for use
- Software needed - Python, Tesseract-OCT (https://tesseract-ocr.github.io/tessdoc/Installation.html), Jupyter notebook.
- Python packages needed - numpy, pandas, sklearn, Pillow, OpenCV, pytesseract, pdf2image, table-ocr (https://github.com/eihli/image-table-ocr), PyTorch.
- The _extract_cells_, _extract_tables_, _ocr_image_ and _ocr_to_csv_ folders contains the files from the table-ocr package which were updated to make them work for the given input document.
- The _data_extraction.ipynb_ file contains the code for reading the PDF document and extracting the data.
- The _output_ folder contains the output of the model - 
  - For each page, an image cotaining all the content (e.g. page_3.png) as well as an image file containing only the text part (tables removed) (e.g. page_3_text.png).
  - The text extracted from the images in the _out_text.txt_ file.
  - For each page containing a table, a folder containg the images and the text of the extracted tables and cells.
- The _review.csv_ file contains the Review sheet of the model output received from the interviewer. It is used to train the classification model.
- The _classification_model.ipynb_ file contains the code for training the classification model and the functions for generating the _Referable Conditions_ and the _Requirement Description_ columns.
- The _systemDesign.docx_ contains the steps for the system design.
