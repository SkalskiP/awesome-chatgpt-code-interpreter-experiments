<h1 align="center">chatgpt 💬 + code interpreter 💻 prompts</h1>

## 👋 hello

Our goal is to push ChatGPT + Code Interpreter to the limit. You'll be surprised what's possible without writing even a single line of code. 🔥

## 💻 code interpreter

TODO

## 💬 prompts

### Detect and track face on the video

Currently, OpenAI does not allow deep learning in the Code Interpreter environment. However, it is still possible to detect and track objects. We just need to be more creative. [Haar Cascade](https://en.wikipedia.org/wiki/Haar-like_feature) was one of the most popular approaches to face detection in old-school computer vision. 

<details close>
<summary>👉 steps</summary>

1. Upload input video.
2. Confirm that ChatGPT can successfully process the video.
3. Run Haar Cascade face detection on a single video frame.
4. Run Haar Cascade face detection on the whole video.

> Process video frame by frame. Use Haar Cascade to detect the face on each frame and draw a red bounding box around it. Save output video in mp4 format.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/45dc0f0c-f770-4766-be06-b238ff0adc5a

5. Use box IoU to remove false positives.

> Looks like on some frames, we have some accidental detections. Use IoU of boxes between the frames to isolate a single bounding box representing the face and discard other false positive boxes.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/19bcd6cc-9160-4c4c-b2fd-e628c355a25d

6. Crop video to follow the face.

> Create video with 800x800 resolution. Loop over each frame of the input video. If no face is detected on that frame, skip it. If the face is detected, use box coordinates to crop the original frame, then paste that cropped frame with the face into an 800x800 black output frame. Return the final video in mp4 format.

https://github.com/SkalskiP/awesome-chatgpt-code-interpreter-prompts/assets/26109316/3ce5a634-ed58-4703-8151-fb799159b14d

</details>

### Using OCR to extract text from images

🚧 coming soon...

### Classification of images from the MNIST dataset

🚧 coming soon...

## 🦸 contribution

We would love your help in making this repository even better! If you know of an amazing prompt you would like to share, or if you have any suggestions for improvement, feel free to open an
[issue](https://github.com/SkalskiP/awesome-code-interpreter-prompts/issues) or submit a
[pull request](https://github.com/SkalskiP/awesome-code-interpreter-prompts/pulls).
