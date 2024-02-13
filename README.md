# pythonOOPib-21
class LittleBell:
    def sound(self):
        print("ding")
 
Кнопка
class Button:
    cnt = 0
    def click(self):    
        self.cnt += 1
    def click_count(self):
        return self.cnt
    def reset(self):
        self.cnt = 0
 
 
Весы
class Balance:
    cnt = 0
    def __init__(self):
        self.r = 0
        self.l = 0
    def add_right(self, num):    
        self.r += num
    def add_left(self, num):
        self.l += num
    def result(self):
        if self.r == self.l:
            return '='
        elif self.r > self.l:
            return 'R'
        else:
            return 'L'
 
Разбивка по чётности
class OddEvenSeparator:
    cnt = 0
    def __init__(self):
        self.e = []
        self.o = []
    def add_number(self, num):
        if num%2:
            self.o.append(num)
        else:
            self.e.append(num)
    def even(self):
        return self.e
    def odd(self):
        return self.o
 
Большой колокольчик
class BigBell:
    def __init__(self):
        self.k = False
    def sound(self):
        if self.k:
            print("dong")
        else:
            print("ding")
        self.k = not self.k
 
Самые короткие и самые длинные слова
class MinMaxWordFinder:
    def __init__(self):
        self.text = []
    def add_sentence(self, s):
        self.text += s.split()
    def shortest_words(self):
        self.text = sorted(self.text, key = len)
        return sorted(list(filter(lambda x: len(x) == len(self.text[0]), self.text)))
    def longest_words(self):
        self.text = sorted(self.text, key = len)
        return sorted(list(set(sorted(list(filter(lambda x: len(x) == len(self.text[-1]), self.text))))))

     
