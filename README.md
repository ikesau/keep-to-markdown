# keep-to-markdown

With this script Google Keep notes can be converted into markdown files. The Json files from the Google Takeout are required.

**Why?** If you want to keep your notes from Google for archiving or importing into another note program, you can use this script.

**Required?** Just Python 3.x and the Google Takeout notes as Json. This script support Linux, Mac and Windows (*new*).

**How?** To run this code use `python keep-to-markdown.py /path/to/Takeout/Keep`. By indicating the path with the Takeout/Keep folder where the Json files are located.

**What?** All converted markdown files will save in the extra folder `notes` with sub folder `resource` for images. The following list show the extracted informations:

* title
* tags
* text content
* task list
* web links
* images



## Example

Example of a converted markdown note:

```markdown
---
title: <Title>
date: <Date> (optional, if title is set)
tags: <tag1>;<tag2>;
---

<textContent>
Example Text ...

<listContent>
*Tasklist*:
- [ ] task1
- [x] task2

<annotations>
*Weblinks:* [link1](http//..); [link2](http://..);

<attachments>
*Attachments:* ![image](resource/image.jpg)

```

*Hint:* The title will be the file name. If there is no title available the created timestamp will be used.



## Future features

- [x] OS compatible
- [ ] save modified Timestamp by default
- [ ] use Google keep colors
- [ ] usability for Joplin import
