**** Creative Theme for Jekyll ****
====================================


Credit 
------
A Jekyll implementation of the [Creative Theme](http://startbootstrap.com/template-overviews/creative/) template by [Start Bootstrap](http://startbootstrap.com) by [Volny](https://volny.github.io).

Source
------
The source code is hosted on a public repo on MobileFristCentury account

Hosting
-------
  - The site is currently hosted on a google bucket (gs://www.mobilefirstcentury.com)
  - google bucket configuration procedure:
    + verify domain from [Google Webmaster toolsll](https://www.google.com/webmasters/tools/)
    + on the domain registrar DNS, add CNAME: CNAME / @ / c.storage.googleapis.com
    + create a new project on [ Google Developers Console ](https://console.developers.google.com/)
    + create a new bucket name www.mobilefirstcentury.com
    + on bucket list panel, select newly created bucket and edit 'Edit default object permissions' properties
      - grant permission to everybody
      - settings: { Entity: User , NAME : allUsers , ACCESS: Reader }

Ðeployment
----------
** note ** 
 - prerequisites
  + [install Google Cloud SDK](https://cloud.google.com/sdk/)
  + authenticate : `gcloud auth login`
 - the project is deployable with a shell script calling gsutils (a command line tool from google included in the gcloud sdk) or with gulp calling the same shell script

### Shell Script method
  # the script builds the site with Jekyll before deploying
  $ deploy.sh
### gulp method
  $ gulp deploy


Todo
----
  - host the site directly on github 
