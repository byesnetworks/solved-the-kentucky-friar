Download Link: https://assignmentchef.com/product/solved-the-kentucky-friar
<br>
Write a program that will drop the final “g” of two-syllable words ending in “-ing” and also replace any occurrence of the word “you” (case-insensitive) with the word “y’all” so as to transform text into a dialect common to the US Deep South (from which your author hails). The given text may come from the command line:

<pre><code>$ ./friar.py 'Do you want to do some cooking with me?'Do y'all want to do some cookin' with me?</code></pre>

Or from an input file:

<pre><code>$ ./friar.py ../inputs/nobody.txtI'm Nobody! Who are y'all?Are y'all -- Nobody -- too?Then there’s a pair of us!Don't tell! they'd advertise -- y'all know!How dreary -- to be -- Somebody!How public -- like a Frog --To tell one's name -- the livelong June --To an admirin' Bog!</code></pre>

Note that one-syllable words ending with “-ing” should be unchanged:

<pre><code>$ ./friar.py swingswing</code></pre>

If provided no arguments, the program should print a brief usage:

<pre><code>$ ./friar.pyusage: friar.py [-h] strfriar.py: error: the following arguments are required: str</code></pre>

Or a longer usage for <code>-h</code> and <code>--help</code>:

<pre><code>$ ./friar.py -husage: friar.py [-h] strSouthern fry textpositional arguments:  str         Input text or fileoptional arguments:  -h, --help  show this help message and exit</code></pre>

Run the test suite to ensure your program works correctly:

<pre><code>$ make testpytest -xv test.py============================= test session starts ==============================...collected 10 itemstest.py::test_exists PASSED                                              [ 10%]test.py::test_usage PASSED                                               [ 20%]test.py::test_two_syllable_ing_words PASSED                              [ 30%]test.py::test_one_syllable_ing_words PASSED                              [ 40%]test.py::test_you_yall PASSED                                            [ 50%]test.py::test_blake PASSED                                               [ 60%]test.py::test_banner PASSED                                              [ 70%]test.py::test_raven PASSED                                               [ 80%]test.py::test_dickinson PASSED                                           [ 90%]test.py::test_shakespeare PASSED                                         [100%]============================== 10 passed in 0.73s ==============================</code></pre>