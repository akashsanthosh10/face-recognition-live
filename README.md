
# Real-Time Face Recognition

This project implements a real-time face recognition system using a webcam. It utilizes the **FaceNet** model for face embeddings and a **Support Vector Machine (SVM)** classifier for face recognition. The face detection is performed using a **Haar Cascade Classifier**.

## Requirements

You need the following Python libraries to run the project:

- `opencv-python`
- `numpy`
- `tensorflow`
- `keras_facenet`
- `sklearn`
- `pickle`

Install the required libraries with:

```bash
pip install opencv-python numpy tensorflow keras_facenet scikit-learn
```

## Files

1. **svm_model_160x160.pkl**: A pre-trained SVM model for face classification, trained on a custom dataset.
2. **faces_embeddings_done_4classes.npz**: A file containing pre-computed face embeddings generated using a custom dataset.
3. **haarcascade_frontalface_default.xml**: A Haar Cascade classifier for face detection.
4. **face_recognition.py**: Python script for running the face recognition system with webcam input.

## Setup Instructions

1. **Train the Custom Model (Optional)**:
    - The `svm_model_160x160.pkl` and `faces_embeddings_done_4classes.npz` files are generated using a custom dataset.
    - To train the embeddings and the SVM model, you need to run the provided Jupyter notebook. The notebook will:
        - Generate face embeddings using the **FaceNet** model.
        - Train an **SVM classifier** on these embeddings.
    - After training, you will get the **SVM model** and the **embeddings file**, which you can use for real-time face recognition.

2. **Download the Haar Cascade Classifier**:
    - Download the `haarcascade_frontalface_default.xml` file and place it in the project folder.

3. **Run the Face Recognition System**:
    - Make sure the `svm_model_160x160.pkl` and `faces_embeddings_done_4classes.npz` files are in the project directory.
    - Run the `face_recognition.py` script to start the face recognition system:

    ```bash
    python face_recognition.py
    ```

    - The webcam will open, and the system will detect and recognize faces in real-time. Press 'q' to exit.

## License

This project is licensed under the MIT License.
