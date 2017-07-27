---
layout: default
title: Using Conferences
permalink: /help/using-conferences/
---

# Conferences

{% if site.xmpp-conference-url and site.xep-0045 == 1 %}

XMPP is normally a single person to single person chat system, but it has the ability to also run conference rooms.  A conference room or MUC (Multiple User Chat) allows users on the same server, or via [federation]({{ site.url }}/help/definitions/#federation), different servers or domains, to all connect to the same chat room.  Similar to how IRC works.

## Managing a Conference

### Conference room options

* <b>Name:</b> The name of the conference room.
* <b>Description:</b> The conference room descriptions
* <b>Persistent:</b> Prevent the room from being deleted after the last user leaves.
* <b>Searchable:</b> Allows users to search for the room in the list of rooms on the server and connect.
* <b>Change Subject:</b> Allow none <u>admins</u> to change the rooms subject.
* <b>Password:</b> Set the password for the room; all users who wish to access the room, must use the password to enter.
* <b>Moderated:</b> Moderated rooms require a admin to approve each message before it is delevered to the rest of the room.
* <b>Members-Only:</b> Only allow members of the room to enter the room.
* <b>History:</b> Maximum number of past messages to return by the server when a user connects.
* <b>Logging:</b> Enable external logging for the room; when enabled, any user on the internet may view this log.

## Joining a Conference

### Connecting from local XMPP server



### Connecting from a federated XMPP server

By default the server will try to use [TLS]({{ site.url }}/help/definitions/#tls) if the other side supports it, and fall back to [dialback]({{ site.url }}/help/definitions/#dialback) if it does not or if the certificate is incorrect or not trusted.

## Conference Plugins

### Pastebin

When someone posts to a room a "large" (greater then 500 characters or 5 lines) message, the server will intercept the message and convert it to a URL pointing to a built-in pastebin server.  Generated URLs will point will have address contaning `https://{{ site.xmpp-conference-url }}/pastebin/`.

<div class="alert alert-warning" role="alert"><b>Note:</b> If a message is sent via <a href="https://conversations.im/omemo/">OMEMO</a>, the pastebin function will not create a link since the server is unable to read the message.</div>

### HTTP File Upload

### Security Labels

A security label, sometimes referred to as a confidentiality label, is a structured representation of the sensitivity of a piece of information.  A security label is used in conjunction with a clearance, a structured representation of what information sensitivities a person (or other entity) is authorized to access, and a security policy to control access to each piece of information.  Security Lables are described in <a href="https://xmpp.org/extensions/xep-0258.html">XEP-0258</a>.

{% if site.fingerprints == 1 %}
## Certificate Fingerprints

One of the benefits of communicating via XMPP is the level of security involved.  To allow users to validate the servers they are connecting to, below is the current fingerprints for each domain name.

<div id="cert-table">
{% if site.fingerprint-sha1 %}
  <div class="cert-title">
    <b>{{ site.baseurl }}<small> - SHA1 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-sha1 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-sha256 %}
  <div class="cert-title">
    <b>{{ site.baseurl }}<small> - SHA256 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-sha256 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-conference-sha1 %}
  <div class="cert-title">
    <b>{{ site.xmpp-conference-url }}<small> - SHA1 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-conference-sha1 }}</pre>
  </div>
{% endif %}
{% if site.fingerprint-conference-sha256 %}
  <div class="cert-title">
    <b>{{ site.xmpp-conference-url }}<small> - SHA256 Fingerprint</small></b>
  </div>
  <div class="cert-content">
    <pre>{{ site.fingerprint-conference-sha256 }}</pre>
  </div>
{% endif %}
</div> <!-- Closing cert-table id div -->
{% endif %}
{% else %}
This server dose not support conferences at this time, sorry.
{% endif %}
