# 4 × 6 Label PDF Splitter

A simple browser tool that splits each PDF page into **2 or 4 separate labels**, with every output page sized exactly **4 × 6 inches** (288 × 432 PDF points).

## Features

- **2-label mode:** split each page into top/bottom or left/right halves.
- **4-label mode:** split each page into a 2 × 2 grid.
- Rotate labels by 0°, 90°, 180°, or 270°.
- Choose normal or reversed output order.
- Scale each section proportionally and center it with a small margin.
- Select a PDF or drag and drop it into the page.
- Download all resulting labels as one PDF.
- Process PDF files in the browser without uploading them to a server.

## Getting started

1. Save the supplied `index(1).html` file as `index.html`.
2. Open `index.html` in your browser.
3. Select a PDF containing two or four labels per page.
4. Choose the rotation and output order. For two labels, also choose the split direction.
5. Click **Split 2 Labels → 4 x 6** or **Split 4 Labels → 4 x 6**.
6. Open the downloaded PDF and check the labels before printing.

An internet connection is needed to load the PDF library from its CDN.

## Split order

| Mode | Default order | Reversed order |
| --- | --- | --- |
| Top / Bottom | Top, bottom | Bottom, top |
| Left / Right | Left, right | Right, left |
| 4 labels | Top-left, top-right, bottom-left, bottom-right | Bottom-right, bottom-left, top-right, top-left |

The split direction setting applies only to 2-label mode. Rotation applies to both modes; the default is 270°.

## Printing

- Select **4 × 6 inch** paper (101.6 × 152.4 mm).
- Use **100% / Actual Size** in the print dialog.
- Check the orientation and barcode readability before printing a full batch.

## Output filenames

- Two labels: `original-name_4x6_split_2_labels.pdf`
- Four labels: `original-name_4x6_split_4_labels.pdf`

A 10-page source PDF produces 20 pages in 2-label mode or 40 pages in 4-label mode.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Complete application: layout, styling, and PDF processing |
| `README.md` | Project description and usage instructions |

## Technology

HTML, CSS, and JavaScript with `pdf-lib` version 1.17.1 loaded from jsDelivr. No build step or backend is required.

## Limitations

The tool divides pages into equal halves or quarters; it does not automatically detect label boundaries. Labels that cross a dividing line can be cut. Choose the mode that matches the layout of the source PDF. Password-protected or damaged PDFs may fail to process.
