# 100 Days Of Code - Log

### Day 1: Jan 1, 2017

**Today's Progress**: 
Getting back [Vuejs + GDrive](https://github.com/tralves/vue-gdrive) project going!
- Created [trello board](https://trello.com/b/wU4VFN4E/vue-gdrive-markdown-editor) and configured [pomello](http://pomelloapp.com/).
- Removing references to xgz. This was the file extension I picked when I wanted this project to be an exegesis tool. The first stage of this app, however, will be a collaborative markdown editor.
- Continuing converting from vuex1 to vuex2.

**Thoughts:** Trying to making some automated tests, but I can't call this TDD...

**Link to work:** [Vuejs + GDrive](https://github.com/tralves/vue-gdrive)


### Day 2: Jan 2, 2017

**Today's Progress**: 
Fixed [issue #6](https://github.com/tralves/raspi-soft-pwm/issues/6) in [raspi-soft-pwm](https://github.com/tralves/raspi-soft-pwm). Bumped lib version to 2.0.2.

**Link to work:** [raspi-soft-pwm](https://github.com/tralves/raspi-soft-pwm)

### Day 3: Jan 3, 2017

**Today's Progress**: Solving bug in JS testing where asserts in one test are being executed in another test.
Testing [Weex-Hakernews](https://github.com/weexteam/weex-hackernews). A Weex+Vue2 demo project!

**Thoughts** Testing JS is hard...

### Day 4: Jan 4, 2017

**Today's Progress**: Tests now work accordingly.

"Unforked" this project so editing this log counts as contributions. Yesterday I did relevant coding, but it did't count as contributions because I commited to a `dev` branch and to a forked project, which doesn't make the day green...

How to "unfork" a project:

1. `git clone --bare https://github.com/tralves/100-days-of-code`
2. Deleted original repository in https://github.com/tralves/100-days-of-code/settings.
3. `cd 100-days-of-code.git` and `git push --mirror https://github.com/tralves/100-days-of-code`

**Thoughts** Testing JS is still hard... There seems to be a lot of interest around Weex. I could make a small test app in Weex...

### Day 5: Jan 5, 2017

**Today's Progress**: Finished tests for CreateOpenFileDialog.js.

### Day 6: Jan 6, 2017

**Today's Progress**: Vuex2 in PageHeader.vue and App.vue. Change url on file create/load.

### Day 7: Jan 7, 2017

**Today's Progress**: Fixed share button. Started refactor to use service classes instead of spreading logic in the components and actions.

**Thoughts** Don't mock wht you don't own! [see this video](https://www.google.com.br/url?sa=t&rct=j&q=&esrc=s&source=web&cd=4&cad=rja&uact=8&ved=0ahUKEwiixMCz1LHRAhVGiZAKHQFYCqgQFggxMAM&url=https%3A%2F%2Fadamwathan.me%2F2017%2F01%2F02%2Fdont-mock-what-you-dont-own%2F&usg=AFQjCNGxU7uhDPvLSN0S1lK9fg9f2uujVw&sig2=eqoZLCVRRBln8fXW37IHIg)

### Day 8: Jan 8, 2017

**Today's Progress**: Developing services/file. 

**Thoughts** Testing with JS is hard mostly because the errors are very cryptic. Today, the problem was testing a function that returns a promise. Nailed it thanks to [this article](https://www.sitepoint.com/promises-in-javascript-unit-tests-the-definitive-guide/).

### Day 9: Jan 9, 2017

**Today's Progress**: Finished services/file. With unit testing!

**Thoughts** Starting to rip some fruits of TDD. Helped doing several refactors to services/file.

### Day 10: Jan 10, 2017

**Today's Progress**: Refactored side menu to its own component. A bit of test refactoring.

**Thoughts** The `services/file.js` is a nice helper between the components and actions to manage some complex operations. I decided not to use it for *every* operation just for the sake of creating yet another layer. Some operations already go through:
```
Component > service > action > mutation
```
4 layers!

### Day 11: Jan 11, 2017

**Today's Progress**: Refactored side menu to its own component. A bit of test refactoring.
I got the realtime collaboration working on my project! 

**Thoughts** It was hard, google documentation sucks a bit, but I did it!
In one night (it's 4am here), after a day of coding and leading youth group.

I deserve the rest of the brave. Good night!

### Day 12: Jan 12, 2017

**Today's Progress**: Since yesterday I stayed up to 4am, today, I just read de Google Realtime API in preparation for future developments.

<!---
### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence)
-->
