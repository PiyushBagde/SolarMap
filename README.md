# 🌞 SolarMap

Welcome to **SolarMap**! This deep learning project is designed to detect small-sized rooftop photovoltaic (PV) panels using satellite imagery. Goal is to provide valuable insights into the adoption of green energy, supporting sustainable infrastructure development.

---

## 🚀 What is SolarMap?

**SolarMap** is an AI-driven tool that analyzes satellite images to accurately identify rooftop solar panels. By counting and mapping these panels, we can gain insights into solar energy adoption in various regions, aiding energy planning and infrastructure development.

---

## 📊 Dataset

The dataset used for training can be accessed on Roboflow:  
👉 [Solar Panel Detection Dataset](https://universe.roboflow.com/solarpanel-3ku0x/solar_panel-cvecl)

---

## ⚙️ Training the Model

### Fine-tuning Process

We fine-tuned the **YOLOv8m** model with the following steps:

- **Initialization**: Used pre-trained weights for better performance.
- **Hyperparameters**: Optimized learning rate, batch size, and epochs.

---

## 🔄 Automated Inference Process

The inference process for detecting solar panels is fully automated! Here’s how it works:

1. **Image Access and Prediction**:
   - Access test images directly from Google Drive.
     - Utilize **SAHI’s** tiled inference for accurate detection of small solar panels.
     Read more about this here 👉 [Slicing Aided Hyper Inference](https://docs.ultralytics.com/guides/sahi-tiled-inference/)

2. **Results Generation**:
   - Annotated images are saved in the corresponding Google Drive folder.
   - Counts of detected solar panels are recorded.

3. **Data Storage**:
   - Results, including image paths and panel counts, are saved in a CSV file named `panel_count.csv`.
   - The CSV file is organized neatly in your Google Drive after processing.

4. **File Management**:
   - Generated files are systematically stored in designated folders, keeping everything organized.

---

## 📈 Results

The SolarMap model, powered by YOLOv8 and **SAHI (Slicing Aided Hyper Inference)**, has shown impressive performance in detecting small rooftop solar panels.

### 📊 Performance Metrics:
| Metric              | Value   |
|---------------------|---------|
| mAP50 (B)           | 80.22%  |
| mAP50-95 (B)        | 63.65%  |
| Precision (B)       | 86.05%  |
| Recall (B)          | 73.68%  |

### 🎯 Key Takeaways:

1. **SAHI Tiled Inference**:  
   Enhanced detection of smaller solar panels by slicing images into manageable tiles, improving accuracy on high-resolution images.

2. **Training and Visualization**:  
   Monitored in real-time using **TensorBoard**, [**ClearML**](https://app.clear.ml/login?redirect=%2Fdashboard), and [**Comet**](https://www.comet.com/). Loss function steadily decreased with precision and recall stabilizing around 86.05%.

3. **Inference on Test Images**:  
   Successfully detected and counted solar panels under various challenging conditions.

4. **Performance on Small Objects**:  
   The model accurately identified tiny solar panels on rooftops, ensuring reliable counts.

---

### 📥 Download Trained Model Weights

You can download the trained model weights here:  
👉 [Download Weights](Weights/best-40.pt)

---

### 🖼️ Output Examples

Here are a couple of examples of the model's output:

![Detection 1](Results/img.png)
![Detection 2](Results/img_1.png)

---

Thank you for exploring **SolarMap**! We hope this project helps advance the understanding and use of solar energy. If you have any questions or feedback, feel free to reach out!
