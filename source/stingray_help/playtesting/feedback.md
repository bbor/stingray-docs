# Ways to get runtime feedback

Stingray provides several different ways for you to get feedback about what is happening in your game. You will probably find it necessary to use many if not all of these methods at different times during your development. Each one may be more convenient than the others, depending on how your gameplay is written, what subsystems of the engine you need to get feedback about, and what kind of information you hope to get.

## The **Log Console**

The **Log Console** shows you all the errors, warnings and information messages written to the Stingray log by all connected instances of the Stingray engine. It's a good idea to get in the habit of watching the log to keep an eye on the engine's activity. When something goes wrong, this log is the first place to look for a hint.

See ~{ Log Console }~.

## In-game HUDs

The Stingray engine has some built-in systems that display diagnostic messages and render debug information in the viewport of the running game. You can use these systems to print performance statistics, visualize performance as a graph, or to debug subsystems like physics and particles.

![In-game HUD for art statistics](../images/perfhud_artist.png)

You toggle the display of these diagnostic systems by sending console commands to the game from the Status bar of the Stingray Editor, or from the **External Console** application (**Window > External Console**).

For details, see ~{ Send commands from the Status bar }~.

For a list of all console commands, see ~{ Console commands }~. In particular, look for the useful `perfhud`, `graph`, and `physics` commands.

### HUDs in the Stingray Editor

While you're working in the Stingray Editor, you can turn the HUDs on in your editor viewport. This shows the performance of the instance of the game engine that is run internally by the editor, powering the viewport display.

Click **View > Performance Hud** in the viewport's visualization settings, and select the HUD you're interested in.

To debug or view performance statistics of a deployed package, use the **External Console** application and connect to **localhost** instead of the default IP address.

## Print to screen from Flow

If you are using the Appkit, you have access to the **Debug > Print To Screen** Flow node. When this node is evaluated, it prints text that you specify to the screen in game. The Flow system does not currently have a runtime debugger, but you can use this node to find out the current state of your variables and to detect what paths your graph evaluation follows.

## Print to the log from Flow or Lua

You can print your own debug messages to the Stingray log from Flow or Lua. You can view them in the **Log Console** just like any of the other kinds of messages that come from the engine.

-	In Flow, use the **Debug > Debug Print** node. (Unlike the **Debug > Print To Screen** node mentioned above, the **Debug Print** node works regardless of whether or not you use the Appkit in your project.)

-	In Lua, you can call the built-in `print()` function. Messages you send this way will show in the **Log Console** as an information message.

-	You can also use the `stingray.Application.console_send()` function to send an error, warning or information message. For example,

	~~~{lua}
	local message = {
		type="message",
		level="error",
		system="custom",
		message="An error occurred!" }
	stingray.Application.console_send(message)
	~~~

## The Lua debugger

The Stingray Editor features a built-in debugger for your Lua code. You can use this system to set breakpoints, step through your code, and see the values of your variables at runtime.

For details on using this system, see ~{ Debugging Lua }~.
