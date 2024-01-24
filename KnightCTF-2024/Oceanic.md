# Oceanic CTF Writeup

## Clue.jpg Metadata Exploration

Utilizing `exiftool` on the `clue.jpg` file revealed encoded information in the comment. Employing `dcode.org`'s cipher identifier, I identified the encryption as base58. Decoding the string yielded: "theoceanisactuallyreallydeeeepp."

![metadata](/images/oceanic.png)

## Delving into the Audio File

Inspecting the provided audio file, initially suspected to contain Morse code, led to the discovery of a Windows program called DeepSound, specializing in audio steganography. Running the program prompted for a password. Utilizing "theoceanisactuallyreallydeeeepp" as the password unveiled a hidden file: `flag.png`.

## Analyzing the Flag.png

Performing a hex dump on the `flag.png` file and searching for "KCTF" exposed the flag: `KCTF{mul71_l4y3r3d_57360_ec4dacb5}`.

![flag](/images/oceanic_hex.png)

