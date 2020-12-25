scene:

start-scene:
button:	continue -> load-scene
	start -> game-scene
	option -> option-scene
	exit -> exit-scene

option-scene:
button:	music vul
	screen solution
	game play: easy/hard
	quality: beautiful

exit-scene:
scroll text -> show thanks and pictures

game-scene: choose level
button:	chapter 1/2/3
	each chapter - level 1/2/3/4/5 -> load-scene

load-scene: load game
load option file
-> game-scene

game-scene:
level 1-1 ~ level 3-5

pause-panel:	resume: back to the game
		save game: save current status
		game setting: change gun color / move speed / music
		select level: select-scene
		main scene: start-scene
		exit game: exit-scene


