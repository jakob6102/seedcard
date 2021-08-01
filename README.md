# seedcard
A cheap and simple way to make metal bitcoin seed backups with just a centre punch.  
<a href="url"><img src="https://github.com/jakob6102/seedcard/blob/54f6e41d9b25fd3b1adae2c670cfc15970443eff/pictures/finished_plate.jpeg" height="340" width="520" ></a>  

    
    
**Overview:**  
This method of seed storage consists of converting a BIP39 24 word seed into its binary form then stamping it into a metal plate using a centre punch. 
This allows you to quickly make very cheap metal backups for your bitcoin seeds with minimal tools.

**Requirments:**  
-Metal plate of minimum size 39x72mm  
-Centre punch   
-Paper, tape & pen  
  
**Step 1: Prepare the metal plate**  
To reduce costs and identifiability this method does not need the metal to have any premade markings on the metal, instead you use a paper grid temporarily taped
to the metal. The grid is 13 columns (11 bits for the seed word, 1 blank space and 1 orientation mark) by 24 rows (24 seed words) with cells 3x3mm. Printable versions 
can be found in this repo, otherwise it is simple enough to hand draw with a ruler. The grid must then be securely fixed to the metal plate.  

This is an example of one I made, the grid is taped to a credit card sized plate of 1.5mm stainless steel:  
<a href="url"><img src="https://github.com/jakob6102/seedcard/blob/af31d04d9bfa1ac8f251f542d759e1714d883d83/pictures/blank_grid-cropped.jpg" height="400" width="400" ></a>  

  
**Step 2: Convert 24 word seed to binary**  
To record a seed densely using just a centre punch, this method requires the seed to be stamped in binary. Currently this means you must convert your 24 word to binary manually using a full BIP39 word list such as this one: https://github.com/hatgit/BIP39-wordlist-printable-en. Simply find each word of your seed on the list and record its binary equivelant on the grid with 1's being marked by a pen. 

For example, the BIP39 word "satoshi" represents the binary string "10111111011" and would be marked on the grid like this:  
![alt text](https://github.com/jakob6102/seedcard/blob/db034f124d1dfd947e9e75fc1d4239834f0aaa48/pictures/satoshi_example.jpeg?raw=true)  

My example fully marked up looks like this:  
<a href="url"><img src="https://github.com/jakob6102/seedcard/blob/db034f124d1dfd947e9e75fc1d4239834f0aaa48/pictures/marked_grid-cropped.jpg" height="400" width="400" ></a>  
This process could be improved by wallets having the option to natively display your seed in binary, either with 1's and 0's or a visual representation such as 
empty circles for a 0 and full circles for a 1. This is a simple addition for wallets to make with the only concern being UI clutter and potential user confusion.  

**Step 3: Stamping the plate**  
Once the grid is marked, simply go along with the centre punch and stamp each cell marked with the pen, I used an automatic centre punch for simplicity and speed but a normal punch and mallet would work just as well. Mark a line down the right hand side to indicate the plates orientation, this can either be a solid line of 1's or this could be used to store passphrase entropy. Once you have stamped the steel, remove the paper guide and burn or otherwise destroy it as it has a copy of your seed on it.  

Here is my example piece once stamped:  
<a href="url"><img src="https://github.com/jakob6102/seedcard/blob/db034f124d1dfd947e9e75fc1d4239834f0aaa48/pictures/stamped_plate-cropped.jpg" height="400" width="400" ></a>  

**Step 4: Recovering the 24 words**  
To recover the original 24 works you must convert the binary strings back to base-10 and then find the corresponding word from the BIP39 word list linked previouly, the conversion should be done using a dumb calculator rather than a computer or phone. Remember to add 1 to your base-10 number if the word list has the words numbered starting at 1 rather than 0.  

Here in my example I printed the grid guide onto clear paper and held it over the steel plate to make the binary more readable:  
<a href="url"><img src="https://github.com/jakob6102/seedcard/blob/a12ff90857793946c268233dbcf0d87859e1ad9e/pictures/plate_with_guide-cropped.jpg" height="400" width="400" ></a>  
Again here the process can be streamlined by wallets allowing the user to enter their seed as binary rather than needing to convert it back to words.   

**Conclusion:**  
Excluding the conversion to binary, this only takes about 10 minutes to create a metal backup for your seed and only requires one cheap tool and a small piece of metal (the card sized plates I had laser cut cost about $1 each). It is as durable as any other metal backup and has the added advantage of being language agnostic. There is some room for human error with the word>binary conversion and this conversion is hard to visually error correct however these issues are alleviated by wallets adding the suggested impovements to display and accept seed binary natively. My hope is that this can be an effective way to make metal backups for any wallet (even mobile or node hot wallets) without breaking the bank.



