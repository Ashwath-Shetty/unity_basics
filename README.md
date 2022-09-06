
# unity_basics
# 
## Folder Structure

    App
    ├── Controllers              
    │    ├── invoice_validation_router.py        # Fast API main fail.
    ├── service 
    ├──  ├── invoice_main_function.py            # text extraction and document verification code
    ├── settings.py                              
    ├── main.py                                  # main fail to run the application.
    ├── Test                                     # Pdf files for test.
    ├── requirements.txt                         # all the libraries and dependencies.
    ├── Readme.md

## Step 1 - installations
<br> - go to anaconda prompt and create the environment conda create invoice_verification python=3.8.13
<br> - pip install requirements.txt
<br> - apt-get install -y poppler-utils
<br> - install tesseract-ocr.exe
<br> - set environmental variable 
     <br> <li>TESSDATA_PREFIX
      <br> <li> C:\Program Files (x86)\Tesseract-OCR\tessdata

## step 2 Running the API
<br> run python main.py
<br> visit http://127.0.0.1:8000/docs#/
<br> click on POST /invoice/validate and click on try it out.

## Step 3 Testing
<li> give the invoice ids on invoices.
<br><br> 1234567890, 1536892680, etc

<li> set the method to tesseract or easyocr
<li> choose pdf file for the testing.
<li> click on execute

<li> scroll down to the response body. you can see the result in Json form.
    <br> {
    <br> "1234567890": True,
    <br> "1536892680": false
    <br> }
<br> here True says that Transaction is completed.
<br> for e.x for invoice id 1234567890 there's a invoice and master document present. for all the scenarios.

