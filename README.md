# learning 
#debug 14,Nov.2018
python
一、 python三种方法统计词频率

1.直接使用dict

2.使用defaultdict

3.使用Counter

1.
import collections
text = "we are family you are perfect you we yes"

frequency = {}

for word in text.split():
    if word not in frequency:
        frequency[word] = 1
    else:
        frequency[word] += 1
print(frequency)
2.
import collections

frequency = collections.defaultdict(int)

text = "we are family you are perfect you we yes"

for word in text.split():
    frequency[word] += 1
print(frequency)
3.
import collections

text = "we are family you are perfect you we yes"
frequency = collections.Counter(text.split())
print(frequency)
