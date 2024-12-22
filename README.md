# **Image Object Replacement with Stable Diffusion and Auto-Generated Masks**

This project demonstrates object replacement in images using **Stable Diffusion 2.1 Base** combined with auto-generated masks. The model processes an input image, identifies objects (e.g., a car), and replaces them with new content specified via a prompt. The solution utilizes advanced techniques in **image segmentation**, **mask generation**, and **text-to-image synthesis**.

## **Key Features**
- **Object Detection and Mask Generation**: Automatically detect and mask objects based on prompts using `facebook/detr-resnet-50` or alternative segmentation models.
- **Object Replacement**: Replace masked objects using **Stable Diffusion** with a quantized implementation for better performance.
- **Visual Results**: Displays before-and-after images to validate the effectiveness of object replacement.
- **Flexible Inputs**: Works with various image types and supports prompts for customization.

---

## **Technologies Used**
- **Python**: Primary programming language.
- **Hugging Face Transformers**: For pre-trained segmentation models (`DETR`, `SegFormer`).
- **Diffusers Library**: For running Stable Diffusion models.
- **PyTorch**: Framework for deep learning.
- **Matplotlib**: Visualization library.
- **Pillow**: For image manipulation.

---

## **Setup Instructions**

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/image-replacement-stable-diffusion.git
cd image-replacement-stable-diffusion
```

### **2. Install Dependencies**
Use the provided `requirements.txt` file to install necessary libraries.
```bash
pip install -r requirements.txt
```

### **3. Login to Hugging Face**
Authenticate with your Hugging Face access token to download models:
```python
from huggingface_hub import login
login(token="YOUR_HF_ACCESS_TOKEN")
```

### **4. Download Pre-Trained Models**
- **Stable Diffusion**:
  - `stabilityai/stable-diffusion-2-1-base`
- **Segmentation Model**:
  - `facebook/detr-resnet-50` or `nvidia/segformer-b0-finetuned-ade-512-512`

### **5. Run the Project**
Execute the notebook or script:
```bash
python main.py
```

---

## **Project Workflow**

### **1. Load the Input Image**
- The user provides an image (e.g., a car photo).
- Example: `/content/car.jpg`.

### **2. Auto-Generate Mask**
- A pre-trained segmentation model generates a mask based on a textual prompt (e.g., "car").
- The `image-segmentation` pipeline is used for this step.

### **3. Replace Object Using Stable Diffusion**
- The masked area is replaced with new content generated using a Stable Diffusion prompt (e.g., "replace car with a futuristic flying car").

### **4. Display Results**
- Before-and-after images are displayed for comparison.

---

## **Known Issues**
1. **Empty Mask Results**: The segmentation model may fail to detect objects if the prompt is too vague or the image lacks clarity.
   - **Solution**: Refine the prompt or use a higher-quality image.
2. **Model Memory Constraints**: Ensure sufficient GPU memory for running Stable Diffusion. Consider using a quantized model.

---

## **Future Improvements**
- Fine-tune the segmentation model for better object detection.
- Expand support for more object categories and prompts.
- Integrate additional features like background replacement.

---

## **Contributing**
Contributions are welcome! Feel free to fork the repository, make changes, and submit a pull request.

---

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## **Contact**
For questions or feedback, reach out to:

- **Name**: Hanzala Mohammad Sadiq Dhukka  
- **Email**: [dhukkahadi2001@gmail.com](mailto:dhukkahadi2001@gmail.com)  
- **LinkedIn**: [Profile](https://www.linkedin.com/in/mohammad-hadi-dhukka-5453611a9/)  
- **GitHub**: [Profile](https://github.com/AbHadi03)  
