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

### Day 22: Feb 2, 2017

**Today's Progress**: Show collaborator list in UI.

**Thoughts** Vue.js is sweeet...

### Day 23: Feb 5, 2017

**Today's Progress**: Creating and managing cursor mapping. Synchronizing a list of cursors to the Vuex store.

### Day 24: Feb 6, 2017

**Today's Progress**: Drawing the cursors.

### Day 25: Feb 7, 2017

**Today's Progress**: Added tooltip to cursors.

### Day 26: Feb 9, 2017

**Today's Progress**: Fixed synchronization and GAPI issues.

### Day 27: Feb 11, 2017

**Today's Progress**: Fixed path bugs when the app in not in the root of the domain.

### Day 28: Feb 12, 2017

**Today's Progress**: Fixed file rename, ask fewer permissions, improved error feedback. Aaaaand Vue-gdrive finished! (for now). The phase 1 of the project is now concluded. [Vuejs + GDrive](https://github.com/tralves/vue-gdrive) is a simple text editor with collaboration! When/if I have more time, I would like to:

- Add funcionality to save to a specific folder;
- Reduce coupling of the modules `GapiIntegration`, `services/file.js` and `actions.js`;
- Better test coverage...

Starting phase 2: making a collaborative markdown editor. To complete this project, I will grab [Vuejs + GDrive](https://github.com/tralves/vue-gdrive) and then:

- Configure new google drive app to edit markdown files (.md)- DONE!;
- Add markdown render;

### Day 29: Feb 13, 2017

**Today's Progress**: Added the markdown parser and the project is finished (for now). 

**Thoughts** There are lot's of things to fix/add/improve. Maybe I could turn this into a real usable product! But for now, I'll leave it at that... Time for the next project: something in Weex!

**Link(s) to work**
1. [Collaborative Markdown Editor](https://tralves.github.io/collaborative-markdown-editor)

### Day 30: Feb 14, 2017

**Today's Progress**: Starting new weex project. Writting a Hello World app. PR'd the `weex-toolkit` project!

**Thoughts** Gotta make a Medium post out of this... Weex is just starting, with most of the devs and docs being in China. There is an opportunity to help this project in the western world. I know Vue and have developed both android and iOS native apps. I am the man for the job... Weex is gonna be YUGE!

### Day 31: Feb 15, 2017

**Today's Progress**: Continue pushing the Weex project. Reading about `weex-toolkit`.

### Day 32: Feb 16, 2017

**Today's Progress**: Continue pushing the Weex project. Experimenting with `weex-pack`.

### Day 33: Feb 17, 2017

**Today's Progress**: Continuing experimenting with `weex-pack`. The most updated branch seems to be `vue2.0`.

### Day 34: Feb 22, 2017

**Today's Progress**: Built a built a To-do app with Weex + Vue2.0! Currently it does not save the state and only works in android/web.

**Thoughts** Gave up trying to find the correct way to create a weex project and just downloaded the hackernews weex app and hacked it.

Next steps:

- make it work in iOS;
- save data in internal storage;
- store data in the cloud (Firebase, maybe?)
- write Medium post about the current state of Weex

**Link(s) to work**

- Vid: https://www.youtube.com/watch?v=AMU0gXuEl_Y
- GitHub: https://github.com/tralves/weex-todo-list

### Day 35: Feb 24, 2017

**Today's Progress**: Pushing on the weex to do app. Fixed the iOS build.

**Link(s) to work** The iOS demo video: https://www.youtube.com/watch?v=4L4ABYDhpsA

### Day 36: Feb 25, 2017

**Today's Progress**: Save/load the To do items in storage in the weex todo list.

### Day 37: Feb 27, 2017

**Today's Progress**: Writting a Medium post about the state of weex.

### Day 38: Mar 1, 2017

**Today's Progress**: Trying a new weex project with [incubator-weex](https://github.com/apache/incubator-weex) project. Scheduled the first Vue.js @ BH meetup!

### Day 39: Mar 3, 2017

**Today's Progress**: Still trying to figure out [incubator-weex](https://github.com/apache/incubator-weex)... I don't even know what it does! :(

### Day 40: Mar 4, 2017

**Today's Progress**: Worked on the bitcoin-bargainer. It now stores information on an sqlite db and... IT IS NOW LIVE! It trades bitcoin with my REAL money!

### Day 41: Mar 5, 2017

**Today's Progress**: More tests with [incubator-weex](https://github.com/apache/incubator-weex) and weexpack.

### Day 42: Mar 7, 2017

**Today's Progress**: A little code pen of a procedural generated tree drawn and animated with canvas.

**Link(s) to work**
1. http://codepen.io/tralves/pen/EWgOxR

### Day 43: Mar 8, 2017

**Today's Progress**: More tests with [incubator-weex](https://github.com/apache/incubator-weex) and weexpack.

### Day 44: Mar 9, 2017

**Today's Progress**: Registered domain (http://www.tiagoalves.co) and set a site as a placeholder for something better. Also registered a Linode account. Interwebs, here I go!

### Day 45: Mar 10, 2017

**Today's Progress**: Fixed some bugs in the bit-bargainer.

### Day 46: Mar 11, 2017

**Today's Progress**: created a linode machine. Moved bit-bargainer there. Configured nginx and php7.1.

### Day 47: Mar 12, 2017

**Today's Progress**: Fixed bug in bit-bargainer. Worked on setting the first Vue.js @ Belo Horizonte meetup!

### Day 48: Mar 13, 2017

**Today's Progress**: Learning more about weex. Inspecting and compiling WeexSDK. Collected some evidence in [this tweet](https://twitter.com/tiagoreisalves/status/841504371015860224)

## Day 49: Mar 20, 2017

**Today's Progress**: Learning more about weex. Someone has to make the tool to add native platforms to Vue 2 projects... That will be me...
<!---
### Day 1: June 27, Monday

**Today's Progress**: I've gone through many exercises on FreeCodeCamp.

**Thoughts** I've recently started coding, and it's a great feeling when I finally solve an algorithm challenge after a lot of attempts and hours spent.

**Link(s) to work**
1. [Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string)
2. [Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence)
-->
