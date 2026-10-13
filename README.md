# Clark PDF extraction patch

This crate is `pdf-extract` 0.12.0 (upstream commit
`b95bf9f6268772d5088f09b0034e488e64294835`) with a three-line CID font
width-range fix. The range end and width use their own fields, and the final
CID is included. No other extraction code has changed.

Original author: Jeff Muizelaar. Original source and MIT license declaration:
https://github.com/jrmuizel/pdf-extract

The package is named `clark-pdf-extract`; its Rust library name remains
`pdf_extract`. `pdfsink-rs` aliases the package at its dependency boundary.

---

## pdf-extract
[![Build Status](https://github.com/jrmuizel/pdf-extract/actions/workflows/rust.yml/badge.svg)](https://github.com/jrmuizel/pdf-extract/actions)
[![crates.io](https://img.shields.io/crates/v/pdf-extract.svg)](https://crates.io/crates/pdf-extract)
[![Documentation](https://docs.rs/pdf-extract/badge.svg)](https://docs.rs/pdf-extract)

A rust library to extract content from PDF files.

```rust
let bytes = std::fs::read("tests/docs/simple.pdf").unwrap();
let out = pdf_extract::extract_text_from_mem(&bytes).unwrap();
assert!(out.contains("This is a small demonstration"));
```

## See also

- https://github.com/elacin/PDFExtract/
- https://github.com/euske/pdfminer / https://github.com/pdfminer/pdfminer.six
- https://gitlab.com/crossref/pdfextract
- https://github.com/VikParuchuri/marker
- https://github.com/kermitt2/pdfalto used by [grobid](https://github.com/kermitt2/grobid/)
- https://github.com/opendatalab/MinerU (uses PyMuPDF and pdfminer.six)

### Not PDF specific
- https://github.com/Layout-Parser/layout-parser
