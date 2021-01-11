# PrivaDia - Privacy in speaker diarization: Detecting “who spoke when” privately

As proven by the recent EU’s General Data Protection Regulation (GDPR), our society is becoming increasingly concerned with how cloud-based applications use their client’s data. Among other data types, speech has received growing interest due to recent advances in speech recognition that have boosted the development of voice-based virtual assistants. However, current speech-based machine learning models are already able to determine characteristics about an individual as private as his/her physical and mental health. It is thus important to find ways to protect the privacy of an individual’s voice, and prevent sensitive information from being leaked. In the midway between simple speech applications and speech recognition lies an enabling technology that not only serves as an intermediate step in complex applications, but is also useful on its own. Automatic Speaker Diarization (ASD), the problem of determining “who spoke when” in a speech recording, is the middle step that can be used to contextualize transcriptions, improve the results of speech recognition systems, and allow users to search and filter speech segments of a specific speaker.
In this exploratory project we aim to develop a proof-of-concept for private ASD, which could be applied to scenarios where data cannot be delegated to an external party, due to legal or ethical constraints, such as criminal investigations, medical interviews and courtroom hearings. This project addresses this privacy issue by combining state-of-the-art diarization methods (based on speaker embeddings obtained from the hidden layers of deep neural networks) with cryptographic techniques such as homomorphic encryption and secure multi-party computation. Notwithstanding its own merits, a private solution for ASD will also provide a basis on which future research can be built upon and will push the current state-of-the-art forward in the direction of fully private end-to-end speech processing applications.


---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
