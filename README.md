# Patika
Patika.dev veri yapıları ve algoritma

# 1. Selection Sort
```
[22,27,16,2,18,6] -> Insertion Sort

Yukarı verilen dizinin sort türüne göre aşamalarını yazınız.
```


* İlk elemanla sağındaki eleman karşılaştırılır. Daha küçük olan sola alınır.

İlk elemanla sağındaki eleman karşılaştırılır. Daha küçük olan sola alınır.
* [22,27,16,2,18,6] 22 ve 27 doğru sırada. Bu şekilde bırakılır.
* [16,22,27,2,18,6] 27 ve 16 karşılaştırılır. 16 daha küçük olduğu için yer değiştirirler. 16, 22'den de küçük olduğu için onunla da yer değiştirir.
* [2,16,22,27,18,6] 2, 27'den, 22'den ve 16'dan küçük olduğu için en başa gelir. Geri kalan elemanlar da aynı mantıkla sıralanır.
* [2,16,18,22,27,6]
* [2,6,16,18,22,27]


```
Big-O gösterimini yazınız.
```
Insertion Sort algoritmasının en kötü durumda çalışması \(O(n^2)\) olarak ifade edilir. Çünkü her eleman, neredeyse tüm diğer elemanlarla karşılaştırılmak zorundadır. Ortalama durumda da yine \(O(n^2)\) olarak ifade edilir. En iyi durumda, yani dizi zaten sıralıysa, \(O(n)\) olur.
```
Time Complexity: Dizi sıralandıktan sonra 18 sayısı aşağıdaki case'lerden hangisinin kapsamına girer? Yazınız
1.Average case: Aradığımız sayının ortada olması
2.Worst case: Aradığımız sayının sonda olması
3.Best case: Aradığımız sayının dizinin en başında olması.
```
Sıralanmış dizi şu şekildedir: [2,6,16,18,22,27]
Yani 18 average case durumundadır.

# MergeSort
[16,21,11,8,12,22] -> Merge Sort
Yukarıdaki dizinin sort türüne göre aşamalarını yazınız.
```
*[16,21,11]       [8,12,22]
*[16]  [21,11]       [8]    [12,22]
*[16]  [21] [11]       [8]    [12] [22]
*[16]  [11,21]       [8]    [12,22]
*[11,16,21]       [8,12,22]
*[8, 11, 12, 16, 21, 22]

```
Big-O gösterimini yazınız.
```
O(n*logn)
```

# BinarySearchTree

**[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] dizisinin Binary-Search-Tree aşamalarını yazınız.**

*Örnek: root x'dir. root'un sağından y bulunur. Solunda z bulunur vb.*

[7, 5, 1, 8, 3, 6, 0, 9, 4, 2] 

                    7                       * root
                5                           1. Aşama  : 5, 7'den küçük bu yüzden 7'nin sol alta gelir.
            1                               2. Aşama  : 1, 5'ten küçük bu yüzden 5'in sol alta gelir
        
---       
                     7          
                5          8                3. Aşama  : 8, 7'den büyük bu yüzden 7'nin sağ alta gelir.
            1       3                       4. Aşama  : 3, 5'ten küçük ama 1'den büyük bu yüzden 5'in sağ altına gelir.
                       6                    5. Aşama  : 6, 7'den küçük ama 5'ten büyük bu yüzden 3'ün sağ altına gelir.
        0                                   6. Aşama  : 0, 1'den küçük bu yüzden 1'in sol altına gelir.
---  
                      7
                5            8
                     3               9      7. Aşama  : 9, 7'den büyük ama 8'den büyük bu yüzden 8'in sağ altına gelir.
            1     4     6                   8. Aşama  : 4, 5'ten küçük ama 3'ten büyük ama 6'dan küçük bu yüzden 6'nın sol altına gelir.
        0        2                          9. Aşama  : 2, 3'ten küçük bu yüzden 3'ün sol altına gelir.

