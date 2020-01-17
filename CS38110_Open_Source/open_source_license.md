# OSS Legal & Licenses Notes 

# Intellectual Property 

_Intellectual property (IP) refers to creations of the mind, such as inventions; literary and artistic works; designs; and symbols, names and images used in commerce._ from [WIPO](https://www.wipo.int/about-ip/en/)

### Copyright
_"Copyright is a legal term used to describe the rights that creators have over their literary and artistic works. Works covered by copyright range from books, music, paintings, sculpture and films, to computer programs, databases, advertisements, maps and technical drawings."_ from [WIPO](https://www.wipo.int/copyright/en/)

Copyright has term lengths. In the United States, copyright lasts for the lifetime of the creator plus 70 years. If there is no single creator, the term lasts for 95 years from the publication of the work or 120 years from the intial creation, whichever is shorter. Copyright can be extended so that works can have copyright in perpetuity. In the United Kingdom, copyright lasts for 50 years after the release, 50 years after first broadcast or 70 years after first making a recording if the work has not been released. All other works in the EU have copyright of the lifetime plus 70 years.  

Fair use is also an important term - it includes any non-infringing use of copyrighted material (comments, parody, criticism, transformative derivative works). In the UK, fair dealing was more restrictive until 2014 when copyrighted works could be parodied, copies could be made for personal use and works could be backedup and/or format shifted. 


### Patents 
_"A patent is an exclusive right granted for an invention. Generally speaking, a patent provides the patent owner with the right to decide how - or whether - the invention can be used by others. In exchange for this right, the patent owner makes technical information about the invention publicly available in the published patent document."_ from [WIPO](https://www.wipo.int/patents/en/)

Patents cannot be non-tangiable entities, business process or algorithms (outside of the US). Patent disputes are often costly affairs and out of court settlements between parties are common. 

### Trademarks
_"An officially registered recognisable sign, design or expression which identifies a product, service or business."_

Used by product logos, branding etc. Might be used to certify products. The organisation holding the trademark grants those it certifies permission to use their mark on a product.


### Copyleft
_"Copyleft, distinguished from copyright, is the practice of offering people the right to freely distribute copies and modified versions of a work with the stipulation that the same rights be preserved in derivative works created later."_

### Patent Pools

---

# Licenses 
Legal contract regarding the use and distribution of software. Grants the user rights to use the software in exchange for agreeing to the terms. Copyright allows creators to require a user to agree to their term, which is done through a EULA (End User License Agreement). A EULA has terms often include restrictions on redistribution, reverse engineering, multiple users etc.
Users don’t normally sign a contract.
They agree through:
Shrink Wrap Licensing
Click Through Licensing

There are [many open source licenses](https://opensource.org/licenses) that developers and organisations [can use](https://choosealicense.com/) when they release their software. The licenses that are included in Aberystwyth's CS38110 module are MIT, GNU GPL, BSD and Apache. 

There are **two main types** of licenses used in open source projects, permissive licenses and copyleft licenses.

## Permissive Licenses: Apache, BSD & MIT

Based off of the [lecture](http://users.aber.ac.uk/mjh25/cs381/reveal/L9-Permissive_licenses.html) by [Malcolm Hutchison](https://www.aber.ac.uk/en/cs/staff-profiles/listing/profile/mjh25/).

> Read [this book](http://class-95799.heinz.cmu.edu/doc/Open-Source-books/Understanding-Open-Source/openbook/osfreesoft/book/ch02.pdf) from O 'Reilly 

Permissive licenses impose no restrictions on developers that their source code should remain open. 

### MIT: Massachusetts Institute of Technology
Projects that use MIT: X.Org, JQuery, Node.js, Ruby on Rails, Lua, Jenkins, MS VS Code 

MIT is perhaps the simplest of the permissive licenses. It opens with a copyright statement which follows with the year and copyright holder. The rest of the license surrenders the rights normally given to a copyright holder. States that the software is presented "as is" and that it does not have a warranty. It grants the user the ability to distribute, modify, etc. the source code that the license covers. 

### BSD: Berkeley Software Distribution
From the University of California Berkeley.

Projects that use BSD: Unix, FreeBSD, NetBSD, OpenBSD (basis of macOS).

BSD is slightly more restrictive than the MIT license. It stipulates that any redistributions must retain the BSD copyright notice, conditions and disclaimer. It also states that the name of the organisation nor the names of the contributors may be used to endorse or promote derivative products without prior written permission. This protects creators from defamation against any derivative works. 

There used to be an additional clause prior to 1999 that stated all advertising materials that mentioned a product released under BSD must display an acknowledgement: "This prooduct includes software developed by the <NAME_OF_ORG>.

Facebook created a BSD+Patent license with an additional clause: "You won’t sue the licensor for patent infringement". This modified license would be terminated if any user or subsidiaries took financial interest in a patent assertion. 

### Apache 

Apache is the most complex of the permissive licenses. 

Projects that use Apache: most of Apache Software Foundation projects use versions 1.x, whereas version 2.0 are in use by non-ASF projects. 

Version 2 of the license was written and published in 2004, and is a departure from v1.x. 

Any derivative works of software which has an Apache 2.0 license: 

Patent clause: 

- You can include code that’s patented if you hold the patent.
- You grant anyone using (or modifying) the code the right to use that patent.
- You lose your rights granted under the license, if you sue somebody else for patent violations arising from this software.

## Copyleft Licenses: GNU GPL

> _""Copyleft licenses" require licensee to license specific developments (if they are not restricted to internal use) to anyone under the original license. This ensures that everyone who profits from open-source software will offer their developments to the developer community."_ from the [Institue for Legal Questions on Free and Open Source Software](https://www.ifross.org/en/what-types-licenses-are-there-open-source-software-and-how-do-they-differ).

### GNU GPL 

The GNU General Public License was first written by Richard Stallman (RMS) and published by the Free Software Foundation (FSF) in 1989. 

"Any code which links to GPL’ed code becomes GPL’ed"

GPL violations - modifying and redistruibtion of code. 

"Any code which links to GPL’ed code becomes GPL’ed"

#### Differences between GPLv2 and GPLv3? 

GPLv3 was first published on June 29th 2007. GPLv3 is highly controversial - it allows DRM to be implemented but users of the license cannot be held liable if they circumnavigate those DRM protections. 

You are not required to accept the GPLv3 license in order to run a copy, but you must do to run the program. Under GPLv3 you must write prominent notices regarding any modifications made.  

#### GNU LGPL

The GNU Lesser General Public License allows developers to use software components released under the license in their proprietary projects. Such projects are not then subject to the copyleft clauses that the GPL imposes. However, any modification to a piece of LGPL software has to be released under the same LGPL license. 

#### GPL Violations 

## Proprietary Licenses: 

--- 

# Relevant Questions from Past Papers 

### 2014-15

- Question 1: This question concerns the licensing of free and open source software.
  - a) Describe five reasons why software patents are a problem for free and open source software and describe the protections against software patents in version 3 of the GNU Public License (GPLv3) and the version 2.0 of the Apache License. [15 marks]
  - b) It is often said that permissive licenses (such as MIT, Apache and BSD) represent a more pragmatic approach to free and open source licensing, while Copyleft licenses (such as the GNU Public License) take a more purist view. Discuss the key differences between the permissive and Copyleft licenses (with reference to both weak and strong Copyleft). Explain what implications the choice of license might have for the inclusion of code under those licenses in other pieces of software and why a developer might choose one type of license over the other. [35 marks]

### 2015-16

- Question 2:
  - a) Describe the terms of an academic or permissive license (such as MIT, BSD, Apache or Academic Free License) [15 marks]
  - b) Describe the terms of the GNU General Public License. [15 marks]
  - c) Provide a detailed discussion of the differences between the “Academic” licenses (MIT, BSD, Apache and Academic Free License), the GNU General Public License and typical proprietary licenses. Provide some indications as to why a developer may want to choose one license over another when releasing their own code. [20 marks]


### 2016-17

- Question 1: A number of different licensing options have been discussed in the course.
  - a) Provide a detailed discussion of the differences between the Apache License, the GNU GPL and the GNU LGPL. Provide some indications as to why a developer may want to choose one license over another when releasing their own code. [40 marks]
  - b) Dual licensing with GPL, such as the MySQL licensing is an option. Discuss how this would affect the use of a MySQL database for use in software that you wanted to sell as a commercial product. [10 marks]
- Question 3: This question is on the subject of software patents, and it is based upon the guest lecture given by Richard M Stallman on 31st October 2011. The talk was essentially the same as given on 8 October 2009 at Victoria University of Wellington, the transcript of which you have studied.
  - a) Describe the fundamental differences between the concepts of Copyright and Patent. [5 marks]
  - b) Using an analogy, possibly from music, illustrate how software patents can be detrimental to the software industry because of the combinatorial nature of software design. [20 marks]
  - c) The patent system was apparently initially devised to protect the rights of ‘the starving genius’, and this argument is often repeated to defend the system itself. Discuss how the patent system is used by large corporations and how this negates the argument and therefore weakens the purpose of having a patent system for software at all. [25 marks]
  
 ### 2017-18 
 
 - Question 1: This question concerns licenses.
  - a) Describe the terms of academic permissive licences (MIT, BSD and Apache) [15 marks]
  - b) Describe the terms of the GNU General Public License. [15 marks]
  - c) Provide a detailed discussion of the differences between academic licenses (MIT, BSD and Apache), the GNU General Public License and typical proprietary licenses. Provide some indications as to why a developer may want to choose one license over another when releasing his own code. [20 marks]

 ### 2018-19
 
- Question 1: This question concerns licenses and intellectual property.
  - a) Open source software has been used in software as a service (e.g. Wordpress hosting) and also in embedded devices (e.g. set-top boxes). How can users be prevented from exercising their freedom fully when code licensed under version 2 of the GNU Public Licence (GPL) is used in these instances, and how does version 3 of the GPL attempt to address these problems? [20 marks]
  - b) This question concerns patents
    - (i) What problems do software patents cause open source software projects? [5 marks]
    - (ii) How do open source licences address the issue of patents? [15 marks]
  - c) The GPL has not [at time of writing] been tested in a UK court, however it has been tested in other European Union (EU) nations, e.g. Germany. Outline an example of the GPL being tested in a German court and describe the outcome. [10 marks]
