## Corresponding Kaggle Notebook Link 
https://www.kaggle.com/code/prasundatta/rsna-str-pulmonary-embolism-eda

## Description

If every breath is strained and painful, it could be a serious and potentially life-threatening condition. A pulmonary embolism (PE) is caused by an artery blockage in the lung. It is time consuming to confirm a PE and prone to overdiagnosis. Machine learning could help to more accurately identify PE cases, which would make management and treatment more effective for patients.
<img src = "https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F603584%2F9a3aac7e7ac865f134201cc2a5cd52f3%2Fkaggle_header3.png?generation=1599585319459400&alt=media" align ="right" width = "600" />

Currently, CT pulmonary angiography (CTPA), is the most common type of medical imaging to evaluate patients with suspected PE. These CT scans consist of hundreds of images that require detailed review to identify clots within the pulmonary arteries. As the use of imaging continues to grow, constraints of radiologists’ time may contribute to delayed diagnosis.

The Radiological Society of North America (RSNA®) has teamed up with the Society of Thoracic Radiology (STR) to help improve the use of machine learning in the diagnosis of PE.

In this competition, you’ll detect and classify PE cases. In particular, you'll use chest CTPA images (grouped together as studies) and your data science skills to enable more accurate identification of PE. If successful, you'll help reduce human delays and errors in detection and treatment.

With 60,000-100,000 PE deaths annually in the United States, it is among the most fatal cardiovascular diseases. Timely and accurate diagnosis will help these patients receive better care and may also improve outcomes.


## Dataset Description
### What files do I need? 
You will need the training and test images, as well as train.csv and test.csv. The images are grouped in directories by study and series. They are in DICOM format, and contain additional metadata that may be relevant to the competition. Each image has a unique identifier -``` SOPInstanceUID.```

The location for each image is given by: ``` <StudyInstanceUID>/<SeriesInstanceUID>/<SOPInstanceUID>.dcm.```

The data provided by the host for this competition and made available below is the RSNA-STR PE CT (RSPECT) dataset. Use of the dataset for non-commercial and/or academic purposes is permitted with citation.
### What should I expect the data format to be?
train.csv contains the three UIDs noted above, and a number of labels. Some are targets which require predictions, and some are informational, which will also be noted below in Data fields.

test.csv contains only the three UIDs.
### Files

- <b> train.csv </b> => contains UIDs and all labels.
- <b> test.csv </b> => contains UIDs.

### Data Fields 
- StudyInstanceUID - unique ID for each study (exam) in the data.
- SeriesInstanceUID - unique ID for each series within the study.
- SOPInstanceUID - unique ID for each image within the study (and data).
- pe_present_on_image - image-level, notes whether any form of PE is present on the image.
- negative_exam_for_pe - exam-level, whether there are any images in the study that have PE present.
- qa_motion - informational, indicates whether radiologists noted an issue with motion in the study.
- qa_contrast - informational, indicates whether radiologists noted an issue with contrast in the study.
- flow_artifact - informational
- rv_lv_ratio_gte_1 - exam-level, indicates whether the RV/LV ratio present in the study is >= 1
- rv_lv_ratio_lt_1 - exam-level, indicates whether the RV/LV ratio present in the study is < 1
- leftsided_pe - exam-level, indicates that there is PE present on the left side of the images in the study
- chronic_pe - exam-level, indicates that the PE in the study is chronic
- true_filling_defect_not_pe - informational, indicates a defect that is NOT PE
- rightsided_pe - exam-level, indicates that there is PE present on the right side of the images in the study
- acute_and_chronic_pe - exam-level, indicates that the PE present in the study is both acute AND chronic
- central_pe - exam-level, indicates that there is PE present in the center of the images in the study
- indeterminate -exam-level, indicates that while the study is not negative for PE, an ultimate set of exam-level labels could not be created, due to QA issues





