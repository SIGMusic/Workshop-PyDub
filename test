import sys
import os

sys.path.insert(0, "/usr/local/lib/python3.7/site-packages")
from pydub import AudioSegment
# print(os.getcwd())


song = AudioSegment.from_mp3("favela.mp3") # importing the mp3
ten_seconds = 10 * 1000;                   # pydub does things in milliseconds
first_10_seconds = song[:ten_seconds]      #getting the first 10 seconds of song
last_5_seconds = song[-5000:]              #getting the last 5 seconds of a song

beginning = first_10_seconds + 6           #increasing the volume of the beginning
end = last_5_seconds - 3                   #decreasing the volume of the end
without_the_middle = beginning + end       #concatenating two clips

backwards = song.reverse()                 #reversing audio, does not change original audio
with_style = beginning.append(end, crossfade=1500)      #crossfade styling


do_it_over = with_style * 2                #repeat clip twice
awesome = do_it_over.fade_in(2000).fade_out(3000)
awesome1 = awesome.reverse()
awesome1.export("mashup1.mp3", format="mp3")
