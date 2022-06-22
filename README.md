# 📮🦆 Pterotale 

Created with GB Studio V3.0

![logo](https://user-images.githubusercontent.com/12164308/174966074-de8e6231-f812-4e24-bb16-34f02cd38bb8.png)
![titlescreen](https://user-images.githubusercontent.com/12164308/174966109-4a989b46-e94f-4362-a5d9-8b214a90f6c6.png)

Plugins Used
1. `dialogueNameTagLargeAvatarPlugin`
<hr>
<br>

# 🎨 Making a large avatar
The workaround used in GB Studio (there's no native support for large avatars) is to use the aforementioned plugin. To do so, we first make a font in the `assets/fonts` folder as such:

![gbs-mono](https://user-images.githubusercontent.com/12164308/174967132-b1081714-628d-4cf8-99e6-5b663a8b65cb.png)
![Hektar](https://user-images.githubusercontent.com/12164308/174967064-301d65f9-6ad8-4a5e-bfeb-65a3f6d6dea1.png)

This is a "font" where the Hektar portrait replaces 
``` 
ABCD
QRST
abcd
qrst
```

Then, to make use of this in GB Studio, we then add a new Dialogue to use the "Hektar Font" and input the letters that will draw the avatar.

![image](https://user-images.githubusercontent.com/12164308/174967356-23a7b85d-bcf2-456e-a557-5869f6152468.png)

## ⚠ Issues
 A caveat/known issue that is extremely annoying to avoid is that we'll need to continuously change back and forth between "Hektar Font" and the default "GBS Mono" font **at the end of every message block.**
- Every message will have to start with "GBS Mono" and end with "Hektar Font"

<hr>

**If we do not explicitly change the font back and forth, the following occurs**  

![image](https://user-images.githubusercontent.com/12164308/174968083-b7152f83-36ea-4c01-bb4c-6091f535c71e.png)

![image](https://user-images.githubusercontent.com/12164308/174968103-7bd36205-dc27-4fa5-a10f-dbf71ad877a3.png)

<hr>

**versus correctly doing so:**

![image](https://user-images.githubusercontent.com/12164308/174968235-b7a3c388-4726-4690-a83a-c9b24d823db6.png)

![image](https://user-images.githubusercontent.com/12164308/174968210-c4855fe0-e266-4ef4-8d71-6089942d56f0.png)

The difference here is that the first **F** is the GBS Mono font `(before *...yawn..*)`, which is why the message comes out normally **BUT** if we don't explicity tell GB Studio to use GBS Mono again, when it redraws the Hektar avatar the **active font will be Hektar font** while it draws the avatar again and never change back to GBS Mono to appropriately write text normally again.

![image](https://user-images.githubusercontent.com/12164308/174969940-d71b64eb-f353-4974-a001-ae1b73cb4001.png)

