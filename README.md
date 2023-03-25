# EDUC450B Video Analysis



This is the repository that stores my attempts at quantitative video data analysis using `FFmpeg` and `R`. 

I am using MacOS, and the troubleshooting and instructions below might not work for the other OSs. 

## FFmpeg

FFmpeg is a free and open-source software for handling videos. It is a cross-platform command line tool. Some of its helpful functions are included in [this website](https://www.labnol.org/internet/useful-ffmpeg-commands/28490/). [This Youtube video](https://www.youtube.com/watch?v=MPV7JXTWPWI) also did an awesome job explaining its main features.

### Installing FFmpeg

Solution 1: 

Use `homebrew` to install `FFmpeg` in the terminal
```
brew install ffmpeg
```
Then, copy the installed folder to the directory `/usr/local/bin`. 

Solution 2: 

Download the software from [the official website](https://ffmpeg.org/download.html).

Follow the instructions in the `INSTALL.md` document.

Then, copy the installed folder to the directory `/usr/local/bin`. 


## R

To work with video data in R, install `imager`:

```
install.packages("imager")
```
*if having problems with loading `imager`, try installing [xQuartz](https://www.xquartz.org/) first.*

`imager` manipulates video data by using FFmpeg. Reset the path of R to include a path to `FFmpeg`. For me, typing this in the R console works:

```
Sys.setenv(PATH = paste("/usr/local/bin/ffmpeg", Sys.getenv("PATH"), sep=":"))
```
