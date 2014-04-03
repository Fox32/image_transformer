image_transformer
=================

A Pub tranformer for converting between image formats. Sometimes you need to
convert the image files of your applications to different formats. If your
designers hand their assets as ```PSD``` files, you need to convert them first
to browser supported format. This packages provides a pub transformer to convert
between different image formats.

This package don't require any additional tools for image conversion due to the
great work of Brendan Duncan and his [```image```](https://github.com/brendan-duncan/image) 
package.

### Configuration

The next step is configurating the transformer for your package. Add it to the 
```dependencies``` and ```transformers``` sections of your ```pubspec.yaml``` 
and add the desired options. The following example converts ```psd``` files to 
```png``` :

```
transformers:
   - image_transformer:
       input_extensions: '.psd'
       output_extension: '.png'
```

You can add multiple instances of the transformer to your ```pubspec.yaml``` if 
you need the files in different output formats.

#### Supported formats

I try to keep track with the formats supported by the ```image``` package. At
the moment the following formats are supported for both input and output formats:

- PNG
- JPG
- TGA
- GIF

Input only:

- WebP
- TIFF
- PSD

#### input_extensions

A input extension or a list of input extensions that should be processed.

#### output_extension

The extension of the format to output.

### License

```
The MIT License (MIT)

Copyright (c) 2014 Oliver Sand

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
