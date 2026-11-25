# Project Report: AI-Based Image Classification System

## 1. Abstract
This project is a web application that classifies images using a pre-trained deep learning model. Users upload a photo or capture one from a webcam. The image is analysed in the browser with TensorFlow.js and MobileNet, and the system shows the predicted object and its confidence percentage.

## 2. Introduction
Image classification assigns a label (such as "cat" or "laptop") to an image. It is a core task in computer vision and is used in medical imaging, security, retail and self-driving cars.

## 3. Objectives
- Build a simple, responsive website for image classification.
- Support both image upload and live webcam capture.
- Use a real pre-trained model and show genuine confidence scores.
- Handle errors such as denied camera permission.

## 4. Technologies Used
| Technology | Purpose |
|---|---|
| HTML | Page structure |
| CSS | Styling and responsive layout |
| JavaScript | Application logic |
| TensorFlow.js | Runs machine learning in the browser |
| MobileNet | Pre-trained image classification model |

## 5. About MobileNet
MobileNet is a lightweight Convolutional Neural Network (CNN) designed for phones and browsers. It uses depthwise separable convolutions, which need far fewer calculations than standard convolutions. It is trained on ImageNet (about 1.2 million images, 1,000 classes).

## 6. System Workflow
1. The user uploads an image or captures a webcam frame.
2. The image is displayed on the page.
3. The image is resized to 224 x 224 pixels and normalised.
4. MobileNet outputs a probability for each of the 1,000 classes.
5. The top 3 predictions are shown; the highest is the final prediction.

## 7. Modules
- **Model loader:** downloads MobileNet, with fallback sources and a Retry button.
- **Upload module:** reads the file with FileReader.
- **Webcam module:** uses `navigator.mediaDevices.getUserMedia`, then captures a frame with a canvas.
- **Classifier:** calls `model.classify(image, 3)`.
- **Result display:** shows name, confidence and progress bars.
- **Reset:** stops the camera and clears the image and results.

## 8. Error Handling
- Camera permission denied, camera not found, camera in use.
- Browser without camera support or page not on https/localhost.
- Invalid file type or unreadable image.
- Model download failure, with a Retry button.

## 9. Limitations
- Limited to 1,000 ImageNet classes; cannot identify people by name.
- Needs internet on first load to download the model.
- Accuracy depends on image quality and lighting.

## 10. Future Scope
- Train a custom model with Teachable Machine for your own classes.
- Add prediction history and downloadable reports.
- Add real-time continuous webcam classification.
- Offline use as a Progressive Web App.

## 11. Conclusion
The project shows how a pre-trained deep learning model can run entirely in a web browser, giving fast classification without a server and without uploading user images anywhere.
