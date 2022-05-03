
postgresql-url_encode
=====================

RPM wrapper for the PostgreSQL url_encode extension

## Dependencies

Postgresql-url_encode uses 'qrpm' to build the RPM. It is a GEM package that
can be installed using the 'gem' command:

    gem install qrpm

'qrpm' is only used to build the RPM

## Usage

    git clone git@github.com:clrgit/postgresql-url_encode.git
    cd postgresql-url_encode
    qrpm

This produces a RPM package in your current directory. Switch to root or use
sudo to install it:

    sudo rpm -i postgresql13-url_encode-1.2.3-0.x86_64.rpm

The package is currently compiling for postgresql13. To change that, you can
specify the version on the 'qrpm' command line like this

    qrpm PG_VERSION=14


