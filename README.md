By woking with Hash we can determine not only if the information are identical to the original information. Also, we can determine if it consists some marware elements. 
As the same malware file will have the same hash address. 

The main idea for this program is compare provided or generated hashs with database of malware hashs. So we are going to check if file can consist some matware files. 
To get data I use this website https://bazaar.abuse.ch/export/ . I can access more than 1022741 hashs that consider to be programs with malware. 
But for now, I will retrict the number of hushs to 10541. To the most recent ones, maybe in the future I will implement with full number of hashs. 

One of the functionalities that we can compare two images and make assumption if images was changed or not similar, we will know that when we will compare hash index. If hash index is not match, so the images are different.
Also, one of the concerns was that if we resize or change name in the picture, the picture will be considered to be different. When basically it stays the same. 
Because of this, I implement this by using 
**ph = imagehash.phash(img)** not by using for chunk in  **iter(lambda: f.read(8192), b""):**
