Panda-Putter
============

What is it?
-----------

Panda-Putter, quite simply, allows you to upload videos to a PandaStream encoding cloud via a bash script, with minimal
dependencies.

Why?
----

I was having issues dealing with RubyGems not loading properly from cron jobs, so I decided to look for another option,
plus I wanted to have a bit of a problem to exercise my brain a little bit.

What does it need?
------------------

* Bash
* OpenSSL (needed for HMAC SHA256 and Base64 encoding)
* cURL (it does the uploady thing)
* Perl URI CPAN module (needed for URL Escaping)

How do I use it?
----------------

1. Get an account with PandaStream
2. Grab your Cloud ID, your Access Key and your Secret Key and add them to the panda-put bash script (lines 10, 13 and 14)
3. Use the following command to upload your video goodness:
   
   `panda-put some_video_file.mov`

4. (Optional) Capture the output, which will be the panda video ID, and do stuff with it.

Notes
-----

This is a very basic script which does one thing and doesn't account for any error cases. Eventually I will return non-zero
codes if the cURL call fails etc, but until then, enjoy and use at your own risk :)

Something Doesn't Work!
-----------------------

That is entirely possibly - send me a message on Github and I might be able to help, or fork the project and try and
fix it yourself (and likely also improve my code) - I welcome pull requests.