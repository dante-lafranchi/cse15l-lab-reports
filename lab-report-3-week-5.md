# Researching Options for the Grep Command
## Option #1: --ignore-case
By default, grep is case-sensitive which means that grep pays attention to the difference between capital and lowercase letters when searching a file for a certain string. However, the "--ignore-case" option for grep makes it so that grep isn't case sensitive and prints every line that has the particular string, regardless of if that string has the exact same capital and lowercase letters in the file as it does in the command. The "--ignore-case" option is useful because more often than not, you probably want to know all the lines that contain the particular string, and you might miss out on vital information if you just see the lines that contain the all lowercase version of the string.

The following example shows how the "--ignore-case" option makes grep print all lines that have any letter case (capital and lowercase) variation of "west", so lines that contain "West" are printed too.
```
grep "west" technical/911report/chapter-3.txt --ignore-case

was focused on the formidable challenges posed by illegal entry over the southwest
terrorists, and rescued all but one of the hostages. In October 1977, a West German
security. Committees with responsibility for the INS focused on the Southwest
contact with the West, since he refused to meet with non- Muslims. The United States
concentrated in the southern part of the country, extending into the North-West
Center rated the chance of success at less than 10 percent. To the northwest, the
```
The following example shows how the "--ignore-case" option makes grep print all lines that have any letter case variation of "early", so lines that contain "Early" are printed too.
```
grep "early" technical/biomed/1471-213X-1-1.txt --ignore-case

Early in CNS development, GABA can modulate neuron 
pathway to be involved in the early development of
early phase of
```
The following example shows how the "--ignore-case" option makes grep print all lines that have any letter case variation of "clearly", so lines that contain "Clearly" are printed too.
```
grep "clearly" technical/plos/journal.pbio.0020019.txt --ignore-case

environmental variation (Waddington 1942). Clearly, such a mechanism would have important
‘knockout’ mutations were clearly beneficial because they sped up adaptation to a new
```

## Option #2: --before-context
The "--before-context" option for grep requires a number which represents the number of lines before each string match that should be printed. The lines leading up to the string match can be viewed as context for the line that contains the string match. The "--before-context" option is useful because it's always important to have context of what happened before an event (the event in this case being the line that contains the string).

The following example shows how the "--before-context" option makes grep print the 4 lines before the line that contains "seized". Without this option, you would be wondering what the documents seized by the German authorities contained.
```
grep "seized" technical/911report/chapter-5.txt --before-context 4

Binalshibh at 54 Marienstrasse for eight months between November 1998 and July
1999. Described as an insecure follower with no personality and with limited
knowledge of Islam, Bahaji nonetheless professed his readiness to engage in
violence. Atta and Binalshibh used Bahaji's computer for Internet research, as
evidenced by documents and diskettes seized by German authorities after
```
The following example shows how the "--before-context" option makes grep print the 4 lines before the line that contains "relationships". Without this option, you would be confused why firms and citizens would redefine their relationships with the government.
```
grep "relationships" technical/911report/chapter-12.txt --before-context 4

This pattern has occurred before in American history. The United States faces a
sudden crisis and summons a tremendous exertion of national energy. Then, as that
surge transforms the landscape, comes a time for reflection and reevaluation. Some
programs and even agencies are discarded; others are invented or redesigned. Private
firms and engaged citizens redefine their relationships with government, working
```
The following example shows how the "--before-context" option makes grep print the 5 lines before the line that contains "laws". Without this option, you would ponder what laws and regulations are being referred to (as there are quite a few out there).
```
grep "laws" technical/government/Gen_Account_Office/ai2132.txt --before-context 5

Systems standards are important for agencies streamlining
operations by redesigning or modifying systems to take advantage of
technological advances. The standards provide the criteria to help
ensure that the systems include effective internal control and meet
the requirements imposed for central reporting and complying with
laws and regulations.
```
## Option #3: --line-number
The "--line-number" option for grep prints the line in the file that contains the string match, along with the line number in the file. This option has very intuitive formatting. The "--line-number" option is useful because you might want to know when a file starts talking about a certain event (the string). You might also want to know how spread out mentions of the string are which can give you an idea of how much of the content in a file revolves around a certain topic.

The following example shows how the "--line-number" option prints the line number of each line that contains "business" in the file, and then prints the actual contents of each line that contains "business". 
```
grep "business" technical/911report/chapter-2.txt --line-number

393:                would let Bin Ladin use Sudan as a base for worldwide business operations and for
410:                business and terrorist enterprises. In time, the former would encompass numerous
414:                finance officers and top operatives used their positions in Bin Ladin's businesses
423:                for terrorist activities. The network included a major business enterprise in
544:                His business aides received word that a Sudanese military officer who had been a
630:                normal costs of doing business increased. Saudi pressures on the Bin Ladin family
638:                taken the oath of fealty to Bin Ladin, serving as one of his business agents. Then
710:                business enterprises he had set up there and then put some of them up for public
```
The following example shows how the "--line-number" option prints the line number of each line that contains "Paris" in the file, and then prints the actual contents of each line that contains "Paris". 
```
grep "Paris" technical/911report/chapter-11.txt --line-number

241:                over Paris, but possibly to crash it into the Eiffel Tower.
```
The following example shows how the "--line-number" option prints the line number of each line that contains "engulfed" in the file, and then prints the actual contents of each line that contains "engulfed". 
```
grep "engulfed" technical/911report/chapter-9.txt --line-number

284:                roof of the North Tower. The roof of the South Tower was also engulfed in smoke
544:                because"it is too engulfed in flames and heavy smoke condition."
```