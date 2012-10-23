# Lunicode.js

A JavaScript Library to convert text in various useless but amusing ways.  
&#x2d9;&#x73;&#x28e;&#x250;&#x28d; &#x253;&#x75;&#x131;&#x73;&#x6e;&#x26f;&#x250; &#x287;&#x6e;&#x71; &#x73;&#x73;&#x1dd;&#x6c;&#x1dd;&#x73;&#x6e; &#x73;&#x6e;&#x6f;&#x131;&#x279;&#x250;&#x28c; &#x75;&#x131; &#x287;&#x78;&#x1dd;&#x287; &#x287;&#x279;&#x1dd;&#x28c;&#x75;&#x6f;&#x254; &#x6f;&#x287; &#x28e;&#x279;&#x250;&#x279;&#x71;&#x131;&#x2e5; &#x287;&#x64;&#x131;&#x279;&#x254;&#x53;&#x250;&#x28c;&#x250;&#x17f; &#x2200;

Extracted from [lunicode.com](http://lunicode.com).

If it looks weird and boxy, you need a Unicode font:

<ul>
	<li><a target="_blank" href="http://dejavu-fonts.org/wiki/Main_Page">DejaVu Sans</a></li>
	<li><a target="_blank" href="http://www.fonts2u.com/code2000.font">Code2000</a></li>
	<li><a target="_blank" href="http://www.lgm.cl/trabajos/unifont/index.en.html">GNU Unifont</a></li>
	<li><a target="_blank" href="http://web.nickshanks.com/fonts/kannada/">Kedage</a></li>
</ul>

Use it like this:

    // Get the Lunicode object, initializing the effects
    var luni = new Lunicode();
    
	// Encode text. Use one of the effects shown below. Here it's "flip"
    var encodedText = luni.tools.flip.encode("Hello World");  // plɹoM ollǝH
    
    // Decode text back to plain ASCII (or reverse encoding)
    var plainText = luni.tools.mirror.decode("ƚxɘT ɿoɿɿiM");  // Mirror Text
    
    // Creepify has a few options. Set them before encoding:
    luni.tools.creepify.options.top = true; 	// add diacritics on top. Default: true 
    luni.tools.creepify.options.middle = true;	// add diacritics in the middle. Default: true 
    luni.tools.creepify.options.bottom = true;	// add diacritics on the bottom. Default: true
    luni.tools.creepify.options.maxHeight = 15; // How many diacritic marks shall we put on top/bottom? Default: 15
    luni.tools.creepify.options.randomization = 100; // 0-100%. maxHeight 100 and randomization 20%: the height goes from 80 to 100. randomization 70%: height goes from 30 to 100. Default: 100
    
    // To convert Unicode text to HTML, use luni.getHTML(text);
    // Also converts \n to <br>\n and multiple spaces to &nbsp; &nbsp; &nbsp; ...
    var html = luni.getHTML("ǝpoɔıu∩̤"); // &#x1dd;&#x70;&#x6f;&#x254;&#x131;&#x75;&#x2229;&#x324;


# Effects


## flip

Flips/Rotates text, including numbers (12345) and some special characters: äöü éáú ÄÖÜ ß ô

o̮ ᙠ ∩̤O̤∀̤ n̗ɐ̗ǝ̗ n̤o̤ɐ̤ :sɹǝʇɔɐɹɐɥɔ lɐıɔǝds ǝɯos puɐ (ގㄣƐᄅ⇂) sɹǝqɯnu ɓuıpnlɔuı 'ʇxǝʇ sǝʇɐʇoᴚ/sdılℲ

## mirror

Mirrors text horizontally. äöü ß èàù. Käseküchlein.

.ᴎiɘ|ʜɔüʞɘꙅɒ̈⋊ .úɒ́ɘ́ ᙠ üöɒ̈ .ʏ||ɒƚᴎoƹiɿoʜ ƚxɘƚ ꙅɿoɿɿiM

## creepify

Adds  
	diacritics
	

Ą̵̛͎̗͎̯͕̺̭͍̩͐̄̄͗̿͛̔̀́̋̄͜d̷̨͉͇̞̲̥͈̝̺̘̪̥̟͚̘̫̑̋̎͜͜ḑ̵̡̛̤̱̣̼̞̥̻͕͗̔̀̐́̆̐̓͌̊͛̐̉̚͝s̴̯̤̓̐͒̓̉͆̿̔̚͝
	̶̭̼͂̃d̴̡̰̯̲̣̘͉͉̯̣̥͋̈́̊̏̓̀͒̚i̷̮̭͋̈́̋͋̉͊̄̓͂̕a̶̳̣̲̓̊͋c̵̡̛̗͕̖̻͇̪͆̌͒͊͛͌̽̐̇̇̀͊̂̈͒̚͜͠ṙ̷̡̹̱̜̖̦̭ĩ̵͍̪̘͚̗̰͓̙͛͆̽̾͒̏̀͗̊̊́̍̉͒̊ţ̶̙͙̙͉̱́̀̈́̿͛͊̎̓̉̕̕͜͝i̵̛̞̭̭̮̱̬̯̙̖̺̼͑͛ͅć̶̢̡̫̻̪̩̤̱̠̰̹̙͒́̀͐͐̚̚͘͝͝ṩ̸̢̧̠͖̩͚̯̳͓̻̪̻̞

## bubbles

Bubbles around normal characters. Uses combining characters for everything else.

Ⓑⓤⓑⓑⓛⓔⓢ ⓐⓡⓞⓤⓝⓓ ⓝⓞⓡⓜⓐⓛ ⓒⓗⓐⓡⓐⓒⓣⓔⓡⓢ    .⃝ Ⓤⓢⓔⓢ ⓒⓞⓜⓑⓘⓝⓘⓝⓖ ⓒⓗⓐⓡⓐⓒⓣⓔⓡⓢ ⓕⓞⓡ ⓔⓥⓔⓡⓨⓣⓗⓘⓝⓖ ⓔⓛⓢⓔ    .⃝

## squares

Squares, via combining characters.

S⃞    q⃞    u⃞    a⃞    r⃞    e⃞    s⃞    ,⃞     v⃞    i⃞    a⃞     c⃞    o⃞    m⃞    b⃞    i⃞    n⃞    i⃞    n⃞    g⃞     c⃞    h⃞    a⃞    r⃞    a⃞    c⃞    t⃞    e⃞    r⃞    s⃞    .⃞

## roundsquares

Round squares, via combining characters.

R⃣   o⃣   u⃣   n⃣   d⃣    s⃣   q⃣   u⃣   a⃣   r⃣   e⃣   s⃣   ,⃣    v⃣   i⃣   a⃣    c⃣   o⃣   m⃣   b⃣   i⃣   n⃣   i⃣   n⃣   g⃣    c⃣   h⃣   a⃣   r⃣   a⃣   c⃣   t⃣   e⃣   r⃣   s⃣   .⃣

## bent

Wonky alternatives to the usual characters.

చօղҟվ ąӀէҽɾղąէìѵҽʂ էօ էհҽ մʂմąӀ çհąɾąçէҽɾʂ.

## tiny

Tiny Capitals.

ᴛɪɴʏ ᴄᴀᴘɪᴛᴀʟꜱ.



# Links and Thanks
<ul>
	<li><a href="http://www.fileformat.info/">FileFormat.info</a> - The best Unicode reference</li>
	<li><a href="http://en.wikipedia.org/wiki/Transformation_of_text">Wikipedia: Transformation of Text</a> - Table for flipped characters and others infos</li>
	<li><a href="http://www.reddit.com/r/unicode">reddit.com/r/unicode</a> - The webs biggest unicode-for-fun community (needs more members)</li>
	<li><a href="http://www.revfad.com/flip.html">David Fadens Flip</a> - Initial inspiration and characters</li>
	<li><a href="http://upsidedown.info/">Thomas Schilds upsidedown.info</a> - Inspiration and comparison</li>
	<li><a href="http://www.macchiato.com/unicode/mirrored-ascii">Macchiato - Mirrored ASCII</a> - Initial codepoints for mirrored text</li>
	<li><a href="http://www.alanwood.net/unicode/enclosed_alphanumerics.html">Alan Wood’s Unicode Resources</a> - Codepoints for Bubble Text</li>
	<li><a href="http://en.wikipedia.org/wiki/Combining_character">Wikipedia: Combining Character</a> - For Creepify, Upsidedown Umlauts, Squares, ...</li>
	<li><a href="http://blogs.msdn.com/b/michkap/archive/2006/02/17/533929.aspx">Michael Kaplan's "What do you get when you combine a base character with a buttload of diacritics?"</a> - Idea for creepify</li>
	<li><a href="http://unicodeemoticons.com/">Unicode emoticons</a>, <a href="http://www.planetminecraft.com/blog/collection-of-unicode-faces/">Collection of unicode faces</a> and <a href="https://gist.github.com/157796">Unicode smileys</a></li>					
	<li><a href="http://funicode.com">funicode.com</a> - Idea and lower case characters for Bent</li>
</ul>