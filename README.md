# ☀️ Solar Panel Fault Detection (Computer Vision)

## 📌 Business Overview
In the renewable energy sector, asset efficiency is king. Environmental factors like dust accumulation, bird droppings, or physical cracks can significantly degrade the performance of solar arrays.

This project leverages **Computer Vision** to automate the inspection process. By analyzing images captured by drones or maintenance cameras, the system classifies the condition of each panel, allowing facility managers to deploy cleaning crews only where needed.

## 🧠 Technical Approach
* **Algorithm:** Convolutional Neural Network (CNN).
* **Technique:** **Transfer Learning** using the **VGG16** architecture (weights pre-trained on ImageNet).
* **Classes Predicted:**
    1.  ✅ **Clean** (Operational)
    2.  ⚠️ **Dusty** (Needs Cleaning)
    3.  ⚠️ **Bird Drop** (Needs Cleaning)
    4.  ❌ **Electrical Damage** (Needs Repair)
    5.  ❌ **Physical Damage** (Needs Replacement)

<img width="765" height="314" alt="image" src="https://github.com/user-attachments/assets/9008b2aa-3751-4f3f-b5f5-7dce77bdaaa0" />

## 📊 Performance & Results
* **Data Augmentation:** Used `ImageDataGenerator` to artificially expand the training set, making the model robust to different lighting conditions and angles.
* **Model Accuracy:** The VGG16 model successfully learned distinct texture patterns (e.g., the specific scatter pattern of dust vs. the crack lines of physical damage).
* **Business Impact:**
    * **Reduced O&M Costs:** Eliminates the need for manual "panel-by-panel" inspection.
    * **Energy Optimization:** Faster detection of "Dusty" panels ensures peak power generation.

## 🛠 Tools Used
* **Deep Learning:** TensorFlow, Keras
* **Model:** VGG16 (Transfer Learning)
* **Visualization:** Matplotlib (Accuracy/Loss Curves), Seaborn (Confusion Matrix)

## 🚀 How to Run
1.  Clone the repository.
2.  Install dependencies: `pip install -r requirements.txt`
3.  Run `Team4FinalProjectCode.ipynb`.
