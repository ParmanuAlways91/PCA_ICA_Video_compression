# PCA_ICA_Video_compression
Experiment on the Berkeley Dataset and a yuv file. Comparison of the downsampling and then comparing the frames using VMAF and MSE. FFMPEG is used to compress the video.
The problem statement was as follows:

Part_1: Principal components of natural images
    Download the Berkeley segmentation dataset and extract 8 × 8 patches from a large
    corpus of patches (you may not need the entire dataset, you need to explore the number
    of sufficiently diverse patches). Perform principal and independent component analysis
    on the corpus of images. You can use FastICA computations available through libraries
    for this. Now compare the mutual information of (a) a pair of nearby pixels, (b) top
    two principal components in terms of their variance (c) top two independent components
    in terms of their variance. To compute the mutual information, you need to estimate
    the empirical joint probability distribution of the respective quantities on the corpus of
    natural images.
    
Image compression and resolution
    The goal of this question is to understand the bit rate below which it is better to downsample
    the video spatially by 2, compress the video and then upsample rather directly
    compress at the desired bit rate. Find this switching bit rate for the bs1 25fps.yuv video
    containing 217 frames available in the link pasted on Teams. You need to implement
    this question for H.264 compression. In order to control the bit rate, you can use ffmpeg
    or other publicly available compression software that allows you to do so. Perform this
    experiment under two scenarios
    (a) One I frame and all other P frames
    (b) All I frames
    Quality needs to be measured in terms of PSNR in the luminance data, and VMAF for
    this experiment. Clearly mention the various settings of the codec that you choose for this
    in the report (Hint: Explore bit rates in the range of 100 to 1000 kpps). Submit a plot of
    the rate vs quality according to both the quality metrics for the two strategies (with and
    without dowmsampling and upsampling) to demonstrate the switching rate.
    
For FFPMEG in windows, Download the FFMEG release version from the https://www.gyan.dev/ffmpeg/builds/
For logging the output of FFPMEG, lavfi is used.
