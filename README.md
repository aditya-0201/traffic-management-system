{\rtf1\ansi\ansicpg1252\cocoartf2821
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\froman\fcharset0 Times-Bold;\f1\froman\fcharset0 Times-Roman;\f2\fmodern\fcharset0 Courier;
}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}}{\leveltext\leveltemplateid1\'01\'00;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}
{\list\listtemplateid2\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid101\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{circle\}}{\leveltext\leveltemplateid102\'01\uc0\u9702 ;}{\levelnumbers;}\fi-360\li1440\lin1440 }{\listname ;}\listid2}
{\list\listtemplateid3\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid201\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{circle\}}{\leveltext\leveltemplateid202\'01\uc0\u9702 ;}{\levelnumbers;}\fi-360\li1440\lin1440 }{\listname ;}\listid3}
{\list\listtemplateid4\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid301\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid4}
{\list\listtemplateid5\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid401\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid5}
{\list\listtemplateid6\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}}{\leveltext\leveltemplateid501\'01\'00;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid6}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}{\listoverride\listid2\listoverridecount0\ls2}{\listoverride\listid3\listoverridecount0\ls3}{\listoverride\listid4\listoverridecount0\ls4}{\listoverride\listid5\listoverridecount0\ls5}{\listoverride\listid6\listoverridecount0\ls6}}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sa321\partightenfactor0

\f0\b\fs48 \cf0 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Intelligent Traffic Management System\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 This project implements a multi-stage intelligent traffic management system using a combination of machine learning and heuristic optimization techniques. The system first predicts future traffic flow using an optimized neural network and then uses that data to optimize and adapt traffic signal timings to minimize congestion.\
This notebook is divided into five key modules:\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls1\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	1	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Traffic Flow Prediction (GA-LSTM)
\f1\b0 \
\ls1\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	2	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Signal Timing Optimization (PSO)
\f1\b0 \
\ls1\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	3	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Mamdani Fuzzy Logic Controller
\f1\b0 \
\ls1\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	4	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Adaptive Neuro-Fuzzy Inference System (ANFIS)
\f1\b0 \
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 1. Traffic Flow Prediction (GA-LSTM)\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 This module builds a traffic flow predictor using a 
\f0\b Long Short-Term Memory (LSTM)
\f1\b0  neural network. To achieve the highest accuracy, a 
\f0\b Genetic Algorithm (GA)
\f1\b0  is employed to find the optimal set of hyperparameters for the LSTM model.\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls2\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Objective:
\f1\b0  Minimize the validation Mean Squared Error (MSE).\
\ls2\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Hyperparameters Tuned:
\f1\b0 \
\pard\tx940\tx1440\pardeftab720\li1440\fi-1440\sa240\partightenfactor0
\ls2\ilvl1
\f2\fs26 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 L
\f1\fs24  (Lookback window)\
\ls2\ilvl1
\f2\fs26 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 u
\f1\fs24  (Hidden units)\
\ls2\ilvl1
\f2\fs26 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 d
\f1\fs24  (Dropout rate)\
\ls2\ilvl1
\f2\fs26 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \uc0\u945 
\f1\fs24  (Learning rate)\
\ls2\ilvl1
\f2\fs26 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 B
\f1\fs24  (Batch size)\
\ls2\ilvl1
\f2\fs26 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Opt
\f1\fs24  (Optimizer: Adam, RMSprop, SGD)\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls2\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Dataset:
\f1\b0  Uses the 
\f2\fs26 metr_la_speed.csv
\f1\fs24  dataset for training.\
\ls2\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Output:
\f1\b0  The best-performing LSTM model is saved as 
\f2\fs26 metr_lstm_ga_optimized.h5
\f1\fs24 .\
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 2. Signal Timing Optimization (PSO)\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 This module takes the predicted traffic flows from the GA-LSTM model and uses them to optimize static traffic signal timings for a network of intersections.\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls3\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Objective:
\f1\b0  Minimize the average vehicle delay across all approaches.\
\ls3\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Method:
\f1\b0  
\f0\b Particle Swarm Optimization (PSO)
\f1\b0 .\
\ls3\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Parameters Optimized:
\f1\b0 \
\pard\tx940\tx1440\pardeftab720\li1440\fi-1440\sa240\partightenfactor0
\ls3\ilvl1\cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Cycle time (C)\
\ls3\ilvl1\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Green splits (S\uc0\u8321 , S\u8322 , ...)\
\ls3\ilvl1\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u9702 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Offsets (O)\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls3\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Fitness Function:
\f1\b0  Uses the 
\f0\b Ak\'e7elik delay model
\f1\b0  to calculate delay based on the predicted flows.\
\ls3\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Output:
\f1\b0  The optimal signal timings are saved in 
\f2\fs26 pso_results.npz
\f1\fs24 .\
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 3. Adaptive Signal Control (Fuzzy Logic & ANFIS)\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 These modules design an adaptive controller to dynamically refine the signal timings based on real-time conditions, building on the PSO-optimized base timings.\
\pard\pardeftab720\sa280\partightenfactor0

\f0\b\fs28 \cf0 Module 3: Mamdani Fuzzy Controller\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 A standard 
\f0\b Mamdani fuzzy logic controller
\f1\b0  is implemented to adjust the signal cycle time.\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls4\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Inputs:
\f1\b0  
\f2\fs26 Queue
\f1\fs24  (vehicles), 
\f2\fs26 Delay
\f1\fs24  (seconds)\
\ls4\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Output:
\f1\b0  
\f2\fs26 \uc0\u916 Cycle
\f1\fs24  (change in cycle time, seconds)\
\ls4\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Rules:
\f1\b0  A 9-rule base (Low/Medium/High for each input) determines the output.\
\pard\pardeftab720\sa280\partightenfactor0

\f0\b\fs28 \cf0 Module 4: ANFIS Controller\
\pard\pardeftab720\sa240\partightenfactor0

\f1\b0\fs24 \cf0 An 
\f0\b Adaptive Neuro-Fuzzy Inference System (ANFIS)
\f1\b0  is developed as a more advanced hybrid controller. It combines the interpretability of fuzzy logic with the learning capabilities of a neural network to automatically tune and refine the fuzzy membership functions and rules from data.\
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 Technologies Used\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls5\ilvl0
\f1\b0\fs24 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Python\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 TensorFlow / Keras\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Pandas & NumPy\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Scikit-learn\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Matplotlib\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Genetic Algorithm (GA)\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Particle Swarm Optimization (PSO)\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Mamdani Fuzzy Logic\
\ls5\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 ANFIS (Adaptive Neuro-Fuzzy Inference System)\
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 How to Use\
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls6\ilvl0
\fs24 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	1	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Clone the repository:
\f1\b0 \uc0\u8232 
\f2\fs26 git clone [https://github.com/aditya-0201/traffic-management-system.git](https://github.com/aditya-0201/traffic-management-system.git)\
\pard\tx220\tx720\pardeftab720\li720\fi-720\partightenfactor0
\ls6\ilvl0\cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	2	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 cd traffic-management-system\
\pard\tx220\tx720\pardeftab720\li720\fi-720\partightenfactor0
\ls6\ilvl0
\f1\fs24 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	3	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls6\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	4	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Install dependencies:
\f1\b0  It is recommended to create a virtual environment.\uc0\u8232 
\f2\fs26 pip install tensorflow pandas numpy scikit-learn matplotlib\
\pard\tx220\tx720\pardeftab720\li720\fi-720\partightenfactor0
\ls6\ilvl0
\f1\fs24 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	5	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \
\pard\tx220\tx720\pardeftab720\li720\fi-720\sa240\partightenfactor0
\ls6\ilvl0
\f0\b \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	6	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Add Dataset:
\f1\b0  This project requires the 
\f2\fs26 metr_la_speed.csv
\f1\fs24  dataset. Please download it and place it in the root of the repository.\
\ls6\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	7	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Update File Paths:
\f1\b0  The notebook currently uses Google Drive paths (e.g., 
\f2\fs26 /content/drive/MyDrive/...
\f1\fs24 ). You must update these paths to read/write from the local repository (e.g., change to 
\f2\fs26 metr_la_speed.csv
\f1\fs24 , 
\f2\fs26 metr_lstm_ga_optimized.h5
\f1\fs24 , etc.).\
\ls6\ilvl0
\f0\b \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	8	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 Run the Notebook:
\f1\b0  Open and run the 
\f2\fs26 Traffic.ipynb
\f1\fs24  notebook using Jupyter or Google Colab.\
\pard\pardeftab720\sa298\partightenfactor0

\f0\b\fs36 \cf0 File Structure\
\pard\pardeftab720\partightenfactor0

\f2\b0\fs26 \cf0 .\
\uc0\u9500 \u9472 \u9472  Traffic.ipynb             # Main Jupyter Notebook with all modules\
\uc0\u9500 \u9472 \u9472  README.md                 # This file\
\uc0\u9500 \u9472 \u9472  metr_la_speed.csv         # (Must be added) Traffic speed dataset\
\uc0\u9500 \u9472 \u9472  metr_lstm_ga_optimized.h5 # (Generated) Trained LSTM model\
\uc0\u9500 \u9472 \u9472  ga_tuning_log.csv         # (Generated) Log from the GA tuning\
\uc0\u9492 \u9472 \u9472  pso_results.npz           # (Generated) Optimized signal timings from PSO\
}