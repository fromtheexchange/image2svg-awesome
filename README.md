[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

# Awesome PNG to SVG

PNG to SVG is all about image tracing and vectorization—the conversion of a raster image (jpg/png) to a vector image (svg).

## Apps

If you are overwhelmed by the variety of options, the general consensus is:

- Vector Magic is the gold standard at $300
- Potrace is the open source champ for monochrome images
- Inkscape is the best free app option for color images (built on potrace)
- Mac apps like Super Vectorizer are a decent value for money at $40
- Getting an Adobe Illustrator subscription solely for image tracing is hard to justify financially at $240/yr

For best results with low resolution images, preprocess them with [an](https://www.stickermule.com/) [AI](https://icons8.com/upscaler) [image](https://topazlabs.com/gigapixel-ai/) [upscaler](https://www.npmjs.com/package/upscaler), and then vectorize them.

Many of the apps listed below do not include command line versions, and are impractical to host online. However, they are script-able with apps like [Keyboard Maestro](https://www.keyboardmaestro.com/main/) and [AutoHotkey](https://www.autohotkey.com/).

To host your own converter online, check out the open source specifications and code examples below.

### Paid options

- [Adobe Illustrator](https://helpx.adobe.com/illustrator/using/image-trace.html)
  - $20.99/mo for Mac/Win
- [Clip Studio](https://support.clip-studio.com/en-us/faq/articles/20200051)
  - $50 for Mac/Win
- [CorelDRAW Graphics Suite 2020](https://www.coreldraw.com/en/tips/design/art/vectorize-an-image/)
  - $500 license for Mac/Win
  - $20.75/mo for Mac/Win
- [DMesh Pro](http://dmesh.thedofl.com/)
  - $10 for Mac
  - Light version available
- [EZImageVectorizer](https://blacknook.github.io/BlackNook/Page_EZImageVectorizer.html)
  - $10 for Mac
- [Graphic Powers](https://www.graphicpowers.com/)
  - $595 lifetime for Win
  - $15/mo for Win
- [Gravit Designer](https://www.designer.io/en/learn/how-to-vectorize-an-image/)
  - $100/yr for Mac/Win/Lnx/Web
  - Lite version available
- [Image Vectorizer](http://image-vectorizer.com/)
  - $5 for Mac
- [ImageQuantization](https://blacknook.github.io/BlackNook/Page_ImageQuantization.html)
  - $5 for Mac
- [iVinci](http://phyar.cn/)
  - $20 for Mac
- [PhotoLine](https://www.pl32.com/tutorial/vector/vector.htm)
  - €59 for Mac/Win
- [Super Vectorizer](http://www.svgvector.com/vectorize-image-mac.html)
  - $40 for Mac
- [TracedLines](https://apps.apple.com/us/app/tracedlines/id1421960922)
  - $10 for Mac
- [Vector Magic](https://vectormagic.com/)
  - $300 license for Mac/Win/Web
  - $10/mo
- [Vector Queue](http://vectorqueue.com/)
  - $6 for Mac
- [Vectorize](https://www.syniumsoftware.com/vectorize)
  - $9 for Mac
- [vectorizer](https://www.vectorizer.io/)
  - $5/mo for Web
- [VectorStyler](https://www.vectorstyler.com/documentation/exporting/tracing/)
  - $100/yr for Mac/Win

### Free alternatives

- [Adobe Capture: Creative Kit](https://apps.apple.com/us/app/adobe-capture-creative-kit/id1040200189)
  - Free for iOS/iPad
- [Autotrace](https://github.com/autotrace/autotrace)
  - Free for Mac/Win/Lnx
- [autotracer.org](https://www.autotracer.org/)
  - Free for Web
- [Drag Potrace](http://www.hi-ho.ne.jp/sato-akira/dragpotrace/)
  - Free for Mac
- [fconvert](https://fconvert.com/autotrace/)
  - Free for Web
- [Geometrize](https://www.geometrize.co.uk/)
  - Free for Mac/Win/Lnx
- [imagetracerjs](https://github.com/jankovicsandras/imagetracerjs)
  - Free for Mac/Win/Lnx
- [Inkscape](https://inkscape.org/)
  - Free for Mac/Win/Lnx
- [Intaglio Vectorize](https://web.archive.org/web/20180819005858/http://www.purgatorydesign.com/Vectorize/index.html)
  - Free for Mac
- [KVEC](https://www.kvec.de/english/)
  - Free for Mac/Win/Lnx
- [Online vectorizer](https://online-converting.com/autotrace/)
  - Free for Web
- [opentoonz](https://opentoonz.github.io/e/)
  - Free for Win
- [Photopea](https://www.photopea.com/tuts/vectorize-raster-images/)
  - Free for Web
- [primitive.lol](https://primitive.lol/)
  - Free for Mac
- [RapidResizer](https://online.rapidresizer.com/tracer.php)
  - Free for Web
- [Vectorization.org](https://www.vectorization.org/)
  - Free for Web
- [Vectornator](https://www.vectornator.io/learn/images)
  - Free for Mac/iOS/iPad

I’m always looking for [more](https://en.wikipedia.org/wiki/Comparison_of_raster-to-vector_conversion_software) [alternative](https://alternativeto.net/software/potrace/) vectorization software! Create a GitHub issue and I’ll add it to the list.

## Specification for NodeJS

The original goal of this document was to outline a specification for NodeJS serverless functions to convert raster images to SVG, and link to other repositories for implementations.

As such, the rest of the document serves as a simple specification for how requests and responses should be structured to convert between raster images and SVG. Check out the related repositories for implementations of the specification.

### Related repositories

- [image2svg-awesome](https://github.com/fromtheexchange/image2svg-awesome)
- [image2svg-client](https://github.com/fromtheexchange/image2svg-client)
- [image2svg-imagetracerjs](https://github.com/fromtheexchange/image2svg-imagetracerjs)
- [image2svg-potrace](https://github.com/fromtheexchange/image2svg-potrace)
- [image2svg-primitive](https://github.com/fromtheexchange/image2svg-primitive)
- [image2svg-kvec](https://github.com/fromtheexchange/image2svg-kvec)

### Matrix

Image Tracing

- [imagetracerjs](https://github.com/jankovicsandras/imagetracerjs) (✅ The Unlicense)
- [primitive](https://www.npmjs.com/package/primitive) (✅ MIT)
- [kvec](https://www.kvec.de/english/) (Freeware)
- [potrace](https://www.npmjs.com/package/potrace) (⚠️ GPLv2)

Serverless

- [Vercel](https://vercel.com/docs/serverless-functions/introduction)
- [Claudia.js](https://claudiajs.com/)

### Request

```jsx
function ImageInput() {
  const [files, setFiles] = React.useState<File[]>();

  const onSubmit = (event) => {
    event.preventDefault();
    if (!files?.length) return;

    async function getSvg() {
      try {
        const formData = new FormData();
        files.forEach((file, index) =>
          formData.append(`image-${index}`, file, file.name)
        );

        const response = await axios.post(url, formData, {
          headers: {
            "Content-Type": "multipart/form-data",
          },
        });
      } catch (error) {
        console.log(error)
      }
    }

    getSvg();
  };

  return (
    <form onSubmit={onSubmit}>
      <input
        id="file"
        name="file"
        type="file"
        multiple
        required
        accept="image/jpeg, image/png, image/webp, image/gif, image/svg+xml, image/heic"
        onChange={(event) => {
          const files = Array.from(event.target.files);
          if (files?.length) {
            setFiles(files);
          }
        }}
      />
    </form>
  );
}
```

### Response

```json
{
  "algorithm": "imagetracerjs",
  "files": [
    {
      "fieldName": "image-1",
      "originalName": "demo-one.png",
      "svg": "<svg>…</svg>"
    },
    {
      "fieldName": "image-2",
      "originalName": "demo-two.jpg",
      "svg": "<svg>…</svg>"
    }
  ]
}
```

### Future plans

To support the continued development of this project, consider donating.

<a href="https://www.buymeacoffee.com/fromtheexchange"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a coffee&emoji=&slug=fromtheexchange&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff"></a>

- ~Add support for color images~
- Plugins for Sketch, Figma, and Adobe XD
- Compare the results of all the apps over a set of images

<!-- - Consider [sqip](https://github.com/axe312ger/sqip/issues/6) -->

### WONTFIX

Contributions welcome.

- [inkscape](https://alpha.inkscape.org/vectors/www.inkscapeforum.com/viewtopic4d78.html?t=11898)
  - Uses potrace under the hood
- [autotrace](https://github.com/autotrace/autotrace)
  - Complex build process with web of dependencies
