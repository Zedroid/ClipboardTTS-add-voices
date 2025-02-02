﻿# ClipboardTTS
 
ADD VOICES
microsoft Richard Canadian could be enabled as Voice = "Microsoft Richard" in clipboardTTS

https://www.ghacks.net/2018/08/11/unlock-all-windows-10-tts-voices-system-wide-to-get-more-of-them/

Activate Text-to-Speech with ` or Pause
Kill Text-to-Speech with Shift+` or Shift+Pause
copy text first

https://www.autohotkey.com/boards/viewtopic.php?style=1&f=76&t=105150


Send the text in your Clipboard to Microsoft's Text-to-Speech Engine. Useful for Visual Novel Text Hookers that send foreign game text to the clipboard. Can be easily launched via an AutoHotkey script.

## Getting Started

On the first program run a "ClipboardTTS.settings" file will be created. It will list all your installed voices, you can uncomment the voice you want.

## Settings

Settings should be rather self explanitory. 

Lines that start with a semicolon are comments and are ignored. The first time you run the program, all the installed **voices** will be listed. Just uncomment the voice you want to use.

    ;Voice = "Microsoft David Desktop"
    ;Voice = "Microsoft Zira Desktop"
    Voice = "Microsoft Eva Mobile"

The **Volume** and **Rate** of Speech settings are simple numeric values.

    ;Volume 0...100
    Volume = 100
    
    ;Rate -10...10
    Rate = 0

**CharLimit** will limit the number of character's processed. Just in case you send it a book full of words and didn't actually want to listen to it all.

    ;Max Character Limit (0 = Unlimited)
    CharLimit = 500

The **Substitutions** section allows you to replace words before they are processed by the speech engine.

    [Substitutions]
    OriginalWord => ReplacementWord


If the speach engine detects extra line returns, it will add a pause to the spoken dialog, this **RemoveLineReturns** setting will remove the extra pause.

	;Remove unwanted pause from Line Returns
	RemoveLineReturns = "true"

**WavePrefix* setting will set the prefix for output to wav files
	WavePrefix = "Audio_TTS "

## Command line parameters
Output to Wave file:
	-w or -w:filename.wav
