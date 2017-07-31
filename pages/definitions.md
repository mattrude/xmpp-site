---
layout: default
title: XMPP Definitions
permalink: /help/definitions/
---

## BOSH
<b>B</b>idirectional-streams <b>O</b>ver <b>S</b>ynchronous <b>H</b>TTP (BOSH) used to transport XMPP [stanzas](#stanza).  The result is an HTTP binding for XMPP communications that is useful in situations where a device or client is unable to maintain a long-lived [TCP](#tcp) connection to an XMPP server.

## Dialback

<b>Dialback</b> is used between two (2) XMPP servers to provide identity verification. Server Dialback uses the Domain Name System ([DNS](#DNS)) as the basis for verifying identity; the basic approach is that when a receiving server accepts a server-to-server connection from an initiating server, it does not process XMPP [stanzas](#stanza) over the connection until it has verified the initiating server's identity.

## Domain

## DNS

## Federation

<b>Federation</b> is the method used by XMPP servers to connect to other XMPP server to allow users from one server to chat with users on other server.

Similar to how email works, federation allows you to communicate with any XMPP service that allows for remove connections (most).

The following diagram provides a high-level overview of this architecture (where `-` represents communications that use XMPP).

<pre><code>        C1
        |
   C2---S1---C3
        |
        |
        |
   C4---S2---C5
        |
        C6
</code></pre>

The symbols are as follows:

* C1, C2, C3, C4, C5, C6 = XMPP clients
* S1, S2 = XMPP servers

## Gateway

## IP Address

## Jabber
Another name for XMPP, the old name.

## JID
A users unique [XMPP](#xmpp-server) address, is called a JID (or for historical reasons, sometimes called a Jabber ID). The JID is structured like an email address with a username and a domain name (or [IP address](#ip-address)) for the server where that user resides, separated by an at sign `@`, such as username@example.com.

## LAN

## OTR

## Presence
A users [XMPP](#xmpp-server) presence indicates if a users is **online**, **away**, or **offline**.

## Prosody

## SRV Records

## Stanza
A group of lines forming the basic recurring metrical unit in [XML](#xml); like a verse in a poem.

## TCP

## TLS

## Transports
One of the original design goals of the early Jabber open-source community was enabling users to connect to multiple non-XMPP messaging systems. This was done through *transports* or *gateways*.

## XEP

## XMPP Server
An XMPP server provides basic messaging, [presence](#presence), and XML routing features. This page lists Jabber/XMPP server software that you can use to run your own XMPP service, either over the Internet or on a [local area network](#lan).

## XML
E<b>X</b>tensible <b>M</b>arkup <b>L</b>anguage (XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable.  XML is the format that messages are sent/received in when communication with XMPP (See [XML](https://en.wikipedia.org/wiki/XML)).
