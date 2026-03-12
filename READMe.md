# DDI_Codebook_Question_Text_Injector_v1.1

An R script that automates the addition of literal questions and AI powered pre/post question texts classification for datasets being documented in the **Metadata Editor**. This tool significantly reduces manual entry effort — saving **more than 50%** of the time that would otherwise be spent manually entering literal questions.

---

## Overview

The script uses the R packages `readxl`, `xml2`, and `dplyr` to read and process a DDI Codebook–based XML file, then populates it with literal questions extracted from an XLS questionnaire.Uses a free AI model installed locally to classify whether question hints are pre/post question texts.

---

## Requirements

- **R** — R software installed on your machine
- **Literal question source** — An XLS file (e.g. an ODK questionnaire in `.xls` format)
- **DDI Codebook XML file** — A codebook-based XML file containing the details about the dataset(s) of interest
- **Ollama** — Installed on your machine with gemma3 running 

---

## Workflow

![Workflow Diagram](workflow.png)

---

## How to Use

1. Ensure **R** is installed on your system.
2. Place the following files in the **same directory**:
   - The XML file generated from the Metadata Editor
   - The XLSX questionnaire containing the literal questions
3. Open `DDI_Codebook_Literal_Question_Injector_v1.0.R` and specify:
   - The **name of the XML file** to read
   - The **XLSX file** containing the literal questions
   - The **name of the output XML file** (the one to be populated with literal questions)
4. Run the script — it will display the **number of variables updated** upon completion.

---

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, provided the original copyright notice and permission notice are included.

## Contributing

Contributions are welcome! To contribute:

1. **Fork** the repository
2. **Create a new branch** for your feature or bug fix (`git checkout -b feature/your-feature-name`)
3. **Commit** your changes (`git commit -m 'Add your message here'`)
4. **Push** to your branch (`git push origin feature/your-feature-name`)
5. **Open a Pull Request** — all changes are reviewed before merging into the main branch
