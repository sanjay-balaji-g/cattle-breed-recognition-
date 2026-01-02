# cattle-breed-recognition-
# 🐄 Cattle Breed Recognition System

This project is a **Cattle Breed Recognition Web Application** built using **YOLOv8**, **Flask**, and a simple **HTML frontend**. It allows users to upload an image of cattle and returns the same image annotated with detected cattle breeds and confidence scores.

---

## 🚀 Features

* Detects and classifies **different cattle breeds** from images
* Uses **YOLOv8 (Ultralytics)** for real-time object detection
* **Flask REST API** backend
* Simple **HTML + JavaScript** frontend for image upload
* Returns detection results as an annotated image

---

## 🏗️ Project Structure

```
cattle-breed-recognition-main/
│
├── website/
│   ├── index.html          # Frontend UI
│   ├── main.py             # Flask backend & YOLO inference
│   └── runs/               # YOLO training & prediction outputs
│
└── README.md
```

---

## 🧠 Model Details

* Framework: **YOLOv8 (Ultralytics)**
* Task: **Object Detection / Breed Classification**
* Model file used:

  ```
  best.pt
  ```

> ⚠️ **Important:** The model path in `main.py` is currently hardcoded:

```python
model = YOLO(r"C:\Users\Mugesh R\runs\detect\train3\weights\best.pt")
```

You must update this path to match the location of `best.pt` on your system.

---

## 🔧 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/cattle-breed-recognition.git
cd cattle-breed-recognition-main
```

### 2️⃣ Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install flask ultralytics opencv-python numpy
```

---

## ▶️ Running the Application

### Start the Flask Server

```bash
cd website
python main.py
```

The server will run at:

```
http://127.0.0.1:5000
```

### Open the Frontend

* Open `index.html` in your browser
* Upload a cattle image
* View the detected breeds and confidence scores

---

## 🔁 API Endpoint

### `POST /predict`

**Request:**

* Form-data with key: `file`

**Response:**

```json
{
  "image": "<base64-encoded-image>"
}
```

---

## 🖼️ Output Example

* Bounding boxes around cattle
* Breed name with confidence score

---

## ⚠️ Known Issues & Improvements

* Model path is system-dependent (should be configurable)
* No error handling for unsupported file types
* Frontend UI is minimal

---

## 🌱 Future Enhancements

* Docker support
* Model selection via config file
* Improved UI (React / Bootstrap)
* Live camera feed detection

---

## 👨‍💻 Author

Developed for academic and experimental purposes in **Computer Vision & Deep Learning**.

---

## 📜 License

This project is open-source and free to use for educational purposes.

---

⭐ If you like this project, consider giving it a star!
