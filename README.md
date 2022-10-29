# Phyton  www.patika.dev

1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. 

l = [[14,'t',['python_kodluyoruz'],23],[[[48]],'patika'],14,5]
flat_list = []
def flatten(x):
    for i in x:
        if isinstance(i, list): flatten(i)
        else: flat_list.append(i)
flatten(l)
print(flat_list)

2-Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün.

l = [[1, 2, 3], 4, 5, 6, [7, 8, 9], 10, 11, [12, 13, 14]]
r_l = []
def is_list(p):
    return isinstance(p,list)

def deep_reverse(l):
    result = []
    for e in l:
        if isinstance(e,list):
            result.append(deep_reverse(e))
        else:
            result.append(e)
    result.reverse()
    return result
print(deep_reverse(l), r_l)
