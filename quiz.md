 # (1) 請問下列程式執行後的結果為何？為什麼？

start     第一行log所以第一個
IIFE      然後進入Function跑完所以第二個 
end       之後 "Timeout" 進入暗樁 所以先執行end 所以第三個
Timeout   其他stack 跑完後 event loop 將它推回stack 所以第四個


# (2) 請問下列程式執行的結果為何？為什麼？

start     第一行log所以第一個
IIFE      然後進入Function跑完所以第二個 
end       之後 "Timeout" 雖然它時間設0 一樣要進暗樁 所以先執行end 所以第三個
Timeout   其他stack 跑完後 event loop 將它推回stack 所以第四個


# (3) 請問下列程式執行的結果為何？為什麼？

foo  為第一個 因為是第一個 console.log
bar  是第二個 因為前面只是定義 接著執行
baz  是第三個 因為前面只是定義 接著執行


# (4) 請問下列程式執行的結果為何？為什麼？

foo  為第一個 因為是第一個 console.log
baz  是第二個 因為前面只是定義 接著執行
bar  是第三個 因為其他stack 跑完後 進入event loop 將它推回stack