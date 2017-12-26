---
title: ch22
description: 한양대학교 에리카 ICT융합학부 오픈소스SW기초수업 자료
categories:
 - tutorial
tags:
---


<!-- more -->

## Screenshots

* Image
![Desktop Preview](https://postfiles.pstatic.net/MjAxNzEyMjZfMTEy/MDAxNTE0Mjc2MTQ1NzMw.CBG1xE5_Ys3KtrNkifCpqbeB12Q1sGirIyaS6Hc4ICQg._1grJChz36oBk47Y05R2YoaQ_dAQzCfV04ZjALzDuTIg.JPEG.vv121102/ch22.jpg?type=w773)
![Desktop Preview](https://postfiles.pstatic.net/MjAxNzEyMjZfOTMg/MDAxNTE0Mjc2MjM0OTc3.0yJZZVTZwZFlmGawFC0rgpxS8rKdrIFwMRzBrljIihMg.iZNsunp1PsNm68nUn0kS_NISB2FqASNZszGvweNfWKkg.PNG.vv121102/KakaoTalk_Photo_2017-12-26-17-16-58.png?type=w773)
![Desktop Preview](https://postfiles.pstatic.net/MjAxNzEyMjZfNzUg/MDAxNTE0Mjc2MjM0OTQ0.Yy8qIJ79Le7tcXsfq1ZWcocPL-6J2EVAjIbdLI_6kVMg.YLSeC8PwiDoTfywMc1sC98BTvmNDnZXlsLU4hQ0DDCAg.PNG.vv121102/KakaoTalk_Photo_2017-12-26-17-16-53.png?type=w773)
![Desktop Preview](https://postfiles.pstatic.net/MjAxNzEyMjZfODYg/MDAxNTE0Mjc2MjM3NDE4.fFxEmWIsDyxvfHFnJA0qXuekdS8yADwqx1zb-_TTFxog.DwsB28nKt7e_ZFqoLar0Tfni50mMgFWEe1v7nPO2DScg.JPEG.vv121102/KakaoTalk_Photo_2017-12-26-17-16-33.jpeg?type=w773)

* Code


	import RPi.GPIO as GPIO
	import time
	import vlc
	import LCD

	GPIO.setmode(GPIO.BCM)
	Button
	GPIO.setup(23, GPIO.IN) # Pause button
	GPIO.setup(24, GPIO.IN) # Stop button
	LED// one for pause
	GPIO.setup(27, GPIO.OUT)
	Turn off LED
	GPIO.output(27, False)

	file ="파일주소"
    
    
	instance = vlc.instance()
    
    
	player=instance.media_player_new()
	
    
	media = instance.media_new(file)
	
    
	player.set_media(media)

	player.play()
	time.sleep(1)
    
	while True():
  	  state = player.get_state()
   	  if GPIO.input(23)==0:
		player.pause()
		if state == 3:
   	         GPIO.output(27, False)
   	    elif state == 4:
   	         GPIO.output(27, True)
		time.sleep(1)
  	   	elif GPIO.input(24)==0 and state == 3:
   	    	break
            
* Video

![Desktop Sidebar Preview]
<iframe width="854" height="480" src="https://www.youtube.com/embed/FhJa0tm1bTM" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>
<iframe width="854" height="480" src="https://www.youtube.com/embed/T3NYgEYmuMk" frameborder="0" gesture="media" allow="encrypted-media" allowfullscreen></iframe>
