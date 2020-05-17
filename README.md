# jianpu-ly.py

[Jianpu-ly.py](http://ssb22.user.srcf.net/mwrhome/jianpu-ly.html) is a Python program to assist with printing jianpu (numbered musical notation) in the GNU Lilypond music typesetter. It is developed by [Silas S. Brown](http://ssb22.user.srcf.net/), a computer scientist at Cambridge University in the UK.

There is also a Chinese version of the introduction of this program, called [在GNU/Linux下使用Lilypond排版简谱](http://www.cnblogs.com/quantumman/p/5189701.html)

This repository was forked from v1.145 on Dec. 18, 2017. It has since been updated to v1.402 (2020).  The original download address is a click away:[JIANPU-LY.PY](http://people.ds.cam.ac.uk/ssb22/mwrhome/jianpu-ly.py).

There are several issues associated with this program which I am trying to solve and improve. So I transferred the program here to work on.

# Update List

## Known Issues
- [x] Continuous four crotchet beat will lead to forever parsing of lilypond: [HERE](https://github.com/dovecho/Jianpu/commit/f4e9b38828b78793a74a478da22c37e35cf06680) (also fixed upstream?)
- [x] Octave note has alignment issues and different layout between 1 and 2 octaves: [HERE](https://github.com/dovecho/Jianpu/commit/d51d69f11ec66d9f3528fb18cc7c216b70b07c25) (also fixed upstream?)

## Want List

The biggest problem is, the music score for different instrument looks totally different. The first thing maybe to collect sufficent music score for different styles of music, and gather the requirement.

### Sovable through JIANPU-LY
- [x] 重复小节的处理 process bar repeats: [HERE](https://github.com/dovecho/Jianpu/commit/d51d69f11ec66d9f3528fb18cc7c216b70b07c25)
- [ ] 上下加三点如何标注 how to add three-point annotation marks (?)

### Solvable through Lilypond Codes

The following issues are solvable by adding Lilypond code inside the jianpu-ly input file (without needing to update jianpu-ly itself), but this does seem a bit of a hack.

- [x] Multi-bar rest marks 多小节休止的标注
- [x] Information about composer etc 作者等人物信息 (actually you can do this in jianpu input.  Put `composer=Name Goes Here` on a line of its own in the input file.  You can do the same for other headings like `title` as well—anything from Lilypond's `header` block can be written this way)
- [ ] Instrument information 乐器信息 (for a single instrument you can put `instrument=whatever` on a line of its own in the jianpu input, but if you want a score with several instruments then you'll have to add Lilypond code)
- [ ] Speed markings 速度信息

### No Idea How to Solve
- [ ] Fingering marks 指法信息 (we need to know what they look like first)
- [ ] Copyright and other information 版权、所有人等信息 (you could try `tagline=` perhaps?  see note above about `header` block)
- [x] How to process grace notes before and after the beat 前倚音、后倚音怎么处理 (this has now been done upstream)
- [ ] How to notate various fingerings 各种指法如何标注 (SSB comment: my Chinese is not good enough to understand how this is different from the 指法信息 item above)
- [x] Multiple notes at one time 同时多音 (simple chords have now been implemented upstream)
- [ ] Polyphonic arpeggios 多音琶音 (SSB: what??)
- [ ] Multiple parts 多声部
