# **DATA 201 Homework 1**
### Mia Ramirez | Thursday, September 10th, 2026

Welcome to my first assignment for the DATA 201 course. Join us in my exploration of different bird species found in Rock Creek Park.

#
## What are my favorite Maryland birds?
### In no particular order, I love these birds...
+ Tufted Titmouse
+ Golden-crowned Kinglet
+ American Oystercatcher
+ Osprey
+ Red-winged Blackbird

## What are the birds most recently seen in Rock Creek Park? [^1] 
![alt text](https://clo-brand-static-prod.s3.amazonaws.com/logos/ebird/clo_ebird_short_web.svg "eBird Logo")
1. Mourning Dove
2. Chimney Swift
3. Red-Bellied Woodpecker
4. Downy Woodpecker
5. Hairy Woodpecker
6. Northern Flicker
7. Eastern Wood-Pewee
8. Red-eyed Vireo
9. American Crow
10. Tufted Titmouse

## Which of the previously listed birds seen in Rock Creek Park are on my list of favorite birds?

+ Drumroll please.
+ ..
+ ...
+ ....
+ ***...the Tufted Titmouse!***
![alt text](https://cdn.download.ams.birds.cornell.edu/api/v1/asset/302627281/1800 "Tufted Titmouse. Isn't it beautiful?")

Tufted Titmice are very adorable birds, at least in my opinion. You can recognize them in the wild by noting their field marks, such as their peach-colored feathers in the "armpit" of their wings, the crest of grey feathers, or even by their birdsong. They might sound like:
> _peter-peter-peter_ , a clear whistling sound.

or they might sound like:
> _tsee day-day-day_, an alarm call.

## What months were my favorite birds seen in Rock Creek Park in the last 5 years? [^2]

| Bird Species           | Jan | Feb | Mar | Apr | May | June | July | Aug | Sept | Oct | Nov | Dec |
| -----------------------| --- | --- | --- | --- | --- | ---- | ---- | --- | ---- | --- | --- | --- |
| Tufted Titmouse        | ✅  | ✅  | ✅  | ✅  | ✅   | ✅   | ✅   | ✅   | ✅   | ✅  | ✅  | ✅ |
| Golden-crowned Kinglet | ✅  | ✅  | ✅  | ✅  | ❌   | ❌   | ❌   | ❌   | ✅   | ✅  | ✅  | ✅ |
| American Oystercatcher | ❌  | ❌  | ❌  | ❌  | ❌   | ❌   | ❌   | ❌   | ❌   | ❌  | ❌  | ❌ |
| Osprey                 | ❌  | ❌  | ✅  | ✅  | ✅   | ✅   | ✅   | ✅   | ✅   | ✅  | ❌  | ❌ |
| Red-winged Blackbird   | ❌  | ✅  | ✅  | ✅  | ✅   | ✅   | ✅   | ✅   | ✅   | ✅  | ✅  | ❌ |

Unfortunately, there are no American Oystercatchers seen in Rock Creek Park. 

## What month should I go to Rock Creek Park to have the best chance of seeing my favorite birds?

Using python, I can create a data frame based on the information above.
```python
import pandas as pd

# initialize data of lists.
birds = {'Month': ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'June', 'July', 'Aug', 'Sept', 'Oct', 'Nov', 'Dec'],
'TUTI':[1,1,1,1,1,1,1,1,1,1,1,1],
'GCKI':[1,1,1,1,0,0,0,0,1,1,1,1],
'AMOY':[0,0,0,0,0,0,0,0,0,0,0,0],
'OSPR':[0,0,1,1,1,1,1,1,1,1,0,0],
'RWBL':[0,1,1,1,1,1,1,1,1,1,1,0]}

# Create DataFrame
df = pd.DataFrame(birds).set_index('Month')

# Get Counts
counts = (df == 1).sum(axis=1)
print(counts.sort_values(ascending=False))
 
#
```
Based on the above, Five months give me the chance to see 4 of my favorite species. I should go birdwatching in Rock Creek Park during  March, April, August, September, or October!

Thanks for taking a peek into the world of bird watching, and learning more about some of my favorite species. If you'd like continue the bird fun...

- [x] Learn Mia's favorite bird species (congrats, you did this!)
- [ ] [Explore the eBird website tutorial on birdwatching](https://ebird.org/about/resources "Explore the eBird website tutorial on birdwatching")
- [ ] [Look for your local birding hotspots](https://ebird.org/hotspots "Look for your local birding hotspots") 

Until next time! 🫡 🐦

[^1]: (As of September 10th, 2026), accessed here:[Rock Creek Park eBird Checklists](https://ebird.org/hotspot/L599606/bird-list?yr=cur "Rock Creek Park eBird Checklists")
[^2]: (As of September 10th, 2026), accessed here:[Rock Creek Park eBird Bird Observation Histograms](https://ebird.org/barchart?byr=2026&eyr=2026&bmo=1&emo=12&r=L599606 "Rock Creek Park eBird Bird Observation Histograms")




