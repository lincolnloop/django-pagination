This is a fork of django-paginator to allow you to change the page variable on
a template-by-template basis.  To use it, simply add a 'by' argument to your
'autopaginate' tag.  For example:

    {% autopaginate comments by pg %}

This will autopaginate the 'comments' queryset using the 'pg' variable in the
GET string.  So, you would access page 2 by using '/path/to/article/?pg=2'.

You can also change the default page variable using the
'PAGINATION_DEFAULT_PAGE_VAR' setting.  The app will then use the value given
as the default page variable site-wide.

**Important:** This fork also removes the pagination middleware, because it is
no longer needed.  If you do not remove this from your MIDDLEWARE_CLASSES, you
will experience errors because the class no longer exists.
