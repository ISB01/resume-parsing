# Resume Parsing Using spaCy
Summarizing Resumes and extracting information from them such as skills, experience and education.
Such a project would be useful for HR, for instance, to extract only required information from resumes in a timely manner.
## Training Data
Collecting data can be very onerous. For a good model, most of the work goes into collecting and preparing data. 
Around 200 resumes, although not enough, can be found in pickle format under **training_data.pkl**. The data is serialized as tuples within which the 2nd element is a dictionary encompassing a list of tuples where the 2nd index of each is a label.  PDF resumes were converted into text, and entities, labels and starting and ending encoding characters were manually identified and included. 
Enlarging the dataset with more various CVs would indubitably yield better outcomes.
## Process
- Loading the training data as well as the NLP model
- Only adding NER (Named Entity Recognition) into the NLP pipeline
- Adding labels to the pipeline
- Training the model and saving it so as to load it and not retrain it every time.
- Test the model using actual resumes by converting PDFs into text using PyMuPDF.
