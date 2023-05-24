# Lab Report 3 - Researching The Grep Command (Week 5)

All of the following commands were found either at the [Geeks for Geeks](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) website or as a result of querying [ChatGPT](https://chat.openai.com/chat) for interesting ways to use the grep command.
## Option 1: -w (whole word)

### Input Command: grep -w "data" biomed/cc103.txt
```bash
grep -w "data" biomed/cc103.txt 
```
In the above line of code, I am using the ```grep -w``` command on the txt file located at ```biomed/cc103.txt```, and in particular I am searching for lines that contain the word "data" in them. 

#### Resulting Output:
     between these individual disorders. Moreover, data drawn
          data exist for these potential treatments. One exception
          considerations, and in the absence of clinical data,
          timing. While no data exist in humans, several lines of
          In practical terms these data from animal studies
          data suggest this intervention would be helpful, there
          are no human data to support the use of diuretics.

### Input Command: grep -w "sepsis" biomed/cc2167.txt
```bash
grep -w "sepsis" biomed/cc2167.txt 
```
In the above line of code, I am using the ```grep -w``` command on the txt file located at ```biomed/cc2167.txt```, and in particular I am searching for lines that contain the word "sepsis" in them. 

#### Resulting Output:
     treatment of adult patients with severe sepsis. Regulatory
        A total of 1821 adult patients with severe sepsis were
        all adult patients with severe sepsis enrolled in clinical
          adult patients with severe sepsis and that were completed
          clinicians treating patients with severe sepsis.
          Severe sepsis was defined in all protocols as the
          sepsis and have been at high risk for death (e.g. as
        estimates for severe sepsis, which ranged between 30% and
        bleeding risk for all patients with severe sepsis. In these
        of severe sepsis with other novel therapeutics that have
        patients with severe sepsis. In a recent large sepsis trial
        diagnosis of severe sepsis and a platelet count of
        severe sepsis population overall may exceed 0.4% [ 12 ] .
        reported in placebo-treated sepsis patients (Opal S,
        use of drotrecogin alfa (activated) reduces sepsis-induced
        international normalized ratio). Risk for sepsis-related
        overall population of severe sepsis patients with no
        end-point of less sepsis-induced death, potentially less
        mortality in severe sepsis. The treatment efficacy and
       
In general, it seems that the ```grep -w``` command is used to search for whole word matches in a given text. When used with the ```-w ```option, grep will only match lines that contain the exact word specified, rather than partial matches within other words as we have seen earlier in prior lectures/labs. The -w option is useful when we want to search for specific words without getting false positives from partial matches that may or may not be present.


## Option 2: -m (maximum)

### Input Command: grep -m 3 "data" biomed/cc103.txt
```bash
grep -m 3 "data" biomed/cc103.txt 
```
In the above line of code, I am using the ```grep -m``` command on the txt file located at ```biomed/cc103.txt```, and in particular I am searching for lines that contain the word "data" in them but I am restricting the responses to a maximum of 3 instances.

#### Resulting Output:
     between these individual disorders. Moreover, data drawn
          A MEDLINE search was conducted using databases from
          data exist for these potential treatments. One exception
        

### Input Command: grep -m 7 "sepsis" biomed/cc2167.txt
```bash
grep -m 7 "sepsis" biomed/cc2167.txt 
```
In the above line of code, I am using the ```grep -m``` command on the txt file located at ```biomed/cc2167.txt```, and in particular I am searching for lines that contain the word "sepsis" in them but I am restricting the responses to a maximum of 7 lines.

#### Resulting Output:
     treatment of adult patients with severe sepsis. Regulatory
        A total of 1821 adult patients with severe sepsis were
        all adult patients with severe sepsis enrolled in clinical
          adult patients with severe sepsis and that were completed
          clinicians treating patients with severe sepsis.
          Severe sepsis was defined in all protocols as the
          sepsis and have been at high risk for death (e.g. as
          
The ```grep -m```command seems to be usually used to restrict the number of matches that grep will return. By utilizing the ```-m``` option, we can set the maximum number of matches to retrieve (example 7 or 3 as shown above), and grep will halt the search for further matches once that limit is attained. This feature is especially beneficial when we are scanning through large files or directories with a large number of files to quickly locate the initial few instances of a given pattern.

 


## Option 3: -c (count)

### Input Command: grep -c "data" biomed/cc103.txt
```bash
grep -c "data" biomed/cc103.txt 
```  
In the above line of code, I am using the ```grep -c``` command on the txt file located at ```biomed/cc103.txt```, and in particular I am finding the number of lines that contain the word "data" in them.

#### Resulting Output:
    8
    
### Input Command: grep -c "sepsis" biomed/cc2167.txt
```bash
grep -c "sepsis" biomed/cc2167.txt 
```  
In the above line of code, I am using the ```grep -c``` command on the txt file located at ```biomed/cc2167.txt```, and in particular I am finding the number of lines that contain the word "sepsis" in them.


#### Resulting Output:
    19
    
In general, the ```grep -c``` command is used to count the number of matches found by grep rather than displaying the actual matching lines as the previous optiond did. It returns a count of the lines that match the specified pattern (e.g 8, 19, etc.). This option is useful when we need to solely determine the total number of occurrences of a pattern in a file or set of files without displaying the matching content itself.


## Option 4: -l (list matching files)

### Input Command: grep -l "atomic" biomed/*.txt
```bash
grep -l "atomic" biomed/*.txt 
```

In the above line of code, I am using the ```grep -l``` command on all .txt files contained in ```biomed/``` , and in particular I am finding all files that contain the word "data" in them.

#### Resulting Output:
     biomed/1471-2091-3-4.txt
     biomed/1471-2105-3-26.txt
     biomed/1471-2121-3-4.txt
     biomed/1471-213X-1-2.txt
     biomed/1471-213X-1-6.txt
     biomed/1471-213X-3-4.txt
     biomed/1471-2156-2-12.txt
     biomed/1471-2164-3-18.txt
     biomed/1471-2180-1-29.txt
     biomed/1471-2180-1-7.txt
     biomed/1471-2202-2-1.txt
     biomed/1471-2202-2-14.txt
     biomed/1471-2202-2-5.txt
     biomed/1471-2202-2-8.txt
     biomed/1471-2202-3-11.txt
     biomed/1471-2202-3-14.txt
     biomed/1471-2202-3-5.txt
     biomed/1471-2202-3-8.txt
     biomed/1471-2202-4-12.txt
     biomed/1471-2202-4-17.txt
     biomed/1471-2202-4-3.txt
     biomed/1471-2288-2-4.txt
     biomed/1471-2334-2-24.txt
     biomed/1471-2407-3-16.txt
     biomed/1471-2474-3-23.txt
     biomed/1472-6769-1-2.txt
     biomed/1472-6793-2-17.txt
     biomed/1472-6807-2-1.txt
     biomed/1472-6807-2-2.txt
     biomed/1472-6807-2-3.txt
     biomed/1472-6807-2-4.txt
     biomed/1472-6807-3-2.txt
     biomed/1472-6882-2-10.txt
     biomed/1472-6882-3-1.txt
     biomed/1472-6890-1-4.txt
     biomed/1472-6963-3-7.txt
     biomed/1475-925X-2-10.txt
     biomed/1476-0711-2-7.txt
     biomed/1477-7819-1-10.txt
     biomed/ar68.txt
     biomed/ar795.txt
     biomed/bcr583.txt
     biomed/cc1044.txt
     biomed/cc2190.txt
     biomed/cc4.txt
     biomed/gb-2001-2-4-research0012.txt
     biomed/gb-2001-3-1-research0001.txt
     biomed/gb-2002-3-12-research0088.txt
     biomed/gb-2002-3-9-research0045.txt
     biomed/gb-2003-4-6-r37.txt


### Input Command: grep -l "sepsis" biomed/*.txt
```bash
grep -l "sepsis" biomed/*.txt 
```
In the above line of code, I am using the ```grep -l``` command on all .txt files contained in ```biomed/``` , and in particular I am finding all files that contain the word "sepsis" in them.

#### Resulting Output:
     biomed/1471-2121-3-11.txt
     biomed/1471-2172-2-10.txt
     biomed/1471-2202-4-17.txt
     biomed/1471-230X-2-23.txt
     biomed/1471-2334-1-13.txt
     biomed/1471-2334-2-26.txt
     biomed/1471-2334-2-5.txt
     biomed/1471-2407-2-12.txt
     biomed/1472-6793-3-3.txt
     biomed/1472-6823-3-1.txt
     biomed/1476-0711-2-3.txt
     biomed/1476-0711-2-7.txt
     biomed/1476-511X-2-2.txt
     biomed/1477-5956-1-1.txt
     biomed/ar778.txt
     biomed/cc103.txt
     biomed/cc1477.txt
     biomed/cc1497.txt
     biomed/cc1498.txt
     biomed/cc1529.txt
     biomed/cc1547.txt
     biomed/cc1843.txt
     biomed/cc2167.txt
     biomed/cc2171.txt
     biomed/cc2358.txt
     biomed/cc300.txt
     biomed/cc303.txt
     biomed/cc343.txt
     biomed/cc350.txt
     biomed/cc367.txt
     biomed/gb-2000-1-1-research002.txt
     biomed/gb-2003-4-4-r24.txt
     biomed/gb-2003-4-5-r32.txt

Based on the above examples, it seems that the -l option in grep lists only the names of files that contain the pattern, rather than showing the matching lines. This would be extremely useful when searching for a pattern in a large number of files, and you only want to see the names of the files that contain the pattern rather than seeing the individual lines where this pattern is detected.





          
