# Case Study
https://forums.rocket.chat/t/support-for-installation-in-subdirectory-will-be-discontinued/6371/15

"""
MRamadan
May 2020
In fact as long as OAuth is supported so I think our requirements will be fulfilled after you take subfolders out. Only one challenge we need to fix

So RC is a part of our community site and our biggest issue was in the login page customize to avoid feeling the user that he is navigating from our site to another system.

Initially, what we did is to add our own custom OAuth provider. We disabled all kind of the authentications and we kept only our custom OAuth. Then we expected the login page will not appear at all and user will be redirect automatically to our site to generate the access token. However what was happened is the rocket chat login page keep showing with only one button that is representing our custom OAuth provider

To overcome that we used the IframeAuthentication which also contains lot of issues because of cross domain iframe security, in fact it was impossible for some browser to use it

Finaly to we came up with deployint it at subfolder to overcome the browser security and be able to allow user login without that Rocket Chat login page

What I am suggesting here after to take subfolder out, we need more control on the login page without iframe in place at all.

For example we can have an option to configure what is the default authentication provider to be used instead of letting the user see the RC login page and click on a button single button representing our Custom OAuth
"""
