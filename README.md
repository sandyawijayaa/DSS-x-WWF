# DSS-x-WWF
Our project goal was to visualize WWF’s impact throughout the globe, as granular as possible. To do so, we received 279 project documents in PDF format and aimed to use LLMs to extract mentioned location and accomplishments, then map this information on an interactive map where user can toggle over a point and be redirected to more information on the project. Our methodology can be extended to other use cases that have similar needs of extracting project information that is previously locked away in PDFs! 
- For a refresher, feel free to look to our [**final deliverable slides**](https://docs.google.com/presentation/d/1YW2CYNjrEAt5dysIbHWvYRd3egFu7fppeRD2v3HvsXM/edit?usp=drive_link) which is focused on the mapping portion and/or [**midterm deliverable slides**](https://docs.google.com/presentation/d/1m_1bnJj2qMifTfkL4VV9VdXoNEnszqHqOpPM-hbufKA/edit#slide=id.g26072e28e31_0_168) which is focused on the LLM information extraction portion.
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
- [PDF Useful or Not (CSV):](https://docs.google.com/spreadsheets/d/1EYuxc9XuewOX6v2YqIXw2X4A9wOfUJ3XP_GpaHJRA4o/edit#gid=0) Manual filtering of all 279 PDFs for which are useful -- is it project document -- and to what extent -- does it have relevant locations.
- [Initial LLM Results using 5 LLM Methods (CSV):](https://docs.google.com/spreadsheets/d/1BdFBiaKmZbQAj1mblekZ91kAR2ZOISdn7aU6gGVsvxc/edit?usp=sharing) Initial results for subset of 20 high quality PDFs.
- [Validation Score Sheet (CSV):](https://docs.google.com/spreadsheets/d/1Y_8f7X6Y-tgKrZ4YFELRaZDDS5qjeh3fxaQKoZrB0o0/edit#gid=18952427) Scores for each LLM using our validation function.
- [Final LLM Results (CSV):](https://docs.google.com/spreadsheets/d/1hsgaDEvRNj4_yIgFxFNaS9ArgLnuGYju8z729BRrwxA/edit#gid=1456584096) All results for 218 PDFs compiled in one sheet for easy comparison, split by location & accomplishment
- [GeoJSON files:](https://drive.google.com/file/d/1PbaWGD5fgpo52bUhKN9Oz2xjoKGEY5tz/view?usp=drive_link) Final grouped dataframe with Geojson information, used for mapping.
