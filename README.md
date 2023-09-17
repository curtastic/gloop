# gloop.js
Fixes your game loop to a certain FPS.

# Features:
- Set your desired FPS and it will run your updateFunc() that many times per second.
- If lagging it will skip draws, to make your updateFunc() always run at the same speed on any device.
- If the device can render 120 FPS and your game is set to 60, this will make sure it doesn't run extra fast on those devices.
- Get the current FPS the game is rendering at. (gloop.dps)
- Supports old devices/browsers including IE11 and iOS9.
# Does not include:
- No delta timing. This is because delta timing can result in different outcomes on slow devices, such as bullets skipping through enemies.

# Example:
```
<html>
	<body>
		<script src="gloop.js"></script>
<script>
var playerX = 0
function updateGame() {
  playerX++
}
function drawGame() {
  console.log(playerX)
}
gloop.start(updateGame, drawGame, 60)
</script>
	</body>
</html>
```
