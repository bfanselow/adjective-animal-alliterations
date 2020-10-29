# "Adjective Animal" Allliterations

### Create random lists of "adjective animal" combinations where both start with a specified letter

#### Scriptname: *laughing_lemur.py*

#### Basic processing logic
  * Grab list of animals from static dict having specified first letter
  * Query datamuse API for list of dictionary words having the same specified first letter
  * Pull out only those words which are *adjectives* (API does not provide for this filtering)
  * Perform a random shuffle on the ordering of both lists
  * Iterate over the list (up to a max of the smaller of the two lists) and combine an adjective with an animal
  * Output the desired number of combinations
  * Optionally generate a table showing both full lists
  
**Since the combinations are created with a random shuffling of both lists, the output will be totally different each time the script is run.**

#### Usage:
```
  $ laughing_lemur.py <LETTER>
     Example: 
      $ laughing_lemur.py B  --->  "brave baboon"
     Optional args: 
       --list <N>: create a list of <N> "adjective animal" alliterations 
       --show: show all animals and adjectives for the specified letter 
 ```

#### Setup/requirements
```
 $ python3 -m venv venv
 $ . venv/bin/activate
 (venv) $ pip install requests
```

#### External Resources:
 * **Adjectives**: https://www.datamuse.com/api - Free api for various word queries.
 
 * **Animals**:    https://a-z-animals.com/animals -  Did a one-time beautiful-soup scrap 
                    of this site to generate a static dictionary contained within this file 
                    for simplicity.

---

#### Examples:
```
(venv) wfanselow % ./laughing_lemur.py P -l 10
posted porpoise
pondering platypus
plaintive pony
plantar piranha
pleasurable porcupine
postural penguin
placed prairie-dog
postoperative pika
porcine puma
posterior pheasant

(venv) wfanselow % ./laughing_lemur.py P -l 50
WARNING: Full animal list for letter (P) is smaller than your requested list size
powerful pademelon
plenary partridge
pointing pig
pleased prairie-dog
poky polar-bear
platitudinous porcupine
positive pony
powered peafowl
pouring piranha
placental penguin
populated pelican
potted porpoise
postural pika
pleated pheasant
polymeric poodle
polymorphous platypus
podgy pigeon
polyphonic puffin
plagued puma
polysyllabic panther
plastered parrot
```
