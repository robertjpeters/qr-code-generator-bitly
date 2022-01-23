# QRCode Generator / Optional Bitly Updater

This application can be used to either generate QR codes, create new Bitly links, update existing Bitly links, or a combination of all three.

## Generating QRCode files only (no API calls to Bitly)

```
qr.exe -csv="C:\Users\robert\Downloads\qrcodes.csv" -borderless=true -qr-codes=true -qr-only=true -format=pdf -output="C:\Users\robert\Downloads" -overwrite=true
```

## Creating new Bitly links or updating existing ones

```
qr.exe -csv="C:\Users\robert\Downloads\qrcodes.csv" -borderless=true -qr-codes=true -format=pdf -output="C:\Users\robert\Downloads" -overwrite=true -key="TEST123"
```

## Limitations
- Bitly restricts the number of API calls to very low amounts - still need to implement a waiting patter for large files

## All CLI Options

```
  -borderless
        Remove the border around qr codes (default true)
  -csv string
        CSV to import
  -format string
        Format to generate - png | pdf | eps | svg (default "png")
  -key string
        API key (required for calls to Bitly)
  -output string
        Output directory
  -overwrite
        Overwrite file if already exists (default true)
  -qr-codes
        Generate qr code images (default true)
  -qr-only
        Generate only qr codes with no calls to Bitly (default true)
```