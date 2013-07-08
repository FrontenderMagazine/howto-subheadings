# How to mark up subheadings, subtitles, alternative titles and taglines 

If you don’t already know, the `hgroup` element is [obsolete][1] in [HTML5][2].

Advice is now provided in the [HTML spec][3] on how to mark up subheadings, subtitles, alternative titles and taglines using existing and *implemented* HTML features.

## Advice for marking up subheadings and the like

The important question for developers is: **How do I mark up these buggers**???

To answer this advice has been [added][4] to the HTML specification on how to mark up subheadings, subtitles, alternative titles and taglines:

> **Note:** Do not use `h1–h6` elements to markup subheadings, subtitles, alternative titles and taglines unless they are intended to be the heading for a new section or subsection.

**Note:** Example below added 10/5/2013

> In the following example the title and subtitles of a web page are grouped using a `header` element. As the author does not want the subtitles to be included the table of contents and they are not intended to signify the start of a new section, they are marked up using p elements. A sample CSS styled rendering of the title and subtitles is provided below the code example.

    <header>
    <h1>HTML 5.1 Nightly</h1>
    <p>A vocabulary and associated APIs for HTML and XHTML</p>
    <p>Editor's Draft 9 May 2013</p>
    </header>

![][]

> In the following example the subtitle of a book is on the same line as the title separated by a colon.

    <h1>The Lord of the Rings: The Two Towers</h1>

![][]

> In the following example part of an album title is included in a `span` element, allowing it to be styled differently from the rest of the title.

    <h1>The Mothers 
    <span>Fillmore East - June 1971</span> 
    </h1>

![][]

> In the following example the title and tagline for a news article are grouped using a header element. The title is marked up using a h2 element and the tagline is in a p element.

    <header>
    <h2>3D films set for popularity slide </h2>
    <p>First drop in 3D box office projected for this year despite hotly tipped summer blockbusters, according to Fitch Ratings report</p>
    </header>

![][]

> **Note:** Some have been [advocating][5] of the use of the `small` element to signify subtitles. This has been under [discussion][6] in the [HTML working group][7], but no compelling arguments for its use have been made. Therefore it is not advised to use `small` to mark up subtitles.

## What about the document outline?

If you want a subtitle to be displayed in the *semi-mythical* [document outline][8], include it along with the heading text as per example 1 and 2 above. If you don’t, put the text in a p element (for example), as per example 3 above.

## Questions for developers

Does the advice in the spec cover the use cases you encounter? If not what other advice should the spec include? Are the examples clear and unambiguous? If not how could they be improved? Any other questions you have, ask away in the comments!

If you are really keen you can [join][9] the likes of Bruce Lawson, Ian Devlin and myself in the HTML working group and take part in discussion there.

## What being *obsolete* in HTML5 means

> must not be used by authors

`hgroup` like other [obsolete features][10],  is non-conforming. This means that a [conformance checker][11] displays an error if the `hgroup` element is found. The following is the error message displayed by the [W3C Markup Validation Service][12]:

> Error: The `hgroup` element is obsolete. To mark up subheadings, consider either just putting the subheading into a `p` element after the `h1-h6` element containing the main heading, or else putting the subheading directly within the `h1-h6` element containing the main heading, but separated from the main heading by punctuation and/or within, for example, a `span` element with differentiated styling. To group headings and subheadings, alternative titles, or taglines, consider using the `header` or `div` elements.

Like for other [obsolete elements][13], browsers will continue their current level of support for `hgroup`. That is, browsers that have parsing and user agent style support will continue to do so, therefore authors that have used `hgroup` in their pages do not need to rush out and remove it. The element effectively has no meaning as its semantics have not been implemented. It’s effectively a `div` with a funny name.

The whys and wherefores

Much has been discussed and written over the past few years on the `hgroup` element and whether it meets the high bar required to include as a feature in HTML, on balance it has been decided it does not. Should this have happened more quickly? Yes , but as [Mike Smith][14] [stated recently][15]:

> People disagree. Organizations disagree. The task of us all working together to try to overcome our disagreements is time-consuming, often very frustrating, and almost never easy.

If you want to read up on the history of `hgroup` there is plenty of stuff available:

## HTML working group [mail archives][16] 2010 (tip of the iceberg):

* [suggestion for abolition of `hgroup` thread (November)][17]
* [`hgroup` and ARIA outline thread][18]
* [suggestion for abolition of `hgroup` thread (December)][19]

### Selected articles on the subject:

* [On the `hgroup` element][20]
* [Farewell, `hgroup`][21]
* [W3C Drops `hgroup` Tag From HTML5 Spec][22]
* [HTML5 Accessibility Chops: data for the masses][23]
* [The `hgroup` hokey cokey][24]
* [`hgroup` removed from the HTML5 specification][25]
* [RIP HTML5 `hgroup` Element][26]

[1]: http://html5doctor.com/howto-subheadings/#obsolete
[2]: http://www.w3.org/html/wg/drafts/html/master/Overview.html
[3]: http://www.w3.org/html/wg/drafts/html/master/common-idioms.html#sub-head
[4]: http://www.w3.org/html/wg/drafts/html/master/common-idioms.html#sub-head
[5]: https://github.com/twitter/bootstrap/issues/7482
[6]: http://lists.w3.org/Archives/Public/public-html/2013Apr/thread.html#msg2
[7]: http://www.w3.org/html/wg/
[8]: http://www.w3.org/html/wg/drafts/html/master/sections.html#outlines
[9]: http://www.w3.org/html/wg/#join
[10]: http://www.w3.org/html/wg/drafts/html/CR/obsolete.html#non-conforming-features
[11]: http://validator.w3.org/nu/
[12]: http://validator.w3.org/
[13]: http://www.w3.org/html/wg/drafts/html/master/obsolete.html#non-conforming-features
[14]: http://people.w3.org/mike//
[15]: http://www.w3.org/QA/2013/04/getting_agreements_is_hard_som.html
[16]: http://lists.w3.org/Archives/Public/public-html/
[17]: http://lists.w3.org/Archives/Public/public-html/2010Nov/thread.html#msg396
[18]: http://lists.w3.org/Archives/Public/public-html/2010Nov/thread.html#msg325
[19]: http://lists.w3.org/Archives/Public/public-html/2010Dec/thread.html#msg0
[20]: http://www.brucelawson.co.uk/2010/on-the-hgroup-element/
[21]: http://www.brucelawson.co.uk/2013/farewell-hgroup/
[22]: http://www.webmonkey.com/2013/04/w3c-drops-hgroup-tag-from-html5-spec/
[23]: http://blog.paciellogroup.com/2012/04/html5-accessibility-chops-data-for-the-masses/
[24]: http://html5doctor.com/the-hgroup-hokey-cokey/
[25]: http://www.iandevlin.com/blog/2013/04/html5/hgroup-removed-from-the-html5-specification
[26]: http://www.sitepoint.com/html5-hgroup-element-dropped/