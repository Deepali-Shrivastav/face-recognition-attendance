# 🎯 Face Recognition Attendance System

A simple Python-based real-time face recognition system to mark attendance using a webcam. This project detects and recognizes faces from a live camera feed and logs their attendance into a dated `.csv` file.

---

## 📁 Project Structure

```
face-recognition-attendance/
│
├── faces/
│   ├── deepali.jpg
│   ├── jay.jpg
│   ├── shweta.jpg
│   ├── shruti.jpg
│   └── shubham.jpg
│
├── main.py
├── README.md
└── requirements.txt
```

---

## ✅ Features

* Real-time face recognition using webcam
* Marks attendance with timestamp into a CSV file
* Avoids duplicate entries for the same person
* Uses `face_recognition`, `OpenCV`, and `numpy`

---

## ⚙️ Requirements

* Python 3.10
* CMake (installed and added to PATH)
* Visual C++ Build Tools (on Windows)
* Webcam

---

## 🛠 Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/Deepali-Shrivastav/face-recognition-attendance.git
cd face-recognition-attendance
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
venv\Scripts\activate      # On Windows
```

### 3. Install CMake

* 📥 Download from: [https://cmake.org/download/](https://cmake.org/download/)
* ✅ During installation, **select “Add CMake to PATH”**
* Confirm installation:

```bash
cmake --version
```

### 4. Install Python Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

If `requirements.txt` is not present, manually install:

```bash
pip install face_recognition opencv-python numpy Pillow
```

> `face_recognition` will also install and compile `dlib`. Make sure CMake is set up properly or this step will fail.

---

## 📸 How to Use

### 1. Add Images of Known People

Place images in the `faces/` folder with these exact names:

```
faces/
├── deepali.jpg
├── jay.jpg
├── shweta.jpg
├── shruti.jpg
└── shubham.jpg
```

> These filenames are **hardcoded** in `main.py`. Modify the names in code if your image names are different.

Each image should clearly show the person’s face.

---

### 2. Run the Script

```bash
python main.py
```

* The webcam will open.
* As known faces are detected, their name will be shown with "Present".
* Attendance is marked once per session per person in a file named `YYYY-MM-DD.csv`.

Press `q` to stop.

---

## 📂 Output

Attendance is saved to a CSV file in the root folder:

```
2025-06-04.csv
```

Format:

```
Name,Time
Deepali,14-17-01
Jay,14-17-12
...
```

---

## 📝 Notes

* Accuracy depends on image clarity.
* Face must be front-facing and well-lit for proper recognition.
* You can add more students by adding their image and editing the code.

---

## 📄 License

MIT License – see [LICENSE](LICENSE) file for details.
