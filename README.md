<h1 align="center">chatgpt 💬 + code interpreter 💻 experiments</h1>

## 👋 hello

We aim to push ChatGPT + Code Interpreter to its limits, show you what's possible and unlock your creativity! Well, and have a lot of fun doing it! 🔥

## 💻 code interpreter

Code Interpreter is an official ChatGPT [plugin](https://openai.com/blog/chatgpt-plugins) for data analytics, image conversions, editing code, and more. Since July 6th, 2023 it is available to all ChatGPT Plus users. It provides OpenaAI models with a working Python interpreter in a sandboxed, firewalled execution environment. Importantly, for the first time, it is possible to upload and download files.

<details close>
<summary>👉 activate code interpreter</summary>

1. Navigate to ChatGPT settings.

2. Activate Code Interpreter in the "Beta features" tab.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/18fadd19-90d0-4e05-9882-6cfac8990f68">

<br>
<br>

3. Select GPT-4 + Code Interpreter environment.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/33e5831a-0098-4252-80ec-80d992a254aa">

</details>

## 💬 prompts

### Detect and track face on the video

Currently, OpenAI does not allow access to pre-trained deep learning models in the Code Interpreter environment. However, it is still possible to detect and track objects. We just need to be more creative. [Haar Cascade](https://en.wikipedia.org/wiki/Haar-like_feature) was one of the most popular approaches to face detection in old-school computer vision. 

<details close>
<summary>👉 steps</summary>

1. Upload input video.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/9ec21cf7-84c6-4be6-a8e4-c439dcee945c

2. Confirm that ChatGPT can successfully process the video.

> Extract the first frame from the uploaded video.

![first_frame_new](https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/8e62d895-821f-4134-b0e4-5438071e2703)

3. Run Haar Cascade face detection on a single video frame.

> Extract the first frame from the uploaded video. Use Haar Cascade to detect the face and draw a red bounding box around it.

![first_frame](https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/65071ecf-f5b2-468a-b85e-8bb1d1a439a3)

4. Run Haar Cascade face detection on the whole video.

> Process video frame by frame. Use Haar Cascade to detect the face on each frame and draw a red bounding box around it. Save output video in mp4 format.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/45dc0f0c-f770-4766-be06-b238ff0adc5a

5. Use box IoU to remove false positives.

> Looks like on some frames, we have some accidental detections. Use IoU of boxes between the frames to isolate a single bounding box representing the face and discard other false positive boxes.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/19bcd6cc-9160-4c4c-b2fd-e628c355a25d

6. Crop video to follow the face.

> Create video with 800x800 resolution. Loop over each frame of the input video. If no face is detected on that frame, skip it. If the face is detected, use box coordinates to crop the original frame, then paste that cropped frame with the face into an 800x800 black output frame. Return the final video in mp4 format.

</details>

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/3ce5a634-ed58-4703-8151-fb799159b14d

### Classification of images from the MNIST dataset

The [MNIST](https://www.kaggle.com/datasets/hojjatk/mnist-dataset) dataset is a widely-used collection of handwritten digits that is used to teach computers how to recognize and understand numbers. It consists of thousands of examples of handwritten numbers from 0 to 9, created by different people in different styles. The images are very small - only 28x28 pixels. Therefore, they are great for training in an environment with limited resources.

<details close>
<summary>👉 steps</summary>

1. Upload the MNIST dataset into the Code Interpreter environment.

2. To save hard drive and memory space, only 10% of the original dataset is loaded.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/7fcf0b4c-9368-478a-b157-dadd4dd4fb83">

<br>
<br>

3. Make sure that Code Interpreter knows how to process data.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/d45fa91c-64de-4a30-9595-3c4f638d04d0">

<br>
<br>

4. Split data into train and test subsets.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/b677c7d7-9380-470e-a32d-4baa8beaff5f">

<br>
<br>

5. Train sci-kit learn [Support Vector Classifier](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html) on the test set.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/fd8b636f-5fcb-456c-abd9-14eadbd779d7">

<br>
<br>

6. Evaluate the trained model on the test set.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/3b0bd652-41dd-4180-9190-dff9bb012a12">

<br>
<br>

7. Visualize false classification results.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/216c9203-36be-4ce1-88d2-8bf2a1b3e411">

<br>
<br>

8. Download the trained model.

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/365dad9b-b40a-4796-81d5-0d722aca3350">

</details>

<img width="600" src="https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-experiments/assets/26109316/c52e63eb-5fb1-4f7f-9908-25171071f354">

### Using OCR to extract text from images

🚧 coming soon...

## 🦸 contribution

We would love your help in making this repository even better! If you know of an amazing prompt you would like to share, or if you have any suggestions for improvement, feel free to open an
[issue](https://github.com/SkalskiP/awesome-code-interpreter-prompts/issues) or submit a
[pull request](https://github.com/SkalskiP/awesome-code-interpreter-prompts/pulls).
