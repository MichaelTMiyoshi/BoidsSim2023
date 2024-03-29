# BoidsSim2023
 
This version of Boids was created in Unity a couple years ago.  But there was something wrong when I cloned the old project.  So I tried it again.  This time, I made sure that I used the .gitignore file that I have used with other Unity projects that does not have too much stuff in it.  (I have not yet tested to make sure that it gets cloned properly to a different computer.)

A couple things.

I used the blank project as a starting point.  Then, I copied over all the assets into the project.  I decided that I wanted to rename the project too so I renamed the folder.  Then, I deleted the visual studio .sln file.  When I opened the copied project in Unity, it made a new .sln file with the project name.  This was a nice piece of new knowledge.  I figured renaming the .sln file would cause problems, so I did not want to try that.  Turns out that Unity is pretty sharp that way.

There were two things that I had to do to make the project work.  The first problem was that the globals and everything in the GameManager script was not working.  This was fixed by adding an empty.  I called the empty Singleton because I learned about Singletons and used it to hold my global variables.  These would normally be the things that need to stay persistent throughout the project (score going from scene to scene for example).  Once the script was associated to the empty, everything worked out fine.

The second problem was that the toggles did not work.  I fixed that after watching this [video](https://www.youtube.com/watch?v=4S_zl9XFcxA).  The fix is that the scene needs to have an EventSystem.  Once the event system was added, the toggles worked.  The video shows this in action.  When copying the project, the EventSystem was not there.

Last thing to note.

The project is not a very good representation of boids.  There are some cool features, but it is not exactly what I was going for.  However, it did teach me lots of good things about Unity and programming in C#.  I do want to make it more like the simulations of boids I have seen other places, but this is a good start.  Good enough to make the repository public.  I think.
