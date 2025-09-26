# LSB_image_Steganography-
🚀 How to Run
1️⃣ Compile the Project

gcc *.c 
2️⃣ Encoding a Message

./a.out -e <source.bmp> <secret.txt> <output.bmp>
Example:

./a.out -e input.bmp secret.txt encoded.bmp
3️⃣ Decoding a Message

./a.out -d <encoded.bmp> <output.txt>
Example:

./a.out -d encoded.bmp decoded.txt
📝 Example Output
Encoding:

INFO: Starting Encoding Process...  
INFO: Copying BMP Header...  
INFO: Embedding Secret Message Length...  
INFO: Encoding Secret Message...  
INFO: Saving Encoded Image...  
INFO: Encoding Completed Successfully!  
Decoding:

INFO: Starting Decoding Process...  
INFO: Reading BMP Header...  
INFO: Extracting Secret Message Length...  
INFO: Decoding Secret Message...  
INFO: Decoding Completed Successfully!  
🔍 How It Works – LSB Technique
The Least Significant Bit of each byte in the image is modified to store bits of the secret message. Since the LSB change is visually negligible, the message is hidden without altering image quality.

Encoding Flow
Read BMP header and copy it to the output file.
Embed the secret message length into pixel data.
Embed each bit of the secret message into LSBs of the image.
Save the new BMP file.
Decoding Flow
Read BMP header.
Extract message length from LSBs.
Read bits from LSBs and reconstruct the secret message.
Save decoded message to a text file.
✨ Built with ❤️ using C and the magic of Steganography ✨
