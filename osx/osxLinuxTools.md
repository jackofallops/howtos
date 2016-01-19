Install Homebrew  

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Add the following line to your .bash_profile or .profile:

    export PATH="$(brew --prefix coreutils)/libexec/gnubin:/usr/local/bin:$PATH"

(alternatively, add to /etc/profile or /etc/bashrc for all users)

GNU Command Line Tools  
GNU Coreutils:

    brew install coreutils

GNU Coreutils contains the usual flavours of UNIX commands, such as ls, cat.

Then you may probably want to install the following ones (For some of the packages, you will need to run `brew tap homebrew/dupes` first, but only once for your system):

    brew install binutils  
    brew install diffutils  
    brew install ed --default-names  
    brew install findutils --with-default-names  
    brew install gawk  
    brew install gnu-indent --with-default-names  
    brew install gnu-sed --with-default-names  
    brew install gnu-tar --with-default-names  
    brew install gnu-which --with-default-names  
    brew install gnutls  
    brew install grep --with-default-names  
    brew install gzip  
    brew install screen  
    brew install watch  
    brew install wdiff --with-gettext  
    brew install wget  

The --default-names option prevents Homebrew from sticking gs onto the front of the commands (means you don't need to remember to add it to use the proper one!)

Some familiar cli tools already exist on OS X, versions may be from the dark ages so you can:

    brew install bash  
    brew install emacs  
    brew install gdb  # gdb requires further actions to make it work. See 'brew info gdb'.  
    brew install gpatch  
    brew install m4  
    brew install make  
    brew install nano  

For security purposes I recommend

    brew install openssh

Others, you may want:

    brew install file-formula
    brew install git
    brew install less
    brew install perl518   # must run "brew tap homebrew/versions" first!
    brew install python
    brew install rsync
    brew install svn
    brew install unzip
    brew install vim --override-system-vi
    brew install macvim --override-system-vim --custom-system-icons
    brew install zsh

Hopefully OSX feels a little more familiar now... :) (I still miss Debian...)

Finally: You may also want to add $HOMEBREW_PREFIX/opt/coreutils/libexec/gnuman to the MANPATH environmental variable, where $HOMEBREW_PREFIX is the prefix of Homebrew, which is /usr/local by default.