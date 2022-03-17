# :zap: Javascript Video Speed Controller

* Wes Bos Youtube Tutorial: [Build a Experimental Video Speed Controller UI - #JavaScript30 28/30](https://www.youtube.com/watch?v=8gYN_EDMg_M&index=28&list=PLu8EoSxDXHP6CGK4YVJhL_VWetA865GOH).
* **Note:** to open web links in a new window use: _ctrl+click on link_

![GitHub repo size](https://img.shields.io/github/repo-size/AndrewJBateman/javascript-video-speedcontroller?style=plastic)
![GitHub pull requests](https://img.shields.io/github/issues-pr/AndrewJBateman/javascript-video-speedcontroller?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/AndrewJBateman/javascript-video-speedcontroller?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/AndrewJBateman/javascript-video-speedcontroller?style=plastic)

## :page_facing_up: Table of contents

* [:zap: Javascript Video Speed Controller](#zap-javascript-video-speed-controller)
  * [:page_facing_up: Table of contents](#page_facing_up-table-of-contents)
  * [:books: General info](#books-general-info)
  * [:camera: Screenshots](#camera-screenshots)
  * [:signal_strength: Technologies](#signal_strength-technologies)
  * [:floppy_disk: Setup](#floppy_disk-setup)
  * [:computer: Code Examples](#computer-code-examples)
  * [:cool: Features](#cool-features)
  * [:clipboard: Status & To-Do List](#clipboard-status--to-do-list)
  * [:clap: Inspiration](#clap-inspiration)
  * [:file_folder: License](#file_folder-license)
  * [:envelope: Contact](#envelope-contact)

## :books: General info

* Tutorial Code using javascript to adjust the speed of a video via rhs bar vertical position on scale.

## :camera: Screenshots

![Example screenshot](./img/video.png).

## :signal_strength: Technologies

* Ran in Google Chrome browser with: [Javascript engine V8 for Windows (x64)](https://v8.dev/).

## :floppy_disk: Setup

* Open index.html in browser. If any code is changed the browser needs to be refreshed.

## :computer: Code Examples

* Function to convert mouse pos in speed bar to video playback speed and bar video speed display.

```javascript
// measure mouse vertical position, convert to % betwen 0.4 and 4 playback speeds. 
// speed bar height & video playbackrate depend on this value, display a speed to 2dp.
function handleMove(e) {
  const y = e.pageY - this.offsetTop;
  const percent = y / this.offsetHeight;
  const min = 0.4;
  const max = 4;
  const height = Math.round(percent * 100) + '%';
  const playbackRate = percent * (max - min) + min;
  bar.style.height = height;
  bar.textContent = playbackRate.toFixed(2) + 'x';
  video.playbackRate = playbackRate;
};
```

## :cool: Features

* Unsplash background changes daily. Displays video playback to 2 dp.

## :clipboard: Status & To-Do List

* Status: Working.
* To-Do: Nothing.

## :clap: Inspiration

* Wes Bos Youtube Tutorial: [Build a Experimental Video Speed Controller UI - #JavaScript30 28/30](https://www.youtube.com/watch?v=8gYN_EDMg_M&index=28&list=PLu8EoSxDXHP6CGK4YVJhL_VWetA865GOH).

## :file_folder: License

* N/A

## :envelope: Contact

* Repo created by [ABateman](https://github.com/AndrewJBateman), email: gomezbateman@yahoo.com
