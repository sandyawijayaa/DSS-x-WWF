# DSS-x-WWF
Our project goal was to visualize WWF’s impact throughout the globe, as granular as possible. To do so, we received 279 project documents in PDF format and aimed to use LLMs to extract mentioned location and accomplishments, then map this information on an interactive map where user can toggle over a point and be redirected to more information on the project. Our methodology can be extended to other use cases that have similar needs of extracting project information that is previously locked away in PDFs!
## Our Timeline
1. Assess which PDFs are actually useful by manually filtering out PDFs that are not project documents (e.g. PDFs on origami instructions mixed into the same folder).  
2. Do initial experimentation using 6 different LLMs -- Mistral, Instructor, PaLM, Spacy, Jurassic2, OpenAI -- to extract information from a subset of 20 high-quality PDFs.
3. Score each LLMs's performance using our validation function to settle on the best one for our use case.
4. Apply the best LLM methodology on full set of 218 PDFs.
5. Create an interactive map with these results a searchbox function using Folium and Mapbox.

## Final Notebooks
- **Getting locations:** Using PaLM + Spacy to get locations for all filtered 218 PDFs _([Christiana] PaLM+spaCy.ipynb)_
- **Getting accomplishments:** Using OpenAI + Summarization Chain to get accomplishments for all filtered 218 PDFs _([Vishali] openai_summarize_chain.ipynb)_
- **Getting GeoJSON:** Using OpenStreetMap to get GeoJSONs for all filtered 218 PDFs _([Sandya] run_all_Mapping.ipynb)_
- **Creating Map:** Map with all completed pieces of information using Mapbox and search box function. _(Cleaned Code.ipynb)_
## Archived Notebooks 
#### 5 LLMs Exploration
- **Mistral** _(Joon_Mistral7B.ipynb)_
- **Instructor** _([Andrew] HuggingFace_Instructor.ipynb)_
- **PaLM** _(Christiana_PaLM_exploration.ipynb)_
- **Spacy + Cohere** _([Vishali] final_spacy_cohere_mapping.ipynb)_
- **Jurassic2** _([Mark] Jurassic2.ipynb)_
#### Quality Control
- **Prompt Engineering:** Prompt engineering notebook to ensure no empty answers _([Christiana] PaLM Prompt Engineering.ipynb) (Joon_PaLM Prompt Engineering.ipynb)_
- **Validation Function:** Scoring function for LLMs _(Mark_Andrew_Validation_Script.ipynb)_
#### Mapping Exploration
- **Mapbox Studio**: Alternative mapping notebook that extracts location information then outputs a file to upload to Mapbox Studio and create a static map _(Joon_MAP.ipynb)_
## Other Useful Files
- **PDF Useful or Not (CSV):** Manual filtering of all 279 PDFs for which are useful -- is it project document -- and to what extent -- does it have relevant locations. 
- **Initial LLM Results using 5 LLM Methods (CSV):**
- **Validation Score Sheet (CSV):**
- **Final LLM Results (CSV):** All results compiled in one sheet for easy comparison, split by location & accomplishment
