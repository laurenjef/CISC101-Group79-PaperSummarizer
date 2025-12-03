// Added strict evidence mode to only include claims, variables and equations that appear in text

### **Module 3 — Guardrails **

Apply these if/else checks to make sure plans are realistic and adapt to edge cases:
  * missing/empty sections: if there is no abstract, summarize the introduction, if other sections are missing regenerate only that section using available source text or summary context
  
  * <50-word sections: automatically expand it using only information from the paper 
  
  * hallucination mitigation: the output does not include content not found in the paper OR not common knowledge strongly associated with it
  
  * long-paper chunking: if the context window is exceeded, chunk the information into section by section outputs




 **Strict Evidence Mode**
 Introduce a **mode or flag** 
 If (`evidence_mode = "strict"`). 
 When it is set to `"strict"`:
    Then
    * Only include claims, equations, and results that appear in the provided text.
    
        If enough information is not available 
         Then notify user 'The source text does not provide enough detail to summarize this section in strict evidence mode.'

 
 **Section Warning Messages**
 If sections are:
   * missing / empty, or
   * too short (< 50 words)

     Then notify user 'This section is insufficient, the summary may be incomplete' 
