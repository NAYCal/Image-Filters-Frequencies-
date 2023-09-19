Author: Alexander Ng
SID: 3037039488
Email: naycal@berkeley.edu
Website: https://inst.eecs.berkeley.edu/~cs180/fa23/upload/files/proj2/naycal

Simply run main.ipynb in order to see the results!

## Code to retrieve and output resulting image
Functions:
- get_file_image(fname): Retrieves the image from the file.
- convert_channel_to_image(r, g, b, alpha=None): Returns a full image from red, green, blue, and alpha channels.
- get_image_channels(image): Returns the r, g, b, and alpha (if alpha exists) channels.
- get_image_channels(image, with_alpha=False): Returns a grayscaled image, useful for gradient calculation.
- red_channel: Returns the red channel of the image.
- green_channel: Returns the green channel of the image.
- blue_channel: Returns the blue channel of the image.
- alpha_channel: Returns the alpha channel of the image.
- save_image(image, name, is_out=True): Saves the image.

### Part 1.1: Finite Difference Operator
Functions:
- gradient_magnitude_x_axis(image): Returns the gradient of the input image with respect to x. Note the image can be any 2D matrix.
- gradient_magnitude_y_axis(image): Returns the gradient of the input image with respect to y. Note the image can be any 2D matrix.
- gradient_magnitude(image): Returns the gradient magnitude of the input image. Note the image can be any 2D matrix.
- binarize(image, threshold): Returns the binarized image on threshold.

### Part 1.2: Derivative of Gaussian (DoG) Filter
- get_gaussian_kernel_2d(ksize, sigma): Returns the gaussian kernel in get_gaussian_kernel_2d

## Part 2: Fun with Frequencies!

### Part 2.1 Image "Sharpening"
- apply_func_image(image, function): Appies function to all channels to image.
- apply_gaussian_blurr(image, kernel_size, kernel_sigma): Applies gaussian blur to image.
- unsharpen_image(image, kernel_size, kernel_sigma): Unsharpens the image.
- highpass_image(image, kernel_size, kernel_sigma): Returns the high frequency of the image.
- sharpen_image(image, alpha=1, kernel_size=33, kernel_sigma=11): Returns a sharpened image.
- optimized_sharpen_image(image, alpha=1, kernel_size=33, kernel_sigma=11): Returns a sharpened image but optimized.

### Part 2.2: Hybrid Images
- create_hybrid_image(im1, im2, high_freq_kernel_size=60, high_freq_kernel_sigma=20, low_freq_kernel_size=40, low_freq_kernel_sigma=20, is_gray=False): Returns a hybrid image.

### Part 2.3: Gaussian and Laplacian Stacks
- get_gaussian_stack(image, depth=5, kernel_size=30, kernel_sigma=20): As name suggests.
- get_laplacian_stack(image, depth=5, kernel_size=30, kernel_sigma=20): As name suggests.

### Part 2.4: Multiresolution Blending (a.k.a. the oraple!)
- get_blending_laplacian_stack(image1, image2, region_mask=None, depth=5, kernel_size=30, kernel_sigma=20, is_aligned=True): Returns laplacian stack of the combined image.
- combine_laplacian_stack(stack, depth=None): Returns the combined laplacian stack.