# JustEmuTarkov Installation

> ***If you are having issues with the installation, review the FAQ at the bottom of this page.***

## Installation Video

<video width="720" height="480" controls>
  <source src="https://files.catbox.moe/ee1k78.mp4">
</video>

## Requirements

- 7zip.
- Server files that match your game client.
- A supported Escape from Tarkov client version. These are available below.
- Binary files that match your EFT client version (named **JET-Binaries-XXXX.7z**), where **XXXX** is your client version.

## Download Center

To download the JET server and JET binaries, the packs are hosted on [justemutarkov.eu](https://justemutarkov.eu/download).

| Client version | Latest supported JET Server version |
|----------------|-------------------------------------|
| 12.8.*         | 1.0.3                               |
| 12.9.*         | 1.1.0                               |
| 12.10.*        | 1.2.0 *(not released)*              |

To download EFT clients supported by JET, you must download one of the below client archives:

- [0.12.7.9018](https://maoci.eu/download?file=EFT0.12.7.9018) *(not supported)*
- [0.12.8.9506](https://maoci.eu/download?file=EFT0.12.8.9506) *(not supported)*
- [0.12.8.9767](https://maoci.eu/download?file=EFT0.12.8.9767) *(not supported)*
    - [Alternate Mirror](https://drive.google.com/file/d/1sTOZ2AcO68pqbc9UjsZ94588ihCnB9Jp/view)
    - [Alternative Mirror #2](https://cdn.storeit.digital/file/JustEmuTarkov/Client.0.12.8.9767.zip)
- [0.12.9.10532](https://cdn.storeit.digital/file/JustEmuTarkov/Client.0.12.9.10532.zip)
- [0.12.9.10988](http://cdn-11.eft-store.com/client/live/distribs/0.12.9.2.10988_11c0b785-b414-46da-90e3-95e2f824cf49/Client.0.12.9.2.10988.zip) *(latest release)*
    - [Alternative Mirror](https://cdn.storeit.digital/file/JustEmuTarkov/EFT.0.12.9.2.10988.zip)

**NOTE:** Make sure the binaries you download from the download center match the client version you download.

## Installation Process

1. Create a master folder where you want your JET-related files to be. We will call this folder `JET`. Inside, create two folders, `Client` and `Server`.

```
JET/
|
|__Server/
|
|__Client/
```

2. Extract your downloaded EFT **client files** to `JET/Client`. This is the folder that will host your game files, such as `EscapeFromTarkov.exe`. We will call this the **client folder**.

3. Extract your downloaded JET **server files** to `JET/Server`. This is the folder that will host your JET server files, such as `Server.exe` and the `db` folder. We will call this the **server folder**.

4. Extract your downloaded JET **client binaries** to `JET/Client` using **7zip**. The binaries should have files such as `JET Launcher.exe` and an `EscapeFromTarkov_Data` folder, which will overwrite the existing files in your client's `EscapeFromTarkov_Data` folder. When moving your binaries to the `JET/Client` folder, you should get a message asking if you want to overwrite existing files, select **Yes.** Your directories should now look similar to the following:

```
JET/
|
|__Server/
|  |__Server.exe
|  |__db/
|  |__res/
|  |__src/
|  |__user/
|
|__Client/
|  |__ ...
|  |__EscapeFromTarkov.exe
|  |__JET Launcher.exe
|  |__launcher.config.json
|  |__EscapeFromTarkov_Data/
|     |__Managed/
|        |__ ...
|        |__NLog.JET.dll
|        |__0Harmony.dll
|        |__Assembly-CSharp.dll
|        |__NLog.dll.nlog
```

5. You are ready to begin playing. Launch `JET/Client/JET Launcher.exe`.
    - **NOTE:** If you are using JET 1.0.3 or older, you will need to open the server and the launcher separately. That means you need to launch `JET/Server/Server.exe` first, and then `JET/Client/JET Launcher.exe`.

6. Press the **Start Server** button.

7. To login, you can use the pre-created account with the username *Maoci* and the password *123*, or you can create your own by pressing the **+** button.
    - The e-mail and password do not need to be legitimate. You can enter whatever text you want into the boxes, as long as you remember them.

8. After choosing what version you want and registering the account, login to your new account. 

9. Press **Start Game**, and you should now be launching JET's EFT.

Addendum. So, to summarize:

- Extract your game files to the *client folder*.
- Extract your server files to the *server folder*.
- Extract your binaries to the *client folder*, and overwrite when asked.

It's really quite simple.

## Install FAQ

**Q:** *I am getting an NLog related error and it's preventing me from running the JET Launcher!*

- **A:** *Go to your `JET/Client/EscapeFromTarkov_Data/Managed/` folder. Now, look for all files related to NLog and go to their properties. At the bottom, you should see an checkbox labeled* **Unblock***. Unblock all NLog files. If this does not work, reinstall your client binaries.*

**Q:** *I am getting a 0Harmony.dll missing error!*

- **A:** *Reinstall your binaries, using 7zip.*

**Q:** *My game is stuck loading when I start!*

- **A:** *Reinstall your binaries, using 7zip.*

**Q:** *My server keeps shutting itself down!*

- **A:** *Disable your antivirus, or set an exception for Server.exe and JET Launcher.exe in its exclusion properties.*

**Q:** *I'm seriously a brainlet and can't figure this shit out!*

- **A:** *Feel free to ask in the support channels/support tickets of any of our affiliated Discord servers. Links to these are [here.](index.md)*
