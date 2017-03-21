// USAGE:

The Array 2 blob class can store and retrieve arrays in textual format with optional compression with the zlib PHP extension.
The class just converts array data into PHP code that would rebuild the array when run. Then it can compress the generated code so it can take less space to store for instance in a database BLOB field.


require_once('arrayToblob.php');
$array_storage = new arrayToblob();

$compress = 1; (0 or 1)
$array_text = $array_storage->Array2Txt($array,$compress);

$decompress = 1; (0 or 1)
$array = $array_storage->Txt2Array($array_text,$decompress);
