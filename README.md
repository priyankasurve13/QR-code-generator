# QR-code-generator
import qrcode

# Define the website URL
website_url = "https://www.youtube.com/@PillaiGroupOnline"

# Generate QR code
qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_L,
    box_size=10,
    border=4,
)
qr.add_data(website_url)
qr.make(fit=True)

# Create an image from the QR Code instance
qr_img = qr.make_image(fill_color="black", back_color="white")
