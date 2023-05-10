# Lab Report 3 - Researching The Grep Command (Week 5)

## Option 1: -w (whole word)

### Input Command: grep -w "data" biomed/cc103.txt
```bash
grep -w "data" biomed/cc103.txt 
```

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
       
In general, it seems that the ```grep -w``` command is used to search for whole word matches in a given text. When used with the ```-w ```option, grep will only match lines that contain the exact word specified, rather than partial matches within other words as we have seen earlier in prior lectures/labs.





 
