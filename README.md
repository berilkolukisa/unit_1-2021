# Unit 1: A classic game 
![](game.gif)

# Criteria A: Planning

## Problem definition

The owner of the local game shop is an enthusiast of classic computer games. He has been looking for a talented programmer that can help him revive his passion for text-based games. He has few requirements for this task:

1. The game has to be entirely text-based.
2. The game must record the time played.
3. The game must record the player name and score.
4. The game should include emoticons, emojis or ascii images for visual purposes.
5. The game should be easy to understand and play.
6. The game should be visually pleasing.



Apart for this requirements, the owner is open to any type of game, topic or genre.

## Proposed Solution

I will design a text based game for a client who is interested in tasting their abilites. The text game will be about testing the user's ability ability in witch rituals, crystals,herbs and astrology and is constructed using the software evaluated according to the criteria shown below.


## Success Criteria
1. The game has to be entirely text-based.
2. The game must record the time played.
3. The game must record the player name and score.
4. The game must have verified info (including the crystals ).
5. The game must have a scoreboard at the end of the game showing the player's name and score.



# Criteria B: Design

## System Diagram
![](system_diagram.PNG)
## Flow Diagrams
![](flow_chart1.PNG)
![](flow_chart2.PNG)
![](flow_chart3.PNG)

## Functional Testing
| Type of testing | Part to test | Question asked | Input | Expected Output | Status |
|---------|----------------|-----------------|---------------|------------------------|-----------|
| Unit Testing | The code to assign a label to the user | 🦋 Now please choose a label for yourself. This will stick your name throughout the game🦋 🧚 press 1 for fairy  🧙‍ press 2 for witch  🧛 press 3 for vampire | 3 |🦋Your username will be 🧛vampire' + user_name | SUCCESFUL |
| Unit Testing| The code to understand user's answer and tells us whether it right or wrong | 🦋Which crystal you are not supposed to put in the water?  1)Clear quartz 2)Ruby  3)Aventurine  4)Tiger’s Eye | 2 |🦋Your answer was right | SUCCESFUL |
| Unit Testing | To code to combine the assigned label and the user's name | 1)🦋 Please enter your name or a name that you want to be referred🦋 2) 🦋 Now please choose a label for yourself. This will stick your name throughout the game🦋  🧚 press 1 for fairy  🧙‍ press 2 for witch   🧛 press 3 for vampire | 1)Beril 2)1 | Your username will be 🧚fairyberil|

## Source Code
```.py
#My game is called Butterfly village. It is a text based game which the users can test their knowledge in astrology, crystals and herbalogy.The user gets to choose a nickname(title) for themselves. After that they get to choose a forest out of three which is the Crystal Forest, The Astrology Forest and the Herbalogy Forest. As a result of their choice, users get to answer five questions on the topic that they have chosen. The questions go from easy to hard and they also have increasing points. I also tried to add explanatory checkpoints in the game so the users will not have hard time figuring out what they are supposed to do in that spesific area.
message= '🦋 Welcome to the butterfly village. In this game you will test your knowledge in crytals, herbs and astrology and compete for the highest place on the butterfly score chart. Wish you the best of luck 🦋'
space='                                                             '
butterfly_line='🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋🦋'
print(message)
print(space)
print(butterfly_line)
user_name=input('🦋 Please enter your name or a name that you want to be referred🦋 ')
label=int(input('🦋 Now please choose a label for yourself. This will stick your name throughout the game🦋 \n 🧚 press 1 for fairy \n 🧙‍ press 2 for witch  \n 🧛 press 3 for vampire'))
#I wanted to add a label part so it will be easier while we are trying to make a scoreboard and it will minimize the chances of users who has the name share the same place at the scoreboard. Also if we will look from a psychological perspective, our users will be connected to our game since they had something that they get to choose.
if label<4:
    #The code generates a username including the title that the user have chosen and the user's name and prints that.
   if label == 1:
       print('🦋Your username will be 🧚fairy' + user_name)
   if label == 2:
       print('🦋Your username will be 🧙witch' + user_name)
   if label == 3:
       print('🦋Your username will be 🧛vampire' + user_name)
else:
   print('🦋Please select a title .')

print(space)
#The user gets to choose a forest( an area of knowledge ) to test their knowledge. The code asks the user for a spesific number which means a forest.
choose_forest=int(input('🦋Now we will move on to our knowledge-test part! In this part we will ask you to choose a forest to test your knowledge .🦋 \n 🌸 press 1 for Crsytal Forest \n 🌸 press 2 for Herbs Forest \n 🌸 press 3 for Astrology Forest  '))
if choose_forest<4:
    #If the value of the number that the user has entered is valid (<4) , the code works to understand which forest that they've chosen.
  if choose_forest==1:
      # If the user has chosen or first forest (Crystal Forest) , the code starts asking the questions related with the topic.
      print('🦋 You have chosen the Crystal Forest . You will receive five questions listed from easy to hard.Here comes your first question.🦋' )
      print(space)
      cq_1=int(input('🦋Which crystal you are not supposed to put in the water? \n 1)Clear quartz \n 2)Ruby \n 3)Aventurine \n 4)Tiger’s Eye '))
      # The answers are numbered from 1-4. All questions have only one right answer and if the user chooses the right answer, they win points. Otherwise, the code adds 0 points.
      answerc1=0
      if cq_1<5:
          if cq_1==1:
              print('🦋Your answer was not right ')
              answerc1+=0
          if cq_1==2:
              print('🦋Your answer was right ')
              answerc1+=1
          if cq_1==3:
              print('🦋Your answer was not right ')
              answerc1+=0
          if cq_1==4:
              print('🦋Your answer was not right ')
              answerc1+=0
      cq_2=int(input('🦋What is the type of crystal that is mostly found on Earth? \n 1)Amethyst \n 2)Calcite \n 3)Opal \n 4)Quartz '))
      answerc2=0
      if cq_2<5:
          if cq_2==1:
              print('🦋Your answer was not right ')
              answerc2+=0
          if cq_2==2:
              print('🦋Your answer was not right ')
              answerc2+=0
          if cq_2==3:
              print('🦋Your answer was not right ')
              answerc2+=0
          if cq_2==4:
              print('🦋Your answer was right ')
              answerc2+=1
      cq_3 = int(input('🦋What is the rarest type of crystal in the world?  \n 1)Red Beryl \n 2)Benitoite \n 3)Taaffeite \n 4)Painite '))
      answerc3=0
      if cq_3<5:
          if cq_3==1:
              print('🦋Your answer was not right ')
              answerc3+=0
          if cq_3==2:
              print('🦋Your answer was not right ')
              answerc3+=0
          if cq_3==3:
              print('🦋Your answer was  right ')
              answerc3+=0
          if cq_3==4:
              print('🦋Your answer was not  right ')
              answerc3+=1
      cq_4 = int(input('🦋Which crystal is the one that you can place under sun? \n 1)Hiddenite \n 2)Calcite \n 3)Prasiolite \n 4)Malachite '))
      answerc4=0
      if cq_4 == 1:
          print('🦋Your answer was not right ')
          answerc4 += 0
      if cq_4 == 2:
          print('🦋Your answer was not right ')
          answerc4 += 0
      if cq_4 == 3:
          print('🦋Your answer was not right ')
          answerc4 += 0
      if cq_4 == 4:
          print('🦋Your answer was  right ')
          answerc4 += 1
      cq_5 = int(input('🦋Which crystal is not believed to work with anxiety? \n 1)Amethyst \n 2)Malachite \n 3)Rhodonite \n 4)Moonstone '))
      answerc5=0
      if cq_5 == 1:
          print('🦋Your answer was not right ')
          answerc5 += 0
      if cq_5 == 2:
          print('🦋Your answer was right ')
          answerc5 += 5
      if cq_5 == 3:
          print('🦋Your answer was not right ')
          answerc5 += 0
      if cq_5 == 4:
          print('🦋Your answer was not right ')
          answerc5 += 0
      print('🦋Your total score is :')
      print(answerc1+answerc2+answerc3+answerc4+answerc5)
  if choose_forest==2:
      print('🦋 You have chosen the Herbs Forest . You will receive five questions listed from easy to hard.Here comes your first question.🦋')
      print(space)
      ch_1 = int(input('🦋Which herb is not supposed to be used in a state of anxiety? \n 1)Chamomille \n 2)Lavender \n 3)Lemon \n 4)Passion Flower' ))
      answerh1 = 0
      if ch_1 == 1:
          print('🦋Your answer was not right ')
          answerh1 += 0
      if ch_1 == 2:
          print('🦋Your answer was not right ')
          answerh1 += 0
      if ch_1 == 3:
          print('🦋Your answer was right ')
          answerh1 += 1
      if ch_1 == 4:
          print('🦋Your answer was not right ')
          answerh1 += 0
      ch_2 = int(input('🦋What is the oldest herb? \n 1)Salt \n 2)Gingko  \n 3)Cinnamon \n 4)Pepper'))
      answerh2 = 0
      if ch_2 == 1:
          print('🦋Your answer was not right ')
          answerh2 += 0
      if ch_2 == 2:
          print('🦋Your answer was right ')
          answerh2 += 2
      if ch_2 == 3:
          print('🦋Your answer was not right ')
          answerh2 += 0
      if ch_2 == 4:
          print('🦋Your answer was not right ')
          answerh2 += 0
      ch_3 = int(input('🦋What is most used herb in the world? \n 1)Cumin \n 2)Sugar  \n 3)Basil \n 4)Salt'))
      answerh3 = 0
      if ch_3 == 1:
          print('🦋Your answer was right ')
          answerh3 += 3
      if ch_3 == 2:
          print('🦋Your answer was not right ')
          answerh3 += 0
      if ch_3 == 3:
          print('🦋Your answer was not right ')
          answerh3 += 0
      if ch_3 == 4:
          print('🦋Your answer was not right ')
          answerh3 += 0
      ch_4 = int(input('🦋What is most expensive herb type in the world? \n 1)Caraway seeds \n 2)Asafoetida \n 3)Sumac \n 4)Saffron'))
      answerh4 = 0
      if ch_4 == 1:
          print('🦋Your answer was not right ')
          answerh4 += 0
      if ch_4 == 2:
          print('🦋Your answer was not right ')
          answerh4 += 0
      if ch_4 == 3:
          print('🦋Your answer was not right ')
          answerh4 += 0
      if ch_4 == 4:
          print('🦋Your answer was right ')
          answerh4 += 4
      ch_5 = int(input('🦋Which one actually count as a herb? \n 1)Salt \n 2)Mud \n 3)Leaf \n 4)Banana'))
      answerh5 = 0
      if ch_5 == 1:
          print('🦋Your answer was not right ')
          answerh5 += 0
      if ch_5 == 2:
          print('🦋Your answer was not right ')
          answerh5 += 0
      if ch_5 == 3:
          print('🦋Your answer was not right ')
          answerh5 += 0
      if ch_5 == 4:
          print('🦋Your answer was right ')
          answerh5 += 5
      print('🦋Your total score is :')
      print(answerh1+answerh2+answerh3+answerh4+answerh5)
  if choose_forest==3:
      print('🦋 You have chosen the Astrology Forest . You will receive five questions listed from easy to hard.Here comes your first question.🦋')
      print(space)
      ca_1 = int(input('🦋If someone was born in 12th of January, what is their sign? \n 1)Sagittarius \n 2)Aquarius \n 3)Capricorn \n 4)Pisces' ))
      answera1 = 0
      if ca_1 == 1:
          print('🦋Your answer was not right ')
          answera1 += 0
      if ca_1 == 2:
          print('🦋Your answer was not right ')
          answera1 += 0
      if ca_1 == 3:
          print('🦋Your answer was right ')
          answera1 += 1
      if ca_1 == 4:
          print('🦋Your answer was not right ')
          answera1 += 0
      ca_2 = int(input('🦋Which is not one of the most common signs? \n 1)Leo \n 2)Cancer \n 3)Virgo \n 4)Scorpio '))
      answera2 = 0
      if ca_2 == 1:
          print('🦋Your answer was not right ')
          answera2 += 0
      if ca_2 == 2:
          print('🦋Your answer was not right ')
          answera2 += 0
      if ca_2 == 3:
          print('🦋Your answer was not right ')
          answera2 += 0
      if ca_2 == 4:
          print('🦋Your answer was right ')
          answera2 += 2
      ca_3 = int(input('🦋Which is the rarest sign? \n 1)Capricorn \n 2)Gemini \n 3)Aries \n 4)Aquarius '))
      answera3 = 0
      if ca_3 == 1:
          print('🦋Your answer was right ')
          answera3 += 3
      if ca_3 == 2:
          print('🦋Your answer was not right ')
          answera3 += 0
      if ca_3 == 3:
          print('🦋Your answer was not right ')
          answera3 += 0
      if ca_3 == 4:
          print('🦋Your answer was not right ')
          answera3 += 0
      ca_4 = int(input('🦋Which is not a full moon date in 2021? \n 1)April 27  \n 2)July 24  \n 3)January 17  \n 4)August 22 '))
      answera4 = 0
      if ca_4 == 1:
          print('🦋Your answer was not right ')
          answera4 += 0
      if ca_4 == 2:
          print('🦋Your answer was not right ')
          answera4 += 0
      if ca_4 == 3:
          print('🦋Your answer was right ')
          answera4 += 4
      if ca_4 == 4:
          print('🦋Your answer was not right ')
          answera4 += 0
      ca_5 = int(input('🦋When was the last solar eclipse? \n 1)December 14 2020  \n 2)January 14 1997 \n 3)October 3 2021  \n 4)March 30 1562 '))
      answera5 = 0
      if ca_5 == 1:
          print('🦋Your answer was right ')
          answera5 += 5
      if ca_5 == 2:
          print('🦋Your answer was not right ')
          answera5 += 0
      if ca_5 == 3:
          print('🦋Your answer was not right ')
          answera5 += 0
      if ca_5 == 4:
          print('🦋Your answer was not right ')
          answera5 += 0
      print('🦋Your total score is :')
      print(answera1 + answera2 + answera3 + answera4 + answera5)
    #Lastly, the code prints out a thank you message to the user and encourages them to play again.
  print('🦋Thanks for playing the game. We hope you like it ! Cannot wait to see you again🦋')
  print('🦋You can also try to test your knowledge in other forest.Wish you the best of luck!🦋')
  ```

## Record of Tasks
| Task No | Planned Action | Planned Outcome | Time estimate | Target completion date | Criterion |
|---------|----------------|-----------------|---------------|------------------------|-----------|
|    1     |      Planning how the game will go, which topics I want to include and what vibe I want my game to give.         | I have a general idea of how I want my game to be about, the storyline and the vibe that I want my game to give.                |  1-2 days           |    27 September 2021                      |           |
|    2    |         Searching for ASCII images, emoticons and emojis that I can use in my game to make it look more visually pleasing .    |  Finding out that I don't want to add any ASCII images or emoticons to my game since they don't fit the aesthetic of the game and one of the goals is the game to be visually satisfying.               |1 day               |       2 October 2021                  |          |
|      3   |    Starting to write the beginning part of the code where it asks for user's name .      |  Having a basic intro to how my game will look like .               |       3 days         |   7 October 2021                    |      |
|    4   |         Learning some user-friendly psychological tricks that I can use in my game.  | Adding the 'user-title' part to my game to have give some optional parts in the game to the user which I've realised while researching that helps the user to connect to the product more.                |   1 day             |   10 October 2021                     |           |
|    5    |       Making detailed research on the three topics that I will be using in my game(crystals,herbalogy,astrology)  |  Finding out there there were a lot of opportunities that I can write questions.               |  1 day            |         12 October 2021               |           |
|    6    |         Writing the questions that I will use in the game.    |  Changing my idea of having 10 questions to 5 questions because along the way I've realised that if I have 10 questions it will cover too many topics that an average user might not know which is not a good thing if we think from user's point of view.               |              2-3 days   |    20 October 2021                 |         |
|    5    |          Grading the questions that I've wrote and listing them easy to hard.    | Having 5 question which all have different levels of easiness.                |      1 day           |     21 October 2021                    |          |
|    6     |         Adding the questions that I wrote to the code.      | My game nearly finishes with all the questions and the extra intro parts.                |             2 days     |     25 October 2021                 |         |
|    7    |         Ending the game.    |                 |               |        25 October 2021                |               |
|    8     |          Doing flowcharts and system diagram.      |                 |   3-4 hours              |  27 October 2021                    |          |
