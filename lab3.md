
# grep -i -r [https://chat.openai.com/]()

```
[cs15lsp23km@ieng6-201]:technical:90$ grep -i -r "BIG " 911report/
911report/chapter-1.txt:    Manager, New York Center: We have several situations going on here. It's escalating big, big time. We need to get the military involved with us. . . . We're, we're involved with something else, we have other aircraft that may have a similar situation going on here.
911report/chapter-11.txt:                dealing with the al Qida threat? . . . Is al Qida a big deal?" One school of     
911report/chapter-13.4.txt:                is not Serbo-Croatian for "big bang," as has been widely reported, but rather a
911report/chapter-3.txt:                often missed the big questions-as did the executive branch. Staff tended as well to
911report/chapter-6.txt:                whom he identified as the big instructor (probably a reference to Bin Ladin)      
911report/chapter-6.txt:                needed to have a big part for Pashtun opponents of theTaliban. They also thought the
911report/chapter-6.txt:                the ban on assassinations in Executive Order 12333. The big issues-who would pay for
911report/chapter-6.txt:                . Is al Qida a big deal? . . . Decision makers should imagine themselves on a future
911report/chapter-6.txt:                the big attack, with lots of casualties, after which some major US retaliation will
911report/chapter-7.txt:            Ali reportedly assumed the operatives he was helping were involved in a big operation 
911report/chapter-7.txt:                that others in Abdullah's circle may have received word that something big would  
911report/chapter-8.txt:                very, very" big was about to happen, and most of Bin Ladin's network was reportedly
```
- In this first command I use `grep` and the options `-i` (non case sensitive) and `-r` (search recursively through a directory and subdirectories) to find every line containing "BIG " without case sensitivity in the txt files from the 911report directory and print them alongside the name of the file it is from.
```
[cs15lsp23km@ieng6-201]:technical:92$ grep -i -r "ALONE " 911report/
911report/chapter-13.3.txt:            4. On the process of identification, see Joseph Malone interview (May 25, 2004).   
911report/chapter-13.4.txt:                continue at its current pace, let alone increase the operational tempo. On Tenet
911report/chapter-13.5.txt:                however, Binalshibh has mentioned only one meeting and has claimed he alone met with
911report/chapter-13.5.txt:                on the lookout) combined with a media campaign. This alone might have delayed or
911report/chapter-13.5.txt:                2004). The CIA's formal analysis of what would happen if Bin Ladin alone was removed
911report/chapter-3.txt:                told us that given the recommendation of his chief operations officers, he alone had
911report/chapter-3.txt:                chance each time has made me a bit angry. . . . [T]he DCI finds himself alone at the
911report/chapter-3.txt:                decision Mr. Director,' and implicitly saying that the Agency will hang alone if the
911report/chapter-5.txt:            Certainly KSM was not alone in contemplating new kinds of terrorist operations. A     
911report/chapter-6.txt:                Kuala Lumpur, let alone that their trail had been lost in Bangkok.
911report/chapter-6.txt:            Clarke was not alone in his enthusiasm. He had backing from Cofer Black and Charles   
911report/chapter-6.txt:                    a goal that was judged impractical and too expensive for the CIA alone to     
911report/chapter-7.txt:                suspect criminal behavior, let alone a terrorist plot to commit mass murder.      
911report/chapter-7.txt:            On July 30, Shehri traveled alone from Fort Lauderdale to Boston. He flew to San      
911report/chapter-7.txt:                and give regards to KSM. Jarrah alone appears to have left a written farewell-a 
```
- In this second command I use `grep` and the options `-i` (non case sensitive) and `-r` (search recursively through a directory and subdirectories) to find every line containing "ALONE " without case sensitivity in the txt files from the 911report directory and print them alongside the name of the file it is from.

# grep -l -r [https://chat.openai.com/]()
```
[cs15lsp23km@ieng6-201]:technical:104$ grep -l -r "big " 911report/
911report/chapter-1.txt
911report/chapter-11.txt
911report/chapter-13.4.txt
911report/chapter-3.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-8.txt
```
- This third command is similar in how it searches recursively through the 911report directory for "big ", but this time it is case sensitive (because of the absence of `-i`) and it only prints the file names of files that contain "big " (-l denotes that the search returns files with matches)

```
[cs15lsp23km@ieng6-201]:technical:105$ grep -l -r "alone " 911report/
911report/chapter-13.3.txt
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-3.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
```
- This fourth command is also similar in how it searches recursively through the 911report directory for "alone ", but this time it's case sensitive and it prints the file names of files that contain "alone " 

# grep -wr [https://chat.openai.com/]()
```
[cs15lsp23km@ieng6-201]:technical:94$ grep -wr "super" plos/
plos/journal.pbio.0030127.txt:        aggregate in super-swarms that can reach a density of 30,000 individuals per square meter,
```
- In this case the `-wr` is specifying that the the search be both recursive over the directory (plos/) and that there must be a matching word in a line rather than just a search for lines with the string within it. Like the first two commands it returns the applicable lines (with the word "super") and the file name.

```
[cs15lsp23km@ieng6-201]:technical:95$ grep -wr "super" 911report/
911report/chapter-11.txt:                dealing with 'catastrophic,''grand,' or 'super' terrorism, when in fact these labels
```
- Also in this case the `-wr` is specifying that the the search be both recursive over the directory (911report/) and that there must be a matching word in a line rather than just a search for lines with the string within it. Like the first two commands it returns the applicable lines (with the word "super") and the file name.

# grep -v [https://chat.openai.com/]()
```
[cs15lsp23km@ieng6-201]:biomed:123$ grep -v "a" rr166.txt




        Introduction
        the fibrotic process [ 2 ] .
        properties
        (TX)A



          to 8.


          2 , 6-keto-PGF
          2 , PGF
          2α , TXB
          vol/vol) for 6-keto-PGF
          2 . Then PGF
          2 , PGE
          ions m/z 569/573 for PGF
          2α , m/z 614/618 for TXB


          1% Tween 20, 10 mM phenylmethylsulphonyl fluoride,


          overnight.





        Results

          ng/10 6cells/30 min, respectively;

          2 ), PGF
          except TXB
          0.61 [0.21-1.64] ng/10 6cells/30 min with IL-1β
          (results not shown).
          HF-NL (0.61 [0.21-1.64] ng/10 6cells/30 min;
          different between the two cell groups (1.73 [0.77-2.53]
          versus 0.75 [0.15-2.58] ng/10 6cells/30 min, in HF-IPF
          1α :TXB
          P = 0.09 [Fig. 2]).


          4).



        Discussion
        2 , TXB
        2 to TXA
        2 :TXA
        [ 13 14 15 16 17 26 ] . TXA
        smooth muscle cells TXA
        c-fos ,
        14 ] .
        of PGI
        fibrogenesis.
        2 to TXA
        in vivo .

        5 6 7 8 ] .
        PGE
        2 production, but they further showed
        2 production in response to TGFβ
        Wilborn
        lungs of subjects with IPF.


        Conclusion
        2 :TXA
        of IPF.





```
- For this command `-v` is specifying that the search it is looking for a simple non case sensitive match for "a" in the lines of rr166.txt. This is a different command compared to the first two because it is not searching recursively through a whole directory, but just one file, and it prints the lines _without_ the match.

```
[cs15lsp23km@ieng6-201]:biomed:124$ grep -v " " rr166.txt

```
- This is another use of `-v` to search the same file for lines absent of " ". Because there is only one line without a space it prints that one line.

## Chat-GPT citation:
- I asked Chat-GPT "command line options for grep"

- It responded with: 
---
The grep command provides several command line options that allow you to modify its behavior and customize the output. Here are some commonly used options for the grep command:

-i or --ignore-case: Ignores case distinctions in both the pattern and the input files. With this option, grep will match patterns regardless of whether they are in uppercase or lowercase.

-r or --recursive: Searches for the pattern recursively in directories and their subdirectories. This option is useful when you want to search for a pattern in multiple files within a directory tree.

-l or --files-with-matches: Only displays the names of files that contain the pattern but does not print the matching lines. This option is handy when you want to identify files that contain a specific pattern.

-v or --invert-match: Inverts the matching logic. Instead of displaying lines that match the pattern, grep will display lines that do not match the pattern. This is useful when you want to exclude certain lines from the output.

-n or --line-number: Prefixes each line of output with the line number within its input file. This option is helpful when you want to know the line numbers of matching lines.

-w or --word-regexp: Matches only whole words that match the pattern. It ensures that the pattern is not part of a larger word.

---
- I used this response to guide the commands I used for grep in the lab report. Chat GPT was only used to explain what the commands do, but I did all the commands by myself in VSCODE referencing the files that were given.
