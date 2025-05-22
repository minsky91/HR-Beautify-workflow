## HR Beautify ComfyUI workflow (SDXL): refine after upscale and go as high as 24K

![HR Beautify Comfy workflow screenshot May 2025](https://github.com/user-attachments/assets/ae10f6a6-fc89-4842-88e4-d3137ec0266d)

HR Beautify (‘HR’ stands for Hires, or High resolution) is an advanced ComfyUI workflow to refine raw upscaled images. It doesn’t include the usual upscale with AI model component, concentrating instead on the best refinement of upscaled hires images possible, optionally beautifying them with a style transfer.

The workflow includes two ControlNets, for the most powerful and flexible img2img guidance, and two IP Adapters, to enhance images with style transfer and composition or reference guidance. For extra refinement, the Power Lora Loader node is included, supporting a potentially unlimited number of detail or style LoRas. Also included in the workflow are three post processing components: enhancing image’s HDR range, advanced image sharpening and color-matching.

The tiling component that enables hires refining is the widely used Tiled Diffusion (TD), together with Tiled VAE Encode & Decode. TD is compatible with all ControlNet models and can assist in processing images of up to **24K** resolution, optionally adding creative detail in the output along the way. 

The workflow includes a note with description of the user-controlled parameters. Full description of the HR Beautify workflow and custom nodes it uses can be found on the github [wiki pages](https://github.com/minsky91/HR-Beautify-workflow/wiki/HR-Beautify-ComfyUI-workflow/).  (Note: because of all the png example images it contains, the download zip is 89 MB large; to get the workflow json only, use this [**download link**](https://github.com/minsky91/HR-Beautify-workflow/blob/main/workflows/HR%20Beautify%20v1.0%20(release).json))

For Krita AI Diffusion users, a custom workflow version is also available, with a largely overlapping set of features.  ([**download link**](https://github.com/minsky91/HR-Beautify-workflow/blob/main/workflows/Krita%20AI%20HR%20Beautify%20v1.0%20(release).json)) Visit the wiki pages to learn more about these workflows and view examples of hires refined images.

![SILVIv2 test image - Before and After screenshot](https://github.com/user-attachments/assets/0c34ac93-e42c-4cb1-b12a-ebdcb64f8508)

![The stage angel - Before and After screenshot](https://github.com/user-attachments/assets/81aa0eb2-5315-4c07-9875-7365eab4e34e)

![The stage angel - detail fragment 1](https://github.com/user-attachments/assets/ebf3e972-0c2c-4be7-8751-6acfba5fb9b6)





TO-DO

As the title suggests, this workflow has been extensively tested for SDXL models only. It will work with SD 1.5 and Flux, but some additional tuning might be necessary, especially for Flux which lacks a good ControlNet Tile Resample model on par with xinsir’s.
