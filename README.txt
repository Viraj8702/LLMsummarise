1.Web Scrapping: The folder includes the WebScrapping notebook and a csv file, in which the csv file contains all the pdf file details from the official website. The HTMLcontent directory is where all the HTML script is extracted from the website along with links to download the PDFs. The sample of 18 PDFs are downloaded and further reduced down to 15, due to only using the file which has INQ(Inquiry) number, as these are the evidence documents. Libraries like Selenium and BeautifulSoup allowed to extract the links and download the PDFs.
[https://selenium-python.readthedocs.io/]

2.PDFExtraction: This is where the various python tools were used to extract the content from the PDFs in the TestingAllPDFExtlib notebook.
	Libraries: PDFminer, PymuPDF, PyPDF, PyPDF2, Pytesseract, TIKA.
	[Note: To run the Pytesseract, the tesseract file is required, which can be downloaded from following link:
		https://github.com/UB-Mannheim/tesseract/wiki]

	FinalPdfExtlib is the notebook where PyPDF2 library is chosen as the library for extracting the content. And the documents are contents are cleaned for email and non email documents

3.LLM Model: The directory includes a python notebook named Selected_LLM_Models_PYPDF2 where multiple models are used to compare from Ollama and store the summaries generated into LLM Summaries directory. Models used are Llama 3 8B, Llama 3.1 7B, Gemma 7B, Gemma 2 9B, Mistral 7B, XwinLM 7B, Qwen 4B, DeepSeek LLM 7B, and Solar 10.7B.
[Reference link: https://dev.to/timesurgelabs/how-to-run-llama-3-locally-with-ollama-and-open-webui-297d]
[https://ollama.com/]

4.LLM_Model_Evaluation: Evaluation of the summaries was performed in the Model_Evaluation notebook. The metrics used were BERT score, where all the scores are stored in the directory BertScore. Model used is 'facebook/bart-large-mnli', where list of models can be found on the official website. And Llama 3 model was prompted to evaluate the summaries and score between 1 to 5, where 5 being the best and 1 being the poor summary. The scores were stored in ModelAverageScores directory. The directory is filled with scores of each models along with the combining all the model scores in AllModelScores csv file. This file contains the average scores of each models and displays the score for all the models used.
[https://pypi.org/project/bert-score/]
[https://arxiv.org/abs/2303.16634]

Docker: It is a platform which allows to host the server. This can be useful if decided to directly communicate with LLMs through a platform like OpenWebUI, which provides user-friendly interface.
Docker link: [https://www.docker.com/]
Open Web UI: [https://docs.openwebui.com/]
	
	