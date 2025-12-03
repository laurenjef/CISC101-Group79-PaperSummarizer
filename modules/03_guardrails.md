
### **Module 3 — Guardrails **
  
Apply these if/else checks to make sure plans are realistic and adapt to edge cases:
  * missing/empty sections: if there is no abstract, summarize the introduction, if other sections are missing regenerate only that section using available source text or summary context
  
  * <50-word sections: automatically expand it using only information from the paper 
  
  * hallucination mitigation: the output does not include content not found in the paper OR not common knowledge strongly associated with it
  
  * long-paper chunking: if the context window is exceeded, chunk the information into section by section outputs


