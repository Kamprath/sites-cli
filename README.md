# sites-cli
This utility allows you to quickly switch between directories served by your web server. The script simply updates a symbolic link that your web server uses as its document root to the location of whichever site you wish to use.

This is useful if you want to avoid using virtual hosts or having to frequently change your web server's document root.

### Requirements
* [PHP CLI](http://php.net/manual/en/features.commandline.php) is required to run this utility

* This script expects `/usr/bin/php` to exist. If your PHP binary is located elsewhere, modify the `sites` file and update the interpreter directive, `#!/usr/bin/php`, with the path to your PHP binary.

### Setup
1. **Download the script**
<br>`cd /usr/local/bin && curl -O https://raw.githubusercontent.com/ravroid/sites-cli/master/sites`

2. **Make the script executable**
<br>`sudo chmod u+x /usr/local/bin/sites`

3. **Run `sites` from your terminal**
<br>The first time that `sites` is run, you will be prompted with configuration.

4. **Configure your web server to serve from the symlink**
<br>For whichever web server you use, change the root directory it serves its files from to the symlink that was created, then restart the web server.

### Usage
**Add a site**
<br>To add a site, use `sites add <name> <absolute path>`.

**Use a site**
<br>To switch the active sites being served, use `sites use <name>`.

**List sites**
<br>To list all sites that have been added, simply run `sites`.

**Show command help**
<br>To a list of available command options, run `sites help`.