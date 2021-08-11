[![Lines of code](https://img.shields.io/tokei/lines/github/Blinue/Magpie)](https://github.com/Blinue/Magpie) [![Help Wanted](https://img.shields.io/github/issues/Blinue/Magpie/help%20wanted?color=%232EA043&label=help%20wanted)](https://github.com/Blinue/Magpie/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)

# MAGPIE
Magpie can enlarge any window to full screen and supports a variety of advanced zoom algorithms, including Lanczos, Anime4K, FSR, FSRCNNX etc.
It is mainly used for the enlarged display of the game window, and is suitable for situations where the full-screen mode is not supported, or the built-in full-screen mode will blur the picture.

If you encounter problems during use, please submit an issue.
<br>
<br>
☛ <a href="https://github.com/Blinue/Magpie/wiki/%E7%BC%96%E8%AF%91%E6%8C%87%E5%8D%97"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Compilation Guide</font></font></a>
<br>
☛ <a href="https://github.com/Blinue/Magpie/wiki/FAQ"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FAQ</font></font></a>

## Instructions
When the window to be enlarged is in the foreground, press the hot key to display the window in full screen, and press the hot key again or switch the foreground window to exit the full screen.

The following is the configuration description:
#### Zoom mode
The program presets a variety of zoom modes:
1. Lanczos: Common traditional interpolation algorithm, good at preserving sharp edges.
2. RAVU: See [About RAVU](https://github.com/bjin/mpv-prescalers#about-ravu). This preset uses a zoom variant.
3. FSRCNNX: A variant of FSRCNN. Excellent performance in various occasions.
4. ACNet: Porting of [ACNetGLSL](https://github.com/TianZerL/ACNetGLSL). Suitable for animation-style image and video enlargement.
5. Anime4K: an open source high-quality real-time animation scaling/noise reduction algorithm.
6. FSR: Suitable for 3D games.
7. Pixels: Enlarge each pixel by an integer multiple to keep the visual effect of the original image intact. Two magnifications of 2x and 3x are preset.

#### Crawl mode
Instruct the program how to grab the source window image
1. WinRT Capture: Use Windows Screen Capture API to capture windows, which is the most recommended method. This API has been provided since Windows 10 v1903.
2. GDI: Use GDI to grab the source window, the speed is slightly slower.

#### Injection mode
If a custom cursor is used in the source window, two cursors may appear on the screen. In order to solve this problem, Magpie provides the function of process injection:
1. No injection: suitable for situations where the source window does not have a custom cursor
2. Runtime injection: Inject the source window thread while performing zooming, and cancel the injection after exiting the full screen
3. Injection at startup: It is suitable for occasions where the runtime injection does not work. The running process cannot be injected. You need to manually select the program to be started and injected.

#### advanced options
* Display frame rate: display the current frame rate in the upper left corner of the screen

## Usage suggestions
1. If you have set DPI scaling, and the window to be enlarged does not support it (shown as the picture is blurred), please enter the compatibility settings of the program first, and set "High DPI Scaling Alternative" to "Application".
2. Some games support adjusting the window size, but simply use linear scaling. In this case, please set it to the original resolution first.

## Disclaimer
Because of the use of process injection technology, this program is very likely to be reported as a virus. For security reasons, you should check the source code and compile it yourself.
The original intention of developing this program does not contain any maliciousness, but the consequences of using it should be borne by you.
