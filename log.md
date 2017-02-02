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

### Day 13: Jan 17, 2017

**Today's Progress**: I'm on vacations (sunny beach, coconut water, etc.)! Still, I found some time to develop the bitcoin-bargainer!

The bitcoin-bargainer is a node service that monitors the bitcointoyou buy/sell prices in order to determine moments to buy/sell bitcoins. The idea was to take advantage of the rapid fluctuations in bitcoin value. The service will start with 0.1BTC and will sell it when it will make more money than the initial value. Then it will buy BTC, then sell, then buy, etc.


### Day 14: Jan 18, 2017

**Today's Progress**: Some improvements on the bitcoin-bargainer. Better logs, bug fixes. 

**Thoughts** Turns out that the btc price doesn't fluctuate that much... It never triggers pruchases/sales. :(

### Day 15: Jan 24, 2017

**Today's Progress**: Adapted the bitcoin bargainer to accept parameters determine the initial BTC value and choose whether to use trade BTC or Litecoin.

### Day 16: Jan 25, 2017

**Today's Progress**: Back to the [Vuejs + GDrive](https://github.com/tralves/vue-gdrive) project! Cleaned a bit of the realtime hacked code. Realtime now works when creating the file. Fixed tests.

**Thoughts** I am not happy with my tests. They are too verbose and too tight to the implementation. Hum... I wonder if they would be better if I had Dependency Injection... Why is it so much easier in Laravel?!

### Day 17: Jan 26, 2017

**Today's Progress**: My wife forbid my from doing anything after 1am. Still, I read somethings about Dependency Injection and gave a lot of thought about the arquitecture of the app. That `services/files` and `actions.js` are very interdependent and they both use the GAPI... it smells...

### Day 18: Jan 27, 2017

**Today's Progress**: Started a small Slack bot project that sends "#TRIGGERED" when someone says something on a channel that should trigger me. Using Laravel and Valet.

### Day 19: Jan 28, 2017

**Today's Progress**: Back to the Vue GDrive thing. Working on saving the document and synchronizing the realtime model with the GDrive file.

**Thoughts** The Realtime document is always updated, so I am using it as the primary source of truth. Then, the session that makes a change will save to the gdrive after some idle time.

### Day 20: Jan 30, 2017

**Today's Progress**: Renaming files with realtime sync.

### Day 21: Feb 1, 2017

**Today's Progress**: Retrieve realtime collaborators, and keep them synced in the vuex store.

<!---
### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence)
-->
