# XML

> * HTML is a language that describes how information is displayed on the screen in the web browser and XML describes how data is organized, stored and retrieved from memory.&#x20;
> * XML is simply text which is "machine-readable," where programs can read and understand it.
> * XML files simply assign tags to data that will be meaningful to the application that needs access to a specific set of data.&#x20;
> * Using XML you can use it to take data from a program like Microsoft SQL, convert it into XML then share that XML with other programs and platforms.
> * They enhance the meaning of the Semantic Web document's content.

* If a document contains certain words that are marked as "**emphasized**" the way those words are rendered can be adapted to the context.&#x20;
* A Web browser might simply display them in italics, whereas a voice browser (which reads Web pages aloud) might indicate the emphasis by changing the tone or the volume of its voice. Each program can respond appropriately to the meaning encoded in the markup.&#x20;
* In contrast, if we simply marked the words as in **italics**, the computer has no way of knowing why those words are in italics. Is it for emphasis or simply for a visual effect? How does the voice browser display this effect?&#x20;

`I just got a new pet dog`

* &#x20;As far as our computer is concerned, this is just text. It has no particular meaning to the computer.&#x20;
* But now consider this same passage marked up using an XML based markup language&#x20;

```
<sentence>

<person href="http://aaronsw.com/"> I </person> just got a new pet <animal> dog
</animal>

</sentence>
```

* Notice that this has the same content, but that parts of that content are labelled.&#x20;
* The name of the tag "sentence" is the label for the content enclosed by the tags.&#x20;
* We call this collection of tags and content an "element."&#x20;
* The computer now knows that "I just got a new pet dog" is a "sentence", "I" is a "person" and that "dog" is an "animal".
* The Semantic Web computer knows that "I" in the above sentence represents a "person" but it does not know which person.&#x20;
* We can provide this sort of information by adding attributes to our elements.&#x20;
* An attribute has both a name and a value.&#x20;

```
<sentence>

<person href="http://aaronsw.com"> I </person> just got a new pet <animal type="dog"
href="http://aaronsw.com/myDog"> dog </animal>

</sentence>
```

{% hint style="danger" %}
A problem with this is that we've used the words "sentence" "person" and "animal" in the markup language. But these are pretty common words. What if others have used these same words in their own markup languages? What if those words have different meanings in those languages?&#x20;
{% endhint %}

{% hint style="success" %}
Solution : Uniquely identify the markup elements by assigning a URI to each of our elements and attributes using XML namespaces. &#x20;
{% endhint %}

* A namespace is just a way of identifying a part of the Web from which we derive the meaning of these names.
