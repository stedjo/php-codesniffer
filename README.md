# PHP CodeSniffer

## Requirements

- PHP installed (for the purpose of this guide we will assume that location of your php installation is c:\php)

## Instructions

1. **Install Pear**
    - Download pear [http://pear.php.net/go-pear.phar](http://pear.php.net/go-pear.phar) and put it inside your php directory
    - Open command terminal (Win + R, type `cmd` and press Enter)
    - Position yourself inside your php directory
    - Run php go-pear.phar

    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/pear_install.png)

    - For the following prompts press Enter to continue
    - After installation has finished, you should be able to check your pear version by typing `pear -V` (you might need to reopen the command prompt for the changes to take affect)
2. **Install PHPCS**
    - Open command terminal (Win + R, type `cmd` and press Enter)
    - Position yourself inside your php directory
    - Run pear install PHP\_CodeSniffer

    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpcs_install.png)

    - After installation has finished, you should be able to check your phpcs version by typing ` phpcs --version` (you might need to reopen the command prompt for the changes to take affect)
    
    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpcs_version.png)

3. **Create your ruleset based on PSR2**
    - Open the _CodeSniffer__Standards_ directory and create new folder called _DevTech_ (C:\php\pear\PHP\CodeSniffer\Standards\DevTech)
    - Copy and paste the attached _ruleset.xml_ file inside of the newly created directory (C:\php\pear\PHP\CodeSniffer\Standards\DevTech\ruleset.xml)
    - After this is done we will need to set up the _Code Style Scheme_ for our projects. This is used when running _Reformat_ on the legacy code, or while creating a new code from the scratch. PhpStorm will use this to structure your code layout, so you won&#39;t have to worry about complying the standard requirements. Go to your IDE _codestyles_ settings directory (mine is _C:\Users\stefan.djokic\.WebIde100\config\codestyles_)and paste the attached file _DevTech.xml_

4. **Configure PhpStorm**
    - Run your PhpStorm and open the Settings panel (Ctrl + Alt + S)  
       _Note: if you want to use this set up for all of your projects you should open your Default Settings panel instead, do this  by clicking on  File-&gt;Default Settings from the main menu bar_
    - Go to _Languages &amp; Frameworks -&gt; PHP -&gt; Code Sniffer_ and hit the _Browse_ button

    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpcs_phpstorm.png)

    - Set the path for your phpcs bat file (mine is C:\php\phpcs.bat) and hit _Apply_
    
    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpcs_phpstorm_path.png)

    - Go to _Editor-&gt;Code Style-&gt;PHP_ and select _DevTech_ from the _Scheme_ dropping menu then hit _Apply_
    
    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpstorm_code_style.png)

    - Go to _Editor-&gt;Inspections_ under _Unused_, check _PHP Code Sniffer validation_ checkbox, then change the _Coding standard_ to _DevTech_ (you might need to press refresh in order to update the list of coding standards) hit _OK_
    
    ![](https://raw.githubusercontent.com/stedjo/php-codesniffer/master/images/phpstorm_inspection.png)

    - That&#39;s it! You&#39;re all set.

   _Note: We are using PSR2 with the exception of using Tab Indents instead of Space Indents. For more information about PSR2 visit_ [_http://www.php-fig.org/psr/psr-2/_](http://www.php-fig.org/psr/psr-2/)

   ### HAPPY CODING!!!