# SymmeTri-Keyboard-Layout

![A basic variant of SymmeTri for 104 US-standard keyboard](https://github.com/WesternGun/SymmeTri-Keyboard-Layout/blob/master/preview/preview-ANSI104-bigenter-deadkey-lights.png)
                              (A basic variant of SymmeTri for 104 US-standard keyboard)

This full view is created via [keyboard-layout-editor on Gist](http://www.keyboard-layout-editor.com).


**SymmeTri**, a symmetrical keyboard layout which supports the three most spoken languages in the world: **Chinese, English and Spanish**. The name "SymmeTri" combines **"Symme"** and **"Tri"**, the first part means "Symmetrical", and the second part "Tri", often meaning "Three" when used as prefix, represents the three languages in question.

### 1. Normal use vs. Programming friendly
It has two version: "Normal" and "Programming". The major difference between these two are in the position of keys on the first line of alphanumerical area: "Normal" has number keys 0-9 on the un-shift state, meaning that you enter numbers solely, and enter symbols with shift pressed; while "Programming" has it reversed: you enter symbols without press <kbd>Shift</kbd>, and numbers are typed "shifted". This is to ease the input of these symbols, whose use is more than common in any programming language.

### 2. Symmetrical layout

#### 2.1 Number/Symbol keys line
About these symbols, another thing to stress is that they are all in pairs, and each pair is symmetrically organized, so that we can enter the left half with left hand, and the right half with right hand with the same finger. These simbols include:
 - `{` and `}` (with little finger)
 - `[` and `]` (with ring finger)
 - `(` and `)` (with middle finger)
 - `<` and `>` (with index finger, normal position)
 - `/` and `\` (with index finger, extend to the middle)

And, the corresponding numbers: 
 - `1` and `0`
 - `2` and `9`
 - `3` and `8`
 - `4` and `7`
 - `5` and `6`

#### 2.2 Main alphanumeric area
And, other symbols are also symmetrically layouted to balance two hands' burden. We know that in legacy QWERTY layout, symbols are mainly located at the right side, where only the weakest finger can reach; so the right hand needs to handle more symbols than the left hand, plus manipulating the mouse if you are a right-hander. This layout tries to solve this problem by moving 5 heavily used symbol keys to the middle(in total 10 symbols) so that both hands can type them too, with the most strong finger, the index. For Spanish users, two dead keys are also moved to the middle so they can type them with the index fingers of both hands to balance the burden.

#### 2.3 CapsLock, Enter and Shift
If you take a look into the legacy QWERTY layout, you may begin to see something ridiculous: on the home line where our fingers initially rest, the position at the both edge of main area are occupied by two different keys: on the left, <kbd>CapsLock</kbd>, and on the right side, <kbd>Enter</kbd>. <kbd>LShift</kbd> and <kbd>RShift</kbd>, <kbd>LCtrl</kbd> and <kbd>RCtrl</kbd>, on the other side, are located below. So, the little finger must lower to an unnatural position to press them, which are certainly more heavily used than <kbd>Enter</kbd> and <kbd>CapsLock</kbd>. So I decide to move <kbd>Shift</kbd> to the home line, by switching <kbd>LShift</kbd> with <kbd>CapsLock</kbd>, and <kbd>RShift</kbd> with <kbd>Enter</kbd>, and after that, all start to make sense again: you just extend both little fingers to press the common <kbd>Shift</kbd> key to the left/right side, symmetrically and without lowering, and you can type in upper case.
The reasons why I don't switch <kbd>CapsLock</kbd> and <kbd>Enter</kbd> with <kbd>Ctrl</kbd>, are two:
 - Keys at the corners are more likely to be pressed accidently by you or by others, e.g., by your kid or your cat, so they should not be crucial enough to do things solely. <kbd>Ctrl</kbd> do not trigger any input event when pressed alone, but <kbd>Enter</kbd> and <kbd>CapsLock</kbd> are more likely to trigger "bigger" things.
 - We get used to "<kbd>Ctrl</kbd>/<kbd>Cmd</kbd>+<kbd>Z</kbd>/<kbd>X</kbd>/<kbd>C</kbd>/..." combinations, and when doing it, we just reach for **the key at the corner** to do it by convention, without realizing what keys they are. No need to change this behaviour to make my keyboard layout harder to learn.

But if you want to switch the <kbd>Control</kbd> keys with the <kbd>CapsLock</kbd> and/or <kbd>Enter</kbd>, there are many ways described in the Internet which are compatible with this keyboard layout. You can:
 - Change registry scancode as I have done in this project
 - Change with AutoHotKeys or other softwares.


### 3. Language support
#### 3.1 English
It supports all English letters and the following punctuations in English:
```
{}[]()<>/\?!'"=+`^-_~&%@;:|$#*,.
```
#### 3.2 Spanish
With the help of MSKLC 1.4 in Windows(and `keymap` in Linux), apart from all regular letters in Spanish, we can type special characters with my keyboard layout, such as:
```
á ó é í ú Á Ó É Í Ú
(ä ö ë ï) ü (Ä Ö Ë Ï) Ü
ñ Ñ ç Ç
(ý Ý ÿ)
```
(those in parenthesis are not needed in Spanish, just defined as showcase; if you use other languages and want to define the combination of dead keys to type letters like `Ŝ`, it is possible and allowed.)

Euro sign:
```
€
```
And other punctuations only in Spanish:
```
·¬¡¿ºª´¨«»
```
#### 3.3 Chinese
We can type Chinese with IMEs like *Microsoft Pinyin* or services like `ibus`, `fcinx`, etc. As long as we have all the 26 letters in English, Chinese input with Pinyin is not a problem. And, for punctuations, apart from the English ones, we have:
```
？！{［（《／‘’“”、》）］｝……——～％｜
```
, all in full length.

In Windows, because these punctuations input event are mapped onto virtual keys, they can be obtained directly by pressing the corresponding virtual keys. For example, `……` was mapped to `VK_OEM6`, and in my keyboard layout, this VK code corresponds to the key between `T` and `Y`. The VK code mapping can be changed directly in the `.klc` files used by MSKLC. In Linux this is controlled by key-mapping and IME. Check the `.klc` file under `Windows` to learn more.

### 4. Adaptality: more of a framework than a layout
People may have learn a non-legacy layout like Dvorak, and when they see this, they may think: "Why do I have to learn a new one?" No, you really don't have to. 

When you use this keyboard layout, you just move your right hand one column to the right, and you are done with all letter keys, because the map of letter keys is the same as legacy QWERTY keyboard! And a little more time to remember the symbol keys' position, but that's easy: it took me 2 hours to get familiar to all keys. No more.

Those who are already masters of Dvorak/Colemak, etc., what I want to say is: **you can adapt my keyboard layout to create one of yourself, because SymmeTri allows you to seamless transfer from your favourite layout to it, as long as yours only changes the letter keys' position**. For example, Dvorak puts `{` and `}` on the QWERTY line, so it is a little harder, but Colemak does not change as much symbols' positions, so we can easily combine Colemak into SymmeTri. For example, it took me 5 minutes to complete this:
![SymmeTri-with-Colemak](https://github.com/WesleyBlancoYuan/SymmeTri-Keyboard-Layout/blob/master/preview/preview-104-smallenter-deadkey-lights-COLEMAK.png)

I think the idea of 1) symmetry and 2) including the most spoken languages in the world are the keys of my keyboard layout. By inventing SymmeTri, I want to express my idea about languages and symbols:
 - Symmetry is one of the most used ways to layout elements in the design of everything, and, maybe the most natural one, because all parts of our body are symmetrical, at least judging from outside. So it is easier to remember. Now, using this layout, it has become hard for me to go back to the QWERTY layout: why `/` is at the right lower corner while `\` is at the right most, on the home line? 
 - Chinese, English and Spanish are the three languages I speak, and they are the top 3 languages most spoken of the world(judging from the number of speakers, the number of countries and influence in real life and on Internet). In the 21st century, I think we will have more and more people speaking more than one, two or even three languages; so current keyboard layouts are not for them: switching from one to another every now and then are far from satisfying.

So here I only establish one example and two principles: 1) it is better to be symmetrical regarding to symbols; 2) it should contain common symbols in English and other composing languages, as many as possible. Based on the principles, we can:
 - Rearrange existent layouts in the symmetrical way, like Dvorak, Colemak, or AZERTY, or even JCUKEN.
 - Invent more keyboard layout to include more than one language, like a Russian-Polish-English JCUKEN layout, or French-Italian-German AZERTY layout.



### 5. Usage and implementation details

With different software/registry tweak, it can be used in Windows/Linux/MacOX.

---
#### 5.1 Windows
 1. Install Microsoft Keyboard Layout Controller 1.4 (aka [MSKLC 1.4](https://www.microsoft.com/en-us/download/details.aspx?id=22339). It is compatible until Windows 10 with 2017 Autumn Creator Update. )
 1.1(optional) Use "kbd swapped.h" to replace the "kbd.h" file in the MSKLC install directory, to swap RShift/LShift/Enter/Capslock while building keyboard layout with MSKLC. "kbd original.h" is for restoring(non-swapped). Details: https://msklc-guide.github.io/. Quote:
 > 03: Remapping System Keys
 > While MSKLC GUI lets you remap most keys on your keyboard, it does not allow you to remap keys like Capslock, Backspace, Ctrl, and others. However, there is a way to do just that, with a bit more work:
 > Step 0: Go to this directory: C:\Program Files (x86)\Microsoft Keyboard Layout Creator 1.4\inc
 > You might have to look elsewhere if you don't have MSKLC installed on your C-drive.
 > Step 1: Find the kbd.h file and copy it to your desktop. Consider creating a backup of it somewhere.
 > Step 2: Open the kbd.h that now sits on your desktop in a text editor. Scroll down to line 1030.
 > Step 3: Rewrite the VK-information to your liking (details below).
 > Step 4: Save this edited kbd.h-file, copy, and paste your saved file back into C:\Program Files (x86)\Microsoft Keyboard Layout Creator 1.4\inc, replacing the existing kbd.h-file that lives there.
 > Step 5: Re-open MSKLC and build your layout as you normally would. If you now use the newly-installed layout, it should operate with the VKs you defined.

 2. Download the `.klc` file in `windows` to import into MSKLC, and compile/package; then install the newly generated executable.
 3. Then, in Windows Registry, under `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts`, search `Chinese`, `Spanish` and `English`, to change `Layout Text` to `Symmetri`, and `Layout file` to `symmetri.dll`. (This file is installed to `C:\Windows\system32\`, or `C:\Windows\SysWOW64\`, depending on whether your machine is x86 or x64 architecture) Backup the folder/keys as you need.
 4. [registry trick](windows/registry_trick/switch%20function%20keys.reg) to swap Function keys. Use another file to restore this change.
 5. Restart to load registry modifications.

Important that the executable is not interchangable between different Windows machines; in each machine it must be obtained by compiling the `.klc` file independantly. I guess it is due to difference between the compilation environment of each machine.



---
#### 5.2 Linux

> Ubuntu users please check this answer: https://askubuntu.com/questions/24916/how-do-i-remap-certain-keys-or-devices
>

For Centos/Red Hat:

 - For virtual console (terminal) keyboard **(not finished yet.)**: 
 put `symmetri.map` into `/usr/lib/kbd/keymaps/legacy/i386/` or `/usr/lib/kbd/keymaps/xkb/`. (All files `/lib/kbd/keymaps/` will be read) and load it with:
 
 ```
 sudo loadkeys symmetri
 ```
 Our main reference is `keymaps(5)`. There we can find very useful information about how to interprete each column of `*.map` files. Be sure to read that.
 
 **Caution**: `loadkeys` changes the layout permanently, even after logout, and **is system-wide**; it means that even if you want to log in with another user after reboot, you will be using the changed layout. It will cause confusion if several users share the same machine, such as the case of a server. Rememeber to change it back when you log out!
 
 
 - For X11:
 You must use `symmetri`: put it in `/usr/share/X11/xkb/symbols`. And load it with `sudo setxkbmap -v symmetri -option caps:shiftlock`. `-option caps:shiftlock` ensures that after pressing CapsLock, you can enter numbers with top line keys without pressing Shift. This is the same behaviour as in Windows when you use the files in `windows` folder.

 If you want to load the "non-programmer" variant, use:
 
 ```
 sudo setxkbmap -v symmetri -variant non-prog -option caps:shiftlock
 ```
 (`-option caps:shiftlock` here will ensure you can enter `{[(</\>)]}` with top line keys without pressing Shift)


<s>(`localectl set-keymap` can be used to `list-x11-keymaps` and `list-x11-keymap-variants symmetri`, but it cannot be used to set layout).</s>

 **Note**: `setxkbmap` is a temporary change and will return default layout when logout. To make it permanent:
 
  - only after login and for certain user: add this line into `$HOME/.profile`, as suggested [here](https://unix.stackexchange.com/questions/99085/save-setxkbmap-settings)(epic answer and a must-read)
  - only after login and for all user: add this line to `/etc/profile`, or create `/etc/profile.d/symmetri.sh` and add:
  ```
  #!/bin/bash
  setxkbmap symmetri <-variant non-prog>  -option caps:shiftlock
  ```
  "<..>": optional.
  
  - before first successful login: see my question [here](https://unix.stackexchange.com/questions/446756/how-can-i-set-the-keyboard-layout-for-the-login-screen-before-the-first-successf) and my answer. Basically you copy the `evdev.lst` and `evdev.xml` file in this repo to the correct location(remember to make a backup of the original file), and then use `setxkbmap symmetri` to change keymap. Then, add a script file in `/usr/profile.d/` to load the keymap before every reboot.
  
  To leave a permanent copy:

  >   @terdon your solution is not working, but thanks for helping me out, I have learned more; at first I am also suspecting if it has something to do with Gnome, but it turned out that it is only X11. And @TimBrandrick, your solution should work in most of the cases, but in my case, not before adding my keyboard layout into the `.../X11/xkb/rules/evdev.xml` (and just in case, `.../X11/xkb/rules/evdev.lst`, because according to some sources, the `lst` file is the compiled version of `xml`, but I doubt whether all processes depending on these files will only read `xml` files; so I add in both. Actually, `xml` has more info than `lst`, but `lst` is easier to understand.)
  > 
  > 
  > So, here's how I did it:
  > 
  > ### 1. Open `.../X11/xkb/rules/evdev.xml`. 
  > (I omit the initial part, because it differs between distributions. In CentOS 7, it is under `/usr/share/`; in Ubuntu <= 8.08, it is under `/etc/`.<sup>1</sup> Strange. )
  > 
  > ### 2. At the end of children nodes of `<layoutList>`, add this part:
  > (change as you need, it is just a template)
  > 
  > 
  >     <layout>
  >       <configItem>
  >         <name>symmetri</name>
  >         <shortDescription>symmetri</shortDescription>
  >         <description>Symmetri (CN, EN and ES)</description>
  >         <languageList>
  >           <iso639Id>us</iso639Id>
  >         </languageList>
  >       </configItem>
  >       <variantList>
  >         <variant>
  >           <configItem>
  >             <name>non-prog</name>
  >             <shortDescription>non-prog</shortDescription>
  >             <description>Symmetri for non-programmer (CN, EN and ES)</description>
  >             <languageList>
  >               <iso639Id>us</iso639Id>
  >             </languageList>
  >           </configItem>
  >         </variant>
  >       </variantList>
  >     </layout>
  > 
  > If your keyboard layout has no variant, `<variantList>` part can be self-closing, like: `<variantList />`.
  > 
  > Note: `iso639Id` should has a value compatible with ISO 639-1 or 639-2 standard.<sup>1</sup> The full table is also given in the reference 1. And, it must be conform with your locale settings. I set `English(U.S)` as my system language, so I fill `us` here.
  > 
  > 
  > ### 3. Save it, and open `.../X11/xkb/rules/evdev.lst`.
  > 
  > ### 4. At the end of `! layout`, add your layout's name. Like:
  > 
  > 
  >     symmetri        Symmetri layout (CN, EN and ES)
  > 
  > ### 5. If your keyboard layout has variant, at the end of `! variant`, add it, too.
  > 
  >     non-prog        symmetri: non-programmer
  > 
  > The variant's name should coincide with the info above in the xml file. (As I test, `localectl list-x11-keymap-variants` will *only* read this file instead of reading the xml, should be an error/bug.)
  > 
  > 
  > ### 6. You can do the same to `base.xml` and `base.lst`, but I did it first and it does not work.
  > 
  > ### 7. Set your keyboard layout with:
  > 
  >     setxkbmap symmetri
  > 
  > or, to set the variant, use:
  > 
  >     setxkbmap symmetri -variant non-prog 
  > 
  > `localectl` can `list-x11-keymap-layouts` and `list-x11-keymap-variants`, but you cannot set variant with it; only `setxkbmap` can.
  > 
  > With this setting, now **after reboot and before first login**, you have your new keyboard layout(**although the variant will not persist!! Only the basic layout will!**)
  > But, once successfully login, the desktop manager will take over, and if you don't configure the new keyboard layout in the `$HOME/.bashrc`/`$HOME/.profile`(for single user)/`/etc/profile.d/xxx.sh`/`/etc/profile`(for all users) file, you will **not** get your new keyboard layout once logout and login back!!!! So these changes will **only** persist before first successful login... you have to use `.bashrc` or profile scripts to tell X server: "not only before login, but also after login I want it for all users!" Cautious: with this change, even if you log out and change user, the layout will be the changed one, not `qwerty(us)`. 
  > 
  > Really frustrating.... there must be a easier way, but I cannot find it.
  > 
  > 
  > 
  > References:(a must read)
  > 
  > 1. http://people.uleth.ca/~daniel.odonnell/Blog/custom-keyboard-in-linuxx11

Another thing is: in Ubuntu, you can edit /etc/default/keyboard file to achieve the same. And then, you update the kernel definition with `update-initramfs -u`. 


To switch the <kbd>CapsLock</kbd> and <kbd>LShift</kbd>, <kbd>Enter</kbd> and <kbd>RShift</kbd> key, you must change keycode in keymap files. What I do is to edit `evdev` file under `/usr/share/X11/xkb/keycodes` and set keyboard layout again with `setxkbmap` to clear xkb cache and load this file(Ubuntu 18.04). The `evdev` file under `/linux` already contains these changes and is ready to use. This keycode change is not applied until every time you log in, so be prepared when you need to decrypt disk or input username/password to log in. 


---
#### 5.3 macOS: 

[Karabiner Elements](https://karabiner-elements.pqrs.org/), tested on v15.3.0 with macOS 15(Sequoia). Put the `karabiner.json` into your `~/.config/karabiner/`, and swap CapsLock-Shift-Enter in "Simple modification"(in "Complex Modification" it does not work well, and v15.3 does not allow me to alter CapsLock light status). Other keys are in "Complex Modifications" as a single rule. 

The rule works for most of the cases(single press, Shift+key, CapsLock+key), but not with CapsLock+Shift+key. See this ticket: https://github.com/pqrs-org/Karabiner-Elements/issues/4180. I will skip it as this is trivial in my opinion.

Dead key combinations for circumflex, grave accent and acute accent letters are not implemented, for 2 reasons:

 - macOS ISO keyboard already has Option + E/U/I + letters, as shown in [this screenshot of Keyboard Viewer](https://github.com/WesternGun/Symmetri-Keyboard-layout/blob/master/mac/keyboard-viewer-dead-key.png?raw=true). With Symmetri rule turned on, they are still available.
 - A usual Mac user may not want to learn a new way to enter those if already familiar with the old way.

 so I skipped that part. If someone would create an issue, I may implement it later.



WesternGun, 22/4/2025

References:

ArchLinux XKB documentation:
https://wiki.archlinux.org/index.php/X_KeyBoard_extension#Using_keymap_.28deprecated.29
, which mentions:
http://pascal.tsu.ru/en/xkb/
https://karabiner-elements.pqrs.org/docs/
https://www.x.org/releases/current/doc/kbproto/xkbproto.pdf
