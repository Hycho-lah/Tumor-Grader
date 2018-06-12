{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf200
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 Update:\
Originally the goal of the project was to develop a classifier for grading tumors. However, a lot of challenges occurred, so the scope of the project changed. The heterogeneity of tumors, especially for the higher grade tumors, was particularly challenging. The focus was then to develop a semi-automatic tumor(and it\'92s site of influence) segmentation and analysis method. The same code and procedure was then applied to tumors of Grade II and III to check its validity. \
\
Findings: \
The segmentation for Grade IV tumor seemed relatively fine. By visual inspection, the segmentation of the tumor\'92s site of influence in the T2-weighted image seemed to work best. The same code works better with Grade III compared to Grade II tumor. This is because Grade III and IV tumors both tend to have white borders on T1-weighted MRI, while Grade II tumors tends to be just a dark shade. Ventricles tend to be segmented well in all cases, but not for skull. This could be due to the varying settings of each MRI image that produced varying skull intensities. In all, this project is a good start for a bigger project in grading tumors. The next steps would naturally be to apply the code to more tumor images, further optimize filters and parameters to increase generalizability, extract relevant features (also including texture analysis), and build classifiers, followed by more feature engineering, parameter tuning and cross-validation testing. \
\
Instructions: \
All notebooks generally have instructions and comments. \
1) Run registration via registration_Grade_IV.ipynb\
2) Get seeds from seed_selection_Grade_IV.ipynb\
3) Run tumor_analysis_Grade_IV.ipynb\
\
Note: If there is no segment extracted for one modality, then an error may appear in the end. In this case, just continue to run the cells below. \
\
The tumor analysis document will print out statistics regarding shape and intensity. \
The sequence of filters and parameters used are optimized for the Grade_IV. \
\
Image information: \
	Subject 1961 has astrocytoma tumor of Grade II\
	Subject 5308 has astrocytoma tumor of Grade III\
	Subject 5342 has astrocytoma tumor of Grade IV\
The first 4 digits of each image represents the subject number. \
Each image is labelled with 3D, T1, T2, Flair to represent 3D, T1-weighted, T2-weighted, Flair MRI images respectively. \
\
List of documents:\
	1 x ReadMe\
	7 x images per subject \
	3 x Registration.ipynb\
	3 x seed_selection.ipynb\
	3 x Tumor_analysis.ipynb\
	2 x supporting python files \
	1 x Tumor_Analysis_Grade_IV.pdf (sample output)\
\
Note: The registration may sometimes result in different images. May need to run multiple times for best effect. \
\
}