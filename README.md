# qprintereasy

Informations

    Until no documentation is available please refer to the main.cpp for a correct usage of this lib.

// Code preparation QTextDocument header, footer, document; header.setHtml( ..... ); footer.setHtml( ..... ); document.setHtml( ..... );
Samples

    One header, one footer on each pages

    You can add one header and one footer to each pages of your document. This is what you can get with a few lines of code.

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header ); pe.setFooter( footer ); pe.setContent( document ); pe.previewDialog();

    One header on first page only, one footer on each pages

    You can add one header into the first page only, one footer to all pages. This is what you can get with a few lines of code.

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header, QPrinterEasy::FirstPageOnly ); pe.setFooter( footer ); pe.setContent( document ); pe.previewDialog();

    One header on first page only, one footer on the second page only

    You can add one header into the first page only, one footer on the second page only. This is what you can get with a few lines of code.

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header, QPrinterEasy::FirstPageOnly ); pe.setFooter( footer, QPrinterEasy::SecondPageOnly ); pe.setContent( document ); pe.previewDialog();

    Header and footer with centered plain text Watermark

    You can add centered plain text watermark on EachPages. This is what you can get with a few lines of code.

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header ); pe.setFooter( footer ); pe.setContent( document ); pe.addWatermarkText( "Adding a plain text\nWATERMARK" ); pe.previewDialog();

    Header and footer with centered plain text Watermark on Even Pages

    You can add centered plain text watermark on EventPages. This is what you can get with a few lines of code.

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header ); pe.setFooter( footer ); pe.setContent( document ); pe.addWatermarkText( "Adding a plain text\nWATERMARK", QPrinterEasy::EventPages ); pe.previewDialog();

    Header and footer with a pixmap watermark on EachPages

    Here is the watermark pixmap
    Here is the result

``` // Code looks like this QPixmap pixWatermark; pixWatermark.load( dir.filePath("pixmapWatermark.png") );

QPrinterEasy pe;
pe.askForPrinter();
pe.setHeader( header );
pe.setFooter( footer );
pe.setContent( document );
pe.addWatermarkPixmap( pixWatermark, QPrinterEasy::EachPages );
pe.previewDialog();

```

    MultiHeaders, one footer, watermark on EvenPages

    sample

// Code looks like this QPrinterEasy pe; pe.askForPrinter(); pe.setHeader( header, QPrinterEasy::FirstPageOnly ); pe.setHeader( header2, QPrinterEasy::EachPages ); pe.setContent( document ); pe.addWatermarkText( "Adding a plain text\nWATERMARK", QPrinterEasy::EventPages ); pe.previewDialog(); 
