<h1 align="center">chatgpt 💬 + code interpreter 💻 experiments</h1>

## 👋 hello

We aim to push ChatGPT + Code Interpreter to its limits, show you what's possible and unlock your creativity! Well, and have a lot of fun doing it! 🔥

## 💻 code interpreter

Code Interpreter is an official ChatGPT plugin for data analytics, image conversions, editing code, and more. It is now available to all ChatGPT Plus users. It provides OpenaAI models with a working Python interpreter in a sandboxed, firewalled execution environment and some temporal hard drive space.

## 💬 prompts

### Detect and track face on the video

Currently, OpenAI does not allow deep learning in the Code Interpreter environment. However, it is still possible to detect and track objects. We just need to be more creative. [Haar Cascade](https://en.wikipedia.org/wiki/Haar-like_feature) was one of the most popular approaches to face detection in old-school computer vision. Importantly, you can upload and download files, opening up many new possibilities!

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

### Using OCR to extract text from images

ChatGPT has access to [Tesseract](https://github.com/tesseract-ocr/tesseract) - one of the most powerful open-source OCR engines. It is not perfect. There are certainly better commercial tools on the market. But it can easily read black text printed on a white sheet of paper.

<details close>
<summary>👉 steps</summary>

1. Upload the input image.

![IC-Basic-Invoice-Template_PDF](https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/1eee9dd1-e866-4b5a-9a96-dcc88ba91c96)

2. Extract text from the image.

> OCR an image for me and generate a text file.

![F0ldRAaX0AITVBO](https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/76c0ab68-e4cb-4003-9a7a-8c4c579c5fec)

3. Annotate the input image with detected text.

> Annotate the input image with detected text using bounding boxes.

</details>

![F0lcjPwWYAASmDX](https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/ea24ed74-2916-4473-8265-97303518a632)

### Classification of images from the MNIST dataset

🚧 coming soon...

## 🦸 contribution

We would love your help in making this repository even better! If you know of an amazing prompt you would like to share, or if you have any suggestions for improvement, feel free to open an
[issue](https://github.com/SkalskiP/awesome-code-interpreter-prompts/issues) or submit a
[pull request](https://github.com/SkalskiP/awesome-code-interpreter-prompts/pulls).
