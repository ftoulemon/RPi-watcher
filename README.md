The goal of this project is to upload a picture to dropbox when a motion is detected by the raspberry pi camera module.


Link to the original repository: https://github.com/andreafabrizi/Dropbox-Uploader

Link to the original motion detector script : http://www.raspberrypi.org/phpBB3/viewtopic.php?t=45235&p=362909

### video time lapse from the pictures

```
cd <directory where the pics are stored>
ls > files.txt
mencoder -nosound -noskip -oac copy -ovc copy -o output.avi -mf fps=10 'mf://@files.txt'
```

If you want to resize the output:

```
ffmpeg -i output.avi -s 640x480 -b 512k -vcodec mpeg1video -acodec copy new.avi
```
