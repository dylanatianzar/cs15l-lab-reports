# Lab 3 Report Dylan Atianzar A17609722
## Grep Terminal Command
## -r alterator
The command: `grep -r "microscope" D:/Documents/GitHub/docsearch/written_2/`
The output:
```
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:The technology center at newMetropolis is for the child in all of us. Experiments with energy, looking at cells in the human body through a **microscope**, or playing some virtual reality games will inspire every visitor whatever their age.
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-History.txt:Rich merchants needed banks and a support infrastructure, which developed quickly in the city. People flooded in to take advantage of the new commercial opportunities, the population rose rapidly and the old medieval city simply could not cope. It was still very much within the boundaries set almost 150 years before. Plans were made for a series of new canals forming in a ring or girdle around the old medieval horseshoe — three in all, Herengracht, Keizersgracht, and Prinsengracht. The canal side lots were sold to the wealthy of the 
city who built the finest houses they could afford. The confidence of the city brought opportunities for the arts and the burgeoning sciences. The artists Rembrandt, Frans Hals, Vermeer, and Paulus Potter were all working in this era, their work much in demand by the merchant classes. At the same time the Guild of Surgeons was learning about the physiology of the body at their meeting place in the Waag, helped by Antonie van Leeuwenhoek who had invented the **microscope**.
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:The technology center at newMetropolis is for the child in all of us. Experiments with energy, looking at cells in the human body through a **microscope**, or playing some virtual reality games will inspire every visitor whatever their age.
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:Next to the museum, and unmistakable by its modern shape and huge green outer walls, is the newMetropolis science and technology center. Opened in 1997, the center was created to bring the latest science and technology literally into the hands of the lay person, whatever their age. Even the location of the building is a technological marvel. It sits high above the entrance to the IJ tunnel, which takes six lanes of traffic under the IJ waterway to Amsterdam’s northern suburbs and north Holland beyond. Inside the center you can try 
your hand at playing the stock exchange by computer, change the wheel on a car, or look at the cells of the body through a **microscope**. There are hands-on experiments for everyone from young children to adults, focusing on five linked themes — Energy, Humanity, Interactivity, Science, and Technology.
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:You could spend a whole day in the Museum of Science complex that straddles the Charles River, playing and learning on the 400-plus interactive exhibits. Some of these, such as those on mathematics and biotechnology would stimulate an MIT graduate, while many others appeal to young children. Highlights include: the electron **microscope** that magnifies objects 25,000 times; a variety of dinosaur models and fossils; games that show how the human body works; stimulating games for learning about energy; and a rain forest re-creation. The demonstrations are thrilling too. Try to catch the world’s biggest Van de Graaff generator going through its paces at the Theater of Electricity. In late 1999 The Museum of Science announced that it was merging with the old Computer Museum and so the museum now has a couple of interactive computer-oriented exhibits.
```
The command: `grep -r "gold"  D:/Documents/GitHub/docsearch/written_2/non-fiction/OUP/Kauffman`
The output:
```
D:/Documents/GitHub/docsearch/written_2/non-fiction/OUP/Kauffman/ch6.txt:I suspect that this familiar ontological move is not always warranted. Let’s take some cases that Phil Anderson uses to exemplify “emergence.” Gold is a yellow, malleable metal familiar to all of us. Nowhere in the quantum mechanical description of atomic **gold** are these macroscopic properties to be found. Moreover, there is no deductive way to arrive at these macroscopic collective properties from the underlying quantum mechanics of atoms of gold. Rather, we observe the macroscopic 
properties, find lawful features of those properties, then attempt to link them 
to suYcient conditions in our quantum mechanical description of matter.
```
The `-r` alterator allows the `grep` command to search for a given string within a directory and its subdirectories. The ability to search for a string in multiple files and folders rather than just one file is the reason why `-r` is so useful. I found this command from ChatGPT.

## -l alterator
The input: `grep -r -l "microscope" D:/Documents/GitHub/docsearch/written_2/"
The output:
```
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-History.txt
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt
D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Boston-WhereToGo.txt
```
The input: `grep -r -l "gold"  D:/Documents/GitHub/docsearch/written_2/non-fiction/OUP/Kauffman`
The output:
`D:/Documents/GitHub/docsearch/written_2/non-fiction/OUP/Kauffman/ch6.txt`

Using the same command as the `-r` examples but adding the `-l` alterator returns just the file names of where the string was found. This is useful when paired with `-r` so that if multiple files have the same string, the terminal doesn't become full of just text and makes it easier to just see the file names of where the string is. I found this command from ChatGPT.

## -C alterator 
The input: `grep -C 1 "microscope" D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt`
The output: 
```
At the Artis complex there is the chance to explore the aquarium, zoo, and planetarium. If looking at the solar system doesn’t excite your child then getting close to tigers and elephants might.
The technology center at newMetropolis is for the child in all of us. Experiments with energy, looking at cells in the human body through a **microscope**, or playing some virtual reality games will inspire every visitor whatever their age.    
The recreation of the Dutch trading ship at the Scheepvaart Museum with its staff playing the part of sailors, brings out the sense of adventure in children.
```
The input: `grep -C 3 "microscope" D:/Documents/GitHub/docsearch/written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt`
The output:
```
Tram rides — although this is the normal method which most Amsterdammers use to 
get to and from work, it is an unusual transportation method for most of the rest of us. Children will love the new adventure.
The wax works of Madame Tussauds will have all the latest stars of music and films, so they can try and guess who the figures are before reading the exhibit details.
At the Artis complex there is the chance to explore the aquarium, zoo, and planetarium. If looking at the solar system doesn’t excite your child then getting close to tigers and elephants might.
The technology center at newMetropolis is for the child in all of us. Experiments with energy, looking at cells in the human body through a **microscope**, or playing some virtual reality games will inspire every visitor whatever their age.    
The recreation of the Dutch trading ship at the Scheepvaart Museum with its staff playing the part of sailors, brings out the sense of adventure in children.   
If you visit Amsterdam in early December children will enjoy the parade as Sinterklaas (Santa Claus) makes his visit to the city on 5 December. He parades through the streets on horseback.
Throughout the summer there are activities in the major parks and pleins. Street theater, face painting, and hands-on art shows will keep up their enthusiasm and interest.
```
The `-C` alterator displays a given amount of lines around the line where the string is found meaning the lines both before and after the found one. Using the same example with different modifiers is made to show how increasing/decreasing the number after the argument produces more or less lines. This is useful again for not filling the terminal up and more importantly, providing context to the string that is found. I found this command from (7) from: [Link](https://arkit.co.in/practical-grep-command-tricks/)
## -L alterator
The input: `grep -rL "found" written_2/travel_guides/berlitz2`
The output:
```
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt
```
The input: `grep -rL "place" written_2/travel_guides/berlitz2`
The output:
```
written_2/travel_guides/berlitz2/Barcelona-History.txt
written_2/travel_guides/berlitz2/Budapest-History.txt
written_2/travel_guides/berlitz2/PuertoRico-History.txt
```
The `-L` alterator displays the file names that do not contain the string. This is useful for finding files without a certain string. I found this command from `grep --help`. I use Windows instead of Mac, so that's why I use "--help".
