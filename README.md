## Batch Face Swap extension for https://github.com/AUTOMATIC1111/stable-diffusion-webui
 Automaticaly detects faces and replaces them.
 
![example1](https://user-images.githubusercontent.com/46696708/211933260-7a27cc13-e33a-4bf1-911f-43e0aa97b96c.png)

## Installation
1. Use `git clone https://github.com/kex0/batch-face-swap.git` from your SD web UI `/extensions` folder. 
Alternatively, install from the extensions tab with url `https://github.com/kex0/batch-face-swap`
2. Start or reload SD web UI.

## Guide
1. Open `img2img` tab.
2. Select `Batch Face Swap` script.
3. Paste a path of the folder containing your images in the `Images directory` textbox.
4. (Optional) It may sometimes fail to find a face if the face is very small in comparison to the size of the image.
So, you can tell it to split the image and look at the smaller portions of the image by using the `How many images to divide into` slider.
(don't worry it will stitch the image back together)
5. Click `Generate`

If you want to adjust `Denoising strength` or `Mask blur` you have to disable the override checkboxes.

You can generate and save the masks without even engaging the stable diffusion image generation by checking the `Save masks to disk` checkbox and pressing 
`Generate masks` button at the very bottom.

Tip:
You can check how many faces do your current settings find before you start generating with the stable diffusion 
by just clicking the `Generate masks` button at the very bottom.

![chrome_blF0pro5Pf](https://user-images.githubusercontent.com/46696708/212803134-88b7b57f-aa01-4fd2-ac14-d71ab173476b.png)

## Example
![example](https://user-images.githubusercontent.com/46696708/211818536-7d3bd06e-f6b1-40e9-854e-9cb44be3b2f8.png)

Prompt:
```ShellSession
detailed closeup photo of Emma Watson, 35mm, dslr
Negative prompt: (painting:1.3), (concept art:1.2), artstation, sketch, illustration, drawing, blender, octane, 3d, render, blur, smooth, low-res, grain, cartoon, watermark, text, out of focus
Steps: 50, Sampler: Euler a, CFG scale: 7, Seed: 4052732944, Size: 512x512, Model hash: a9263745, Batch size: 8, Batch pos: 1, Denoising strength: 0.5, Mask blur: 4
```
