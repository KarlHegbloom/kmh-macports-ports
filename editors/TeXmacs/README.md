# TeXmacs Devel MacPort Instructions #

First of all, of course you must have MacPorts installed. Follow the
directions at <https://www.macports.org> if you have not already done
so. Next, install the `git` package, and then clone this repository,
create a port index there, and then add it to the MacPorts
configuration. Finally, use the `port` command to install the TeXmacs
package:

``` shell
sudo port install git
mkdir Source
cd Source
git clone https://github.com/KarlHegbloom/kmh-macports-ports
cd kmh-macports-ports
portindex
sudo vi /opt/local/etc/macports/sources.conf
```

Just before the last line, add the line:

```
file:///Users/<YOURNAME>/Source/kmh-macports-ports
```

Now run `port search TeXmacs` to get the version information you'll
need to run the install command, *i.e.,*

``` shell
port search TeXmacs
sudo port install TeXmacs @v1.99.9-20171120-kmh_1
```

The actual installation of TeXmacs will take quite some time if none
of the prerequisite packages are installed yet. You'll need a fast
network connection and plenty of patience.

Once it is installed, run `texmacs` from the terminal command line.
