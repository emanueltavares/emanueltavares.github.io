## About me

Hi, my name is Emanuel Tavares and I'm a Unity 3D developer from Brazil. I created this website to showcase projects that I worked with as part of a team.

## Projects

### Vinicius Run

[Oktagon Games](http://www.oktagongames.com/) is a mobile game startup that I have been working remotely as a freelancer for more than a year. I always wanted to do remote work before but could never find anything; now that they gave me something, I will always be grateful to them.

Working remote seems like a dream come true to many people. Remote work brings perks like being close to family, no commuting, no dress code and no interruptions, if you do not have noisy neighbors and/or family. Not everything is perfect, though.

You need to invest a lot of money in your office, be it chairs, desks, software, even paperclips. Everything adds up in the end. To make matters worse, team communication becomes a lot more important. In the presence of remote workers, teams usually resort to text messages to talk to each other. However, emotion is harder to convey by writing than talking, which results in a lot of misunderstandings. And after all that, you still need energy to manage yourself. If you have a tendency to procrastinate, you are going to have a very hard time.

Being able to work remotely with [Oktagon Games](http://www.oktagongames.com/) for more than a year was a great personal accomplishment for me. As the year went by, I managed to help them in a few games. Vinicius Run is the latest one. It is an infinite runner starring Rio 2016 Olympic Games mascot, Vinicius. Your objective is to make Vinicius run as long as possible while dodging monkeys, crazy owls, turtles, capybaras, snakes and other obstacles.

![Vinicius Run](/images/vinicius0.jpg)

The game is free-to-play and has two virtual currencies: rubies and coins; former can be used to buy consumable power-ups and the latter can buy enhancements for our mascot, allowing him to run faster, jump higher and have more health. Both currencies can be obtained by collect them in a run and completing missions; rubies can also be bought with real money. If you don’t feel like spending anything, the game occasionally offers power-ups and rubies in exchange for watching an ad.

![Vinicius Run](/images/vinicius1.jpg)

The game took four months to create. Considering how polished it looks, you can bet that an insane amount of work was done. To speed things up, Oktagon acquired the source code of an infinite runner from one of their partners, which served as a base for the game. Here I list my contributions:

-   In the base game, players could complete missions while they are doing a run. By completing one, you get rewards. I ported that system to Vinicius Run. A few things that changed were that some missions could repeat from time to time, to always give you something to do, even after you complete everything. I also tied some missions to Google Play achievements, linked the information that would be displayed in a GUI to a localization system and created a simple in-game notification that congratulates you when you finish something. I gave a little help in displaying all the missions in the UI, most of it was developed by a coworker.
-   If you do a lot of runs, the game eventually awards you with collectables, usually a concept art or a wallpaper for your phone. Images came straight from Oktagon server, which checked the player progress to see if he was cheating. I implemented a system that checked if the player was eligible for a collectable after the end of each run. If he was, I would save the game and synchronize it with the remote server. I also made the UI panel that displays what collectables you have.
-   I integrated Google Play Games. Specifically, I implemented Leaderboards, Achievements and Google Events. I set up a Leaderboards for “Biggest Distance” which ranked the players who have traveled the biggest distance in a single run. There was also another that ranked the total traveled in all runs, but we did’nt use it. Besides missions, I also created achievements for the first time you run, when you log in Facebook for the first time, when you buy enhancements and other things. As for Google Events, it is a unique analytics system from Google. Its events cannot receive any kind of parameters, except a positive number. It is useful if you want to count things, like how many miles Vinicius traveled, what was the greatest distance Vinicius traveled in a single run, how many rubies and coins you spent, etc. You can also link events to Quests, which grant rewards to players who can accomplish certain events.
-   Facebook integration was simple, players can log in it, share their runs and invite their friends to play.
-   I implemented remote and local notifications for iOS and Android. Local notifications were used to convince the player to come back to the game after he quits it for a really long time. Remote notifications were used to broadcast announcements to all players or to send a message to a specific user. Local and Remote Notifications in iOS are already supported in Unity. To implement notifications in Android I had to use two plugins, one for remote and other for local.
-   I was responsible for processing payments. It was the first time I was assigned to a billing task and it was pretty tense, since a screw-up here can cost a lot. After I though that I had finished this task, a lot of bugs occurred later and, given that I was already working in another project, a coworker fixed it. I am far from proud with my implementation, I still have a lot to learn when it comes to billing.

![Vinicius Run](/images/vinicius2.jpg)

Working on this project was very demanding, we had a very tight deadline and the game was supposed to be fun, beautiful and solid, regardless. I had a lot of difficult on some tasks, specially billing, which, in the end, someone else had to finish. I lost the opportunity to work on more features because some tasks demanded a lot from me. Building the project was far from easy given that some plugins refused to work along with others. I lost count on how many dex limit errors I saw. However, I’m proud of the final product, it feels like a Rio 2016 themed game and it is by far the most polished game I have worked. It is available to play on [Android](https://play.google.com/store/apps/details?id=com.oktagongames.viniciusrun) and [iOS](https://itunes.apple.com/us/app/rio-2016-vinicius-run/id1126468969?mt=8).

### Pooks

Pooks was the first game I helped Oktagon Games with. It is a beautiful game where you combine potions of the same color to get points. The concept is similar to 2048, but instead of combining equal numbers, you combine potions with the same color. The development started in Hive Digital and went on until the it was 80% done. After that, the project went on hiatus for an indefinite time. How Oktagon got involved with the game? I don’t know all the details, but I suppose Hive hired Oktagon to finish the game.

When we eventually released the game, it was not that different from what Hive had already made. The game already had six books (or worlds) with 12 chapters (or stages) each. With the exception of the first, books are locked and can only be accessed if you have the required number of stars, which you get by getting a good score when you complete a chapter, and beating every chapter from the previous book.

![Pooks](/images/pooks0.jpg)

A chapter is a 2048 game with a few gists. Board size can go beyond 4x4 tiles, a few potions are placed beforehand and, in latter chapters, some unmovable obstacles too. Winning conditions ranged from combining potions until a specific one is created to combining potions over specific tiles of the board. To add assault to injury, you also needed a passing score. Accordingly to how many points you got, you receive from zero to four stars, which unlock new books you to play.

![Pooks](/images/pooks1.jpg)

When all is said and done, the game looked gorgeous and it was fun to play but also very rough around the edges, the controls felt “off”, it had a few bugs, the gameplay needed balancing and there wasn’t a clear monetization strategy. The game had one virtual currency but there was nothing to buy. After careful consideration about which features would be improved, added or removed, we started working.

![Pooks](/images/pooks2.jpg)

Since it was my first project with them, Oktagon assigned another coworker to split the work with me. After two months, they became confident in what I was doing and reassigned the coworker to another project. I also had the help of our Team Leader, who took care of the back-end of the game. My contributions were:

-   Google Play and App Store Achievements integration.
-   A lot of ad services: FuseSDK, AdColony, UnityAds and Admob. Some were used to give rewards and others play during transitions.
-   Analytics, with Kochava, which only tracks installs, and GameAnalytics, which tracks the rest.
-   Facebook integration: you can ask your friends for lives, even if they don’t play the game. You can also share your scores.
-   Power-ups: they can destroy obstacles, shuffle the board, undo a movement and so on. We created them for monetization. After you run out of them, you can get new ones by spending virtual currency.
-   Second chance: if you fail any chapter and have one power-up that can help, you get the chance to use it before the game is over. You can also get a second chance if you “lost” after the objective was completed, but do not have enough points to beat the chapter’s high-score.

![Pooks](/images/pooks3.jpg)

I faced a few challenges when I was working in this game: since it was my first game with Oktagon Games, I wanted to show how capable I was in programming. Some sections of the game are very polished thanks to how much driven I was. This is a game that I really believed it could be a huge success. Vinicius Run came right after it, but I’m still a lot more fond of the former. It is available to play on [Android](https://play.google.com/store/apps/details?id=com.oktagongames.oktpooks).

### Talking Rocks

My first actual job in game development was in [Skillab](http://www.skillab.com/). Up to that point I was developing research projects with Unity 3D and never had finished a game. My first assignment was to develop this game, along with an artist and a game designer. The game was going to be called Talking Rocks.

![Talking Rocks](/images/talkingrocks0.png)

Talking Rocks is an educational match-3 game with a vikings motif. You control either a male or a female viking on a mission to collect English words to complete a Magic Scroll and beat the game. Words are scattered among five islands with five stages each. In each stage, you play a match-3 game with a time limit. To win, you have to obtain enough points by matching three or more stones before the time runs. As you get more points, you also get English words. After you finish this section, you have to complete a mini-game using the words you previously collected. The mini-games were simple, usually they involved dragging said English words to images or naming objects with a virtual keyboard, nothing too fancy. After completing the mini-game you can go to the next stage.

The project was completed in six months. The game was launched in three platforms: [Android](https://play.google.com/store/apps/details?id=com.skillab.talkingrocks), [iOS](https://itunes.apple.com/br/app/talking-rocks/id783718100?mt=8) and [Microsoft Store](https://www.microsoft.com/pt-br/store/p/talking-rocks/9wzdncrds4kl). The first five levels of the game were available to everyone to play. After you complete them, the game requires you to pay to give you access to the remaining levels. After I left the company, [Skillab](http://www.skillab.com/) changed the game’s business model: all stages are available from the beginning but ads will show up between transitions.

![Talking Rocks](/images/talkingrocks1.jpg)

I went through a lot of challenges developing this game. As I said before, [Skillab](http://www.skillab.com/) was my first **real** job, with a contract and everything. I was a difficult person to get along at work, I had, and still have, a strong personality when it comes to developing a game, I did not agree with a lot of the game design decisions, I complained thousands of times that the game would be too shallow, preachy and confusing. I fought a lot of lost battles, said things when I was supposed to be quiet and kept my mouth shut when I shouldn’t. All of those things did a number on my psychological health. However, not only I managed to endure that, but I’m very sure that I grew a lot more as a person than as a developer when I worked there.

The technical challenges I found mostly concerned my lack of experience. I learned how to use subversion; learned how to properly use a few design patterns; learned how to create plugins for Android; and how to properly import textures and assets. I also had a lot of difficulty porting the game to iOS and Windows Phone 8.1, so much that a few coworkers had to help. I never forget the pain I went through to adapt the code for the iOS AOT compiler. I had a lot of problems with Windows thanks to its very strict submission requirements. As an example, one of the mini-games required a virtual keyboard to be played. That is easy to do in iOS and Android, since Unity provides a function that calls the native input keyboard from the devices. But Windows? Oh, boy, we had to create our own from scratch. By “we”, I mean a coworker that had already created one for an XNA game. Finishing those ports was a team effort.

![Talking Rocks](/images/talkingrocks2.jpg)

Overall, the game was a great experience for me in the sense that it gave me confidence that I could actually have a career creating games, that I had something that I could point and say “I helped create that!”. It also helped me to have a better sense of scope, to know that the best solution for a task is not always feasible; to know when to give up doing something in a way to try another; to ask for help without compromising too much of my coworkers’ time and help them without compromising mine.

### Word Trip

This was the second game I developed in [Skillab](http://www.skillab.com/). I don’t know how long it took to complete, as I left the company when the game was very close to being finished. I worked in it for three months.

![Word Trip](/images/wordtrip0.jpg)

Word Trip is very similar to Talking Rocks, gameplay-wise. Players incarnate a tourist who travels across the city, going into museums, fast-food joints, hospitals, police departments, you name it. At every location, there is a mini-game were, after you complete it, you win English Words that will be useful in other mini-games. All this collecting is supposed to help you learn English. Word Trip features a lot drag-and-drop mini-games, just like Talking Rocks. There’s also a few word hunts, word fills and others in the same fashion.

![Word Trip](/images/wordtrip1.jpg)

Working in this game was a lot easier for me. I had more experience, was better at estimating my tasks and faster at completing them. I also went out of my way to polish the animations in the game as much as I can. The art department also learned a lot with Talking Rocks and contributed a lot to make the game look nice. The animations of the title screen and the stage selection are things that I’m still proud of having done.

![Word Trip](/images/wordtrip2.jpg)

I gave much attention to presentation because that was the only way I had any agency on making the game better. The game design was not that different from Talking Rocks, I felt the mini-games were overly simple and shallow and the game gave no context or clear motivation to do them. Giving how much headache I had with Talking Rocks’ game design, I did not bother complaining this time.

![Word Trip](/images/wordtrip3.jpg)

Two months in and [Skillab](http://www.skillab.com/) hired a junior programmer and assigned him to Word Trip. He was very inexperienced in Unity 3D and I trained him as best as I could. Working with someone else was very interesting, having somebody to watch your back and exchange ideas about the project made a lot of difference to me. Usually, people don’t like training others; this is the only experience that I had and it was great, maybe I was lucky. While I worked there, he coded two types of mini-games, I coded the others and glued all of them together in the map. After I left, banner ads were included. Besides that, I’m not sure if they changed anything else. Some bugs that I couldn’t fix were still present in the release version. You can play it on the following platforms: [Android](https://play.google.com/store/apps/details?id=com.skillab.wordtrip) and [iOS](https://itunes.apple.com/br/app/word-trip/id944208330?mt=8).
