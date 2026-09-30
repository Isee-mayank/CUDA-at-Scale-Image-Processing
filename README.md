# CUDA-Accelerated Batch Image Processing

## Project Overview

This project demonstrates GPU-accelerated batch image processing using CUDA and CuPy. It processes multiple images in a single execution and converts RGB images into grayscale images using a custom CUDA kernel.

The main objective is to understand how parallel computing can be used to perform repetitive image processing operations efficiently on a GPU.

## Objectives

* Process a large batch of images in one execution.
* Implement a custom CUDA kernel for grayscale conversion.
* Use GPU parallelism to process image pixels.
* Save processed images for visual comparison.
* Record execution time and processing results.

## Technologies Used

* Python
* CUDA
* CuPy
* NumPy
* Pillow (PIL)
* Google Colab
* NVIDIA Tesla T4 GPU

## Project Structure

```text
CUDA-at-Scale-Image-Processing/
│
├── README.md
├── CUDA_at_Scale_Image_Processing.ipynb
├── execution_log.txt
├── input_images/
├── output_images/
└── screenshots/
```

## How It Works

1. A dataset of input images is generated.
2. The images are loaded and converted into numerical arrays.
3. Image data is transferred to the GPU.
4. A custom CUDA kernel calculates grayscale values for image pixels.
5. The processed images are transferred back to the CPU.
6. The output images are saved to the output directory.
7. Execution time and processing details are recorded.

## Execution Environment

The project was executed in Google Colab using an NVIDIA Tesla T4 GPU.

The GPU environment was verified using the `nvidia-smi` command, and CuPy was used to execute the custom CUDA kernel.

## Results

The batch processing experiment successfully processed 100 images of size 256 × 256 pixels.

* Number of images processed: 100
* Total execution time: 0.8096 seconds
* Average time per image: 0.008096 seconds
* Processing status: Successful

The reported total time includes image loading, data transfer, GPU processing, and saving the output files. It is not a kernel-only benchmark.

## How to Run

1. Open `CUDA_at_Scale_Image_Processing.ipynb` in Google Colab.
2. Select **Runtime → Change runtime type**.
3. Choose a GPU accelerator.
4. Run the notebook cells in sequence.
5. Check the generated images in the output directory.

## Conclusion

This project provided practical experience with CUDA programming, GPU memory transfers, parallel image processing, and performance measurement. Processing a batch of images helped demonstrate how GPU computing can be applied to repetitive tasks and highlighted the importance of considering data transfer and file I/O when measuring overall performance.

## Author

Mayank Pande

## Note

This project is an educational demonstration of GPU-accelerated image processing.
