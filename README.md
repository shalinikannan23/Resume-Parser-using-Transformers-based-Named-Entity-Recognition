# Resume-Parser-using-Transformers-and-Sentence-Embeddings

## Objective
This project is an **NLP-based automation system** that extracts structured information such as **Name, Skills, Degree, Institutions, and Work Experience** from resumes in `.txt` or `.pdf` formats.  
It uses **transformer-based Named Entity Recognition (NER)** and **semantic similarity** to process unstructured text into structured JSON output.  
This tool is designed for **real-world HR automation tasks** like resume screening and candidate shortlisting.

---

## Use Case
Simulates a **real-world recruitment workflow** by:
- Parsing resumes automatically
- Converting unstructured resume text into structured, machine-readable fields
- Saving recruiter time and reducing human error in manual screening

---

## Approach
The pipeline is designed as follows:

1. **Text Extraction**  
   - Uses **PyMuPDF** for PDF text extraction  
   - Reads raw text from `.txt` files

2. **Data Cleaning**  
   - Removes special characters, bullets, and URLs

3. **Named Entity Recognition (NER)**  
   - Uses **Hugging Face Roberta-large-NER model** for extracting:
     - Names
     - Institutions / Organizations

4. **Pattern Matching (Regex + Keywords)**  
   - Extracts degrees and experience

5. **Skill Detection with Semantic Matching**  
   - Uses **Sentence Transformers embeddings** for fuzzy skill matching against a predefined skill list

6. **Output Generation**  
   - Consolidates extracted fields into **structured JSON** format

---

## Extracted Information

The script categorizes extracted data into:

- **Name**
- **Degree**
- **Institution / Organization**
- **Work Experience**
- **Skills**

---

## Technologies Used

- **Python** (Standalone script or Google Colab)
- **Hugging Face Transformers** (Roberta NER)
- **Sentence Transformers** (Semantic embeddings)
- **PyMuPDF** for PDF text extraction
- **Regular Expressions (re)** for pattern matching

---

## Workflow

1. Upload `.txt` or `.pdf` resume file.
2. Extract raw text from the resume (PyMuPDF for PDFs).
3. Apply **Roberta NER model** to detect names and institutions.
4. Use **regex and keyword matching** to extract degrees and experience.
5. Use **semantic similarity** to detect skills from text.
6. Output the results as structured JSON.

---

## Possible Enhancements:

- Enable batch processing for multiple resumes.

- Build a web interface using tools like Streamlit or Gradio for end-user interaction.

