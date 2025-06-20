# pdf_to_text
Extract text from image-based or scanned PDFs using Tesseract OCR in Google Colab. Converts PDF pages to images and saves output as .txt, .docx, and .json.
# 📄 PDF Text Extraction using Tesseract OCR & Google Colab

This project extracts text from scanned or image-based PDFs using **OCR (Optical Character Recognition)** powered by **Tesseract** and **pdf2image** in Google Colab. It converts each PDF page into an image, extracts the text using Tesseract, and saves the result in `.txt`, `.docx`, and `.json` formats.

---

## 🚀 Features

✅ Upload and convert PDF pages into images  
✅ Extract text from each page using Tesseract OCR  
✅ Save output as:
- `extracted_text.txt` – plain text
- `extracted_text.docx` – formatted Word document
- `extracted_text.json` – structured page-wise text

---

## 📦 Dependencies

The notebook uses the following:

```bash
!apt-get install poppler-utils -y
!apt install tesseract-ocr -y
!pip install pdf2image pytesseract pillow python-docx
🛠️ How It Works
Upload a PDF file (scanned or image-based)

Each page is converted into a PNG image

Text is extracted from each image using Tesseract OCR

Outputs are saved in 3 formats and downloaded automatically

🧪 Sample Code Snippet

python
images = convert_from_path(pdf_path)

for i, image in enumerate(images):
    text = pytesseract.image_to_string(image).strip()
    all_text += f"\n--- Page {i+1} ---\n{text}\n"
    doc.add_heading(f'Page {i+1}', level=2)
    doc.add_paragraph(text)
    text_data[f"Page_{i+1}"] = text

📂 Output Files
File Name	Description
extracted_text.txt	All extracted text (plain format)
extracted_text.docx	Word file with page-wise sections
extracted_text.json	Page-wise key-value text mapping

📁 Folder Structure

pdf-text-extraction/
├── pdf_pages/                  # Saved PNG images from PDF
├── extracted_text.txt          # Full extracted text
├── extracted_text.docx         # Word version
├── extracted_text.json         # Structured JSON
├── notebook.ipynb              # Google Colab code (if exported)
└── README.md                   # Project documentation

📥 Usage Instructions
*Open the notebook in Google Colab
*Upload a PDF using the file uploader
*Wait for extraction and downloads
*View results in .txt, .docx, or .json

🙋 Author
Madhu Mitha
📧 AI-Powered PDF Reader using OCR
🌐 GitHub: @madhumithagopinath

