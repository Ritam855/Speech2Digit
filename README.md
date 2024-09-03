🎤 Digit Recognition using Hidden Markov Models and LPC
Welcome to the Digit Recognition project! This project implements a system that recognizes spoken digits (0-9) using Hidden Markov Models (HMMs) and Linear Predictive Coding (LPC) features. The system is built entirely from scratch in C++ and processes speech data through several stages, including data normalization, feature extraction, and training a model for digit recognition.

📂 Project Structure
The project is divided into several key sections:

Universe Creation:

Normalize data, calculate Linear Predictive Coding (LPC) coefficients, and transform them into Cepstral Coefficients.
Apply LBG Algorithm to create a codebook for feature vector quantization.
HMM Training:

Initialize HMM parameters.
Use the Baum-Welch algorithm for parameter estimation.
Train models for each digit.
Recognition:

Apply the Viterbi algorithm to recognize digits from the input speech data.
🚀 Getting Started
Prerequisites
Windows OS (or modify for your OS)
C++ Compiler (Visual Studio recommended)
Basic understanding of HMM, LPC, and speech processing concepts
Compilation and Execution
Clone the Repository

bash
Copy code
git clone https://github.com/yourusername/digit-recognition-hmm.git
cd digit-recognition-hmm
Compile the Code

Open the project in Visual Studio or use the command line:
bash
Copy code
cl Digit_Recognition.cpp
Run the Program

bash
Copy code
Digit_Recognition.exe
File Descriptions
Digit_Recognition.cpp: Main program file containing the implementation of the entire system.
234101043_universe.csv: The universe file containing all Cepstral Coefficient vectors.
234101043_codebook.csv: The generated codebook used for quantizing feature vectors.
Training Files: Located in 234101043_dataset/English/txt/, these are the speech files used to train the model.
🛠️ Key Functions
🎧 Data Processing
normalize_data(char file[100]): Normalize the speech data by removing DC offset and clipping.
durbinAlgo(): Apply Durbin's algorithm to compute LPC coefficients.
cepstralTransformation(): Transform LPC coefficients into Cepstral coefficients.
🧠 HMM Training
initialization(): Initialize the HMM parameters.
calculate_alpha(): Compute forward probabilities.
calculate_beta(): Compute backward probabilities.
calculate_gamma(): Compute the Gamma matrix for state prediction.
🔍 Recognition
predict_state_sequence(): Use the Viterbi algorithm to predict the most likely sequence of states.
calculate_score(): Evaluate the model by calculating the probability of observing the sequence given the model.
🌟 Features
Dynamic Time Warping (DTW) for feature alignment.
Baum-Welch Algorithm for HMM training.
Cepstral Coefficients as features for better speech recognition accuracy.
Viterbi Algorithm for efficient decoding.
