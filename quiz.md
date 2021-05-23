 # (1) 請問下列程式執行後的結果為何？為什麼？

start     為第一個  因為第一行

IIFE      為第二個 因為由上往下 

end       為第三個  因為"Timeout" 它先進入Webapis 然後在callback queue等待
          其他stack 跑完後之後才將它推回stack

Timeout   為第四個  自己先進入Webapis 然後在callback queue等待
          其他stack 跑完後之後才將自己推回stack


# (2) 請問下列程式執行的結果為何？為什麼？

start     為第一個  因為是第一行log

IIFE      為第二個  因為進入Function跑完

end       為第三個  因為"Timeout" 它先進入Webapis 其他stack 跑完後
          雖然它設為0 還是要在callback queue等待 之後才將它推回stack

Timeout   為第四個 自己先進入Webapis 其他stack 跑完後
          雖然它設為0 還是要在callback queue等待 之後才將自己推回stack


# (3) 請問下列程式執行的結果為何？為什麼？

foo  為第一個 因為是第一個 console.log

bar  為第二個 因為前面只是定義 接著執行

baz  為第三個 因為前面只是定義 接著執行


# (4) 請問下列程式執行的結果為何？為什麼？

foo  為第一個 因為是第一個 console.log

baz  為第二個 因為前面只是定義 接著執行

bar  為第三個 它先進入Webapis 其他stack 跑完後 它在callback queue等待
     之後才將它推回stack