# jianpu-ly.py

[Jianpu-ly.py](http://people.ds.cam.ac.uk/ssb22/mwrhome/jianpu-ly.html) is a Python program to assist with printing jianpu (numbered musical notation) in the GNU Lilypond music typesetter. It is developed by [Silas S. Brown](http://people.ds.cam.ac.uk/ssb22/), a computer scientist at Cambridge University in the UK.

There is also a Chinese version of the introduction of this program, called [在GNU/Linux下使用Lilypond排版简谱](http://www.cnblogs.com/quantumman/p/5189701.html)

The original version of the file is v1.145 at the time the repository is built on Dec. 18, 2017. The original download address is a click away:[JIANPU-LY.PY](http://people.ds.cam.ac.uk/ssb22/mwrhome/jianpu-ly.py).

However, there're several issues associated with this program, and I am trying to solve and improve it. So I transfer the program here, and make it better.

# Update List

## Known Issues
- [x] Continuous four crotchet beat will lead to forever parsing of lilypond: [HERE](https://github.com/dovecho/Jianpu/commit/f4e9b38828b78793a74a478da22c37e35cf06680)
- [x] Octave note has alignment issues and different layout between 1 and 2 octaves: [HERE](https://github.com/dovecho/Jianpu/commit/d51d69f11ec66d9f3528fb18cc7c216b70b07c25)

## Want List

The biggest problem is, the music score for different instrument looks totally different. The first thing maybe to collect sufficent music score for different styles of music, and gather the requirement.

### Sovable through JIANPU-LY
- [x] 重复小节的处理: [HERE](https://github.com/dovecho/Jianpu/commit/d51d69f11ec66d9f3528fb18cc7c216b70b07c25)
- [ ] 上下加三点如何标注

### Solvable through Lilypond Codes

Maybe only use Lilypond codes inside the jianpu file can solve the problem. There will be no update of the Jianpu-ly.py. The thing is, such method seems to be a dirty work..

- [x] 多小节休止的标注
- [ ] 作者等人物信息
- [ ] 乐器信息
- [ ] 速度信息

### No Idea How to Solve
- [ ] 指法信息
- [ ] 版权、所有人等信息
- [ ] 前倚音、后倚音怎么处理
- [ ] 各种指法如何标注
- [ ] 同时多音
- [ ] 多音琶音
- [ ] 多声部
