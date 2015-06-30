# Flickr Set Tag

Generates image galleries from a Flickr set or a Flickr tag.

Usage:

    {% flickr_set flickr_set_id %}
or:
    {% flickr_set set: flickr_set_id %}
or:
    {% flickr_set tag: flickr_tag %}

Examples:

    {% flickr_set 72157625102245887 %}
    {% flickr_set set: 72157625102245887 %}
    {% flickr_set tag: birds %}

There are two ways of specifying a set for reasons of backwards compatibility.

Default Configuration (override in _config.yml):

  flickr_set:
    gallery_tag:   'p'
    gallery_class: 'gallery'
    a_href:        nil
    a_target:      '_blank'
    image_rel:     ''
    image_size:    's'
    api_key:       ''
    user:          '' 
    user_id:       ''

By default, thumbnails are linked to their corresponding Flickr page.
If you override a_href with a size ('s', 'm', etc), the thumbnail will
link to that size image. This is useful in combination with the image_rel
parameter and a lightbox gallery.

You must provide an API Key in order to query Flickr. It must be configured in _config.yml.

To correctly provide a link to the Flickr page for each photo, your username is required, i.e. the one that appears in the url of your photos.

To correctly search for tags within your account, your user_id or NSID is required; use http://idgettr.com to find it if necessary.