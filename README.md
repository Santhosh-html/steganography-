1. 🔧 Add Support for JPEG Input Automatically Converting to PNG
Update the script or instructions to automatically convert .jpg or .jpeg images to .png, as PNG is required for preserving data without compression artifacts.

Documentation Change:

Note: If you provide a .jpg image, it will be automatically converted to .png for better quality and to support lossless steganography.

2. 📁 Organize Project Structure
Recommend a clearer project directory layout:

lua
Copy
Edit
steganography/
│
├── res/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── output.png
│
├── steganography.py
├── requirements.txt
├── README.md
3. 🧪 Add Test Section for Developers
New Section:

markdown
Copy
Edit
## Running Unit Tests

To run tests for the Steganography class:

```bash
python -m unittest discover tests
Make sure you have a tests/ folder with test cases for merge() and unmerge().

yaml
Copy
Edit

4. 🧠 **Explain Merge Bit Manipulation Briefly**
Add a short example for more clarity on how LSB is used in code:

**New Subsection:**
```markdown
### How the Merge Works

To hide one image inside another, we use 4 bits from each image:

- Keep the **4 most significant bits** from the cover image.
- Take the **4 most significant bits** from the hidden image.
- Combine them into one new byte.

For example:
- Original image pixel: `11110000`
- Hidden image pixel: `10100000`
- Merged pixel becomes: `11111010`
5. 🛠️ Add CLI Help Example
Improve usability by showing how to access help:

bash
Copy
Edit
python steganography.py --help
And show example output:

plaintext
Copy
Edit
usage: steganography.py [-h] {merge,unmerge} ...

Merge or unmerge hidden image into a cover image.
6. 📸 Support Image Preview with Matplotlib (Optional)
Add code snippet:

python
Copy
Edit
import matplotlib.pyplot as plt

img = Image.open("res/output.png")
plt.imshow(img)
plt.axis("off")
plt.show()
7. ✍️ Minor Wording Fixes
Before:

Change the leftmost bit from 1 to 0 (11111111 to 01111111)

After:

Change the most significant bit from 1 to 0 (e.g., 11111111 → 01111111)

8. 🌐 Add a “References” Section
List sources in a proper format:

markdown
Copy
Edit
## References

- [Steganography - Wikipedia](https://en.wikipedia.org/wiki/Steganography)
- [RGB Color Model - Wikipedia](https://en.wikipedia.org/wiki/RGB_color_model)
- [Digital Image - Wikipedia](https://en.wikipedia.org/wiki/Digital_image)
