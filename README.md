# java-week2-mini3
115-1 Java 程式語言｜Week 2 作業
迷你 compiler：三個整數的加法敘述轉成 Mini-3 assembly
測試1:
<img width="225" height="124" alt="image" src="https://github.com/user-attachments/assets/edd4c515-1837-42d7-abe2-e1ba56fc489a" />

測試2:

1.
input 
int result = 1 + 20 + 6 ; 
output 
movi R1, 1
movi R2. 20
ADD R0, R1, R2
movi R2, 6
ADD R0, R0, R2
STORE [0], R0

2.
input
int result = 0 + 9 + 5 ; 
output 
movi R1, 0
movi R2. 9
ADD R0, R1, R2
movi R2, 5
ADD R0, R0, R2
STORE [0], R0

3.
input
int result = 30 + 92 + 14 ; 
output 
movi R1, 30
movi R2. 92
ADD R0, R1, R2
movi R2, 14
ADD R0, R0, R2
STORE [0], R0

回答1:第一次 ADD 之後，為什麼能用第三個整數覆蓋 R2 ？
因為ADD完之後 R0已經紀錄了R1+R2的值了 就算R2值被覆蓋或是被替換都不會影響R0的值 所以可以直接覆蓋 如果為了第三個int去設R3 可能會占用到額外的記憶體空間 這樣會浪費 這是我的想法

回答2：若輸入改成 int result=7+3+1; ，目前程式為什麼無法按預期讀取？
我不知道 但我的猜測是 可能是因為把文字連接在一起 可能會造成錯誤判讀 沒有特別去用程式設定 程式會以為你還沒輸入完成還在輸入中 而沒有作用以上是我的猜測
