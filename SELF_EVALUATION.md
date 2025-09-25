# Self-Evaluation: Emoji Vacation

## Checklist

### Correctness

- [X] Image background shows trees 60% of the time, and mountains 50% of the time (mountains and trees may both appear in one image)
- [X] The program draws a “family” of emojis, containing a number of emojis based on the parameters to `createFamily()`
- [X] Each emoji in the family is randomly selected, based on your implementation of `createRandomEmoji()`
- [X] When run, your program iterates through an endless slideshow of these emoji photos, each with randomized backgrounds and emoji styles
  - [X] There is a pause for three seconds on each image so that a viewer may enjoy the slideshow!
- [ ] (Optional) Additional randomly-selected background scenery
- [ ] (Optional) A dark transition between each slide of the slideshow
- [ ] (Optional) Child and adult emojis are shown in a random order
- [ ] (Optional) Modify the background to include multiple times of day in the random scenery

### Code Style

Check these items from the [Comp 127 Style Guide](https://comp127.innig.net/resources/style-guide/):

- [X] all classes are in packages
- [X] package names start with a lowercase letter
- [X] newly created Java files have a header comment with
    - [ ] author name
    - [ ] brief description of class, and
    - [ ] acknowledgement, if appropriate
- [X] identifier (variable and method) names are descriptive
- [X] variable and method names are in lowerCamelCase (no CapitalizedNames,
  names_with_underscores)
- [X] class names are singular nouns
- [X] class names are in UpperCamelCase
- [X] proper indentation:
    - [X] opening curly braces (“{”) are at the end of the line
    - [X] closing curly braces (“}”) are on their own line
    - [X] the indentation of closing braces is the same as the indentation of the
      opening statements they match
    - [X] lines are indented according to how deeply they are nested
- [X] completed TODOs are deleted
- [X] extra blank lines are deleted
- [X] unneeded commented lines of code are deleted
- [X] print statements used for testing are deleted


## Reflection

Briefly reflect in writing on your experience solving this exercise. Just a
sentence or two in response to each question is plenty.

**What did you miss? What did you wish you did better?**
At first, I forgot that I had to delete the to-do comments but now that I've read self-evaluation I did so.


**What challenges did you face, and how did you overcome them?**
The canvas.pause(3000) method working before generateVacationPhoto() back in exercise 8 froze the slideshow. I used javax.swing Timer to take advantage of its design which waits till commands are executed until moving on to next lines of code. 


**What is something that was interesting or exciting, or a lesson you learned
  from this experience that you want to remember?**
It was exciting to watch the slideshow! It's cool that all of it feels so alive when there was nothing but code involved.