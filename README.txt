Directory structure:
Main_d
	Hi.docx
	t4_main.txt
	test_1.xlsx
	test_1c.csv
	test_1d.dat
	sub_d1	
		t2test.docx
		t3.txt
		test_1x.xml
		testpdf
	sub_d2
		t1.txt
		t2.txt
		test_2c.csv
	sub_d3
		t4_main.txt
		test_1.xlsx
		test_1c.csv
		test_1d.dat

Assumption:
1. As discussed over email, I have assumed only text files can be given as a parameter. 
2. I have also written a case to handle .xlsx files.
3. The extension will be given as 'xlsx','dat' etc.
4. If the extension is not recognised, the system should output "Incorrect file type"

The code will return all the files matching the directory and the subdirectories and return the respective number of lines.

Unit test cases:
---File input-----
1. If path is not defined:
Output:
Path is required

2. If extension is empty (It should take txt by default):
Output:
-------------
t4_main.txt  6
t3.txt  4
t1.txt  8
t2.txt  5
-----------------------
Number of files found : 4
Total number of lines : 23
Average lines per file : 5.75

----File output-------

1. passing .txt file extension
Output : 
t4_main.txt  6
t3.txt  4
t1.txt  8
t2.txt  5
-----------------------
Number of files found : 4
Total number of lines : 23
Average lines per file : 5.75

2. passing .csv file extension
Output:
test_1c.csv  3
test_2c.csv  1
-----------------------
Number of files found : 2
Total number of lines : 4
Average lines per file : 2.0

3. passing .dat file extension
test_1d.dat  4
-----------------------
Number of files found : 1
Total number of lines : 4
Average lines per file : 4.0 

4. extension="l1"
Output:
No files found for the extension, try changing the extension to a valid one


