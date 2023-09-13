# QRcode-Generator
This Python script generates a QR code for a specified URL using the qrcode library. QR codes are commonly used to store URLs, text, or other data that can be easily scanned by a mobile device or QR code reader.
Prerequisites
Before running the script, make sure you have the qrcode library installed. You can install it using pip:
pip install qrcode[pil]
Usage
Open the script in your preferred Python IDE or text editor.

Modify the data variable to contain the URL or data you want to encode in the QR code. For example:


data = "https://github.com/raktimbar100"
Customize the QR code by adjusting the parameters in the qrcode.QRCode initialization. You can modify the version, box_size, and border as needed. Here's what each parameter does:

version: The QR code version (1 to 40). Higher versions store more data.
box_size: The size of each QR code box (in pixels).
border: The border size around the QR code (in boxes).
Run the script. This will generate a QR code image with the specified data and parameters.

The generated QR code image will be saved as "test.png" in the current directory.
import qrcode

qr = qrcode.QRCode(
    version=15,
    box_size=10,
    border=5
)

data = "https://github.com/raktimbar100"
qr.add_data(data)
qr.make(fit=True)
img = qr.make_image(fill_color="black", back_color="white")
img.save("test.png")

This will generate a QR code for the URL "https://github.com/raktimbar100" with the specified parameters.
<a href="test.png"></a>
