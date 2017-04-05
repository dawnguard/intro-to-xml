# Introduction to XML

A beginner's introduction to XML

## What is XML?

XML stands for eXtensible Markup Language. It is a way of categorically describing data/information (Don't worry, it'll all make sense after looking at some examples).

## A Note

The time is 1pm, Jake's girlfriend (Ana) is supposed to come over to his house at 3pm. Jake receives a phone call from a friend, who wants his help with some important. He promises Jake that it'll be finished by 3:30pm.

Jake tries to call Ana on her phone but it is switched off, she often forgets to charge its battery so it probably ran out.

He writes a note for Ana explaining that he'll be back by 3:30pm and sticks it on the front door before leaving. This is the note that he wrote:

```
Ana,

Had to go out for some important work. I'll be back by 3:30 x

- Jake
```

Now let's convert this note into XML:

```xml
<xml>
	<note>
		<to>Ana</to>
		<message>Had to go out for some important work. I'll be back by 3:30 x</message>
		<from>Jake</from>
	</note>
</xml> 
```

The opening and closing brackets (< and >) with text inside of them are called tags.

Tags always come in pairs: `<xml>` and `</xml>`, `<note>` and `</note>`, to and `</to>`, you get the picture. The first tag (the one without the '/') of the tag pair is called the opening tag. The second tag (the one with the '/' at the beginning) of the tag pair is called the closing tag.

Let's take the case of `<xml>` ... `</xml>`. Whatever that comes between the opening and closing tags (...) has now been 'tagged' or 'categorized' as XML. In other words, we know that all the text between the `<xml>` and `</xml>` tags is xml.

Same for the other tags (All the stuff between `<note>` and `</note>` is the content of the note. The text between `<from>` and `</from>` is the name of the sender).


So what did we just do, by writing that note in xml? We organized the  contents of the note into distinct categories (think of each tag pair as a ctegory; we organised the note into 3 named categories- 'to', 'from' and 'message').

Now you must be thinking: "We just organized the contents of the note into different categories. But WHY? It still made complete sense as a normal note before it was turned into XML".

You're right. It makes no sense to do that in this case. The note and its conversion into XML was just an example for you to easily understand how to store data/information using XML.

## A Practical Use Case

You must be wanting to hear about a more practical use of storing data in XML. Consider this example:

----

John writes short notes about his school friends every day. He writes them using the xml format in a text editor.

Here are some example notes:

```xml
<xml>
	<note>
		<name>Jake</name>
		<type>Good</type>
		<body>He helped me with my homework :)</body>
	</note>
</xml>
```

```xml
<xml>
	<note>
		<name>Jake</name>
		<type>Good</type>
		<body>He helped me with my homework :)</body>
	</note>
</xml>
```

```xml
<xml>
	<note>
		<name>Jake</name>
		<type>Good</type>
		<body>He helped me with my homework :)</body>
	</note>
</xml>
```

---

So there's 3 categories of data in the notes that John writes:

- Name: The name of the friend he's writing the note about.
- Type: Is it a 'good' note about the friend, or a 'bad' note?
- Body: The actual content of the note.


By the end of the year, John and Jake become best friends. John decides to send Jake the notes he wrote about him. It's as simple as writing a couple of lines couple of lines of code which instruct the computer to compile the `<body>` of all notes which have "Jake" as the `<name>`; in a text file, with a paragraph break after each note to separate them.

He then realizes that he also had written some 'bad' notes about Jake, which he doesn't want Jake to see. He modifies his code so that it only compiles the notes which have "Jake" as the `<name>` and "Good" as the `<type>`.

And now John has a text document of all the 'good' notes he has written about Jake over the past year. He sends it as an email to Jake.


Imagine if he had simply typed the notes, without categorizing them using XML. He would have to open each text file for every single day, determine if the note is 'good' or 'bad', then copy and paste it into the email/document if it is a 'good' one.

So by using XML to store his notes, John saved himself a lot of time and effort.

*That's all, folks!*

----

<a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-nd/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a>.
