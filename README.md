<!--
author:   André Dietrich, Sebastian Zug, Mark Jacob

email:    LiaScript@web.de

version:  1.0.0

language: en

narrator: US English Female

comment:  LiaScript presentation on OER and sustainability at the OER22
          conference in London.

import: https://raw.githubusercontent.com/liaTemplates/AVR8js/main/README.md

-->

































# Open-courSe web development with LiaScript Markdown


https://github.com/LiaPlayground/OER22

[qr-code](https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/OER22/main/README.md)

https://liascript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/OER22/main/README.md










































## Markdown --> Static text

[Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)  was initially created by John Gruber in 2004 for fast blogging.

1. ~~**Lists**~~
2. ordered or

   * unordered
   * ones ...


| Tables          |        in         |                 Markdown |
|:--------------- |:-----------------:| ------------------------:|
| are             |        ...        |               ___cool___ |
| and can contain | nearly everything | $ f(x) = \frac{1}{x^2} $ |

Images:

![images](https://farm2.static.flickr.com/1618/26701766821_7bea494826.jpg)































## LiaScript --> Interacitivity

















































### Multimedia

![Photo of Jupiter](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Latest_NASA_photo_of_Jupiter_taken_this_Sunday_by_the_Juno_probe.png/1280px-Latest_NASA_photo_of_Jupiter_taken_this_Sunday_by_the_Juno_probe.png)
?[hear a horse](https://www.w3schools.com/html/horse.mp3 "hear a horse")
!?[Fun with Tables](https://www.youtube.com/watch?v=Y_7q9T5jYHo)
??[VTK VolumeContour](https://kitware.github.io/vtk-js/examples/VolumeContour/index.html)
??[Circuit simulation](https://www.falstad.com/circuit/circuitjs.html?startCircuit=majority.txt)
??[Bust of Nefertiti](https://sketchfab.com/3d-models/bust-of-nefertiti-foia-results-8c60faca6152405e9d35784efa8b9aa1)





































### Presentation formats

    --{{0}}--
But you can also include other features such as spoken text.

    --{{1}}--
Reveal Additional content:

      {{1}}
> “Live as if you were to die tomorrow.
> Learn as if you were to live forever.”
>
> -- Mahatma Gandhi

    --{{2}}--
Reveal and hiding is also possible:

     {{2-4}}
Animations work also __inline__: {3 |> Deutsch Male}{Schöne Grüße aus Freiberg.}


    --{{4 Ukrainian Female}}--
Первоначально создан в 2004 году Джоном Грубером (англ. John Gruber) и Аароном
Шварцем. Многие идеи языка были позаимствованы из существующих соглашений по
разметке текста в электронных письмах...

    {{4}}
Type "voice" to see a list of all available languages.






















### Quizzes

alsjfdaslkf

[[X]] ja
[[ ]] no
[[ ]] adfasf

[( )] asdfsa
[(X)] asfsd
[[?]] hint 1
[[?]] hint 2
********************************

afdasda

$$
   \sum_{i=1}^\infty\frac{1}{n^2}
        =\frac{\pi^2}{6}
$$

********************************










































### Surveys

















































### Textbased images



#### Tables


| Animal          | weight in kg | Lifespan years | Mitogen |
| --------------- | ------------:| --------------:| -------:|
| Mouse           |        0.028 |              2 |      95 |
| Flying squirrel |        0.085 |             15 |      50 |
| Brown bat       |        0.020 |             30 |      10 |
| Sheep           |           90 |             12 |      95 |
| Human           |           68 |             70 |      10 |


#### Diagrams


                                Multiline
1.9 |
    |                 ***                  (* main curve)
  y |               *     *
  - | r r r r r r r*r r r r*r r r r r r r
  a |             *         *
  x |            *           *
  i | B B B B B * B B B B B B * B B B B B
  s |         *                 *
    | *  * *                       * *  *
 -1 +------------------------------------
    0              x-axis               1


#### ASCII-Art



```` ascii
   ____[]
  | ___ |
  ||   ||  device
  ||___||  loads
  | ooo |----------------------------------------------------------.
  | ooo |    |                          |                          |
  | ooo |    |                          |                          |
  '_____'    |                          |                          |
             |                          |                          |
             v                          v                          v
   .-------------------.  .---------------------------.  .-------------------.
   | Loadable module C |  |     Loadable module A     |  | Loadable module B |
   '-------------------'  |---------------------------|  |   (instrumented)  |
             |            |         .-----.           |  '-------------------'
             '------------+-------->| A.o |           |             |
                 calls    |         '-----'           |             |
                          |    .------------------.   |             |
                          |   / A.instrumented.o /<---+-------------'
                          |  '------------------'     |    calls
                          '---------------------------'
````







#### Interacitivity


The first value defines some kind of range:
<script input="range" value="2" output="range">@input</script>
, while the second can be interpreted as range
<script input="range" value="50" output="amplitude">@input</script>.
You can double-click on any gray element to inspect and edit its javascript code.


<script run-once style="display: inline-block; width: 100%">
function func(x) {
    x /= 10;
    return Math.sin(x) * Math.cos(x * @input(`range`) + 1) * Math.sin(x * 3 + 2) * @input(`amplitude`);
}

function generateData() {
    let data = [];
    for (let i = -200; i <= 200; i += 0.1) {
        data.push([i, func(i)]);
    }
    return data;
}

let option = {
    animation: false,
    grid: {
        top: 40,
        left: 50,
        right: 40,
        bottom: 50
    },
    xAxis: {
        name: 'x',
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    yAxis: {
        name: 'y',
        min: -100,
        max: 100,
        minorTick: {
            show: true
        },
        splitLine: {
            lineStyle: {
                color: '#999'
            }
        },
        minorSplitLine: {
            show: true,
            lineStyle: {
                color: '#ddd'
            }
        }
    },
    dataZoom: [{
        show: true,
        type: 'inside',
        filterMode: 'none',
        xAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }, {
        show: true,
        type: 'inside',
        filterMode: 'none',
        yAxisIndex: [0],
        startValue: -20,
        endValue: 20
    }],
    series: [
        {
            type: 'line',
            showSymbol: false,
            clip: true,
            data: generateData()
        }
    ]
}

"HTML: <lia-chart option='" + JSON.stringify(option) + "'></lia-chart>"

</script>


































### Extendability

https://github.com/topics/liascript-template

<div id="example">
<wokwi-led color="red"   pin="13" label="13"></wokwi-led>
<wokwi-led color="green" pin="12" label="12"></wokwi-led>
<wokwi-led color="blue"  pin="11" label="11"></wokwi-led>
<wokwi-led color="blue"  pin="10" label="10"></wokwi-led>
<span id="simulation-time"></span>
</div>

``` cpp
byte leds[] = {13, 12, 11, 10};
void setup() {
  Serial.begin(115200);
  for (byte i = 0; i < sizeof(leds); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

int i = 0;
void loop() {
  Serial.print("LED: ");
  Serial.println(i);
  digitalWrite(leds[i], HIGH);
  delay(250);
  digitalWrite(leds[i], LOW);
  i = (i + 1) % sizeof(leds);
}
```
@AVR8js.sketch(example)



























## Problems in OER

<div style="width:100%;height:0;padding-bottom:100%;position:relative;"><iframe src="https://giphy.com/embed/XASpmEbRCZV4pgQOIG" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/weareeverise-edtech-elearning-educationtechnologyday-XASpmEbRCZV4pgQOIG">via GIPHY</a></p>


### Content last

![FeaturePhone](./pic/nokia.jpeg)


### Authoring & Community

<div style="width:100%;height:0;padding-bottom:75%;position:relative;"><iframe src="https://giphy.com/embed/qgQUggAC3Pfv687qPC" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/dommespace-domme-space-programador-qgQUggAC3Pfv687qPC">via GIPHY</a></p>


### Sustainability

![Adresse nicht gefunden](pic/AdresseNichtGefunden.png "Source: ['Adresse nicht gefunden' – Auf den digitalen Spuren der E-Teaching-Förderprojekte](https://www.pedocs.de/volltexte/2011/3215/pdf/Haug_Wedekind_Adresse_nicht_gefunden_D_A.pdf)")


### Dissemination & Hosting

`https://liascript.github.io/course/?YOUR_COURSE_URL.md`

{{1}}
* ### Plattforms with Version-Control:

  1. [GitHub](https://github.com)
  2. [GitLab](https://gitlab.com)
  3. ...

{{2}}
* ### Web 3.0 with Browser-Support

  1. [Brave-Browser](https://brave.com) with [IPFS](https://ipfs.io)
  2. [Beaker-Browser](https://beakerbrowser.com) with [Hyper](https://hypercore-protocol.org)
  3. ...

{{3}}
* ### Online stores

  1. [DropBox](https://www.dropbox.com)
  2. [NextCloud](https://nextcloud.com/)
  3. ... any ordinary webstore

{{4}}
* ### Collaborative online editors ...

  1. [CodiLia](https://github.com/liascript/codilia)
  2. ...

{{5}}
> __TODO:__ Create an Android App
>
> https://www.npmjs.com/package/@liascript/exporter


## Additional Resources

* __Project-Website:__ https://LiaScript.github.io
* __Open-Source:__ https://github.com/liascript
* __YouTube:__ https://www.youtube.com/channel/UCyiTe2GkW_u05HSdvUblGYg
* __Additional resources:__

  - Documentation: https://github.com/LiaScript/docs
  - Courses: https://github.com/topics/liascript-course
  - Templates: https://github.com/topics/liascript-template
  - Blog: https://aizac.herokuapp.com

* __Editor:__ https://atom.io

  - Liascript-Preview: https://atom.io/packages/liascript-preview
  - Liascript-Snippets: https://atom.io/packages/liascript-snippets

* __Development-Server:__ https://www.npmjs.com/package/@liascript/devserver
