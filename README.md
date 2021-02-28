# Evernote Encrypted Notes Decryption

All **credits** belong to [Lee Maguire](https://gist.github.com/gwire/0db858e055cc2bae953b435f5116aaa8). I had a hard time finding that script. My purpose with this repository is to present that script in a more usable format.

## How to decrypt

**Step 1:** Export all encrypted notes by using the search option.

Go to search box in Evernote. Click on "Add Search Option". Select "Contains". Then from the second dropdown list, select "Encryption".

Select all notes and export to `.enex` format. Let's call the file `encrypted.enex`.

**Step 2:** Clone this repository and install dependencies. To do that, run the following commands.

```sh
git clone https://github.com/aviaryan/Evernote-Decrypt.git
cd Evernote-Decrypt
brew install pipenv
pipenv sync
```

**Step 3:** Decrypt using the script. Run the following command.

```sh
# <password> is your Evernote encryption password
pipenv run python EnexDecrypt.py -p <password> < encrypted.enex > decrypted.enex
```

**Step 4:** You now have a decrypted Enex file. You can import it back into Evernote to export it as HTML. Or you can use [this tool](https://github.com/wormi4ok/evernote2md) to convert the `decrypted.enex` file into markdown files.


-----

## Update Reamde

New format

```
pipenv run python EnexDecrypt.py -p <password> < enc_jour.enex
```

Add an `-o` for output file.
