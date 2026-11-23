# Search this PC

Find your photos, videos and documents by describing them: "dog on a beach", "plumbing appointment letter",
"receipt total". It understands what is in pictures and video frames, the text of PDFs, Word files and notes, and the
text inside scanned pages. Everything runs on your own computer; nothing about your files is sent anywhere.

## Install (Linux, x86-64)

1. Download `search-this-pc-linux-x86_64.tar.gz` from the [latest release](https://github.com/jfj-oss/search-this-pc/releases/latest).
2. Unpack it and run the installer (no root needed):

   ```sh
   tar xzf search-this-pc-linux-x86_64.tar.gz && ./search-this-pc/install.sh
   ```

3. Open **Search this PC** from your app menu (or go to http://127.0.0.1:4574/). The first time it downloads its two
   search models once (about 1.1 GB) and asks which folders to search.

Optional: `tesseract` (text in scanned pages and photos of documents) and `ffmpeg` (searching inside videos). The page
tells you the exact install command for your system if they are missing.

Works on any graphics card, or none. The first indexing of a big photo folder takes a while; after that only new
files are read.

## Models

The `models-v1` release holds the image/text model (OpenCLIP ViT-B/32, `laion2b_s34b_b79k`, MIT licence) converted to
ONNX for this app. Text search uses [nomic-embed-text v1.5](https://huggingface.co/nomic-ai/nomic-embed-text-v1.5)
(Apache-2.0), downloaded from its own page.
