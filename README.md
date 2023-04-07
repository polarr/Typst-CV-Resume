# Typst-CV-Resume

This Typst CV template is inspired by Latex template [Deedy-Resume](https://github.com/deedy/Deedy-Resume).
You can use it for both of industry and academia. I have create a function to import your publication list.

In original Typst, we cannot create a reference list withou citation. So I modified the code for this purpose. Currently, I only create the Chicago style citation and reference list. If you want to use other citation styles, you need to modify the code.

**remember: you need to use `json` file exported from Zotero with BetterBibTeX. I did not test other ways.**

## Use

This project include **three** files:

- `example.typ`: the main file
- `typstcv.typ`: the template file
- `bib.json`: the bibliography file

You can use `example.typ` as a template to create your own CV. You can also download `typstcv.typ` as a template. Then create a new file with the following code:

<details>
    <summary>Click me</summary>

```
# import "typstcv.typ": *
# main(
name: [#lorem(2)], //name:"" or name:[]
address: [#lorem(4)],
lastupdated: "true",
date:"2023.4.7",
contacts: (
(text:"08856",link:""),
(text:"example.com",link:"https://www.example.com"),
(text:"github.com",link:"https://www.github.com"),
(text:"123@example.com",link:"mailto:123@example.com"),
  ),
bibfile: [bib.json],
[
    // About
    #section("About")
    #descript[#lorem(50)]
    #sectionsep
    #section("Education")
    #subsection[#lorem(4)]
    #term[xxxx-xxxx][UK]
    #subsectionsep
    #subsection[#lorem(4)]
    #term[xxxx-xxxx][UK]
    #sectionsep
    #section("Skills")
    #descript("Programming Languages")
    #info[Python, C++, Java, JavaScript, HTML, CSS, SQL, LaTeX]
    #subsectionsep
    #descript("Frameworks")
    #info[React, Node.js, Express, Flask, Django, Bootstrap, jQuery]
    #subsectionsep
    #descript("Tools")
    #info[Git, GitHub, Docker, AWS, Heroku, MongoDB, MySQL, PostgreSQL, Redis, Linux]
    // Award
    #section("Awards")
    #awarddetail[2018][Scholarship][University]
    #awarddetail[2017][Grant][Organisation]
    #awarddetail[2016][Scholarship][University]
    #sectionsep
],
[
    //Experience
    #section("Experience")
    #subsection[#lorem(4)]
    #term[xxxx-xxxx][UK]
    #descript[#lorem(4)]
    #info[#lorem(20)]
    #subsectionsep
    #subsection[#lorem(4)]
    #term[xxxx-xxxx][UK]
    #descript[#lorem(4)]
    #info[#lorem(20)]
    #subsectionsep
    #subsection[#lorem(4)]
    #term[xxxx-xxxx][UK]
    #descript[#lorem(4)]
    #info[#lorem(20)]
    #sectionsep
    // Projects
    #section("Projects")
    #descript[#lorem(2)]
    #info[#lorem(40)]
    #subsectionsep
    #descript[#lorem(2)]
    #info[#lorem(40)]
    #subsectionsep
    #descript[#lorem(2)]
    #info[#lorem(40)]
    #sectionsep
    // Publication
    #section("Publications")
    #chicago(json("bib.json"))
],
)
```

</details>

## Example
I only test the template on macOS. If you want to use it on other platforms, you should use template in the `openfont` folder. Then, modify the font in `typstcv.typ` to the font installed on your PC.

**MacFont**
![U5Emap](https://cdn.jsdelivr.net/gh/jxpeng98/imagerepo@main/2023/04/U5Emap.png)
**PT Sans**
![qxLtUZ](https://cdn.jsdelivr.net/gh/jxpeng98/imagerepo@main/2023/04/qxLtUZ.png)

## Todo

Create more citation styles for citations.
