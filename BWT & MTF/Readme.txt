this script implements the BWT & MTF encoder: Compress and decompress data using BWT and MTF
This package can be used to compress and uncompress data using the Burrows-Wheeler transform (BWT) and Move-To-Front (MTF) encoder.
These data processing algorithms are commonly used in compression schemes end Each of these algorithms are implemented in separate classes and do not require any special PHP extensions.


/* Example usage: */

require('bwt.class.php');
require('mtf.class.php');

$original = "Hello World, this is my test message.";

$bwt = new BWT();
$mtf = new MTF();

$encoded = $mtf->encode( $bwt->transform( $original ) );

$decoded = $bwt->inverse( $mtf->decode( $encoded ) );

print $decoded;
