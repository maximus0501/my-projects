HTML and hashtags

HTML-ize object:
```python
htmlize(obj)
```
```python
>>> import tagslib
>>> tagslib.htmlize(50)
'<pre>50 (0x32)</pre>'
>>> tagslib.htmlize('python')
'<p>python</p>
>>> print(tagslib.htmlize([1, 2, 3]))
<ul>
<li><pre>1 (0x1)</pre></li>
<li><pre>2 (0x2)</pre></li>
<li><pre>3 (0x3)</pre></li>
</ul>
```
Generate a hashtag:
```python
hashtag(s, norm=True, cap=None)
```
```python
>>> tagslib.hashtag('python prog')
#PythonProg
>>> tagslib.hashtag('python prog', norm=False)
PythonProg
>>> tagslib.hashtag('python prog', cap=(0))
#Pythonprog
>>> tagslib.hashtag('python prog', cap=('prog'))
#pythonProg
```
Generate HTML tag:
```python
htmltag(name, *content, cls=None, **attrs)
```
```python
>>> htmltag('br')
<br/>
>>> htmltag('img', src='C:\some_folder\some_img.png')
<img src="C:\some_folder\some_img.png">
>>> htmltag('int', num=42)
<int num="42">
>>> htmltag('p', 'text', cls='animate-text')
<p class='animate-text>text</p>
>>> htmltag('p', 'hello', 'world')
<p>hello</p>
<p>world</p>
```
