## Real Time Kernel ထည့်ခြင်း
လက်ရှိ Linux Kernel Version က
```
$ uname -r
6.2.0-33-generic
```
realtime kernel သုံးဖို့ ubuntu pro သုံးမှရပါမယ်။ pro ကို subscription ယူပြီး 
```
$ sudo apt update && sudo apt upgrade -y
$ sudo apt install ubuntu-advantage-tools

# check pro version
$ pro version

# attach
$ sudo pro attach C1426YN9Wq65pGwYnncfa8HuygJz72
# Ubuntu Desktop မှာဆိုရင်တော့ "Software & Updates" ကို သွားပြိး "Ubuntu Pro" tab မှာ "Enable Ubuntu Pro" လုပ်ပါ။

# ပြီးရင်တော့ enable လုပ်ပါ။
$ pro help realtime-kernel
$ sudo pro enable realtime-kernel --beta

# ပြီးရင်တော့ reboot ချပါ။ ပြီရင် kernel ကို ပြန်စစ်ကြည့်တဲ့အခါ အောက်ပါအတိုင်း realtime ဖြစ်သွားရင်ရပါပြီ။
$ uname -r
5.15.0-1046-realtime
```
တကယ်လို့ rt kernel ကို ကိုယ့်ဟာကို build ပြီးသုံချင်ရင်တော့ https://docs.ros.org/en/humble/Tutorials/Miscellaneous/Building-Realtime-rt_preempt-kernel-for-ROS-2.html 
