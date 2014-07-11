tokuhirom's maven repo
======================

This is a @tokuhirom's maven repo.
I'm using [camerick's method](http://cemerick.com/2010/08/24/hosting-maven-repos-on-github/) for creating maven repository. Maven central is too hard for me.

## How do I use the libraries in this repository?

You can use this repository by following:

    <repositories>
        <repository>
            <id>tokuhirom</id>
            <url>https://tokuhirom.github.io/maven/releases/</url>
        </repository>
    </repositories>

## How do I create the maven repository like this?

Add the 'distributionManagement' section in your project pod.xml.

    <distributionManagement>
        <repository>
            <id>repo</id>
            <url>https://tokuhirom.github.io/maven/releases/</url>
        </repository>
        <snapshotRepository>
            <id>snapshot-repo</id>
            <url>https://tokuhirom.github.io/maven/snapshots/</url>
        </snapshotRepository>
    </distributionManagement>

And I wrote a tiny utility script.  You can install it by cpanm command.

    curl -L http://cpanmin.us | perl - -nv git://github.com/tokuhirom/mvnutil.git

Please look [tokuhirom/mvnutil](https://github.com/tokuhirom/mvnutil/) for more details.

