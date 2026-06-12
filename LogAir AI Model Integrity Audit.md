# LogAir AI Model Integrity Audit(tm) 

***Act as an Aviation Quality Assurance Auditor. Review the uploaded maintenance logbooks and generate a 'Transcription Safety and Accuracy Report' to warn the end-user of potentially corrupted data. Present this report as a table with the following columns:**

A) For each source, output the Source file name at the top of the table bolded.  Summarize the number of maintenance events in the source.  Determine a figure of merit for the number of maintenance questionabled maintenance events / total number of maintenance events * 100 as a percent

B) 1. **Page Number / Date Range / Hobbs Time:** Identify the specific page or entry.   
2. **Estimated Legibility Score (1-10):** Grade how clear and legible the original handwriting appears to you (10 is pristine, 1 is heavily faded or illegible).   
3. **Missing Critical Data:** Note if standard fields (Hobbs/Tach times, Dates, A&P Signatures) appear to be missing, smeared, or unreadable on this page.   
4. **Spelling/Formatting Anomalies:** List any gibberish words, corrupted alphanumeric numbers (e.g., 'PN-12\#4'), or nonsensical aviation terms found on this page.  

***Important: Only populate this table with pages or entries where the Legibility Score is 7 or below, or where you detect anomalies or missing data. Skip pages with clean, high-confidence data.**
  
C) Before generating the final Logbook Summary, evaluate the legibility and data extraction quality of the uploaded documents. Assign a 'Data Integrity Grade' using the following rubric:

***Grade A (High Confidence): Handwriting is clear; dates, Hobbs/Tach times, and AD numbers follow a logical sequence with no obvious gaps or gibberish words.\***

***Grade B (Moderate Confidence): Mostly legible, but contains minor OCR anomalies (e.g., a few unrecognized words or minor formatting breaks in part numbers).\***

***Grade C (Caution - Manual Review Required): Significant legibility issues; frequent missing signatures, illogical jumps in engine hours, or heavy use of unrecognized jargon.\***

***Grade F (Severely Compromised): Handwriting is largely illegible, resulting in missing chronological data and corrupted text throughout.\***

***Print the Data Integrity Grade at the very top of the report, followed by a one-sentence justification for the grade, and a list of specific page numbers that caused any downgrades.**

Version: 1.2.3 6/12/2026
