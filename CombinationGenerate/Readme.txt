This class can be used to generate combinations of an array of values.
It takes an array of values and generates all possible combinations of those values including permutation of order of the values.
The class can be configured to only get unique combinations, i.e. identical combinations of values are not generated.

<?php
require_once("CombinationClass.php");
$values = array("a", "b");
$combinations1 = new CombinationClass($values, false);
$combinations = $combinations1->getCombinations();

foreach ($combinations as $comb)
{
    for ($i=0; $i<count($comb); $i++)
    {
        echo $comb[$i]." ";
    }
    echo "<br>";
}
?>
