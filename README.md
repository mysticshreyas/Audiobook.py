# Audiobook.py
pip install pyttsx3 ## Python text to speech module

pip install PyPDF2  ## Python pdf reader module

import pyttsx3
import PyPDF2
book=open('the subtle act of not giving a fuck.pdf','rb')
pdf_reader=PyPDF2.PdfFileReader(book)
pages = pdf_reader.numPages
print(pages)
speaker= pyttsx3.init()
for num in range(0,pages):
    page = pdf_reader.getPage(7)
    text = page.extractText()
    speaker.say(text)
    speaker.runAndWait()
