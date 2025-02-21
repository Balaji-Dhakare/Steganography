# Secure Data Hiding in Image Using Steganography

This project implements a simple steganography technique to hide a secret message within an image, with added password protection for decryption.

## Introduction

This project demonstrates a basic approach to steganography, concealing text data within an image file.  It uses the Least Significant Bit (LSB) method, modifying the least significant bits of pixel values to encode the message.  A password is required for decryption, adding a layer of security.  This is a simplified example for educational purposes and may not be suitable for highly sensitive data.

## Methodology

The code reads a message from the user and embeds it into the provided image ("mypic.jpg" by default).  It uses a dictionary to map characters to numerical values and vice-versa.  The message characters are encoded by changing the least significant bits of the image's red, green, and blue (RGB) pixel values sequentially. The pixel coordinates (n, m) are incremented for each character, and the color channel (z) cycles through the RGB values.  The modified image is saved as "encryptedImage.jpg".

Decryption requires the same password.  If the correct password is entered, the code reverses the embedding process, extracting the hidden message from the stego-image.

**Limitations:**

* **Security:** This is a basic implementation.  More sophisticated steganography techniques and encryption methods would be needed for stronger security.  The LSB method is vulnerable to certain steganalysis attacks.
* **Capacity:** The amount of data that can be hidden depends on the image size and complexity.
* **Error Handling:**  The code lacks robust error handling (e.g., checking if the image path is valid, handling potential exceptions).

## Requirements

* Python 3
* OpenCV (cv2) library: `pip install opencv-python`

## Installation

1. Save the Python code (e.g., as `steganography.py`).
2. Place the image you want to use for steganography (e.g., `mypic.jpg`) in the same directory as the script.  **Important:** Replace `"mypic.jpg"` in the code with the actual path to your image if it's different.
3. Install the required libraries using pip, as mentioned above.

## Usage

1. Open a terminal or command prompt and navigate to the directory where you saved the files.
2. Run the script: `python steganography.py`
3. The script will prompt you to enter the secret message and a password.
4. The stego-image ("encryptedImage.jpg") will be created in the same directory.
5. To decrypt, run the script again and enter the same password.

## Contributing

Contributions are welcome!  Please fork the repository and submit a pull request with your changes.  Consider adding error handling, improving security, or implementing more advanced steganography techniques.


## Contact

Balaji Dhakare

https://www.linkedin.com/in/balaji-dhakare/(#contact)
