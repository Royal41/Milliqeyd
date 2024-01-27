## $PATH nedir?

#PATH icra edilə bilən proqramları saxlayan qovluqları təyin edir
#echo $PATH" əmrinin köməyi ilə müvafiq istifadəçinin yoluna baxmaq çox sadədir 

yol budur:   /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin: /usr/games:/usr/local/games:


PATH dəyişənini dəyişdirməliyik ki, o, "ls" təqlidimizi saxladığımız kataloqa işarə etsin ! Bunu "export PATH=/tmp:$PATH" əmrindən istifadə edərək edirik
(burada esas mesele oldur ki faylin yolun deyisirik ki biz emri icra edende biz istediyimiz yoldan gedib emri gotursun)

bele gorsenmelidir...
------
 #user5@polobox:/tmp$ echo $PATH
  /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
  user5@polobox:/tmp$ export PATH=/tmp:$PATH
  user5@polobox:/tmp$ echo $PATH
  /tmp:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
-----

## PATH -da yolu teyin etmek

# echo $PATH
# tmp

#export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games

#echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games
