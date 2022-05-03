
postgresql-url_encode
=====================

RPM wrapper for the PostgreSQL url_encode extension

## Dependencies

Postgresql-url_encode uses 'qrpm' to build the RPM. It is a Ruby GEM package
that can be installed using the 'gem' command:

    gem install qrpm

'qrpm' is only used to build the RPM. The RPM can be installed on hosts without
'qrpm'

## Usage

    git clone git@github.com:clrgit/postgresql-url_encode.git
    cd postgresql-url_encode
    qrpm

This produces a RPM package in your current directory. Switch to root or use
sudo to install it:

    sudo rpm -i postgresql13-url_encode-1.2.3-0.x86_64.rpm

The package is currently compiling for postgresql13. To change that, you can
specify the version on the 'qrpm' command line like this

    qrpm pg_version=14

If you're using a postgres installation with a different naming convention for
your postgres packages or a different postgres diretory, you can define a customize name by setting PG_NAME:

    qrpm pg_name=postgres pg_directory=/usr/postgres

You can even use pg_version in your definition of the other variables:

    qrpm pg_version=14 pg_name='postgres-$pg_version' pg_directory='/usr/postgres-$pg_version'

Be careful to quote the variable with a `'` around the value or around the whole
expression so that bash doesn't expand them

