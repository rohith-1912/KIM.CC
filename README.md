# KIM.CC

**📘 MCQ Generator – README**

**🔗 Project Repository**
**GitHub Link:** https://github.com/rohith-1912/mcqGenerator

**📌 Project Overview**

The MCQ Generator is an automated question-generation tool that uses advanced language models to convert input text into high-quality multiple-choice questions. The system accepts raw content (notes, paragraphs, textbook pages, etc.) and produces structured MCQs along with options and correct answers in a clean JSON format. It is designed to help educators, students, and training teams quickly generate assessments without manually crafting questions.
The project includes a generation chain for producing MCQs and a review chain that validates and corrects malformed JSON to ensure error-free output. This improves the reliability of the pipeline, especially when dealing with long or noisy inputs such as OCR-converted text.

**⚙️ Key Features**

*Automatic MCQ generation using LLMs

*JSON-structured output for easy integration

*Review chain for correcting invalid or incomplete responses

*Supports long text input and noisy data

*Robust error handling and logging

**🚧 Challenges Faced**

One of the biggest challenges in this project was ensuring that the LLM produced consistent, valid JSON output across all types of input. At first, the model frequently returned partial or malformed JSON, especially when the input text was lengthy or contained mixed formatting. To fix this, I implemented a secondary review chain that validates the JSON and re-prompts the model for corrections whenever parsing fails. Handling unpredictable LLM responses required additional retry logic, exception handling, and structured validation steps. Another challenge was managing noisy input, such as text extracted from scanned PDFs, which often caused ambiguity in question generation. Through multiple iterations of prompt engineering and validation, the MCQ generation pipeline became stable, reliable, and production-ready.
