# soundcloudish

soundcloudish.glitch.me

### The Team and Responsibilities
Perdo de V Oporto - server and database
Manas Mehta - styling, server and database, components & connections, visualizer, architecture
Brandon Navarro - visualizer, components
Joseph Caltabiano - components & connections, architecture

### The Project
We designed and created a music visualizer creation and sharing platform. A user can create a new account or log in with an old account. For graders - you can create a new account and add your own visualizers. You can also log in with username: "mmehta", password: "pass" for the testing account that already includes some visualizers. 

The landing page displays a social media style feed of the ten most recent visualizers created by other users. You can click on one of these to lead the visualizer into the top half of the winodw and start playing the associated song. 

Click on your profile name in the upper right and you will be directed to your profile page. In here, you can create and edit a new visualizer and choose a song for it from the provided list. When you are ready you can upload your vis so other's can see your work!

### Technologies
We used a wide array of technologies and libraries for this project. Much of the project was centered around React, which allowed us to compartmentalize the application using the component structure, as well as handle network requests and component updates in an efficent way. Using React meant we also used parcel to bundle our files for both development and production. 

For the server, we use Express along with helmet and compression. Passport was used for user auth. We used firebase for our database. __ **EXPLAIN MORE**

The visualization was created using web audio api and dat.gui. The visualization is constructed by capturing the frequency data of the song and using those frequencies to manipulate how the rectangles are drawn onto the canvas. The frequency data of the song is read and the visualization updated by continually requesting a new animation frame. You are also able to change various aspects of the visualizer such as the height & length of each bar or the color.

We also wanted to include the option of uploading a threejs visualizer, however due to time constraints and lack of manpower, we were not able to get it integrated into the app. The threejs visualizer was built (and works) and would allow users to create a visualization of a bunch of shapes in 3D space that would rotate and change their color intensity to based on the frequency data of the song.


### Challenges
The main challenge we faced was the loss of a group member. They realized they would be NR'ing the course so decided to spend their time during the last week on other work. With a student short, we were stretched to complete our original goals, especially because that student had been partly responsible for the visualizer aspect, the heart of our project. As a result we were not able to create a polished product to the specifications we originally aimed for. We had to cut some features, for example providing a preloaded list of mp3s instead of letting the user upload a song from their computer. Some features were still not able to be finished completely, such as the visualizer and some styling. 

Another challenge we faced was knowing technologies well enough to envision how they would work with the project, but not well enough to see where problems would arise. One example here would be the song upload/download. You can see in the code where we tried to get this working but we were unable. Another example was using easy-peasy, a wrapper for Redux state storage. With our initial design, this made sense to use because it gave us the ability to pass information between components as needed, and triggered rerenders automatically. However, our design changed over time and we realized we would no longer need this state storage. You can still see the traces of our attempts with it in the code. 
