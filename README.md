**HTMN'S LOFI PLANET GENERATOR 2.0**


**Overview**

Upon looking at the assignment description I found some of the examples quite inspiring in terms of coming up with ideas for the build. I decided to take the suggestion of "A Procedural planet" a little more literally and decide to create a project that involved an infinite amount of procedural planets. I am very interested in the world of VJing and audio response visuals, and find that when I'm studying and programming I like to have LoFi music on in the background. Normally this kind of music would be accompanied by anime AMV's or still Manga images, but I decided to try use the procedural generation aspect of the project to try and provide a customisable visual for listening to music.
The idea is that the user can select their music of choice from whatever streaming platform or service/database they choose, randomly generate a planet to their liking, and leave the planet to spin and twirl endlessly while their music plays. I think this allows the player to interract with it just enough to feel involved, but also not enough to distract them for their other work at hand.



**A detailed description of what your assignment does and how it works**

The idea is that the user can select their music of choice from whatever streaming platform or service/database they choose, randomly generate a planet to their liking, and leave the planet to spin and twirl endlessly while their music plays. I think this allows the player to interract with it just enough to feel involved, but also not enough to distract them for their other work at hand.
The basic concept is that the world is made of a series of interlocking triangles/polygons. These shapes recognise what is next to them on all three sides and when the generate/randomise button is selected, they transform on a random basis.

The base class for the project specifies the mesh for the triangles and their indices, aswell as the neighbouring triangles and their colours. This also contains the code that checks whether triangles touch each other and if so, replaces them. This is used for when we generate mountains and suc on the project as they add new vertices.

The planet itself is built using and icosphere, which is basically just a low poly sphere created of equal triangles. The more triangles that are added, the smoother and more rounded the planet appears. I used a subdivide function for this.
I used another base class which kept a few triangles/polys in another hash set, and used this to extrude/intrude the planets surface. This uses a constructor and an iteration index set to (-1) so it can differentiate between new triangles and old ones. Theres also a function for removing dupes of triangles.

The function for making new landmasses works by using a new hash set that has any new triangles created. Every time its called it creates a new size for the continent and it gets added to the hash set. This is then extruded. The extrusions work by removing the triangles where the extrusions will go and replacing them with the generated extrusions by reiterating them through the same index. 

To keep it from being too smooth on the extrusions, we added bumps by taking the list of all triangles that are part of the land masses and used multipliers to raise them slighty. We also addded mountiansi n the same way, but by just increasing the ranges of values to amke them higher.

Lastly, a shader script is used to define the colours of each of the elements; Water, land, mountains etc. This can be altered by the player if they have the project files, but i decided to just enter values myself that suited the game.

The result is a simple visualiser that allows players to start with an "earth-like" planet in front of them, and through procedural generation they can create as many "alien" planets as they like in the visualiser. As previously mentioned, this is perfectly used when someone needs a visualiser for some music when theyre studying or chilling in a room and they dont want to watch tv etc. It's there to be a much more chilled vibe and something that can be just left to run if they wish. For the purpose of this, I also added music too the project, but this is optional.



**Which parts of the assignmemnt you developed yourself vs parts that come from the examples we made on the course or that come from tutorials**

Much of this project was a mix of all of the three above combined. The basis of the project was mostly my design, which i wrote out in somewhat of a pseudocode first. Certain aspects of the project such as the extrusions and some of the functions I hadnt used too much before like the Hash sets and the code for the icospheres proved very difficult for me, at which point I was able to garner help from others in the class, friends in fourth year, two much older friends I met in the study room of my apartment building who are masters students in computer programming, and of course reddit and other websites. I used online tutorials quite heavily and as sometimes I can get lost in my code and need a little guidance to point me in the right direction. There were some great uity tutorials that had bits and pices of useful info that I could piece together to get to my final product. These resources are very import to me as they really help me to overcome my shortcomings as a programmer and further my skills.

Overall, while many of the troubleshooting and the "how can I make thsi work the way it's supposed to" stuff did require help and collaboration. I do find that it was good to have it that way though as I learned a lot about some pretty neat stuff in unity and coding that I wouldnt have otherwise known before. I like working with others and learning not only from my mistakes, but from their solutions.



**What you are most proud of about the assignment**

Honestly, the end result being what I envisioned is what I am most proud of. I am not the most talented programmer by any means, so when given the brief it was honestly quite daunting. That being said, I wanted to go outside the box a little and bring something a little more chilled out and experiential to the table, and have a "game" that could be used with the most minimal interration but still be enjoyed by the user. This is what I am most proud of.



**Youtube Link**
https://youtu.be/tucj6BVVMAI
