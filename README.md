#!/usr/bin/perl
use File::Find ;
my $dir='/cygdrive/c/Documents and Settings/walt/Downloads';
my @array ;
print "$dir\n" ;
　
　
find(\&wanter, $dir);
　
sub wanter {
    push(@array,$_) ;
}
　
foreach $reader(@array) {
     if ($reader =~ /$\.jpg/) {
         print "$reader\n"  ;
         system ("cygstart /cygdrive/c/'Documents and Settings'/walt/Downloads/$reader");
         sleep 120 ;
      }
}
　
　
　
　
