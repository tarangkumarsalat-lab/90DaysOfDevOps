- Linux Process Management – Cheat Sheet

- --> 1️ " ps " – Process status dekhne ke liye

Common usage:-

ps :- Its showing Current shell processes or its dispaly your current active process

ps -e :- showing all System's processes

ps -ef :- with Full detail (UID, PID, PPID, CMD)

ps aux :- Most popular command (BSD style)

- --> 2 top – Live process monitoring

top :- display Real-time processes(CPU, RAM usage).

Important keys:

q → exit

k → process kill

r → priority change (nice)

 - --> 3 htop – Advanced top (GUI jaisa) , 

Better version of top (install karna padta hai)

Coomand --> sudo apt install htop

command --> htop

Mouse + color support

- --> 4 kill – Process ko terminate karna
- 
PID ke basis par process band karta hai.

kill PID -- For example kill -9 1234 

- --> 5 pkill – Process name se kill

PID yaad nahi? Naam se kill karo.

command --> pkill firefox

- --> 6 killall – Same name ke saare processes kill

command --> killall chrome

- --> 7 bg – Background me process bhejna

  Stopped job ko background me chalao.

  command --> bg

- --> 8 fg – Foreground me lana

  Background job ko foreground me lao -- Command --> fg

- --> 9 jobs – Background jobs list
 
 Command --> jobs

  - --> 10 nice – Process priority set karna
   
  Priority range: -20 (high) to 19 (low)  --> nice -n 10 command  for exampele :- nice -n 5 firefox

 - --> 11 renice – Running process ki priority badalna
     
  renice -n -5 -p 1234

 - --> 12 uptime – System running time + load
       
  uptime

  - --> 13 watch – Command ko bar-bar run karna
         
 watch ps -ef

 - Quick Summary Table
 Command	Kaam
ps	--> Process info

top -- >	Live monitoring

htop -->	Advanced monitoring

kill -->	PID se kill

pkill -->	Name se kill

killall -->	All same-name kill

bg -->	Background me

fg -->	Foreground me

jobs -->	Jobs list

nice -->	Priority set

renice -->	Priority change

      
