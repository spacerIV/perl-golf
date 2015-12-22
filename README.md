## Find all words longer than 6 letters and with all letters in alphabetical order.

### Long way

    perl -nE 'chomp;  next if (length $_ < 6 ); my @o = split //,lc $_; my @s = sort @o; say @o if ( @o ~~ @s ) ' /usr/share/dict/words  

### Golfed 

    perl -nE 'chomp;if(y///c>5){@o=/./g;@s=sort@o;say@o if(@o~~@s)}' /usr/share/dict/words


#### Tips

- y///c is one character shorter than length
- ($x=~/./g) is two characters shorter than (split//,$x)


#### here we go
