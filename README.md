```print('MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM')
print('MMMMMMMMMMMMMMWNXKOOONMMMMMMMMMMMMM')
print('MMMMMMMMMMNkl:; .. ,,:lkWMMMMMMMMMM')
print('MMMMMMMMXo' ',......... KMMMMMMMMM')
print('MMMMMMMX..lkO0K0Okxdooc  ;NMMMMMMMM')
print('MMMMMMMx.okkOO0KKK0Okxxd,.:XMMMMMMM')
print('MMMMMMMx.oxkkOO0KK0Okxxo, .KMMMMMMM')
print('MMMMMMM0.cxxdollddlllooo, .XMMMMMMM')
print('MMMMMMMWdcoc:;;,ll,;;:cl:.xMMMMMMMM')
print('MMMMMMMMNxxxxddokOldxxdoocXMMMMMMMM')
print('MMMMMMMMWkddxddl:;;ooolllkWMMMMMMMM')
print('MMMMMMMMMXdlllcc:::cclc:dWMMMMMMMMM')
print('MMMMMMMMMMKlcoddooodoc;;KMMMMMMMMMM')
print('MMMMMMMMMMWd:;:c::;;,'':co0NMMMMMMM')
print('MMMMMN0xoc.:k:,,,.....ckc ...cdOXWM')
print('XOkd:..... :KKkl;'';lk0Oo ........:')
print('...........:NXNXc..;OXKKl  ...   ..')
print('....  .....,NN0l,..,coKKo   ..     ')
print('...    ....;NKO0:..0KOkXk   .....  ')
print('    .......:WWW0...OWWWWO.  ....   ')
print('    .......:WWWo...cWWWWK.. ....   ')
print('     ......cWW0.....XWWWN.. ....   ')
print('     ..... lWWc.....OWWWW,. ...    ')
```
# CTF-Tool---miniJohn-C++
CTF Tool to perform a dictionary attack or a brute force on a hash
IT SUPPORTS - MD5 , SHA1 , SHA256 , SHA512

# INSTALLATION
After cloning the project locally , you need to run these commands : 
## LINUX:
```
$ cd Passwords/ | find "$(pwd)" -type f -name "*.txt" >> fisiere
$ cp fisiere cmake-build-debug/
$ cp lista_romana cmake-build-debug/
```
## WINDOWS:
```
cd Passwords\
for /r %i in (*.txt) do @echo %i >> fisiere
copy fisiere cmake-build-debug\
copy lista_romana cmake-build-debug\
```
# USAGE:

# 1. Brute force attack on a hash<br />
- Here you can modify the characters that you want to use in this , just go to <mark>brute.cpp</mark> line 54<br />
  ```std::string letters = "abcdefghijklmnopqrstuvwxyz";```
and modify as you want
```
 $ g++ brute.cpp -o brute
 $ ./brute <hash> <hash_name> <number_of_characters>
```
 - Example : ./brute ab56b4d92b40713acc5af89985d4b786 MD5 5
 - It should print : 
   - Found: abcde
   - Algo: MD5

# 2. Dictionary attack on a hash
```
 $ g++ -pthread -o dict dictionary.cpp
 $ ./dict <hash>
```
- Example : ./dict bc250e0d83c37b0953ada14e7bbc1dfd
- It should print : 
  - Found: tesla
  - Algo: MD5
  - Path: somewhere in Passwords

# Build project
 Or more easily
 ```
 $ mkdir -p build
 $ cd build
 $ cmake ..
 $ make
 ```
  - And then to use it: <br />
    ``` Dictionary attack - $ ./miniJohn <hash>  ``` <br />
    ``` Brute force attack - $ ./bruteForce <hash> <hash_name> <number_of_characters> ```


