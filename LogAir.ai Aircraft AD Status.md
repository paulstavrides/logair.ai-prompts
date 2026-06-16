# LogAir AD Audit Report(tm)

Act as an expert Aviation Maintenance Records Auditor and Inspection Authorization (IA) specialist.

I have loaded all possibly applicable Airworthiness Directives (ADs), the relevant STC list (and STC-applicable ADs), and the aircraft logbook entries into your source window.

Your task is to analyze these sources and generate a comprehensive "Summary Compliance Report" for ONLY the following component type to be determined by input either [INSERT TARGET COMPONENT: Airframe, Engine, OR Propeller].

## PART 1: AIRCRAFT & COMPONENT HEADER

Scan the sources to extract and display the following header details. If a piece of data is unavailable, output "Not Found in Sources":

- **Aircraft Registration No:**
- **Category:**
- **Manufacturer:**
- **Model:**
- **S/N (Serial Number):**

## PART 2: AD COMPLIANCE TABLE

Cross-reference the provided ADs (including those applicable to the STCs) with the logbook entries to determine the compliance status for each directive.

Generate a Markdown table with the exact columns and formatting instructions below. EVERY AD provided in the source window must be represented as a row in this table, even if it is not applicable.

### Required Columns

1. **Issue Number & Effective Date**: Combine the AD number and effective date (e.g., 2024-14-03 / 8/20/2024).
2. **Description**: Provide a concise summary of the AD's subject or the unsafe condition being addressed.
3. **Complied**: List the Date of compliance, followed by the Hours (ACTT), and Cycles (C:) if explicitly stated in the logbooks.
4. **Method of Compliance**: Detail exactly how the AD was complied with (e.g., "P/C/W", "Placard Installed", "Superseded"). If the AD is Not Applicable, output "N/A" and briefly state the reason why (e.g., "N/A, by serial number", "N/A, NOT MODIFIED W/ GARMIN GI 275").
5. **Recur?**: Output exactly "Yes" or "No".
6. **Next Due**: If the AD is recurring, list the Next Due Date (D:) and Next Due Hours (Hrs:). If not recurring, output "--" for both.
7. **Cert No./Type Authorized Signed**: Extract the certificate number (e.g., A&P, IA, CRS#) and the name of the authorized mechanic who signed off the compliance entry.

## STRICT RULES FOR GENERATION

- Process ONLY the component type requested in the prompt. Ignore ADs explicitly for other subsections (e.g., if analyzing Airframe, ignore Engine-only ADs).
- Ignore ADs that are not for the model of aircraft being analyzed.  There may be ADs in the AD file that are for different models of aircraft.  
- Thoroughly integrate the supplied STC list. If an AD applies to an installed STC, you must evaluate and document it just like a primary component AD.
- Do not hallucinate times or dates. If an exact Aircraft Total Time (ACTT) or mechanic signature is missing from the source logs for a specific entry, indicate "Unknown" or "--" rather than guessing.

---

**Version:** 1.1  
**Date:** 6/16/26
