# ARRI-K1S1-OCIO-Config
Based on the [ARRI LUT Generator](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator) I have created a minimal OCIO config of ARRI K1S1 for full CG projects. This is **one of the most popular LUTs ever created** in its most minimalistic and simple form:
* Inputs (textures) are in "linear"
* Rendering and Nuke working space are also in "linear"
* View Transform is for Rec.1886 display

There is no need to go wide gamut or do anything complex to **craft beautiful images**. Enjoy!

# Image Examples
<p>
    <img ![hue_sweep_arri_k1s1] width="192" height="108" src="https://github.com/user-attachments/assets/f60b6392-eee7-4308-9628-72700af0b0f2" >  
    <img ![photographic_scene_arri_k1s1] width="192" height="108" src="https://github.com/user-attachments/assets/e3bcd6d3-98ca-4aa1-90cb-00a410396fcb" >
    <img ![lego_sailors_arri_k1s1] width="192" height="108" src="https://github.com/user-attachments/assets/9b84b9ae-f2af-495b-9142-eb887412df9e" >
    <img ![louise_sun_arri_k1s1] width="192" height="108" src="https://github.com/user-attachments/assets/1d23af95-0315-4686-b0ad-41dfe2fe78f8" >
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is XYZ which is the base of all colourimetry
* "linear" stands for "linear_bt.709"
* "cineonlog_rec709" can be used for a matte-painting workflow in Photoshop
* "logc3_arriwg3" is the shaper space. It can be used for color timing and some log operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* An inverse of the View Transform has been provided even though it is not perfect
* One may easily add several colorspaces or displays for HDR output if needed (such as "p3_d65_pq")

# Looks
* 87 looks from the [ARRI Look Library](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/arri-look-library-app) have been uploaded
* The use of Looks is highly recommended with ARRI K1S1
* To use one of the looks, you need to combine it with a View. Like this for instance:

```- !<View> {name: ARRI K1S1 Vibrant, colorspace: ARRI K1S1 - Rec.709 - 2.4 Gamma, looks: 5210 Vibrant}```

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017         | Original Blender Color Management used on [this movie](https://www.youtube.com/watch?v=uf3ALGKgpGU) |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017         | RED Image Processing Pipeline |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2021         | Color Encoding System developed by the Academy |
| [Sony Venice](https://sonycine.com/resources/luts/)                                              | Sony / Picture Shop  | 2022         | LUT files made in partnership with [Picture Shop](https://www.pictureshop.com/) |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022         | The new ARRI Alexa35 workflow described [here](https://www.youtube.com/watch?v=s_RXjVeC_7s) |
| [Tony](https://github.com/h3r2tic/tony-mc-mapface)                                     | Tomasz Stachowiak    | 2023         | A cool-headed display transform |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023         | Blender Color Management used on [this video game](https://www.youtube.com/watch?v=mVjBRZqajYY) |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024         | Baselight Color Management Workflow explained [here](https://youtu.be/DL4n6LErMbw?t=325) |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024         | Minimal AgX OCIO Config using Linear BT.709 |
| [JP-2499](https://github.com/jedypod/JP2499)                                                     | JP Zambrano          | 2024         | A popular picture formation pipeline described [here](https://www.liftgammagain.com/forum/index.php?threads/2499-drt-an-alternative-picture-formation-pipeline.18639/) |
| [Open DRT](https://github.com/jedypod/open-display-transform)                                    | Jed Smith            | 2024         | State-of-the-art Color Management Workflow |
