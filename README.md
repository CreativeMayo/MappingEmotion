# MappingEmotion
The objective now is to create an additional feature called "Emotional Mapping," using vector embedded databases, GPT text analysis, and Three.js visualizations to help users visualize their internal emotional makeup and enhance the effectiveness of the service.

## Prompt 

Overview**: We are helping older Gen Zers, Millennials and potentially even younger Gen Xers deal with their unresolved personal issues. If their trauma is too great, then we simply recommend that people see professional help. We have had feelings of being lost, felt depression, deep melancholy, eating disorders and nihilism as well as lower levels of social anxiety. These issues do not seem to be very unique to the two of us so we are going to help people talk through their issues and direct them to resources as well as give them personal tasks to complete which we will hold them accountable to. The website is called webuildawareness.com and we are offering free half an hour consultation to provide this service of self understanding, processing of repressed emotion (samskaras) and self awareness. The website also allows people to input youtube videos (what we refer to as stimuli) and then add text boxes of what is being said. Once a text box has been added, the user can add emotional responses to those text boxes. Having people add videos that they find interesting or emotionally stimulating and then adding their emotional, sensory responses and thoughts, will hopefully allow us to see patterns of behaviour indicative of their internal states. We are currently using Carl Jung’s model of the mind as a framework when constructing our free clients, as well as other western and eastern philosophies.

Objective**: Now that the website is almost up and running, I wish to begin the creation of an additional supplementary MVP. I have gone through various failed renditions, this time, I wish to attempt to create something called: “Emotional Mapping”. The idea is to utilise vector embedded databases, GPT text analysis and Three.js visualisations in order to help people visualise their internal emotional makeup. “Seeing is believing”, so if successful, this will help both the free client as well as us.

MVP Spec**:
1. I locally host the MVP written in javascript
2. I send a HTML POST via Postman using the following format ‘@username text’
3. Usernames are stored so that multiple emotional inputs can be added together into an Emotional Map of that user
4. The text is sent to ChatGPT’s API with a prompt saying it should analyse the emotional makeup of the text based on a defined criteria of sentiment which must include the emotions listed below
5. The sentiment of that input is then converted into a vector combination so it can be stored in the vector embedded database 


### Example vector

From my understanding I will create a vector output from a user based on the three dimensions model:

const emotionalbundle (PierseMorgan_ontate) =
    valence : -0.65 // negative response, range from -1.0 to 1.0
    arousal : 0.78 // high arousal, range from 0 to 1
    dominance : 0.9 // very high dominance, range from 0 to 1

Based on the example given I would expect these vector inputs to be categorised  as "anger"

### List of emotional categories

From the three vector fields provided, please create a complete set of ranges and combinations for all the emotions that can be modelled starting from: [Joy: high valence, high arousal, high dominance
Serenity: high valence, low arousal, high dominance
Interest: high valence, high arousal, low dominance
Satisfaction: high valence, low arousal, low dominance
Anger: low valence, high arousal, high dominance
Distress: low valence, high arousal, low dominance
Sadness: low valence, low arousal, low dominance
Boredom: low valence, low arousal, high dominance
Fear: negative valence, high arousal, variable dominance
Surprise: variable valence, high arousal, variable dominance
Disgust: negative valence, variable arousal, variable dominance]

These emotional categories require quantifiable vector counterparts. To account for overlap and subjectivity, we need to include context from that client's previous emotional inputs. This will mean that points within a person's emotional mappings are likely to drift and change in categorisation over time. See this as a feature and print a response when a conflict occurs for us and the client to discuss and make a decision. This correction of overlaps and conflicts will further provide clarity in emotional understanding whilst also avoiding database and coding conflicts 

6. Finally the inputted points will be visualised using the three.js library.


Please create an overview of the MVP. Ask any questions that you need for clarification. Once the overview is complete, I will need you to walk me through the technical process as well as write code for the project. I am a beginner coder and am creating an MVP, so the faster and simpler this is the better.
