# Abhishek S Nambiar

**M.Tech Artificial Intelligence, SRM Institute of Science and Technology (2025–2027)**

Healthcare AI · Machine Learning · NLP and LLMs · Time Series Forecasting

I come from a Biomedical Engineering background and spent 5+ years in US healthcare operations before moving into AI. This repository collects my coursework and mini projects from the M.Tech program, with a focus on applying ML and language models to healthcare data.

[LinkedIn](https://www.linkedin.com/in/abhishek-s-nambiar-639125126)

---

## Featured projects

### MedBot: medical Q&A assistant with LoRA fine-tuning and RAG
*Large Language Models course*

An educational prototype that combines a fine-tuned small language model, retrieval over public health pages, and two simple tools in one chat interface.

- Fine-tuned **Qwen2.5-1.5B-Instruct** with **LoRA** (rank 16) on the MedQuAD question–answer dataset; validation loss 1.04 after one epoch.
- **Retrieval-augmented generation** using Sentence Transformers (`all-MiniLM-L6-v2`) and FAISS over MedlinePlus, CDC and WHO pages. Answers include source URLs.
- Tools: a BMI calculator and an **openFDA** drug-label lookup, served through a **Gradio** app.
- Limitations: small source collection, no formal factuality evaluation, user-selected tool modes. Not for medical use.

**Stack:** PyTorch, Hugging Face Transformers and PEFT, Sentence Transformers, FAISS, Gradio
**Notebook:** [rag_medbot (1).ipynb](rag_medbot%20%281%29.ipynb)

---

### Time series forecasting: climate and air quality
*Time Series Analysis and Forecasting course*

Two case studies comparing classical forecasting models on chronological holdout sets.

| Experiment | Data | Models | Result |
|---|---|---|---|
| Univariate | Delhi daily climate, aggregated to monthly mean temperature | AR, MA, ARMA, ARIMA, SARIMA | SARIMA(1,1,0)×(1,0,0,12) was best: RMSE 2.50 °C, MAE 1.69 °C |
| Multivariate | UCI Air Quality (CO and NOx) | VAR(9), VARMAX(1,1) | VARMAX had the lower mean RMSE (136.2 vs 152.3); VAR was slightly better for CO |

Stationarity was checked with ADF and KPSS tests, and VAR lag order with AIC, BIC, FPE and HQIC. Results come from a single holdout period, so they should not be read as general rankings.

**Stack:** Python, pandas, NumPy, statsmodels, Matplotlib
**Notebooks:**
[Univariate: Delhi climate](TSF_Univariate_Forecasting_Delhi_Climate%20%281%29.ipynb) ·
[Multivariate: Air Quality](TSF_Multivariate_VAR_VARMA_AirQuality%20%281%29.ipynb)

---

### Hospital Performance Analytics dashboard
*Advanced Data Visualization course (team project)*

An interactive **Tableau** dashboard and three-point story built on 1,000 hospital admission records across 9 departments (synthetic academic dataset).

- KPIs: average length of stay 4.17 days, 10.5% 30-day readmission flag rate, 65.9% emergency admissions.
- General Medicine has the highest volume (206 admissions); Oncology has the longest average stay (6.68 days).
- Filters by department and admission type.

**Stack:** Tableau
**Workbook:** [Hospital_Performance_Analytics.twb](Hospital_Performance_Analytics.twb)

---

## More coursework

| Course | Work |
|---|---|
| Computer Vision Techniques | Lane detection mini project: [notebook](CVT_Miniproject.ipynb) and [slides](CVT_Lane_Detection_Mini_Project.pptx) |
| Deep Learning Architectures | [Notebook](DLA_LLJ.ipynb) |
| Reinforcement Learning Algorithms | [Mini project notebook](RLA_miniproject.ipynb) |
| NLP | [Hackathon notebook](NLP%20hackathon.ipynb) |
| Other | [LLM](LLM) folder |

---

## Skills

- **Languages and libraries:** Python, pandas, NumPy, Matplotlib, scikit-learn, statsmodels
- **ML and AI:** supervised learning, deep learning, NLP, LLM fine-tuning (LoRA), RAG, time series forecasting, reinforcement learning, computer vision
- **Tools:** Hugging Face, FAISS, Gradio, Tableau, Jupyter and Colab
- **Domain:** US healthcare operations (claims and denials), clinical data, biomedical engineering

## Notes

- These are academic projects. Models and dashboards are not validated for clinical or operational use.
- Projects that use restricted clinical datasets (such as MIMIC-IV) do not include the data or patient-level outputs, in line with the data use agreements.
- Large model files, such as LoRA adapter weights, are not stored in this repository.

## Contact

Chennai, India · [LinkedIn](https://www.linkedin.com/in/abhishek-s-nambiar-639125126) · cordialabhishek@gmail.com
