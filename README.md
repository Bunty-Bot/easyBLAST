# EzBlast

Repository for the code of the software application: EzBlast. 
EzBlast was developed for the course Software Engineering (INF32306) of Wageningen University.

Briefly, EzBlast is a bioinformatic application that can perform BLASTN and BLASTP searches to identify nucleotide 
and protein sequences that are similar to the query sequence. Moreover, the programme can compute basic statistics
of nucleotide and protein sequences. EzBLAST provides a more user-friendly tool compared to the [NCBI BLAST webpages]
(https://blast.ncbi.nlm.nih.gov/Blast.cgi).

The Class MainGui allows the user to navigate to and use all functionalities of the EzBLAST application.

For further clarification of what the program does and how to run it, please read the system description in the UserStories_21042026_final.docx

**The functionality of running BLASTP and BLASTN with a custom database only works on windows.**
**The SSEARCH36 programme was not available for Mac and Linux.**

**If the BLASTP and BLASTN tools with the default database do not work, the UniProt SwissProt API may be under maintenance.**

* To perform BLASTP: press the BLASTP button.
* To perform BLASTN: press the BLASTN button.
* To calculate the statistics: press the File statistics button.
* To view the output of old BLASTP or BLASTN files: press the Upload .tsv file button. 
* Each section has a help button that explains how to use the tool.

## Repository overview
The repository contains six folders:
* `src/` - Contains all the Java scripts of the application.
* `tools/` - Contains the ssearch36 tool, which is an alternative to BLAST using a custom database.
* `referenced_libraries/` - Contains all JAR files needed to run the UniProt SwissProt BLAST from class BlastpSearch.
* `project_data/` - Contains FASTA files used in some of the test classes.
* `example_fasta_files/` - Contains FASTA files which can be used as input into the tools of the program for testing. 
* `documentation/` - Contains use case diagrams, user stories, class diagrams, sequence diagrams and acceptance tests.
* `.settings/` - Configuration files for Eclipse.

Where `src/` contains:
* `/gui/` - Contains all GUI classes.
* `/tests/` - Contains all test classes.
* `/utilities/` - Contains all utility classes.

**Note**: The gui and utility classes have Javadoc annotation regarding their functionality.

And `documentation/` contains:
* `/Class diagram/` - Contains all class diagrams made during the project.
* `/Sequence diagram/` - Contains all sequence diagrams made during the project.
* `/Use case diagram/` - Contains all use case diagrams, user stories, use case descriptions, and acceptance test.

And `example_fasta_files/` contains:
* `single_dna_query_for_statistics.fasta` - single dna query, use for checking File Statistics
* `multiple_dna_query.fasta` - multiple dna queries, use to run BLASTN (Upload Input Sequence in BLASTN)
* `dna_database.fasta` - database of dna sequences (Upload Database in BLASTN)
* `single_protein_query_for_statistics.fasta` - single protein query, use for checking File Statistics 
* `multiple_protein_query.fasta` - multiple protein queries, use to run BLASTP (Upload Input Sequence in BLASTP)
* `protein_database.fasta` - database of protein sequences (Upload Database in BLASTP)


Where `/Use case diagram/` contains:
* `useCase_acceptanceTests/` - Contains all acceptance tests of the user stories. 
* `useCase_descriptions/` - Contains all use case descriptions.
* `useCase_diagrams/` - Contains all use case diagrams.
* `useCase_progressPoints/` - Contains tasks in MOSCOW style for each iteration.
* `useCase_userStories/` -  Contains all user stories.

## Requirements
* [JDK](https://jdk.java.net/21/) - Used version: 21.

## Usage
1. Clone this GIT repository.
2. Open the repository in a Java compatible IDE.
3. Run class MainGui in the gui package in the `src` folder.
4. Navigate from the MainGui to the functionality that you want to use.
5. If you want to use BLASTP, use the `multiple_protein_query.fasta` and  `protein_database.fasta` files from `example_fasta_files/`
6. If you want to use BLASTN, use the `multiple_dna_query.fasta` and `dna_database.fasta` files in `example_fasta_files/`
7. If you want to use File Statistics, either upload the `single_protein_query_for_statistics.fasta` or `single_dna_query_for_statistics.fasta` files.

See the Javadoc of the classes in the gui package, the user stories, and the acceptance tests
for a detailed description about the functionality that the programme offers.

## Support
For questions, reach out to any of the authors:

[chris.ambagtsheer@wur.nl](mailto:chris.ambagtsheer@wur.nl), [loran.wijga@wur.nl](mailto:loran.wijga@wur.nl), 
[milan.vissers@wur.nl](mailto:milan.vissers@wur.nl), [nick.phoonleiyung@wur.nl](mailto:nick.phoonleiyung@wur.nl),
[rick.markus@wur.nl](mailto:rick.markus@wur.nl), [shreyas.bapat@wur.nl](mailto:shreyas.bapat@wur.nl),
[swayam.belokar@wur.nl](mailto:swayam.belokar@wur.nl) or [wouter.driessen@wur.nl](mailto:wouter.driessen@wur.nl). 

## Authors
* Chris Ambagtsheer, Loran Wijga, Milan Vissers, Nick Phoon, Rick Markus, Shreyas Bapat,
Swayam Belokar, Wouter Driessen

## License
This project is licensed under a [MIT license](https://opensource.org/license/mit).
